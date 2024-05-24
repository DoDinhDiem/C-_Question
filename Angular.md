### Câu hỏi cơ bản về Angular:

1. **Angular là gì?**

   - **Trả lời:** Angular là một framework phát triển ứng dụng web mã nguồn mở do Google phát triển. Nó sử dụng TypeScript, một ngôn ngữ lập trình được xây dựng trên JavaScript, để tạo ra các ứng dụng web động, có khả năng mở rộng cao.

2. **Sự khác nhau giữa AngularJS và Angular là gì?**

   - **Trả lời:** AngularJS (phiên bản 1.x) là phiên bản đầu tiên của Angular và sử dụng JavaScript. Angular (phiên bản 2 trở lên) là phiên bản mới hơn, được viết lại hoàn toàn bằng TypeScript, và cung cấp nhiều cải tiến về hiệu suất, kiến trúc, và khả năng mở rộng.

3. **Component trong Angular là gì?**

   - **Trả lời:** Component là thành phần cơ bản của Angular, đại diện cho một phần giao diện người dùng (UI). Mỗi component bao gồm HTML template, CSS styles, và logic TypeScript.

   ```typescript
   @Component({
     selector: "app-example",
     template: "<h1>{{ title }}</h1>",
     styles: ["h1 { color: red; }"],
   })
   export class ExampleComponent {
     title = "Hello, Angular!";
   }
   ```

4. **Data Binding trong Angular là gì?**

   - **Trả lời:** Data Binding là một kỹ thuật kết nối dữ liệu giữa component và template. Angular hỗ trợ bốn kiểu data binding chính:
     - **Interpolation:** Kết nối dữ liệu từ component đến template ({{ value }}).
     - **Property Binding:** Kết nối thuộc tính của HTML element với dữ liệu từ component ([property]="value").
     - **Event Binding:** Kết nối sự kiện của HTML element với phương thức trong component (event)="handler()".
     - **Two-way Binding:** Kết nối dữ liệu hai chiều giữa component và template ([(ngModel)]="value").

5. **Directive trong Angular là gì?**
   - **Trả lời:** Directive là một cách để thao tác DOM trong Angular. Có ba loại directives chính:
     - **Component:** Là directive có template.
     - **Structural Directive:** Thay đổi cấu trúc của DOM (ngIf, ngFor).
     - **Attribute Directive:** Thay đổi giao diện hoặc hành vi của các phần tử DOM (ngClass, ngStyle).

### Câu hỏi nâng cao về Angular:

1. **Lifecycle hooks trong Angular là gì?**

   - **Trả lời:** Lifecycle hooks là các phương thức được gọi tại các thời điểm khác nhau trong vòng đời của một component. Một số lifecycle hooks phổ biến:
     - **ngOnInit:** Được gọi khi component được khởi tạo.
     - **ngOnChanges:** Được gọi khi các input properties của component thay đổi.
     - **ngOnDestroy:** Được gọi ngay trước khi component bị hủy.

   ```typescript
   export class MyComponent implements OnInit, OnChanges, OnDestroy {
     ngOnInit() {
       console.log("Component initialized");
     }
     ngOnChanges(changes: SimpleChanges) {
       console.log("Input properties changed", changes);
     }
     ngOnDestroy() {
       console.log("Component destroyed");
     }
   }
   ```

2. **Reactive Forms và Template-driven Forms trong Angular khác nhau như thế nào?**

   - **Trả lời:**
     - **Template-driven Forms:** Được tạo dựa trên template HTML, sử dụng directives như `ngModel`. Thích hợp cho các form đơn giản.
     - **Reactive Forms:** Được quản lý bằng code TypeScript, sử dụng `FormControl`, `FormGroup`, và `FormBuilder`. Thích hợp cho các form phức tạp và cung cấp khả năng kiểm soát và kiểm tra tốt hơn.

   ```typescript
   // Reactive Form Example
   this.form = this.fb.group({
     name: ["", Validators.required],
     email: ["", [Validators.required, Validators.email]],
   });

   // Template-driven Form Example
   <form #form="ngForm">
     <input name="name" ngModel required />
     <input name="email" ngModel required email />
   </form>;
   ```

3. **Giải thích về Dependency Injection trong Angular.**

   - **Trả lời:** Dependency Injection (DI) là một mẫu thiết kế cho phép quản lý và cung cấp các phụ thuộc của đối tượng. Angular có một hệ thống DI mạnh mẽ cho phép tự động cung cấp các dịch vụ và phụ thuộc cho các components và services.

   ```typescript
   @Injectable({
     providedIn: "root",
   })
   export class MyService {
     constructor() {}
   }

   @Component({
     selector: "app-example",
     templateUrl: "./example.component.html",
     styleUrls: ["./example.component.css"],
   })
   export class ExampleComponent {
     constructor(private myService: MyService) {}
   }
   ```

4. **Lazy Loading Modules trong Angular là gì và tại sao nó quan trọng?**

   - **Trả lời:** Lazy Loading là kỹ thuật tải các modules chỉ khi cần thiết, giúp giảm thời gian tải ban đầu của ứng dụng. Điều này cải thiện hiệu suất và trải nghiệm người dùng. Trong Angular, bạn có thể cấu hình lazy loading cho các modules bằng cách sử dụng `loadChildren` trong định tuyến.

   ```typescript
   const routes: Routes = [
     {
       path: "feature",
       loadChildren: () => import("./feature/feature.module").then((m) => m.FeatureModule),
     },
   ];
   ```

5. **Angular Universal là gì?**

   - **Trả lời:** Angular Universal là một công cụ để thực hiện Server-Side Rendering (SSR) cho các ứng dụng Angular. SSR giúp cải thiện hiệu suất, SEO, và trải nghiệm người dùng bằng cách render các trang trên server trước khi gửi đến client.

   ```typescript
   import { NgModule } from "@angular/core";
   import { ServerModule } from "@angular/platform-server";
   import { AppModule } from "./app.module";
   import { AppComponent } from "./app.component";

   @NgModule({
     imports: [AppModule, ServerModule],
     bootstrap: [AppComponent],
   })
   export class AppServerModule {}
   ```

### Các khái niệm và kỹ thuật nâng cao:

1. **NgModules trong Angular là gì và vai trò của chúng là gì?**

   - **Trả lời:** NgModules là các khối xây dựng cơ bản để tổ chức các ứng dụng Angular. Chúng nhóm các components, directives, pipes, và services thành các khối logic. NgModules giúp phân chia ứng dụng thành các phần có thể quản lý và tái sử dụng được.

2. **Giải thích về Angular Router và cách sử dụng nó.**

   - **Trả lời:** Angular Router là một hệ thống định tuyến mạnh mẽ cho phép điều hướng giữa các views hoặc components khác nhau trong ứng dụng Angular. Router cho phép cấu hình các routes, xử lý các tham số, và quản lý các guards cho bảo mật.

   ```typescript
   const routes: Routes = [
     { path: "", component: HomeComponent },
     { path: "about", component: AboutComponent },
     { path: "**", redirectTo: "" },
   ];

   @NgModule({
     imports: [RouterModule.forRoot(routes)],
     exports: [RouterModule],
   })
   export class AppRoutingModule {}
   ```

3. **Giải thích về các Guards trong Angular.**

   - **Trả lời:** Guards trong Angular là các dịch vụ được sử dụng để kiểm soát quyền truy cập vào các routes. Các loại guards bao gồm:
     - **CanActivate:** Kiểm tra xem route có thể được kích hoạt hay không.
     - **CanActivateChild:** Kiểm tra xem các routes con có thể được kích hoạt hay không.
     - **CanDeactivate:** Kiểm tra xem route có thể được hủy kích hoạt hay không.
     - **Resolve:** Lấy dữ liệu trước khi route được kích hoạt.
     - **CanLoad:** Kiểm tra xem module có thể được tải không (dùng cho lazy loading).

   ```typescript
   @Injectable({
     providedIn: "root",
   })
   export class AuthGuard implements CanActivate {
     constructor(private authService: AuthService, private router: Router) {}

     canActivate(next: ActivatedRouteSnapshot, state: RouterStateSnapshot): boolean {
       if (this.authService.isLoggedIn()) {
         return true;
       } else {
         this.router.navigate(["/login"]);
         return false;
       }
     }
   }
   ```

4. **Pipes trong Angular là gì và cách tạo một custom pipe.**

   - **Trả lời:** Pipes là các công cụ chuyển đổi dữ liệu hiển thị trong template. Angular cung cấp nhiều pipes tích hợp sẵn như `DatePipe`, `UpperCasePipe`, và `CurrencyPipe`. Bạn cũng có thể tạo custom pipes bằng cách kế thừa `PipeTransform`.

   ```typescript
   @Pipe({ name: "customPipe" })
   export class CustomPipe implements PipeTransform {
     transform(value: string, ...args: any[]): string {
       // Transform logic here
       return modifiedValue;
     }
   }
   ```

5. **State Management trong Angular là gì và tại sao nó quan trọng?**
   - **Trả lời:** State

Management là cách quản lý trạng thái của ứng dụng. Trong các ứng dụng phức tạp, việc quản lý trạng thái trở nên quan trọng để đảm bảo tính nhất quán và dễ bảo trì. Các công cụ như NgRx cung cấp các giải pháp state management dựa trên Redux, giúp quản lý trạng thái một cách hiệu quả và rõ ràng.

```typescript
// Actions
export const increment = createAction("[Counter Component] Increment");
export const decrement = createAction("[Counter Component] Decrement");

// Reducer
const counterReducer = createReducer(
  initialState,
  on(increment, (state) => state + 1),
  on(decrement, (state) => state - 1)
);

// Selector
export const selectCount = (state: AppState) => state.count;
```

Hy vọng rằng danh sách các câu hỏi và câu trả lời này sẽ giúp bạn chuẩn bị tốt cho các cuộc phỏng vấn về Angular. Nếu bạn cần thêm thông tin hoặc có câu hỏi khác, hãy để tôi biết!
