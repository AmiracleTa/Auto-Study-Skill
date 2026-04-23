# browser

Use agent-browser directly as needed. Check the agent-browser skill for details.

## Use this file when

- Need to open or connect to a browser through CDP.

## Default

- The default CDP port is 9344 (**not** browser of openclaw).
- On Windows, use a browser profile stored at `%LOCALAPPDATA%\AutoStudy\browser`.
- On macOS, use a browser profile stored at `~/Library/Application Support/AutoStudy/browser`.

## What to do

Check the default CDP port, which is usually 9344. If a browser session is already available on that port, attach to it directly. Otherwise, start or restore Chrome on the current host, or start Windows Chrome when running from WSL, then attach as needed.

If you need to switch to a different persistent profile or other launch options, close existing `agent-browser` sessions first. A running daemon may ignore new launch options such as `--profile`.
