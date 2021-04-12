---
description: Fonctions DMO
ms.assetid: 0a380dc0-23f0-4ef0-898a-3b5afddf5eaa
title: Fonctions DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f41750f5e442d93d3cacb2499bf2986a53cda6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480672"
---
# <a name="dmo-functions"></a><span data-ttu-id="36695-103">Fonctions DMO</span><span class="sxs-lookup"><span data-stu-id="36695-103">DMO Functions</span></span>

<span data-ttu-id="36695-104">Cette section décrit les fonctions de Microsoft DirectX Media Object (DMO).</span><span class="sxs-lookup"><span data-stu-id="36695-104">This section describes the Microsoft DirectX Media Object (DMO) functions.</span></span>



| <span data-ttu-id="36695-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="36695-105">Function</span></span>                                             | <span data-ttu-id="36695-106">Description</span><span class="sxs-lookup"><span data-stu-id="36695-106">Description</span></span>                                                   |
|------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="36695-107">**DMOEnum**</span><span class="sxs-lookup"><span data-stu-id="36695-107">**DMOEnum**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum)                           | <span data-ttu-id="36695-108">Énumère les DMOs répertoriés dans le registre.</span><span class="sxs-lookup"><span data-stu-id="36695-108">Enumerates DMOs listed in the registry.</span></span>                       |
| [<span data-ttu-id="36695-109">**DMOGetName**</span><span class="sxs-lookup"><span data-stu-id="36695-109">**DMOGetName**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmogetname)                     | <span data-ttu-id="36695-110">Récupère le nom d’un DMO à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="36695-110">Retrieves the name of a DMO from the registry.</span></span>                |
| [<span data-ttu-id="36695-111">**DMOGetTypes**</span><span class="sxs-lookup"><span data-stu-id="36695-111">**DMOGetTypes**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmogettypes)                   | <span data-ttu-id="36695-112">Récupère les types de supports enregistrés pour une DMO.</span><span class="sxs-lookup"><span data-stu-id="36695-112">Retrieves the media types registered for a DMO.</span></span>               |
| [<span data-ttu-id="36695-113">**DMORegister**</span><span class="sxs-lookup"><span data-stu-id="36695-113">**DMORegister**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister)                   | <span data-ttu-id="36695-114">Inscrit un DMO.</span><span class="sxs-lookup"><span data-stu-id="36695-114">Registers a DMO.</span></span>                                              |
| [<span data-ttu-id="36695-115">**DMOUnregister**</span><span class="sxs-lookup"><span data-stu-id="36695-115">**DMOUnregister**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister)               | <span data-ttu-id="36695-116">Annule l’inscription d’un DMO.</span><span class="sxs-lookup"><span data-stu-id="36695-116">Unregisters a DMO.</span></span>                                            |
| [<span data-ttu-id="36695-117">**MoCopyMediaType**</span><span class="sxs-lookup"><span data-stu-id="36695-117">**MoCopyMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mocopymediatype)           | <span data-ttu-id="36695-118">Copie une structure de type de média vers une autre.</span><span class="sxs-lookup"><span data-stu-id="36695-118">Copies one media type structure to another.</span></span>                   |
| [<span data-ttu-id="36695-119">**MoCreateMediaType**</span><span class="sxs-lookup"><span data-stu-id="36695-119">**MoCreateMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mocreatemediatype)       | <span data-ttu-id="36695-120">Alloue une nouvelle structure de type de média.</span><span class="sxs-lookup"><span data-stu-id="36695-120">Allocates a new media type structure.</span></span>                         |
| [<span data-ttu-id="36695-121">**MoDeleteMediaType**</span><span class="sxs-lookup"><span data-stu-id="36695-121">**MoDeleteMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-modeletemediatype)       | <span data-ttu-id="36695-122">Supprime une structure de type de média précédemment allouée.</span><span class="sxs-lookup"><span data-stu-id="36695-122">Deletes a media type structure that was previously allocated.</span></span> |
| [<span data-ttu-id="36695-123">**MoDuplicateMediaType**</span><span class="sxs-lookup"><span data-stu-id="36695-123">**MoDuplicateMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-moduplicatemediatype) | <span data-ttu-id="36695-124">Duplique une structure de type de média.</span><span class="sxs-lookup"><span data-stu-id="36695-124">Duplicates a media type structure.</span></span>                            |
| [<span data-ttu-id="36695-125">**MoFreeMediaType**</span><span class="sxs-lookup"><span data-stu-id="36695-125">**MoFreeMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mofreemediatype)           | <span data-ttu-id="36695-126">Libère les membres alloués d’une structure de type de média.</span><span class="sxs-lookup"><span data-stu-id="36695-126">Frees the allocated members of a media type structure.</span></span>        |
| [<span data-ttu-id="36695-127">**MoInitMediaType**</span><span class="sxs-lookup"><span data-stu-id="36695-127">**MoInitMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-moinitmediatype)           | <span data-ttu-id="36695-128">Initialise une structure de type de média.</span><span class="sxs-lookup"><span data-stu-id="36695-128">Initializes a media type structure.</span></span>                           |



 

## <a name="related-topics"></a><span data-ttu-id="36695-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36695-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36695-130">Référence DMO</span><span class="sxs-lookup"><span data-stu-id="36695-130">DMO Reference</span></span>](dmo-reference.md)
</dt> </dl>

 

 



