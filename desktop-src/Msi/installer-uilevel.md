---
description: La propriété UILevel de l’objet installer est une propriété en lecture-écriture qui indique le type d’interface utilisateur à utiliser lors de l’ouverture et du traitement des packages suivants dans l’espace de processus actuel.
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: Installer. UILevel, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UILevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: de6bda93b5607e00544a69c917a6a238b596c581
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012077"
---
# <a name="installeruilevel-property"></a>Installer. UILevel, propriété

La propriété **UILevel** de l’objet [**installer**](installer-object.md) est une propriété en lecture-écriture qui indique le type d’interface utilisateur à utiliser lors de l’ouverture et du traitement des packages suivants dans l’espace de processus actuel.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes



| Niveau de l’interface utilisateur   | Valeur | Description                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msiUILevelNoChange     | 0     | Ne modifie pas le niveau de l’interface utilisateur.                                                                                                                                                                          |
| msiUILevelDefault      | 1     | Utilise le niveau d’interface utilisateur par défaut.                                                                                                                                                                             |
| msiUILevelNone         | 2     | Installation sans assistance.                                                                                                                                                                               |
| msiUILevelBasic        | 3     | Progression et gestion des erreurs simples.                                                                                                                                                                |
| msiUILevelReduced      | 4     | L’interface utilisateur créée et les boîtes de dialogue de l’Assistant ont été supprimées.                                                                                                                                                    |
| msiUILevelFull         | 5     | Interface utilisateur créée avec les assistants, la progression et les erreurs.                                                                                                                                                    |
| msiUILevelHideCancel   | 32    | En cas de combinaison avec la valeur msiUILevelBasic, le programme d’installation affiche des boîtes de dialogue de progression, mais n’affiche pas de bouton **Annuler** dans la boîte de dialogue pour empêcher les utilisateurs d’annuler l’installation. |
| msiUILevelProgressOnly | 64    | En cas de combinaison avec la valeur msiUILevelBasic, le programme d’installation affiche des boîtes de dialogue de progression, mais n’affiche pas de boîtes de dialogue modales ou de boîtes de dialogue d’erreur.                                        |
| msiUILevelEndDialog    | 128   | S’il est associé à une valeur ci-dessus, le programme d’installation affiche une boîte de dialogue modale à la fin d’une installation réussie ou en cas d’erreur. Aucune boîte de dialogue ne s’affiche si l’utilisateur annule. |



 

Voir aussi [détermination du niveau d’interface utilisateur à partir d’une action personnalisée](determining-ui-level-from-a-custom-action.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




