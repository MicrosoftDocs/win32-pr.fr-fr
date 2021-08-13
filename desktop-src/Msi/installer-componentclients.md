---
description: La propriété ComponentClients en lecture seule retourne un objet StringList énumérant l’ensemble des clients d’un composant spécifié.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Installer. ComponentClients, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentClients
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c94a30247bbfc39675308308457c369785bd9a67413a5b0b62af143e17e2112b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632711"
---
# <a name="installercomponentclients-property"></a>Installer. ComponentClients, propriété

La propriété **ComponentClients** en lecture seule retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble des clients d’un composant spécifié.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a>Valeur de la propriété

GUID de chaîne qui représente le code de composant du composant. Les codes des composants sont spécifiés dans la colonne ComponentId de la [table des composants](component-table.md).

## <a name="remarks"></a>Remarques

Pour énumérer les clients du composant, une application peut itérer au sein de l’objet [**StringList**](stringlist-object.md) à l’aide d’une construction for each. Étant donné que les clients ne sont pas triés, les nouveaux composants possèdent un index arbitraire. Cela signifie que la fonction peut retourner des clients dans n’importe quel ordre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




