# Observer React

Create components which re-render for each value emitted by an Observable.

## Usage

```jsx
import { Observer } from "observer-react"

// Then, in some rendering body or pure return

    <Observer
        of={this.props.stagedFile.uploadProgress)}
        init={() => <LoadingSpinner/>}
        next={percentComplete => <ProgressBar progress={percentComplete * 0.01}/>}
        complete={() => <Okay/>}
    />
```
