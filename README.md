# ui
Cross platform UI library for Hascal

```typescript
if ui_begin_window(ctx, "My Window", ui_rect(10, 10, 140, 86)) {
  ui_layout_row(ctx, 2, ([int]) { 60, -1 }, 0)

  ui_label(ctx, "First:")
  if ui_button(ctx, "Button1") {
    print("Button1 pressed\n")
  }

  ui_label(ctx, "Second:")
  if ui_button(ctx, "Button2") {
    ui_open_popup(ctx, "My Popup")
  }

  if ui_begin_popup(ctx, "My Popup") {
    ui_label(ctx, "Hello world!")
    ui_end_popup(ctx)
  }

  ui_end_window(ctx)
}
```
