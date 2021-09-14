---
description: 'En savoir plus sur : recherche d’enregistrements dans l’index'
title: Recherche d’enregistrements dans l’index
TOCTitle: Searching Records in the Index
ms:assetid: 9141b1d6-81b6-49ad-a5d4-2409fe0d511a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269342(v=EXCHG.10)
ms:contentKeyID: 32765631
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 89a4ffe1f1c13280f236442ae218580fa5699741
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118310"
---
# <a name="searching-records-in-the-index"></a>Recherche d’enregistrements dans l’index


_**S’applique à :** Windows | Windows Serveurs_

## <a name="searching-records-in-the-index"></a>Recherche d’enregistrements dans l’index

Les clés de recherche sont créées pour rechercher une seule entrée ou un ensemble d’entrées dans un index. Les clés de recherche peuvent uniquement être construites pour les colonnes clés de l’index et peuvent contenir une ou plusieurs valeurs de colonne. La clé de recherche est construite avec un seul appel ou une série d’appels à [JetMakeKey](./jetmakekey-function.md), et peut être récupérée avec [JetRetrieveKey](./jetretrievekey-function.md) à l’aide de JET_bitRetrieveCopy. Une fois la clé de recherche construite, elle peut être utilisée pour déplacer le curseur vers l’enregistrement dans l’index.

Il existe trois méthodes pour rechercher des enregistrements dans une table :

1.  Recherchez une seule entrée d’index. Pour ce faire, créez la clé de recherche avec [JetMakeKey](./jetmakekey-function.md), puis accédez à cet enregistrement avec [JetSeek](./jetseek-function.md).

2.  Rechercher l’index enregistrement par enregistrement. Les enregistrements peuvent parcourir un enregistrement à la fois en appelant [JetMove](./jetmove-function.md). Le curseur peut être déplacé vers le premier enregistrement de l’index en spécifiant JET_MoveFirst dans le paramètre *cRow* de [JetMove](./jetmove-function.md). De la même façon, le curseur peut être déplacé vers l’avant, vers l’arrière ou vers la dernière entrée de l’index.

3.  Effectuer une recherche dans un jeu d’enregistrements. Pour ce faire, définissez une plage d’entrées d’index à rechercher, puis parcourez les enregistrements de manière séquentielle. Pour plus d’informations, consultez [la section recherche dans une série d’enregistrements]() de cette rubrique.

### <a name="searching-through-a-set-of-records"></a>Recherche dans un ensemble d’enregistrements

Le diagramme ci-dessous illustre le déplacement du curseur dans une plage d’entrées d’index définies par des appels à [JetSeek](./jetseek-function.md) et [JetSetIndexRange](./jetsetindexrange-function.md).

Utilisez la procédure suivante pour effectuer une recherche dans un jeu d’enregistrements dans un index.

### <a name="to-search-a-set-of-records-in-an-index"></a>Pour rechercher un jeu d’enregistrements dans un index

1.  Créez la clé de recherche pour le premier enregistrement dans le jeu d’enregistrements à rechercher avec [JetMakeKey](./jetmakekey-function.md).

2.  Déplacez le curseur vers l’enregistrement indiqué dans la clé de recherche avec [JetSeek](./jetseek-function.md).

3.  Créez une autre clé de recherche pour la dernière entrée d’index de la plage avec [JetMakeKey](./jetmakekey-function.md).

4.  Définissez la plage d’index avec [JetSetIndexRange](./jetsetindexrange-function.md) à l’aide de la clé créée à l’étape 3.

5.  Appelez [JetMove](./jetmove-function.md) pour vous déplacer de façon séquentielle dans chaque enregistrement de la plage d’index, comme indiqué dans le diagramme suivant.

![ESE_Documentation_IndexRange](images/Gg269342.ESE_Documentation_IndexRange(EXCHG.10).gif "ESE_Documentation_IndexRange")

Le curseur dans le diagramme ici peut uniquement se déplacer dans la plage d’index définie dans l’appel à [JetSetIndexRange](./jetsetindexrange-function.md). Si l’application tente de déplacer le curseur au-delà de la plage d’index, ESE renvoie une erreur Jet_errNoCurrentRecord à partir de l’appel à [JetMove](./jetmove-function.md). Notez que tout type de navigation avec ce curseur autre que le déplacement vers l’enregistrement suivant ou précédent annulera la plage d’index. Pour plus d’informations, consultez [JetSetIndexRange](./jetsetindexrange-function.md) .

Le type de données entré dans le paramètre *pvData* pour [JetMakeKey](./jetmakekey-function.md) doit correspondre au type de données et aux propriétés spécifiées pour la colonne. Par exemple, l’appel de [JetMakeKey](./jetmakekey-function.md) avec « Ben Miller » spécifié dans le paramètre *pvData* pour un type de colonne JET_coltypText est une correspondance de type de données valide. Si vous souhaitez créer une clé de recherche pour effectuer une recherche entre les noms « Olivier Miller » et « Max Stevens » dans un index, déplacez le curseur vers l’enregistrement portant le nom « Olivier Miller » en appelant [JetSeek](./jetseek-function.md). Appelez [JetMakeKey](./jetmakekey-function.md) une deuxième fois et spécifiez un pointeur vers une chaîne contenant le nom « Max Stevens ». La plage d’index est définie pour limiter le curseur à déplacer entre les noms « Olivier Miller » et « Max Stevens » dans l’appel à [JetSetIndexRange](./jetsetindexrange-function.md).
