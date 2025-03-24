using System.Collections;
using System.Collections.Generic;
using UnityEngine;

namespace Valve.VR.InteractionSystem.Sample
{
  public class TeleportOnClick : MonoBehaviour
    {
        public GameObject destination;
        public GameObject playerToTeleport;
        public void teleportPlayer(Hand hand)
        {
            playerToTeleport.transform.position = destination.transform.position;
            Debug.Log("Teleporting player!"); 
           
        }
    }
}
