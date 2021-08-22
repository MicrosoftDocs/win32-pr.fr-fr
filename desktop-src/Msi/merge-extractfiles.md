---
description: La méthode ExtractFiles de l’objet Merge extrait le fichier .cab incorporé à partir d’un module, puis écrit ces fichiers dans le répertoire de destination.
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: Merge. ExtractFiles, méthode (Advpub. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFiles
- IMsmMerge.ExtractFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e56d6572526e2aecfc12dc5b2bb9a365be6d3c53b6fb1707fe197c056d05c377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926559"
---
# <a name="mergeextractfiles-method"></a>Merge. ExtractFiles, méthode

La méthode **ExtractFiles** de l’objet [**Merge**](merge-object.md) extrait le fichier .cab incorporé à partir d’un module, puis écrit ces fichiers dans le répertoire de destination.

## <a name="syntax"></a>Syntaxe


```JScript
Merge.ExtractFiles(
  Path
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chemin d’accès* 
</dt> <dd>

Le répertoire de destination complet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Tous les fichiers du répertoire de destination portant le même nom sont remplacés. Le chemin d’accès est créé s’il n’existe pas déjà.

**ExtractFiles** extrait toujours les fichiers en utilisant des noms de fichiers courts pour le chemin d’accès. Pour utiliser des noms de fichiers longs pour le chemin d’accès, utilisez la [**méthode ExtractFilesEx**](merge-extractfilesex.md).

### <a name="c"></a>C++

Consultez fonction [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                                     |
| En-tête<br/>  | <dl> <dt>Advpub. h (inclure Mergemod. h)</dt> </dl> |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl>                  |



 

 
