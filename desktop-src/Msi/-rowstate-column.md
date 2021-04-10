---
description: Le nom de colonne réservé \_ RowState représente l’état non persistant associé à chaque ligne de table dans une table de base de données de programme d’installation.
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState colonne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a2964d7d11c1c2429ad95e9de2b8bdb148954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034414"
---
# <a name="_rowstate-column"></a><span data-ttu-id="ce035-103">\_RowState (colonne)</span><span class="sxs-lookup"><span data-stu-id="ce035-103">\_RowState Column</span></span>

<span data-ttu-id="ce035-104">Le nom de colonne réservé \_ RowState représente l’état non persistant associé à chaque ligne de table dans une table de base de données de programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="ce035-104">The reserved column name \_RowState represents the non-persistent state associated with each table row in an installer database table.</span></span> <span data-ttu-id="ce035-105">La pseudo-colonne est de type [entier](integer.md), et la valeur se compose d’un jeu d’indicateurs binaires.</span><span class="sxs-lookup"><span data-stu-id="ce035-105">The pseudo-column is of type [Integer](integer.md), and the value consists of a set of bit flags.</span></span> <span data-ttu-id="ce035-106">Tous les bits sont lisibles, mais seuls les bits UserInfo et Temporary peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="ce035-106">All the bits are readable, but only the UserInfo and Temporary bits can be set.</span></span> <span data-ttu-id="ce035-107">Ces données sont disponibles uniquement tant que les tables sont verrouillées ou en cours d’utilisation (c’est-à-dire qu’une vue contenant les tables existe).</span><span class="sxs-lookup"><span data-stu-id="ce035-107">This data is available only as long as the tables are locked or in use (that is, while a view containing the tables exists).</span></span> <span data-ttu-id="ce035-108">Le tableau suivant indique les attributs qu’une ligne peut avoir.</span><span class="sxs-lookup"><span data-stu-id="ce035-108">The following table shows the attributes a row can have.</span></span>



| <span data-ttu-id="ce035-109">Nom</span><span class="sxs-lookup"><span data-stu-id="ce035-109">Name</span></span>           | <span data-ttu-id="ce035-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce035-110">Value</span></span> | <span data-ttu-id="ce035-111">Signification</span><span class="sxs-lookup"><span data-stu-id="ce035-111">Meaning</span></span>                                                        |
|----------------|-------|----------------------------------------------------------------|
| <span data-ttu-id="ce035-112">iraUserInfo</span><span class="sxs-lookup"><span data-stu-id="ce035-112">iraUserInfo</span></span>    | <span data-ttu-id="ce035-113">0x01</span><span class="sxs-lookup"><span data-stu-id="ce035-113">0x01</span></span>  | <span data-ttu-id="ce035-114">L’attribut est destiné à un usage externe.</span><span class="sxs-lookup"><span data-stu-id="ce035-114">The attribute is for external use.</span></span> <span data-ttu-id="ce035-115">Cette valeur peut être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="ce035-115">This value can be updated.</span></span>  |
| <span data-ttu-id="ce035-116">iraTemporary</span><span class="sxs-lookup"><span data-stu-id="ce035-116">iraTemporary</span></span>   | <span data-ttu-id="ce035-117">0x02</span><span class="sxs-lookup"><span data-stu-id="ce035-117">0x02</span></span>  | <span data-ttu-id="ce035-118">La ligne n’est pas persistante.</span><span class="sxs-lookup"><span data-stu-id="ce035-118">The row is not persistent.</span></span> <span data-ttu-id="ce035-119">Cette valeur peut être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="ce035-119">This value can be updated.</span></span>          |
| <span data-ttu-id="ce035-120">iraModified</span><span class="sxs-lookup"><span data-stu-id="ce035-120">iraModified</span></span>    | <span data-ttu-id="ce035-121">0x04</span><span class="sxs-lookup"><span data-stu-id="ce035-121">0x04</span></span>  | <span data-ttu-id="ce035-122">Une ligne a été mise à jour.</span><span class="sxs-lookup"><span data-stu-id="ce035-122">A row has been updated.</span></span>                                        |
| <span data-ttu-id="ce035-123">iraInserted</span><span class="sxs-lookup"><span data-stu-id="ce035-123">iraInserted</span></span>    | <span data-ttu-id="ce035-124">0x08</span><span class="sxs-lookup"><span data-stu-id="ce035-124">0x08</span></span>  | <span data-ttu-id="ce035-125">Une ligne a été insérée.</span><span class="sxs-lookup"><span data-stu-id="ce035-125">A row has been inserted.</span></span>                                       |
| <span data-ttu-id="ce035-126">iraMergeFailed</span><span class="sxs-lookup"><span data-stu-id="ce035-126">iraMergeFailed</span></span> | <span data-ttu-id="ce035-127">0x0F</span><span class="sxs-lookup"><span data-stu-id="ce035-127">0x0F</span></span>  | <span data-ttu-id="ce035-128">Une tentative de fusion avec des données non-clés non-identiques a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="ce035-128">An attempt was made to merge with non-identical, non-key data.</span></span> |



 

<span data-ttu-id="ce035-129">Les bits 6 à 8 sont réservés.</span><span class="sxs-lookup"><span data-stu-id="ce035-129">Bits 6 through 8 are reserved.</span></span>

 

 



