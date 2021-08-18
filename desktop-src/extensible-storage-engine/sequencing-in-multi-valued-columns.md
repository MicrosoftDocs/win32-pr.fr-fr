---
description: 'En savoir plus sur : séquencement dans les colonnes à valeurs multiples'
title: Séquencement dans des colonnes à valeurs multiples
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 45c8c192becdb616b94360b491bd66f9e6fa492542da320a5536527c2bd45605
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016019"
---
# <a name="sequencing-in-multi-valued-columns"></a>Séquencement dans des colonnes à valeurs multiples


_**S’applique à :** Windows | Windows Serveurs_

## <a name="sequencing-in-multi-valued-columns"></a>Séquencement dans des colonnes à valeurs multiples

Les valeurs d’une colonne à valeurs multiples sont identifiées par un numéro d’index appelé *itagSequence*. Ce nombre est une référence à une valeur unique de la colonne. Ce nombre est utilisé lorsque de nouvelles valeurs sont définies, récupérées ou énumérées dans la colonne. Le *itagSequence* est utilisé dans différentes structures, notamment :

  - [JET_RETINFO](./jet-retinfo-structure.md)

  - [JET_SETINFO](./jet-setinfo-structure.md)

  - [JET_SETCOLUMN](./jet-setcolumn-structure.md)

  - [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)

  - [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)

Ce *itagSequence* démarre à 1 pour chaque valeur de la colonne à valeurs multiples. Le numéro de séquence est augmenté lorsque de nouvelles valeurs sont ajoutées à la colonne. La définition d’une valeur dans une colonne avec un *itagSequence* de 0 indique que la valeur doit être ajoutée au jeu de valeurs déjà dans cette colonne. L’utilisation d’un *itagSequence* supérieur au nombre de valeurs actuellement définies pour une colonne a le même effet. La spécification du *itagSequence* d’une valeur existante remplacera cette valeur, et non pas une nouvelle valeur. Si vous définissez une valeur existante sur NULL, cette valeur est supprimée de l’ensemble de valeurs déjà dans cette colonne. Cela déplace toutes les valeurs suivantes de la colonne vers le haut d’un emplacement, de sorte que l’accès ultérieur à ces valeurs par *itagSequence* sera d’un nombre inférieur à celui utilisé précédemment.

Le diagramme suivant illustre un *itagSequence* dans une colonne à valeurs multiples. La colonne nommée ColA comporte trois entrées : val1, val2 et val3 avec *itagSequence* respectivement 1, 2 et 3.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")
