---
description: Génère un ensemble de noms WWPN (World World-of-Port).
ms.assetid: 36f393eb-6f34-4ae3-a976-c5da60211f3e
title: Méthode GenerateWwpn de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GenerateWwpn
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1952954d107185fdcc31634b9d0e19bd4cd3450db5a63d78aa3ef823cdf38afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532519"
---
# <a name="generatewwpn-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode GenerateWwpn de la \_ classe VirtualSystemManagementService MSVM

Génère un ensemble de noms WWPN (World World-of-Port). Les WWPN sont générés à partir de la plage préconfigurée définie par les propriétés **MinimumWWPNAddress** et **MaximumWWPNAddress** de la classe [**\_ VirtualSystemManagementServiceSettingData MSVM**](msvm-virtualsystemmanagementservicesettingdata.md) . Si le nombre valide de WWPN pouvant être générés est inférieur au nombre demandé, les entrées restantes du tableau *GeneratedWwpn* auront l’entrée non valide « 0000000000000000 » et la valeur de retour indiquera la réussite (0).

## <a name="syntax"></a>Syntaxe


```mof
uint32 GenerateWwpn(
  [in]  uint32 NumberOfWwpns,
  [out] string GeneratedWwpn[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NumberOfWwpns* \[ dans\]
</dt> <dd>

Nombre de WWPN à générer.

</dd> <dt>

*GeneratedWwpn* \[ à\]
</dt> <dd>

Tableau de chaînes, chacune contenant un WWPN généré. Elle est mise en forme sous forme de chaîne sous la forme « 01:23:45:67:89 : AB : CD : EF ».

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Échec** (32768)
</dt> <dt>

**Accès refusé** (32769)
</dt> <dt>

**Non pris en charge** (32770)
</dt> <dt>

**État inconnu** (32771)
</dt> <dt>

**Délai d’expiration** (32772)
</dt> <dt>

**Paramètre non valide** (32773)
</dt> <dt>

Le **système est en cours d’utilisation** (32774)
</dt> <dt>

**État non valide pour cette opération** (32775)
</dt> <dt>

**Type de données incorrect** (32776)
</dt> <dt>

Le **système n’est pas disponible** (32777)
</dt> <dt>

**Mémoire insuffisante** (32778)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




