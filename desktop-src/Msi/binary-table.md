---
description: La table binaire contient les données binaires pour les éléments tels que les bitmaps, les animations et les icônes. La table binaire est également utilisée pour stocker des données pour les actions personnalisées. Consultez Limitations OLE sur les flux.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Table binaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4069c7e684e7d90c94b4b04f3d5839058f3570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525021"
---
# <a name="binary-table"></a><span data-ttu-id="71206-105">Table binaire</span><span class="sxs-lookup"><span data-stu-id="71206-105">Binary Table</span></span>

<span data-ttu-id="71206-106">La table binaire contient les données binaires pour les éléments tels que les bitmaps, les animations et les icônes.</span><span class="sxs-lookup"><span data-stu-id="71206-106">The Binary table holds the binary data for items such as bitmaps, animations, and icons.</span></span> <span data-ttu-id="71206-107">La table binaire est également utilisée pour stocker des données pour les actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="71206-107">The binary table is also used to store data for custom actions.</span></span> <span data-ttu-id="71206-108">Consultez [limitations OLE sur les flux](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="71206-108">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

<span data-ttu-id="71206-109">La table binaire contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="71206-109">The Binary table has the following columns.</span></span>



| <span data-ttu-id="71206-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="71206-110">Column</span></span> | <span data-ttu-id="71206-111">Type</span><span class="sxs-lookup"><span data-stu-id="71206-111">Type</span></span>                         | <span data-ttu-id="71206-112">Clé</span><span class="sxs-lookup"><span data-stu-id="71206-112">Key</span></span> | <span data-ttu-id="71206-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="71206-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="71206-114">Nom</span><span class="sxs-lookup"><span data-stu-id="71206-114">Name</span></span>   | [<span data-ttu-id="71206-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="71206-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="71206-116">O</span><span class="sxs-lookup"><span data-stu-id="71206-116">Y</span></span>   | <span data-ttu-id="71206-117">N</span><span class="sxs-lookup"><span data-stu-id="71206-117">N</span></span>        |
| <span data-ttu-id="71206-118">Données</span><span class="sxs-lookup"><span data-stu-id="71206-118">Data</span></span>   | [<span data-ttu-id="71206-119">Binaire</span><span class="sxs-lookup"><span data-stu-id="71206-119">Binary</span></span>](binary.md)         | <span data-ttu-id="71206-120">N</span><span class="sxs-lookup"><span data-stu-id="71206-120">N</span></span>   | <span data-ttu-id="71206-121">N</span><span class="sxs-lookup"><span data-stu-id="71206-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="71206-122">Colonnes</span><span class="sxs-lookup"><span data-stu-id="71206-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="71206-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="71206-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="71206-124">Clé unique qui identifie les données binaires particulières.</span><span class="sxs-lookup"><span data-stu-id="71206-124">A unique key that identifies the particular binary data.</span></span> <span data-ttu-id="71206-125">Si les données binaires sont destinées à un contrôle, la clé apparaît dans la colonne de texte du contrôle associé dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="71206-125">If the binary data is for a control, the key appears in the Text column of the associated control in the [Control table](control-table.md).</span></span> <span data-ttu-id="71206-126">Cette clé doit être unique parmi tous les contrôles nécessitant des données binaires.</span><span class="sxs-lookup"><span data-stu-id="71206-126">This key must be unique among all controls requiring binary data.</span></span>

</dd> <dt>

<span data-ttu-id="71206-127"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Métadonnée</span><span class="sxs-lookup"><span data-stu-id="71206-127"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="71206-128">Données binaires non mises en forme.</span><span class="sxs-lookup"><span data-stu-id="71206-128">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="71206-129">Validation</span><span class="sxs-lookup"><span data-stu-id="71206-129">Validation</span></span>

<dl>

[<span data-ttu-id="71206-130">ICE03</span><span class="sxs-lookup"><span data-stu-id="71206-130">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="71206-131">ICE06</span><span class="sxs-lookup"><span data-stu-id="71206-131">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="71206-132">ICE17</span><span class="sxs-lookup"><span data-stu-id="71206-132">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="71206-133">ICE29</span><span class="sxs-lookup"><span data-stu-id="71206-133">ICE29</span></span>](ice29.md)  
</dl>

 

 



