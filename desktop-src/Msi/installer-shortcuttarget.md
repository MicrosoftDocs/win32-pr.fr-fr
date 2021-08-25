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
ms.openlocfilehash: b54e334314c0bfd0fb721b175d0a14894d8a509ea02ff36e324903bb1fdbffaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893999"
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

## <a name="remarks"></a>Remarques

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

 

 




