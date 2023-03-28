<script>
    const skills = [
        {
            id: 0,
            level: 80,
            description: 'Flutter'
        },
        {
            id: 1,
            level: 70,
            description: 'Python'
        },
        {
            id: 2,
            level: 75,
            description: 'ReactJS'
        },
    ];
</script>

<style>
    /* your styles go here */
</style>

<div class="Skills">
    <h3>Skills</h3>
    { #each skills as { level, description } }
        <li> <strong>{ description }</strong>: { level }%</li>
    { /each }
</div>