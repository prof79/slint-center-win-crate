# slint-center-win 0.2.0

Center a [Slint](https://slint.dev) window running on a `winit` backend.

## Usage

```rust
use slint_center_win::center_window;

slint::include_modules!();

fn main() -> Result<(), slint::PlatformError> {
    // See: https://slint.dev/releases/1.5.1/docs/rust/slint/docs/generated_code/struct.SampleComponent
    let ui = AppWindow::new()?;

    // Window must be shown first so sizes get calculated properly
    // Don't know if there is a better way, slight redraw artifacting on move
    ui.show()?;

    center_window(ui.window());

    // ...

    ui.run()
}
```

## Releases

### v0.2.0

Updated/streamlined for Slint v1.5.*.

### v0.1.2

Initial release.

## Disclaimer

Neither do I claim this to be pretty nor working in all cases.

Please see external discussions [#4376](https://github.com/slint-ui/slint/issues/4376) and [#3859](https://github.com/slint-ui/slint/discussions/3859).

-- prof79
