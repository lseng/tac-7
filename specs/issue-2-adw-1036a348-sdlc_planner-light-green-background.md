# Chore: Background color update to light green

## Metadata
issue_number: `2`
adw_id: `1036a348`
issue_json: `{"number":2,"title":"Background color update","body":"/chore - adw_sdlc_ZTE_iso - Update the background color to the equivalent light green color"}`

## Chore Description
Update the application's background color from the current light sky blue (#E0F6FF) to an equivalent light green color. This change should provide a fresh appearance while maintaining good readability and visual hierarchy across the application. The light green color should be chosen to match the tone and brightness of the current light sky blue, ensuring a smooth visual transition.

## Relevant Files
Use these files to resolve the chore:

- `app/client/src/style.css` - Contains the CSS variable `--background` (line 9) that controls the application's background color. This is the primary file that needs to be updated.
- `app_docs/feature-6445fc8f-light-sky-blue-background.md` - Documentation showing the previous background color change to light sky blue, providing context on how background changes should be implemented.
- `app_docs/feature-f055c4f8-off-white-background.md` - Documentation showing an earlier background color change, providing additional context on the implementation pattern.

## Step by Step Tasks
IMPORTANT: Execute every step in order, top to bottom.

### 1. Update Background Color Variable
- Open `app/client/src/style.css`
- Locate the `--background` CSS variable on line 9
- Change the value from `#E0F6FF` (light sky blue) to an equivalent light green color
- Select a light green hex color that matches the tone and brightness of the current light sky blue (suggested: `#E0F6E8` or similar light mint green)
- Ensure the new color maintains good contrast with existing text colors (`--text-primary: #2c3e50` and `--text-secondary: #495057`)

### 2. Verify CSS Variable Usage
- Confirm that the `--background` variable is properly used in the `body` selector (line 30: `background: var(--background);`)
- No other changes should be needed as all sections inherit this background color through the CSS variable system

### 3. Run Validation Commands
Execute the validation commands listed below to ensure the chore is complete with zero regressions.

## Validation Commands
Execute every command to validate the chore is complete with zero regressions.

- `cd app/server && uv run pytest` - Run server tests to validate the chore is complete with zero regressions
- `cd app/client && bun run build` - Build the client to ensure there are no build errors

## Notes
- The light green color should be equivalent in tone and brightness to the current light sky blue (#E0F6FF)
- Suggested light green colors: `#E0F6E8` (light mint green), `#E0F5E8` (pale green), or `#DFF6E5` (light sage green)
- The change is purely visual and should not affect any functionality
- All UI components (buttons, cards, modals) should maintain their proper visual hierarchy with the new background
- This follows the same pattern as previous background color updates (off-white and light sky blue)
- Consider creating documentation in `app_docs/` after implementation to maintain the pattern of documenting visual changes
