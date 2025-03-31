# hide-admin-notifications
Simple Snippet to hide admin notifications

```
function hide_all_admin_notices() {
    global $wp_filter;

    if (isset($wp_filter['admin_notices'])) {
        // Remove all actions hooked to the 'admin_notices' hook.
        unset($wp_filter['admin_notices']);
    }
}

add_action('admin_init', 'hide_all_admin_notices');
```
