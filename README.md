# Week7-Assignment
 - Assembled a bunch of free assets, including an exibition hall, rotating planets, Moon and Mars terrians.
 - Earth-Moon Orbit rotation, Mars rotation. (by y-axis)  
 - Poorly made UI interaction in mainScene, canvas show when player get into trigger zone which covered the earth- moon Orbit and the Mars, hide when exit trigger zone.  
 - Player controller: movement (WASD& Four Arrows), interaction：in mainScene (N jump to MoonScene, M jump to MarsScene ), in MoonScene & MarsScene( click "Space" jump back to mainScene).  
 - First-person camera responds to mouse motion.  
 - Sound effect in MarsScene(have to wait a few seconds).  
 - ESC key for exit game.

# Week8-Assignment updated  
- Used raycast interaction replaced the UI action.
- Last version the canvas will be activated via OnTriggerEnter, which the active zone is actually a box collider zone.

        Ray ray = new Ray(transform.position, transform.forward);
        RaycastHit hit;

        if (Physics.Raycast(ray, out hit, distance))
        {
            if (hit.collider.CompareTag("TrackingObject"))
            {
                canvas.SetActive(true);
            }
        }
        else
        {
            canvas.SetActive(false);
        }
