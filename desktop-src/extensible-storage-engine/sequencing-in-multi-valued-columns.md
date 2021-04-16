---
description: 'En savoir plus sur : séquencement dans les colonnes à valeurs multiples'
title: Séquencement dans des colonnes à valeurs multiples
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 54f4bd7734cb8c1bf5a87eb444c3205d89f4a6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550715"
---
# <a name="sequencing-in-multi-valued-columns"></a><span data-ttu-id="1d127-103">Séquencement dans des colonnes à valeurs multiples</span><span class="sxs-lookup"><span data-stu-id="1d127-103">Sequencing in Multi-Valued Columns</span></span>


<span data-ttu-id="1d127-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="1d127-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="sequencing-in-multi-valued-columns"></a><span data-ttu-id="1d127-105">Séquencement dans des colonnes à valeurs multiples</span><span class="sxs-lookup"><span data-stu-id="1d127-105">Sequencing in Multi-Valued Columns</span></span>

<span data-ttu-id="1d127-106">Les valeurs d’une colonne à valeurs multiples sont identifiées par un numéro d’index appelé *itagSequence*.</span><span class="sxs-lookup"><span data-stu-id="1d127-106">The values in a multi-valued column are identified by an index number called the *itagSequence*.</span></span> <span data-ttu-id="1d127-107">Ce nombre est une référence à une valeur unique de la colonne.</span><span class="sxs-lookup"><span data-stu-id="1d127-107">This number is a reference to a single value of the column.</span></span> <span data-ttu-id="1d127-108">Ce nombre est utilisé lorsque de nouvelles valeurs sont définies, récupérées ou énumérées dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="1d127-108">This number is used when new values are set, retrieved, or enumerated in the column.</span></span> <span data-ttu-id="1d127-109">Le *itagSequence* est utilisé dans différentes structures, notamment :</span><span class="sxs-lookup"><span data-stu-id="1d127-109">The *itagSequence* is used in various structures, including:</span></span>

  - [<span data-ttu-id="1d127-110">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="1d127-110">JET_RETINFO</span></span>](./jet-retinfo-structure.md)

  - [<span data-ttu-id="1d127-111">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="1d127-111">JET_SETINFO</span></span>](./jet-setinfo-structure.md)

  - [<span data-ttu-id="1d127-112">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="1d127-112">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)

  - [<span data-ttu-id="1d127-113">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="1d127-113">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)

  - [<span data-ttu-id="1d127-114">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="1d127-114">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)

<span data-ttu-id="1d127-115">Ce *itagSequence* démarre à 1 pour chaque valeur de la colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="1d127-115">This *itagSequence* starts at 1 for every value in the multi-valued column.</span></span> <span data-ttu-id="1d127-116">Le numéro de séquence est augmenté lorsque de nouvelles valeurs sont ajoutées à la colonne.</span><span class="sxs-lookup"><span data-stu-id="1d127-116">The sequence number is increased when new values are added to the column.</span></span> <span data-ttu-id="1d127-117">La définition d’une valeur dans une colonne avec un *itagSequence* de 0 indique que la valeur doit être ajoutée au jeu de valeurs déjà dans cette colonne.</span><span class="sxs-lookup"><span data-stu-id="1d127-117">Setting a value in a column with an *itagSequence* of 0 indicates that the value is to be appended to the set of values already in that column.</span></span> <span data-ttu-id="1d127-118">L’utilisation d’un *itagSequence* supérieur au nombre de valeurs actuellement définies pour une colonne a le même effet.</span><span class="sxs-lookup"><span data-stu-id="1d127-118">Using an *itagSequence* greater than the number of values currently set for a column will have the same effect.</span></span> <span data-ttu-id="1d127-119">La spécification du *itagSequence* d’une valeur existante remplacera cette valeur, et non pas une nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="1d127-119">Specifying the *itagSequence* of an existing value will overwrite that value, not insert a new one.</span></span> <span data-ttu-id="1d127-120">Si vous définissez une valeur existante sur NULL, cette valeur est supprimée de l’ensemble de valeurs déjà dans cette colonne.</span><span class="sxs-lookup"><span data-stu-id="1d127-120">Setting an existing value to NULL will remove that value from the set of values already in that column.</span></span> <span data-ttu-id="1d127-121">Cela déplace toutes les valeurs suivantes de la colonne vers le haut d’un emplacement, de sorte que l’accès ultérieur à ces valeurs par *itagSequence* sera d’un nombre inférieur à celui utilisé précédemment.</span><span class="sxs-lookup"><span data-stu-id="1d127-121">This will move all the subsequent values in the column down by one slot such that subsequent access to those values by *itagSequence* will be by a number one less than what was previously used.</span></span>

<span data-ttu-id="1d127-122">Le diagramme suivant illustre un *itagSequence* dans une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="1d127-122">The following diagram shows an *itagSequence* in a multi-valued column.</span></span> <span data-ttu-id="1d127-123">La colonne nommée ColA comporte trois entrées : val1, val2 et val3 avec *itagSequence* respectivement 1, 2 et 3.</span><span class="sxs-lookup"><span data-stu-id="1d127-123">The column named ColA has three entries: Val1, Val2 and Val3 with *itagSequence* of 1, 2, and 3 respectively.</span></span>

<span data-ttu-id="1d127-124">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span><span class="sxs-lookup"><span data-stu-id="1d127-124">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span></span>
