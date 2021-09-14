---
description: la propriété Version de l’objet Installer est une propriété en lecture seule qui est la représentation sous forme de chaîne de la Version actuelle de Windows Installer. La chaîne est retournée sous la forme suivante.
ms.assetid: 9af262f0-b573-471d-aac6-6a72e8cb5314
title: Installer. version, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Version
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 29af85b8fc1afe468dc87d5516da9a528024c73a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012074"
---
# <a name="installerversion-property"></a>Installer. version, propriété

la propriété **Version** de l’objet [**Installer**](installer-object.md) est une propriété en lecture seule qui est la représentation sous forme de chaîne de la Version actuelle de Windows Installer. La chaîne est retournée sous la forme suivante.

*majeure*. *mineure*. *générer*. *mettre à jour*

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.Version
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




