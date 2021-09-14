---
description: La méthode ExtractFilesEx de l’objet Merge extrait le fichier .cab incorporé à partir d’un module, puis écrit ces fichiers dans le répertoire de destination.
ms.assetid: 8b063052-4f92-466a-9c52-bda26ed13d5c
title: Merge. ExtractFilesEx, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFilesEx
- IMsmMerge.ExtractFilesEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: be6aa1001be0d3ecd6cbb9c4cd1d8c04b4649f10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021337"
---
# <a name="mergeextractfilesex-method"></a>Merge. ExtractFilesEx, méthode

La méthode **ExtractFilesEx** de l’objet [**Merge**](merge-object.md) extrait le fichier .cab incorporé à partir d’un module, puis écrit ces fichiers dans le répertoire de destination.

## <a name="syntax"></a>Syntaxe


```JScript
Merge.ExtractFilesEx(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chemin d’accès* 
</dt> <dd>

Le répertoire de destination complet.

</dd> <dt>

*fLongFileNames* 
</dt> <dd>

Défini pour spécifier à l’aide de noms de fichiers longs pour les segments de chemin d’accès et les noms de fichiers finaux.

</dd> <dt>

*pFilePaths* 
</dt> <dd>

Il s’agit d’une liste de chemins d’accès complets pour les fichiers qui ont été extraits avec succès.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Tous les fichiers du répertoire de destination portant le même nom sont remplacés. Le chemin d’accès est créé s’il n’existe pas déjà.

### <a name="c"></a>C++

Consultez fonction [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




