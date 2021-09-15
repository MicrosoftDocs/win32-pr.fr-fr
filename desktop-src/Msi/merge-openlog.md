---
description: La méthode OpenLog de l’objet Merge ouvre un fichier journal qui reçoit les messages de progression et d’erreur. Si le fichier journal existe déjà, le programme d’installation ajoute de nouveaux messages. Si le fichier journal n’existe pas, le programme d’installation crée un fichier journal.
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: Merge. OpenLog, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenLog
- IMsmMerge.OpenLog
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 46dc029c88b44540817e93e1e559829d88b9f62b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413978"
---
# <a name="mergeopenlog-method"></a>Merge. OpenLog, méthode

La méthode **OpenLog** de l’objet [**Merge**](merge-object.md) ouvre un fichier journal qui reçoit les messages de progression et d’erreur. Si le fichier journal existe déjà, le programme d’installation ajoute de nouveaux messages. Si le fichier journal n’existe pas, le programme d’installation crée un fichier journal.

## <a name="syntax"></a>Syntaxe


```JScript
Merge.OpenLog(
  Filename
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom du fichier* 
</dt> <dd>

Nom de fichier complet pointant vers un fichier à ouvrir ou à créer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Les clients peuvent envoyer leurs propres messages à ce fichier journal par le biais de la méthode [**log**](merge-log.md) .

### <a name="c"></a>C++

Consultez fonction [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
