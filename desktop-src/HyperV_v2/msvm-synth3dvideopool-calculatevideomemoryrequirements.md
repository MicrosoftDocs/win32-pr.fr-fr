---
description: Calcule la quantité de mémoire vidéo requise pour une machine virtuelle RemoteFX.
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: Méthode CalculateVideoMemoryRequirements de la classe Msvm_Synth3dVideoPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool.CalculateVideoMemoryRequirements
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2a9fd80e777a9d166b896c2ce51d03bd91bbabfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113630"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a>Méthode CalculateVideoMemoryRequirements de la \_ classe Synth3dVideoPool MSVM

Calcule la quantité de mémoire vidéo requise pour une machine virtuelle RemoteFX.

## <a name="syntax"></a>Syntaxe


```mof
uint32 CalculateVideoMemoryRequirements(
  [in]  uint32 monitorResolution,
  [in]  uint32 numberOfMonitors,
  [out] uint64 requiredVideoMemory
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*monitorResolution* \[ dans\]
</dt> <dd>

Résolution maximale de l’écran pour l’ordinateur virtuel. Il doit s’agir de l’une des valeurs suivantes.



| Valeur                                                                        | Signification                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>0</dt> </dl> | La résolution maximale est de 1024 768.<br/>  |
| <dl> <dt>1</dt> </dl> | La résolution maximale est de 1280 1024.<br/> |
| <dl> <dt>2</dt> </dl> | La résolution maximale est de 1600 1200.<br/> |
| <dl> <dt>3</dt> </dl> | La résolution maximale est de 1920 1200.<br/> |



 

</dd> <dt>

*numberOfMonitors* \[ dans\]
</dt> <dd>

Nombre maximal d’analyses pour l’ordinateur virtuel. Le nombre minimal d’analyses est de 1 et la valeur maximale dépend de la résolution d’écran maximale. Le tableau suivant définit le nombre maximal d’analyses autorisées pour différentes résolutions.



| Résolution             | Nombre maximal d’écrans |
|------------------------|------------------|
| 1024 768<br/>  | 4<br/>     |
| 1280 1024<br/> | 4<br/>     |
| 1600 1200<br/> | 3<br/>     |
| 1920 1200<br/> | 2<br/>     |



 

</dd> <dt>

*requiredVideoMemory* \[ à\]
</dt> <dd>

Reçoit la quantité de mémoire vidéo requise, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un code d’État, qui peut prendre l’une des valeurs suivantes.



| Code/valeur de retour                                                                                                                                                                | Description                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**Terminé sans erreur**</dt> <dt>0</dt> </dl>                    | Vendu.<br/>                                |
| <dl> <dt>**Paramètres de méthode activés-travail démarré**</dt> <dt>4096</dt> </dl> | Travail démarré.<br/>                               |
| <dl> <dt>**Échec**</dt> <dt>32768</dt> </dl>                                 | Échec.<br/>                                    |
| <dl> <dt>**Accès refusé**</dt> <dt>32769</dt> </dl>                          | Accès refusé.<br/>                             |
| <dl> <dt>**Non pris en charge**</dt> <dt>32770</dt> </dl>                          | Non pris en charge.<br/>                             |
| <dl> L' <dt>**État est inconnu**</dt> <dt>32771</dt> </dl>                      | L’état est inconnu.<br/>                         |
| <dl> <dt>**Délai d’expiration**</dt> <dt>32772</dt> </dl>                                | Délai d’expiration.<br/>                                   |
| <dl> <dt>**Paramètre non valide**</dt> <dt>32773</dt> </dl>                      | Un paramètre n'est pas valide.<br/>                  |
| <dl> Le <dt>**système est en cours d’utilisation**</dt> <dt>32774</dt> </dl>                      | Le système est en cours d’utilisation.<br/>                          |
| <dl> <dt>**État non valide pour cette opération**</dt> <dt>32775</dt> </dl>       | L’État n’est pas valide pour cette opération.<br/> |
| <dl> <dt>**Type de données incorrect**</dt> <dt>32776</dt> </dl>                    | Type de données incorrect.<br/>                       |
| <dl> Le <dt>**système n’est pas disponible**</dt> <dt>32777</dt> </dl>                | Le système n’est pas disponible.<br/>                   |
| <dl> <dt>**Mémoire Insuffisante**</dt> <dt>32778</dt> </dl>                          | Mémoire insuffisante.<br/>                             |



 

## <a name="remarks"></a>Notes

Cette méthode est généralement appelée sur le système hôte pour déterminer si l’ordinateur hôte dispose de suffisamment de mémoire vidéo pour héberger une machine virtuelle RemoteFX. Pour ce faire, vous comparez la quantité de mémoire vidéo calculée par cette méthode avec la propriété [**MSVM \_ PhysicalGPUInfo. AvailableVideoMemory**](msvm-physicalgpuinfo.md) pour déterminer si l’ordinateur hôte dispose de suffisamment de mémoire vidéo. Vous pouvez utiliser ces informations pour déterminer si une machine virtuelle peut être déplacée vers le système hôte.

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

[**MSVM \_ PhysicalGPUInfo**](msvm-physicalgpuinfo.md)
</dt> <dt>

[**MSVM \_ Synth3dVideoPool**](msvm-synth3dvideopool.md)
</dt> </dl>

 

 




