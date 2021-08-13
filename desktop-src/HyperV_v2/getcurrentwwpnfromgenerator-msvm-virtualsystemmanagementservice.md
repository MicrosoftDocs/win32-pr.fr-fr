---
description: Offre la possibilité de prévisualiser le nom WWPN (World-World Name Name) actuel sans que le WWPN soit réservé.
ms.assetid: 7fc02099-744e-4a56-ae4b-1f5fd6a1eb45
title: Méthode GetCurrentWwpnFromGenerator de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetCurrentWwpnFromGenerator
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 196ad781075128eab42c6daabf7d6ccd6906df1e67e348ebea0d9418cbb08c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393281"
---
# <a name="getcurrentwwpnfromgenerator-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode GetCurrentWwpnFromGenerator de la \_ classe VirtualSystemManagementService MSVM

Offre la possibilité de prévisualiser le nom WWPN (World-World Name Name) actuel sans que le WWPN soit réservé. Le WWPN est généré à partir de la plage préconfigurée définie par les propriétés **MinimumWWPNAddress** et **MaximumWWPNAddress** de la classe [**\_ VirtualSystemManagementServiceSettingData MSVM**](msvm-virtualsystemmanagementservicesettingdata.md) . Si la plage définie par ces propriétés est épuisée, le WWPN généré aura l’entrée non valide « 0000000000000000 » et la valeur de retour indiquera Success (0).

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetCurrentWwpnFromGenerator(
  [out] string CurrentWwpn
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CurrentWwpn* \[ à\]
</dt> <dd>

Chaîne qui aura la valeur de l’objet WWPN actuel tel qu’il est utilisé par le générateur WWPN. Il s’agit de la même valeur que celle qui sera le premier WWPN généré par l’appel suivant à [**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md). Elle est mise en forme sous forme de chaîne sous la forme « 01:23:45:67:89 : AB : CD : EF ».

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

 

 




