---
description: 'En savoir plus sur : structure JET_LOGINFO'
title: Structure JET_LOGINFO
TOCTitle: JET_LOGINFO Structure
ms:assetid: b34b3f24-5d19-4e11-a657-a0e59204d628
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294063(v=EXCHG.10)
ms:contentKeyID: 32765678
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f5619211a5fc76bb080b81b22c08c9e369abf93
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983162"
---
# <a name="jet_loginfo-structure"></a>Structure JET_LOGINFO


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_loginfo-structure"></a>Structure JET_LOGINFO

La structure **JET_LOGINFO** retourne des informations structurées sur l’ensemble des fichiers du journal des transactions qui doit faire partie d’un jeu de fichiers de sauvegarde. La structure **JET_LOGINFO** est l’ensemble minimal d’informations nécessaires pour représenter une plage de journaux récupérés avec [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) ou spécifiés pour une récupération matérielle avec [JetExternalRestore2](./jetexternalrestore2-function.md).

```cpp
typedef struct {
  unsigned long cbSize;
  unsigned long ulGenLow;
  unsigned long ulGenHigh;
  tchar szBaseName[JET_BASE_NAME_LENGTH + 1];
} JET_LOGINFO;
```

### <a name="members"></a>Membres

**cbSize**

Taille de la structure en octets.

Ce membre permet l’expansion future de cette structure tout en activant la compatibilité descendante. Il doit toujours être défini sur sizeof (JET_LOGINFO).

**ulGenLow**

Numéro de fichier journal le plus bas (ou le plus ancien) qui est restauré. La fidélité complète d’un long non signé doit être conservée, mais dans les versions actuelles du moteur, ce nombre est un nombre hexadécimal compris entre 0x00000 et 0xFFFFF. Cela peut changer dans les versions ultérieures.

**ulGenHigh**

Numéro de fichier journal le plus élevé (ou le plus récent) qui est restauré. La fidélité complète d’un long non signé doit être conservée, mais dans les versions actuelles du moteur, ce nombre est un nombre hexadécimal compris entre 0x00000 et 0xFFFFF. Cela peut changer dans les versions ultérieures.

**szBaseName**

Préfixe utilisé pour nommer les fichiers du journal des transactions.

La valeur retournée dans ce membre est toujours égale au paramètre de [JET_paramBaseName](./transaction-log-parameters.md) pour l’instance qui a généré ces informations.

### <a name="remarks"></a>Remarques

Les fichiers journaux de transactions sont nommés en fonction du nom de base de l’instance et du numéro de génération du fichier journal. Le nom est au format BBBXXXXX. Sign. BBB correspond au nom de base du fichier journal et sa longueur est toujours de trois caractères. XXXXX correspond au numéro de génération du fichier journal en valeur hexadécimale de zéro et est toujours de cinq caractères. LOG est l’extension de fichier qui est toujours donnée aux fichiers journaux des transactions par le moteur.

L’utilisation de ces informations structurées est déconseillée, car elle permet à l’application d’avoir une connaissance approfondie de ce schéma de nommage pour les fichiers journaux des transactions. Si le schéma de nommage change à l’avenir, une telle application ne fonctionnera plus correctement. Il est concevable que le format de journal change pour incorporer 8 chiffres hexadécimaux à l’avenir. Les applications doivent utiliser la liste explicite des noms de fichiers retournés par [JetGetLogInfo](./jetgetloginfo-function.md) à la place.

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté comme <strong>JET_LOGINFO_W</strong> (Unicode) et <strong>JET_LOGINFO_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Voir aussi

[JetExternalRestore2](./jetexternalrestore2-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
