---
description: La propriété ModuleFiles de l’objet GetFiles retourne toutes les clés primaires de la table de fichiers pour le module actuellement ouvert.
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: GetFiles. ModuleFiles, propriété (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles.ModuleFiles
- IMsmGetFiles.get_ModuleFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d13d624f2cfb24bfa6946ca6c45fe799602f55b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021682"
---
# <a name="getfilesmodulefiles-property"></a>GetFiles. ModuleFiles, propriété

La propriété **ModuleFiles** de l’objet [**GetFiles**](getfiles-object.md) retourne toutes les clés primaires de la [table de fichiers](file-table.md) pour le module actuellement ouvert. Les clés primaires sont retournées sous la forme d’une collection de chaînes. Le module doit être ouvert par un appel à la méthode [**OpenModule**](merge-openmodule.md) de l' [objet Merge](merge-object.md) avant d’appeler **ModuleFiles**.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

Notez que l’ordre des fichiers figurant dans la collection ne peut pas être dans le même ordre que celui indiqué dans la table file.

Si le module n’a pas de table de fichiers ou ne contient pas de fichiers dans la langue particulière, ModuleFiles retourne une collection de chaînes vide.

### <a name="c"></a>C++

Consultez la fonction [**obtenir \_ ModuleFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
