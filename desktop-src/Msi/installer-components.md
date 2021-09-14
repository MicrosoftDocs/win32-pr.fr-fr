---
description: La propriété composants en lecture seule retourne un objet StringList énumérant l’ensemble des composants installés pour tous les produits.
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: Installer. Components, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Components
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6767be5182b15836c071bf8b00ed8441f6031dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121654"
---
# <a name="installercomponents-property"></a>Installer. Components, propriété

La propriété **composants** en lecture seule retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble des composants installés pour tous les produits.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

Pour énumérer les composants, une application peut itérer au sein de l’objet [**StringList**](stringlist-object.md) à l’aide d’une construction for each. Comme les composants ne sont pas triés, tous les nouveaux composants possèdent un index arbitraire. Cela signifie que la fonction peut retourner des composants dans n’importe quel ordre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




