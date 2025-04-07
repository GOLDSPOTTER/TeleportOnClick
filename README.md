using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using static UnityEngine.UI.Image;

namespace Valve.VR.InteractionSystem.Sample
{
  public class TeleportOnClick : MonoBehaviour
    {
        public GameObject destination;
        public GameObject playerToTeleport;

        public void teleportPlayer(Hand hand)
        {
            Debug.Log("Teleporting player!");

            GameObject Camera = GameObject.Find("FallbackObjects");
            if (Camera != null)
            {
                playerToTeleport.transform.position = destination.transform.position;
                Camera.transform.localPosition = new Vector3(0, 1.75f, 0);
            }
   
           
        }
    }
}
