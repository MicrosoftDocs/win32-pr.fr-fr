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
ms.openlocfilehash: b3d2aeb845647317751eba53caae1609f8d3d66f9f7d373aa7faa24e3b8cdfb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119295545"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




