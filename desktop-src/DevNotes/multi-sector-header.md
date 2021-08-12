---
description: Représente l’en-tête multisecteur.
ms.assetid: 0fad0e93-b940-4b52-be16-c5f177884dfb
title: Structure MULTI_SECTOR_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MULTI_SECTOR_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9e34e23d3d2bf2ecfbc1c668e02c177e4d1516c73acabccc88aa7190ec33e211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667216"
---
# <a name="multi_sector_header-structure"></a>\_Structure d' \_ en-tête multisecteur

\[Cette structure est valide uniquement pour la version 3 des volumes NTFS ; elles peuvent être modifiées dans les versions ultérieures.\]

Représente l’en-tête multisecteur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _MULTI_SECTOR_HEADER {
  UCHAR  Signature[4];
  USHORT UpdateSequenceArrayOffset;
  USHORT UpdateSequenceArraySize;
} MULTI_SECTOR_HEADER, *PMULTI_SECTOR_HEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**Signature**
</dt> <dd>

Signature. Cette valeur est une pratique pour l’utilisateur.

</dd> <dt>

**UpdateSequenceArrayOffset**
</dt> <dd>

Offset du tableau de séquence de mise à jour, à partir du début de cette structure. Le tableau de séquence de mise à jour doit se terminer avant la dernière valeur USHORT dans le premier secteur.

</dd> <dt>

**UpdateSequenceArraySize**
</dt> <dd>

Taille du tableau de séquences de mise à jour, en octets.

</dd> </dl>

## <a name="remarks"></a>Remarques

Notez qu’il n’y a aucun fichier d’en-tête associé pour cette structure.

Cette définition de structure est valide uniquement pour la version majeure de la version 3 et la version mineure 0 ou 1, comme indiqué par [**FSCTL \_ obtenir les \_ \_ \_ données du volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

L’en-tête multisecteur et le tableau de séquence de mise à jour assurent la détection de transferts multisectoriels incomplets pour les appareils qui ont une taille de secteur physique supérieure ou égale au Stride du numéro de séquence (512) ou qui ne transfèrent pas les secteurs dans le désordre. Si un appareil dont la taille des secteurs est inférieure au Stride du numéro de séquence et qu’il transfère parfois des secteurs dans le désordre, le tableau de séquences de mise à jour ne fournit pas de détection absolue des transferts incomplets. Le nombre de séquences Stride est défini sur un nombre suffisamment petit pour fournir une protection absolue pour tous les disques durs connus. Il n’est pas défini sur une taille inférieure ou il peut y avoir un temps d’exécution excessif ou une surcharge d’espace.

Le tableau de séquences de mise à jour se compose d’un tableau de *n* valeurs **UShort** , où *n* est la taille de la structure protégée divisée par le numéro de séquence Stride. Le premier mot contient le numéro de séquence de mise à jour, qui est un compteur cyclique du nombre de fois où la structure conteneur a été écrite sur le disque. Les *n* valeurs **UShort** enregistrées sont ensuite remplacées par le numéro de séquence de mise à jour lors de la dernière écriture sur le disque de la structure conteneur.

Chaque fois que la structure protégée est sur le point d’être écrite sur le disque, le dernier mot de chaque Stride de numéro de séquence est enregistré à sa position respective dans le tableau des numéros de séquence, puis remplacé par le numéro de séquence de mise à jour suivant. Après l’écriture, ou chaque fois que la structure est lue, le mot enregistré du tableau des numéros de séquence est restauré à sa position réelle dans la structure. Avant de restaurer les mots enregistrés lors des lectures, tous les numéros de séquence à la fin de chaque Stride sont comparés au numéro de séquence réel au début du tableau. Si l’une de ces comparaisons n’est pas égale, un transfert multisecteur ayant échoué a été détecté.

La taille du tableau est déterminée par la taille de la structure conteneur. Le tableau de séquences de mise à jour doit être inclus à la fin de l’en-tête de la structure protégée en raison de sa taille variable. L’utilisateur doit s’assurer que l’espace correct est réservé pour la structure conteneur : (taille de la structure/512 + 1) \* sizeof (UShort).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Table de fichiers maîtres](master-file-table.md)
</dt> </dl>

 

 
