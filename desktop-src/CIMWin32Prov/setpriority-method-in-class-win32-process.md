---
description: SetPriority&\# 32 ; La méthode de classe WMI tente de modifier la priorité d’exécution du processus.
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: Méthode SetPriority de la classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.SetPriority
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: decd5892d480e4f236ae9d7acdc1a25c018557166535c963eb35dc3f6f62ffa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675568"
---
# <a name="setpriority-method-of-the-win32_process-class"></a>Méthode SetPriority de la \_ classe Process Win32

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPriority** tente de modifier la priorité d’exécution du processus.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Priorité* \[ dans\]
</dt> <dd>

Nouvelle classe de priorité pour le processus. Notez que ces valeurs sont différentes de celles explicitement indiquées dans la propriété **Priority** du [**\_ processus Win32**](win32-process.md).

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inactif** (64)


</dt> <dd>

Spécifié pour un processus avec des threads qui s’exécutent uniquement lorsque le système est inactif. Les threads du processus sont reportés par les threads d’un processus qui s’exécutent dans une classe de priorité plus élevée, par exemple un économiseur d’écran. La classe idle-priority est héritée par les processus enfants.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Inférieure** à la normale (16384)


</dt> <dd>

Indique un processus qui a une priorité supérieure à la **\_ \_ classe de priorité inactive**, mais qui se trouve en dessous de la **\_ \_ classe de priorité normale**.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)


</dt> <dd>

Spécifié pour un processus sans besoins de planification spéciaux.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Au-dessus** de la normale (32768)


</dt> <dd>

Indique un processus qui a une priorité supérieure à la **\_ \_ classe de priorité normale**, mais qui se trouve en dessous de la **\_ \_ classe de priorité élevée**.

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**Haute priorité** (128)


</dt> <dd>

Spécifié pour un processus qui exécute des tâches critiques à l’heure qui doivent être exécutées immédiatement. Les threads du processus prévalent sur les threads de processus de classe de priorités normale ou inactive. Par exemple, la Liste des tâches, qui doit répondre rapidement lorsqu’elle est appelée par l’utilisateur, quelle que soit la charge sur le système d’exploitation. Soyez extrêmement vigilant lorsque vous utilisez la classe de priorité élevée, car une application de classe de priorité élevée peut utiliser presque tout le temps processeur disponible.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Temps réel** (256)


</dt> <dd>

Spécifié pour un processus qui a la priorité la plus élevée possible. Les threads du processus devancent les threads de tous les autres processus, y compris les processus du système d’exploitation qui effectuent des tâches importantes. Par exemple, un processus en temps réel qui s’exécute depuis plus d’un intervalle très court peut empêcher le vidage du cache disque ou la non-réponse d’une souris.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Achèvement réussi** (0)
</dt> <dt>

**Accès refusé** (2)
</dt> <dt>

**Privilèges insuffisants** (3)
</dt> <dt>

**Échec inconnu** (8)
</dt> <dt>

**Chemin introuvable** (9)
</dt> <dt>

**Paramètre non valide** (21)
</dt> <dt>

**Autre** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Remarques

pour définir la priorité en temps réel, l’appelant doit disposer de **SeIncreaseBasePriorityPrivilege** (**privilège de \_ priorité de \_ BASE \_ \_ SE INC**). Sans ce privilège, la priorité la plus élevée peut être définie sur la priorité haute.

## <a name="examples"></a>Exemples

L’exemple de [modification de la priorité d’un processus en cours d’exécution](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript modifie la priorité d’une instance en cours d’exécution de Notepad.exe de la normale à au-dessus de la normale.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Processus Win32**](win32-process.md)
</dt> </dl>

 

