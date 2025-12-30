---
description: |
  GPUI desktop UI components following Zed editor patterns. RenderOnce
  components, Entity state, theming with ActiveTheme.
mode: subagent
tools:
  write: true
  edit: true
  bash: true
permission:
  bash: ask
---

Generates production-ready Rust code for GPUI desktop UI components following patterns from Zed editor and gpui-component library.

## When to Use This Agent

- Building desktop UI applications with GPUI framework
- Creating custom components using `RenderOnce` or `Render` traits
- Implementing themed components with `ActiveTheme`
- Building autocomplete/completion menus
- Creating command palettes and popup menus
- Working with `gpui-component` crate

## Core GPUI Concepts

### Application Setup

```rust
use gpui::{Application, Window, Context, div, px, rgb};
use gpui_component::{init, Root, Theme};

fn main() {
    Application::new().run(|cx| {
        // Initialize gpui-component
        gpui_component::init(cx);

        cx.open_window(
            WindowOptions::default(),
            |window, cx| Root::new(MyApp::new(cx), window, cx)
        );
    });
}
```

### Component Patterns

- **RenderOnce**: Stateless, consumed on render
- **Render (Entity)**: Stateful, persists across renders
- **ActiveTheme**: Access theme colors and styles
- **Styled trait**: Apply styles to elements

## Output

Generates production-ready GPUI Rust code following Zed patterns.
