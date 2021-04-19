---
description: La propriété ShortcutTarget de l’objet installer examine un raccourci et retourne son produit, son nom de fonctionnalité et son composant, le cas échéant.
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: Installer. ShortcutTarget, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ShortcutTarget
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1c53d43188af9ed8f58ddd54916761e346f1bad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535360"
---
# <a name="installershortcuttarget-property"></a>Installer. ShortcutTarget, propriété

La propriété **ShortcutTarget** de l’objet [**installer**](installer-object.md) examine un raccourci et retourne son produit, son nom de fonctionnalité et son composant, le cas échéant.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a>Valeur de la propriété

Chemin d’accès complet et nom de fichier du fichier.

## <a name="remarks"></a>Notes

ShortcutTarget retourne un [**objet record**](record-object.md) qui contient trois champs :

-   Le champ 1 est un GUID pour le code de produit du raccourci, s’il est disponible. Ce champ peut avoir la valeur null.
-   Le champ 2 est l’ID de fonctionnalité du raccourci, s’il est disponible. Ce champ peut avoir la valeur null.
-   Le champ 3 est un GUID pour le code du composant, s’il est disponible. Ce champ peut avoir la valeur null.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




