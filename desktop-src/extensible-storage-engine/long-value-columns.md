---
description: En savoir plus sur les colonnes de valeur longue
title: Colonnes de valeur longue
TOCTitle: Long Value Columns
ms:assetid: 0690f9d3-1a58-4e53-92e1-213630fc88f4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269179(v=EXCHG.10)
ms:contentKeyID: 32765482
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: bb5618227d49de9e246adf69868a3cb2dc498dca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236561"
---
# <a name="long-value-columns"></a>Colonnes de valeur longue


_**S’applique à :** Windows | Windows Serveurs_

## <a name="long-value-columns"></a>Colonnes de valeur longue

Les types de colonnes ESE JET_coltypLongText et JET_coltypLongBinary sont appelés types de colonne de valeur longue. Ces colonnes sont des chaînes volumineuses et des objets binaires volumineux qui peuvent être stockés dans des arborescences B + séparées de l’index primaire. Lorsque des valeurs de type long sont stockées séparément de l’enregistrement principal, elles sont indexées en interne sur un ID de valeur long (couvercle) et un décalage d’octet et sont accessibles sous forme de flux. Les colonnes de valeur longue sont ajoutées à la table dans l’appel à [JetAddColumn](./jetaddcolumn-function.md) avec le membre **coltyp** de la structure [JET_COLUMNDEF](./jet-columndef-structure.md) définie sur JET_coltypLongText ou JET_coltypLongBinary. La taille maximale d’une longue valeur de colonne binaire ou de texte long est de 2 Go-1.

Le moteur ESE prend en charge les opérations d’ajout, de remplacement de plage d’octets et de taille pour les colonnes de valeur longue afin de prendre en charge des implémentations de flux efficaces sur ces types de colonnes. Par défaut, les données de valeur long sont stockées dans une arborescence B + distincte si elle est supérieure à 1024 octets, ou si l’enregistrement ne tient pas sur une seule page de base de données lorsque les données de valeur long sont stockées dans l’enregistrement. L’application a la possibilité de remplacer le comportement par défaut en définissant des options pour stocker les données de valeur longue dans l’enregistrement (JET_bitSetIntrinsicLV) ou pour les forcer à les stocker dans l’arborescence B + (JET_bitSetIntrinsicLV) distincte. Ces valeurs sont définies dans le paramètre *Grbit* dans [JetSetColumn](./jetsetcolumn-function.md), ou le membre **Grbit** [JET_SETCOLUMN](./jet-setcolumn-structure.md) utilisé dans l’appel à [JetSetColumns](./jetsetcolumns-function.md) comme suit :

  - Ajouter : (JET_bitSetAppendLV)

  - Remplacement de la plage d’octets : (JET_bitSetOverwriteLV)

  - Définir la taille : (JET_bitSetSizeLV)

  - Forcer la séparation : (JET_bitSetSeparateLV)

  - Stocker dans l’enregistrement : (JET_bitSetIntrinsicLV)

Les données de valeur long sont définies en indiquant l’offset dans l’objet blob de valeur long et la longueur des données de la valeur de type long dans l’objet BLOB. Le décalage de l’objet blob de valeur long est défini dans le membre **ibLongValue** de [JET_SETINFO](./jet-setinfo-structure.md) structure (pour [JetSetColumn](./jetsetcolumn-function.md)) ou le membre **IbLongValue** de la structure [JET_SETCOLUMN](./jet-setcolumn-structure.md) (pour [JetSetColumns](./jetsetcolumns-function.md)). Le membre **pvData** de [JET_SETCOLUMN](./jet-setcolumn-structure.md), et le paramètre *PvData* dans l’appel à [JetSetColumn](./jetsetcolumn-function.md) contient les données de valeur long. Les mises à jour des colonnes de valeurs longues doivent être effectuées à l’intérieur d’une transaction.

Les données de valeur long sont toujours stockées dans une table distincte lorsque l’application définit la JET_bitSetSeparateLV ou la JET_bitSetIntrinsicLV, sinon elle est décidée de manière heuristique. Le moteur ESE stocke la valeur long séparée si elle est supérieure à 1024 octets ou si l’enregistrement ne tient pas sur une page de base de données unique si elle est stockée dans l’enregistrement.

Le diagramme suivant montre les données de valeur longue stockées dans une table distincte. Lorsqu’une valeur long est stockée en dehors de l’enregistrement, un nouvel ID à long terme est créé pour faire référence à sa valeur. Cela permet à plusieurs enregistrements de faire référence à la même valeur de colonne. Les nombres de références aux données sont augmentés si plus d’un enregistrement dans les données pointe vers les mêmes données de valeur longue.

![ESE_Documentation_longvaluedtree2](images/Gg269179.ESE_Documentation_longvaluedtree2(EXCHG.10).gif "ESE_Documentation_longvaluedtree2")

ESE prend également en charge une fonctionnalité de magasin d’instances uniques qui permet à plusieurs enregistrements de référencer le même objet binaire volumineux comme si chaque enregistrement avait sa propre copie des informations. ainsi, vous évitez les copies en double des données de valeur de colonne. Cette fonctionnalité est activée dans l’appel à [JetPrepareUpdate](./jetprepareupdate-function.md) avec l’option JET_prepInsertCopy définie dans le paramètre *PREP* .
