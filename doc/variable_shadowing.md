# Variable shadowing

https://en.wikipedia.org/wiki/Variable_shadowing

Examples of variable shadowing with synergy with affine types (move semantics):

    x = x.unwrap // e.g. change from an object to its primitive type

    x = x.validate // e.g. if valid, then return self, else throw

    x = x.sanitize // e.g. untaint, trim, chop, etc.

Examples of variable shadowing for functional changes:

    x = typecast(x)  // e.g. change from one type to another type

    x = decorate(x) // e.g. add info to the object

    x = combine(x, y, z) // e.g. merge, intersect, union, min, max 

Example of variable shadowing for changing mutability/immutability:

    let mut vec = Vec::new(); // vec is mutable
    vec.push(a);
    let vec = vec; // vec immutable

Some languages allow variable shadowing.

Some languages allow variable shadowing with type changes.

Some languages can show warnings when a variable shadowing happens, or when a variable is unused.

Some languages (e.g. Rust) have variable shadowing automatically from supporting shadowing-in-general (idents in enclosing scopes) and the ability to declare new variables mid-block. Each new decl opens a new implicit scope from its point-of-decl to the end of its lexical block.
