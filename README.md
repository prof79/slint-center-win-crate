# slint-center-win 0.1.2
Center a [Slint](https://slint.dev) window running on a `winit` backend.

## Usage
    use slint_center_win::center_window;

    slint::include_modules!();

    fn main() -> Result<(), slint::PlatformError> {
        // See: https://slint.dev/releases/1.3.2/docs/rust/slint/docs/generated_code/struct.SampleComponent
        let ui = AppWindow::new()?;

        // Window must be shown first so sizes get calculated properly
        // Don't know if there is a better way, slight redraw artifacting on move
        ui.show()?;

        center_window(ui.window());

        // ...

        ui.run()
    }

## Disclaimer
Neither do I claim this to be pretty nor working in all cases.

Please see external discussions [#4376](https://github.com/slint-ui/slint/issues/4376) and [#3859](https://github.com/slint-ui/slint/discussions/3859).

-- prof79
