
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Trampoline : MonoBehaviour
{
    public float jumpStrength = 2  ;
    void OnTriggerEnter(Collider other)
    {
        other.GetComponent<Jump>().jumpStrength *= 2;
    }
    void OnTriggerExit(Collider other)
    {
        other.GetComponent<Jump>().jumpStrength /= 2;
    }

}
