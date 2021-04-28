---
description: La méthode ModifyServiceSettings de la classe Msvm_MetricService-modifie les données de paramètre pour le service.
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: Méthode ModifyServiceSettings de la classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 088aec001dd63de7344256fd9e114b6ff73e4425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112177"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a>Méthode ModifyServiceSettings de la \_ classe MetricService MSVM

Modifie les données de paramètre pour le service.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SettingData* \[ dans\]
</dt> <dd>

Contient une instance incorporée de la classe [**MSVM \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md) qui contient les données de paramètre modifiées pour le service.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne l’une des valeurs suivantes.



| Code/valeur de retour                                                                                                                                                                | Description                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**Terminé sans erreur**</dt> <dt>0</dt> </dl>                    | Réussite.<br/>                                |
| <dl> <dt>**Paramètres de méthode activés-travail démarré**</dt> <dt>4096</dt> </dl> | Paramètres de méthode vérifiés, tâche démarrée.<br/> |
| <dl> <dt>**Échec**</dt> <dt>32768</dt> </dl>                                 | Échec.<br/>                                 |
| <dl> <dt>**Accès refusé**</dt> <dt>32769</dt> </dl>                          | Accès refusé.<br/>                          |
| <dl> <dt>**Non pris en charge**</dt> <dt>32770</dt> </dl>                          | Non pris en charge.<br/>                          |
| <dl> L' <dt>**État est inconnu**</dt> <dt>32771</dt> </dl>                      | L’état est inconnu.<br/>                      |
| <dl> <dt>**Délai d’expiration**</dt> <dt>32772</dt> </dl>                                | Délai d’attente.<br/>                               |
| <dl> <dt>**Paramètre non valide**</dt> <dt>32773</dt> </dl>                      | Paramètre non valide.<br/>                      |
| <dl> Le <dt>**système est en cours d’utilisation**</dt> <dt>32774</dt> </dl>                       | Le système est en cours d’utilisation.<br/>                       |
| <dl> <dt>**État non valide pour cette opération**</dt> <dt>32775</dt> </dl>       | État non valide pour cette opération.<br/>       |
| <dl> <dt>**Type de données incorrect**</dt> <dt>32776</dt> </dl>                    | Type de données incorrect.<br/>                    |
| <dl> Le <dt>**système n’est pas disponible**</dt> <dt>32777</dt> </dl>                | Le système n’est pas disponible.<br/>                |
| <dl> <dt>**Mémoire Insuffisante**</dt> <dt>32778</dt> </dl>                          | Mémoire insuffisante.<br/>                          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

