# Tree component

Add import and use the component

```tsx title="TreeExample.tsx"
import {classes, st} from './tree-example.st.css';
// highlight-start
import {Tree} from 'stylable-components';
// highlight-end

export interface TreeExampleProps {
    className?: string;
}

export const TreeExample = ({className}: TreeExampleProps) => {
    return (
        <div className={st(classes.root, className)}>
            // highlight-start
            <Tree/>
            // highlight-end
        </div>
    );
};
```

Now you'd need some mandatory props;

First — tree data structure; component works with whole object up-front.

Second — ID getter

getId: (item: TreeItem) => string
