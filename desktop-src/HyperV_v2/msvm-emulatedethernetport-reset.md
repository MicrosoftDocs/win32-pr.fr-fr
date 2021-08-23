---
description: Réinitialise l’appareil virtuel.
ms.assetid: e4eb3952-a58e-4acd-85df-205d6ed23133
title: Méthode Reset de la classe Msvm_EmulatedEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPort.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1860738c08ad5711a610e76b17d2e19e7d062d67501d17ecfbc74de8e0f1117e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525039"
---
# <a name="reset-method-of-the-msvm_emulatedethernetport-class"></a>Méthode Reset de la \_ classe MSVM EmulatedEthernetPort

Réinitialise l’appareil virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 Reset();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

La méthode retourne l'une des valeurs suivantes :

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md)
</dt> </dl>

 

 




