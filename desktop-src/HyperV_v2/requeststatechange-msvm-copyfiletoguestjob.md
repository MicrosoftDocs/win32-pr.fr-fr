---
description: Modifie l’état de la tâche.
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: 'Msvm_CopyFileToGuestJob :: RequestStateChange, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: adf5d866989f3b3518cf53b52e073239e023e3c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520599"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a>MSVM \_ CopyFileToGuestJob :: RequestStateChange, méthode

Modifie l’état de la tâche.

## <a name="syntax"></a>Syntaxe


```C++
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RequestedState* \[ dans\]
</dt> <dd>

Nouvel état. Les valeurs possibles sont les suivantes :

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Démarrer** (2)


</dt> <dd>

Modifie l’État en’Running'.

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspendre** (3)


</dt> <dd>

Arrête temporairement le travail. Le client peut ensuite redémarrer le travail avec « Start ». Le client peut éventuellement entrer l’État « service » en suspens (ce qui est spécifique à un travail).

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminer** (4)


</dt> <dd>

Arrête le travail proprement dit, en enregistrant les données, en conservant l’État et en arrêtant tous les processus sous-jacents de manière ordonnée.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Met immédiatement fin à la tâche, sans qu’il soit nécessaire d’enregistrer les données ou de conserver l’État.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)


</dt> <dd>

Place le travail dans un état de service spécifique au fournisseur. Le client peut éventuellement redémarrer le travail.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (7.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*TimeoutPeriod* \[ dans\]
</dt> <dd>

Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État. Le format d’intervalle doit être utilisé pour spécifier le délai d’attente. La valeur 0 ou **null** indique que le client n’a aucune exigence de temps pour la transition. Si cette propriété ne contient pas 0 ou **null** et que l’implémentation ne prend pas en charge ce paramètre, un code de retour de 4098 (**utilisation du paramètre timeout non pris en charge**) doit être retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.



| Code/valeur de retour                                                                                                                                                               | Description                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**Terminé sans erreur**</dt> <dt>0</dt> </dl>                   | Opération réussie.<br/>                                                                |
| <dl> <dt>**Utilisation du paramètre timeout non prise en charge**</dt> <dt>4098</dt> </dl> |                                                                                    |
| <dl> <dt>**Échec**</dt> <dt>32768</dt> </dl>                                |                                                                                    |
| <dl> <dt>**Accès refusé**</dt> <dt>32769</dt> </dl>                         | Accès refusé.<br/>                                                          |
| <dl> <dt>**Non pris en charge**</dt> <dt>32770</dt> </dl>                         |                                                                                    |
| <dl> L' <dt>**État est inconnu**</dt> <dt>32771</dt> </dl>                     |                                                                                    |
| <dl> <dt>**Délai d’expiration**</dt> <dt>32772</dt> </dl>                               |                                                                                    |
| <dl> <dt>**Paramètre non valide**</dt> <dt>32773</dt> </dl>                     |                                                                                    |
| <dl> Le <dt>**système est en cours d’utilisation**</dt> <dt>32774</dt> </dl>                      |                                                                                    |
| <dl> <dt>**État non valide pour cette opération**</dt> <dt>32775</dt> </dl>      | La valeur spécifiée dans le paramètre *RequestedState* n’est pas prise en charge.<br/> |
| <dl> <dt>**Type de données incorrect**</dt> <dt>32776</dt> </dl>                   |                                                                                    |
| <dl> Le <dt>**système n’est pas disponible**</dt> <dt>32777</dt> </dl>               |                                                                                    |
| <dl> <dt>**Mémoire Insuffisante**</dt> <dt>32778</dt> </dl>                         |                                                                                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\\\\\Virtualisation racine \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




