---
description: La propriété SourcePath de l’objet session est une propriété en lecture seule qui fournit le chemin d’accès complet au dossier désigné sur le média source ou l’image serveur.
ms.assetid: ed8eea4f-e15e-4d56-ac0c-e18f9cb46d07
title: Session. SourcePath, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SourcePath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a868e68e26f28d4fc2137e735ddc6d4c6ab0066
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541515"
---
# <a name="sessionsourcepath-property"></a>Session. SourcePath, propriété

La propriété **SourcePath** de l’objet [**session**](session-object.md) est une propriété en lecture seule qui fournit le chemin d’accès complet au dossier désigné sur le média source ou l’image serveur.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Session.SourcePath
```



## <a name="property-value"></a>Valeur de la propriété

Nom d’une propriété de dossier obligatoire et sensible à la casse, comme spécifié par une clé primaire de la [table de répertoires](directory-table.md). Une erreur est générée si le dossier n’existe pas.

## <a name="remarks"></a>Notes

Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




