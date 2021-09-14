---
description: La méthode ExtractCAB de l’objet Merge extrait le fichier .cab incorporé à partir d’un module et l’enregistre dans le fichier spécifié. Le programme d’installation crée ce fichier s’il n’existe pas déjà et est remplacé s’il existe.
ms.assetid: a6fe8b69-8f4a-45f7-b7e6-7620a00500bb
title: Merge. ExtractCAB, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractCAB
- IMsmMerge.ExtractCAB
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d0bdc79fb0087456d035bf732faca384b35b2a9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021341"
---
# <a name="mergeextractcab-method"></a>Merge. ExtractCAB, méthode

La méthode **ExtractCAB** de l’objet [**Merge**](merge-object.md) extrait le fichier .cab incorporé à partir d’un module et l’enregistre dans le fichier spécifié. Le programme d’installation crée ce fichier s’il n’existe pas déjà et est remplacé s’il existe.

## <a name="syntax"></a>Syntaxe


```JScript
Merge.ExtractCAB(
  FileName
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FileName* 
</dt> <dd>

Fichier de destination complet.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="c"></a>C++

Consultez fonction [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
