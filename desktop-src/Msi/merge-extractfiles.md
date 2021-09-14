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
ms.openlocfilehash: 3869dc37b841d386891eb70940054bd78805bf94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011902"
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

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Tous les fichiers du répertoire de destination portant le même nom sont remplacés. Le chemin d’accès est créé s’il n’existe pas déjà.

**ExtractFiles** extrait toujours les fichiers en utilisant des noms de fichiers courts pour le chemin d’accès. Pour utiliser des noms de fichiers longs pour le chemin d’accès, utilisez la [**méthode ExtractFilesEx**](merge-extractfilesex.md).

### <a name="c"></a>C++

Consultez fonction [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                                     |
| En-tête<br/>  | <dl> <dt>Advpub. h (inclure Mergemod. h)</dt> </dl> |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl>                  |



 

 
