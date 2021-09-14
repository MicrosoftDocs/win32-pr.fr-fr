---
description: La propriété Environment de l’objet installer est une propriété en lecture-écriture qui est la valeur de chaîne d’une variable d’environnement du processus en cours.
ms.assetid: f59a270f-9bd8-4d17-96e2-cb3c62a31cad
title: Installer. Environment, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Environment
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3983eceecd8bc709bea4a094c61c9886c73def3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121621"
---
# <a name="installerenvironment-property"></a>Installer. Environment, propriété

La propriété **Environment** de l’objet [**installer**](installer-object.md) est une propriété en lecture-écriture qui est la valeur de chaîne d’une variable d’environnement du processus en cours.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a>Valeur de la propriété

Nom de la variable d’environnement à lire ou à écrire. Cela ne tient pas compte de la casse.

## <a name="remarks"></a>Notes

La définition d’une variable d’environnement avec la propriété d' **environnement** affecte uniquement la session active. Pour apporter des modifications persistantes à une variable d’environnement, utilisez la [table d’environnement](environment-table.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




