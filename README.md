# -


  скрипт для батута








using System.Collections;
using System.Collections.Generic;
using UnityEngine;

  public class Trampoline : MonoBehaviour
  {
    
    public float jumpFactor = 2.5f;

    void OnTriggerEnter(Collider other)
    {
        //Увеличение прыжка игрока
        other.GetComponent<jump>().jumpstrength *= jumpFactor;
    }

    void OnTriggerExit(Collider other)
    {
        //Уменьшение скорости прыжка бега игрока
        other.GetComponent<jump>().jumpStrength /= jumpFactor;
    }
}

