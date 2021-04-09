---
description: 'En savoir plus sur : colonnes'
title: Colonnes
TOCTitle: Columns
ms:assetid: bc16ca4c-e3c9-43db-ac16-284d7cc0926d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294073(v=EXCHG.10)
ms:contentKeyID: 32765688
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 86f7d2bbb3925434ddbfff52e987b6e408af9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114091"
---
# <a name="columns"></a><span data-ttu-id="78697-103">Colonnes</span><span class="sxs-lookup"><span data-stu-id="78697-103">Columns</span></span>


<span data-ttu-id="78697-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="78697-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="columns"></a><span data-ttu-id="78697-105">Colonnes</span><span class="sxs-lookup"><span data-stu-id="78697-105">Columns</span></span>

<span data-ttu-id="78697-106">Une table peut être créée avec un ensemble initial de colonnes en appelant [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou sans un ensemble initial de colonnes en appelant [JetCreateTable](./jetcreatetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="78697-106">A table can be created either with an initial set of columns by calling [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) or without an initial set of columns by calling [JetCreateTable](./jetcreatetable-function.md).</span></span> <span data-ttu-id="78697-107">Dans ESE, les tables peuvent contenir jusqu’à 127 colonnes de longueur fixe, 128 colonnes de longueur variable et 64 993 colonnes avec balises.</span><span class="sxs-lookup"><span data-stu-id="78697-107">Tables in ESE can contain up to 127 fixed-length columns, 128 variable-length columns, and 64,993 tagged columns.</span></span> <span data-ttu-id="78697-108">Les colonnes sont identifiées par leur nom et leur ID et peuvent être ajoutées de manière dynamique à la table à l’aide de [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="78697-108">Columns are identified by their name and ID and can be dynamically added to the table with [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="78697-109">Les colonnes sont créées avec un type de données spécifique et un ensemble facultatif d’attributs, par exemple si la colonne est de longueur fixe ou si elle peut être NULL ou non.</span><span class="sxs-lookup"><span data-stu-id="78697-109">Columns are created with a specific data type and an optional set of attributes, such as whether the column is fixed-length or whether it can be NULL or not.</span></span>

<span data-ttu-id="78697-110">Le type d’une colonne détermine les données qui peuvent être stockées dans la colonne et de nombreuses propriétés de la colonne, y compris son ordre d’indexation.</span><span class="sxs-lookup"><span data-stu-id="78697-110">The type of a column determines the data that may be stored in the column and many of the properties of the column, including its order for indexing.</span></span> <span data-ttu-id="78697-111">ESE prend en charge un large éventail de types de colonnes, dont la taille est comprise entre 1 et 2 Go (2146483647 caractères ASCII ou 1073741823 caractères Unicode).</span><span class="sxs-lookup"><span data-stu-id="78697-111">ESE supports a wide range of column types, ranging in size from 1 bit to 2 GB (2146483647 ASCII characters or 1073741823 Unicode characters).</span></span> <span data-ttu-id="78697-112">Pour obtenir la liste complète des types de données de colonne pris en charge par ESE, consultez la rubrique [JET_COLTYP](./jet-coltyp.md) .</span><span class="sxs-lookup"><span data-stu-id="78697-112">For a complete list of the column data types supported by ESE, see the [JET_COLTYP](./jet-coltyp.md) topic.</span></span> <span data-ttu-id="78697-113">Les rubriques ci-dessous décrivent quelques-uns des types de colonnes pris en charge par ESE :</span><span class="sxs-lookup"><span data-stu-id="78697-113">The topics below discuss a few of the columns types supported by ESE:</span></span>

  - [<span data-ttu-id="78697-114">Colonnes avec balises, fixes et variables</span><span class="sxs-lookup"><span data-stu-id="78697-114">Tagged, Fixed and Variable Columns</span></span>](./tagged-fixed-and-variable-columns.md)

  - [<span data-ttu-id="78697-115">Colonnes version, incrémentation automatique et tiers de confiance</span><span class="sxs-lookup"><span data-stu-id="78697-115">Version, Auto-Increment and Escrow Columns</span></span>](./version-auto-increment-and-escrow-columns.md)

  - [<span data-ttu-id="78697-116">Colonnes de valeur longue</span><span class="sxs-lookup"><span data-stu-id="78697-116">Long Value Columns</span></span>](./long-value-columns.md)

  - [<span data-ttu-id="78697-117">Colonnes éparses à valeurs multiples</span><span class="sxs-lookup"><span data-stu-id="78697-117">Multi-Valued Sparse Columns</span></span>](./multi-valued-sparse-columns.md)

  - [<span data-ttu-id="78697-118">Colonnes définies par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="78697-118">User Defined Columns</span></span>](./user-defined-columns.md)

  - [<span data-ttu-id="78697-119">Utilisation de colonnes dans une table</span><span class="sxs-lookup"><span data-stu-id="78697-119">Using Columns in a Table</span></span>](./using-columns-in-a-table.md)
