# Example

## [17.1] Hello world

Create a project

`nc project add hello_world`

```
// generated tree
hello_world/
 - concept/ // project source code
    - program.ngl // the main file containing the entry point of the program

 - ngl.ngl // description of ngl itself
 - project.ngl // description of the project
```

```
// project.ngl
ngl::io = [ngl::console] // ngl default write to console
```

```
// program.ngl
// ngl:cluster:use<io> // only required on conflicts

ngc:program
{
    ngc:write<[Hello world]>
}


```

## [17.2] Cluster

## [17.3] Web framework

````
// /home/
// /game/{game_id}
// /game/{game_id}/spec/{player_id}

ngc:view
{
    .ngl.data.shape ngs:html
}

ngc controller
{
    <ngc> name
    // ngl:meta<name>.shape // for app:game, shape = ngc<ngc:integer>
    framework.post_data< ngl:meta<name>.required<0>.name > // post_data["id"]
    ngl:meta<name>.parameterize<0, post_data_value>
}

ngc:application<web> app
{
    ngc home
    ngc game
    {
        ngc:integer <id>

        ngc spec
        {
            ngc:integer <player_id>
        }
    }
}

ngc:view<app:home>
{
    <p>Hi $app.user$ is home</p>
}

// app:game required parameters are parameterized by controller
ngc:controller<app:game>
{
    .id
}

````

## [17.4] Parallelism
## [17.5] Executors
## [17.6] GUI