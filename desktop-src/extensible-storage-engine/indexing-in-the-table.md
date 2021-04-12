---
description: 'En savoir plus sur : l’indexation dans la table'
title: Indexation dans la table
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5d09fde8c5fcdcf2411f6d40c5a3a70912bed27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034107"
---
# <a name="indexing-in-the-table"></a><span data-ttu-id="7520f-103">Indexation dans la table</span><span class="sxs-lookup"><span data-stu-id="7520f-103">Indexing in the Table</span></span>


<span data-ttu-id="7520f-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="7520f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="indexing-in-the-table"></a><span data-ttu-id="7520f-105">Indexation dans la table</span><span class="sxs-lookup"><span data-stu-id="7520f-105">Indexing in the Table</span></span>

<span data-ttu-id="7520f-106">Un index est un ensemble de colonnes clés qui définissent un classement permanent des enregistrements dans une table.</span><span class="sxs-lookup"><span data-stu-id="7520f-106">An index is a set of key columns that define a persistent ordering of records in a table.</span></span> <span data-ttu-id="7520f-107">Les enregistrements sont des entrées d’index dans l’index primaire.</span><span class="sxs-lookup"><span data-stu-id="7520f-107">Records are index entries in the primary index.</span></span> <span data-ttu-id="7520f-108">Un index principal et plusieurs index secondaires peuvent être définis pour créer des ordres de données différents dans la table.</span><span class="sxs-lookup"><span data-stu-id="7520f-108">One primary index and multiple secondary indexes can be defined to create different orders of data in the table.</span></span>

<span data-ttu-id="7520f-109">Bien qu’il soit possible de définir plusieurs index, les enregistrements sont physiquement stockés dans les arborescences B + dans l’ordre spécifié par l’index primaire.</span><span class="sxs-lookup"><span data-stu-id="7520f-109">Although multiple indices can be defined, the records are physically stored in B+ trees in the order specified by the primary index.</span></span> <span data-ttu-id="7520f-110">L’index primaire est toujours un index cluster et doit également être unique.</span><span class="sxs-lookup"><span data-stu-id="7520f-110">The primary index is always a clustered index, and must also be unique.</span></span> <span data-ttu-id="7520f-111">L’index primaire doit être déclaré avant la première mise à jour de la table afin de conserver le classement de l’index.</span><span class="sxs-lookup"><span data-stu-id="7520f-111">The primary index must be declared before the first table update to preserve the index ordering.</span></span> <span data-ttu-id="7520f-112">Quand aucun index primaire n’est défini par l’application, les données sont stockées dans l’ordre dans lequel les enregistrements sont ajoutés à la table.</span><span class="sxs-lookup"><span data-stu-id="7520f-112">When no primary index is defined by the application, the data is stored in the order in which records are added to the table.</span></span> <span data-ttu-id="7520f-113">Cet index spécial est désigné sous le terme d’index séquentiel.</span><span class="sxs-lookup"><span data-stu-id="7520f-113">This special index is referred to as a sequential index.</span></span>

<span data-ttu-id="7520f-114">Les arborescences B + séparées sont utilisées pour trier les enregistrements en fonction de l’index secondaire.</span><span class="sxs-lookup"><span data-stu-id="7520f-114">Separate B+ trees are used to order records according to the secondary index.</span></span> <span data-ttu-id="7520f-115">Les entrées d’index de l’index secondaire contiennent des pointeurs vers les données stockées en fonction de l’index primaire.</span><span class="sxs-lookup"><span data-stu-id="7520f-115">Index entries in the secondary index contain pointers to the data stored according to the primary index.</span></span> <span data-ttu-id="7520f-116">Les entrées d’index des enregistrements de l’index primaire doivent être uniques, car l’index secondaire pointe vers l’enregistrement à l’aide de la clé primaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="7520f-116">The index entries for records in the primary index must be unique because the secondary index points to the record using the primary key of the record.</span></span> <span data-ttu-id="7520f-117">Les index secondaires peuvent avoir ou non une contrainte d’unicité.</span><span class="sxs-lookup"><span data-stu-id="7520f-117">Secondary indices may or may not have a uniqueness constraint.</span></span> <span data-ttu-id="7520f-118">Pour plus d’informations, consultez la rubrique [vue d’ensemble de la base de données](./database-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="7520f-118">For more information, see the [Database Overview](./database-overview.md) topic.</span></span>
