# JustRead


app.get('/deleteResource', (req, res) => {
    const { id, action } = req.query;

    if (action === 'delete') {
        // Perform the delete operation
        // Assume deleteResourceById is a function that deletes the resource
        deleteResourceById(id);
        res.send(`Resource with ID ${id} deleted`);
    } else {
        res.status(400).send('Invalid action');
    }
});
