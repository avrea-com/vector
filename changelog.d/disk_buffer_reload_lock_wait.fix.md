Fixed configuration reloads that change a sink's disk buffer intermittently failing with
`failed to lock buffer.lock; is another Vector process running and using this buffer?`. The new
buffer now waits for the previous instance in the same process to release its lock.

authors: fingon
