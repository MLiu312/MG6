# MG6
1. The entire for loop will complete before the Update finishes, so extremely long for-loops will cause the game to lag, as each Update() must wait for the loop to complete first.

2. If the player is still in the air but no longer rising, the platform will attempt to nudge them out, as the logic of "if (_rigidbody.linearVelocityY > 0)" only checks if the player has any positive upwards movement, meaning if the player is falling downwards but is still in the air, the game will re-enable colliders, and thus the platforms will turn solid and try to move the player out.
