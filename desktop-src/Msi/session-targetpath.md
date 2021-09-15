---
description: La propriété TargetPath de l’objet session est une propriété en lecture-écriture qui fournit le chemin d’accès complet au dossier désigné sur le lecteur cible de l’installation.
ms.assetid: 563b874e-c669-4f5b-b3fa-eeb6b6e578f2
title: Session. TargetPath, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.TargetPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6c5917f845da0eec944e797d5f49f52d0ec26913
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238655"
---
# <a name="sessiontargetpath-property"></a>Session. TargetPath, propriété

La propriété **targetPath** de l’objet [**session**](session-object.md) est une propriété en lecture-écriture qui fournit le chemin d’accès complet au dossier désigné sur le lecteur cible de l’installation.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Session.TargetPath
Session.TargetPath = propVal 
```



## <a name="property-value"></a>Valeur de la propriété

Nom d’une propriété de dossier obligatoire et sensible à la casse, comme spécifié par une clé primaire de la [table de répertoires](directory-table.md). Une erreur est générée si le dossier n’existe pas.

## <a name="remarks"></a>Notes

N’essayez pas de configurer le chemin d’accès cible si les composants qui utilisent ces chemins d’accès sont déjà installés pour l’utilisateur actuel ou pour un autre utilisateur. Vérifiez la propriété [**ProductState**](productstate.md) pour déterminer si le produit qui contient le composant est installé.

Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




