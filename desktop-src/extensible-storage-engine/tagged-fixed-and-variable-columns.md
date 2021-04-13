---
description: 'En savoir plus sur : colonnes avec balises, fixes et variables'
title: Colonnes avec balises, fixes et variables
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 3f27237c5f75874f7320f675affe20f3833084b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484872"
---
# <a name="tagged-fixed-and-variable-columns"></a>Colonnes avec balises, fixes et variables


_**S’applique à :** Windows | Serveur Windows_

## <a name="tagged-fixed-and-variable-columns"></a>Colonnes avec balises, fixes et variables

Les colonnes de longueur variable, corrigées et marquées sont les types de colonnes primaires pris en charge par ESE. Les colonnes avec balises ne sont pas présentes dans un enregistrement sauf si les données sont stockées dans la colonne et peuvent être fixes ou de longueur variable. Les colonnes avec balises peuvent également contenir plusieurs valeurs dans un seul enregistrement. Les colonnes fixes prennent la même quantité d’espace dans chaque ligne et requièrent 1 bit pour représenter la valeur NULL. Les colonnes de longueur variable requièrent 2 octets pour représenter la taille et la valeur NULL, et occupent une quantité variable d’espace dans chaque enregistrement. Pour plus d’informations sur les colonnes avec balises et fixes, consultez l’option Jet_bitColumnTagged et Jet_bitColumnFixed dans le membre **Grbit** de [JET_COLUMNDEF](./jet-columndef-structure.md) structure utilisée dans l’appel à [JetAddColumn](./jetaddcolumn-function.md).

Les colonnes de longueur variable sont déterminées par le type de colonne défini dans le paramètre *coltyp* de l’appel à [JetAddColumn](./jetaddcolumn-function.md). Les types de colonnes suivants peuvent être fixes ou de longueur variable selon que l’option Jet_bitColumnFixed est définie :

  - JET_coltypBinary

  - JET_coltypText

  - JET_coltypLongBinary

  - JET_coltypLongText

En général, les données de l’enregistrement sont stockées avec la plage fixe en premier, la plage de variables suivante et la plage marquée stockée en dernier. Le diagramme suivant montre comment les enregistrements sont stockés dans la table. Comme indiqué dans le diagramme, la plage avec balises peut contenir des colonnes avec plusieurs valeurs.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")
