---
description: Demande une réinitialisation.
ms.assetid: c69b5c65-8f00-48ed-8602-7e0c5a76653d
title: Méthode Reset de la classe Msvm_Processor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Processor.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aaa0c74ac71e4c3d1be4b9580353c15f5ed94dca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518295"
---
# <a name="reset-method-of-the-msvm_processor-class"></a>Méthode Reset de la \_ classe de processeur MSVM

Demande une réinitialisation.

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

[**\_Processeur MSVM**](msvm-processor.md)
</dt> </dl>

 

 




