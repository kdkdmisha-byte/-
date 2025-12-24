# -
вау

первые скрипты

  скрипт для батута

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Trampoline : MonoBehaviour
{
    public float jumpFactor = 2.5f;

    void OnTriggerEnter(Collider other)
    {
        //Увеличение скорости бега игрока
        other.GetComponent<FirstPersonMovement>().runSpeed *= speedFactor;
    }

    void OnTriggerExit(Collider other)
    {
        //Уменьшение скорости бега игрока
        other.GetComponent<FirstPersonMovement>().runSpeed /= speedFactor;
    }
}
