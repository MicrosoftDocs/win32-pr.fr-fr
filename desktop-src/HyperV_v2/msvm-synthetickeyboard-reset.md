---
description: 'Méthode Reset de la classe Msvm_SyntheticKeyboard : réinitialise le clavier virtuel.'
ms.assetid: 2a943dd8-3b94-4b20-8786-7f9d8b0aeaa6
title: Méthode Reset de la classe Msvm_SyntheticKeyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7b519177c604ccd7017e8007715672d2cbcd0e101230efd191aaec3c0d8d90d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392047"
---
# <a name="reset-method-of-the-msvm_synthetickeyboard-class"></a>Méthode Reset de la \_ classe MSVM SyntheticKeyboard

Réinitialise le clavier virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 Reset();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

En cas de réussite, retourne 0 ; Sinon, retourne une erreur.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ SyntheticKeyboard**](msvm-synthetickeyboard.md)
</dt> </dl>

 

 




