---
description: La méthode CreateSourceImage de l’objet Merge permet au client d’extraire les fichiers d’un module vers une image source sur le disque après une fusion, en tenant compte des modifications apportées au module au cours de la configuration du module.
ms.assetid: c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9
title: Merge. CreateSourceImage, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CreateSourceImage
- IMsmMerge.CreateSourceImage
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 3e50fca7adaeced7f6f2130aeb86cf1ee74db18ae505575c8ce37b1bb85a4010
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926639"
---
# <a name="mergecreatesourceimage-method"></a>Merge. CreateSourceImage, méthode

La méthode **CreateSourceImage** de l’objet [**Merge**](merge-object.md) permet au client d’extraire les fichiers d’un module vers une image source sur le disque après une fusion, en tenant compte des modifications apportées au module au cours de la configuration du module. La liste des fichiers à extraire est extraite de la table de fichiers du module pendant le processus de fusion. La liste des fichiers se compose de chaque fichier copié avec succès à partir de la table de fichiers du module dans la base de données cible. Les entrées de table de fichiers qui n’ont pas été copiées en raison de conflits de clé primaire avec les lignes existantes dans la base de données ne font pas partie de cette liste. Au moment de la création de l’image, le répertoire de chacun de ces fichiers provient de la base de données ouverte (après la fusion). Le chemin d’accès spécifié dans le paramètre *path* est la racine de l’image source pour l’installation. *fLongFileNames* détermine si des noms de fichiers longs sont utilisés pour les segments de chemin d’accès et les noms de fichiers finaux. La fonction échoue si aucune base de données n’est ouverte, si aucun module n’est ouvert ou si aucune fusion n’a été effectuée.

## <a name="syntax"></a>Syntaxe


```JScript
Merge.CreateSourceImage(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chemin d’accès* 
</dt> <dd>

Chemin d’accès de la racine de l’image source pour l’installation.

</dd> <dt>

*fLongFileNames* 
</dt> <dd>

*fLongFileNames* détermine si des noms de fichiers longs sont utilisés pour les segments de chemin d’accès et les noms de fichiers finaux.

</dd> <dt>

*pFilePaths* 
</dt> <dd>

Il s’agit d’une liste de chemins d’accès complets pour les fichiers qui ont été extraits avec succès.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Tous les fichiers du répertoire de destination portant le même nom sont remplacés. Le chemin d’accès est créé s’il n’existe pas déjà.

### <a name="c"></a>C++

Consultez fonction [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




