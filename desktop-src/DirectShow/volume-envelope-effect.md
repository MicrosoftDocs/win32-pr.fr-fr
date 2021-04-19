---
description: Effet d’enveloppe de volume
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: Effet d’enveloppe de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9364b88b1928e533a031f0700cb8a2c44bc9822d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544955"
---
# <a name="volume-envelope-effect"></a><span data-ttu-id="0fbc7-103">Effet d’enveloppe de volume</span><span class="sxs-lookup"><span data-stu-id="0fbc7-103">Volume Envelope Effect</span></span>

> [!Note]  
> <span data-ttu-id="0fbc7-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0fbc7-104">\[Deprecated.</span></span> <span data-ttu-id="0fbc7-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0fbc7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0fbc7-106">L’effet enveloppe du volume définit le volume sur un flux audio.</span><span class="sxs-lookup"><span data-stu-id="0fbc7-106">The Volume Envelope effect sets the volume on an audio stream.</span></span>

<span data-ttu-id="0fbc7-107">ID de classe (CLSID) : {036A9790-C153-11D2-9EF7-006008039E37}</span><span class="sxs-lookup"><span data-stu-id="0fbc7-107">Class ID (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}</span></span>

<span data-ttu-id="0fbc7-108">Nom de la variable CLSID : CLSID \_ AudMixer</span><span class="sxs-lookup"><span data-stu-id="0fbc7-108">CLSID Variable Name: CLSID\_AudMixer</span></span>

<span data-ttu-id="0fbc7-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0fbc7-109">Properties</span></span>



| <span data-ttu-id="0fbc7-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="0fbc7-110">Property</span></span> | <span data-ttu-id="0fbc7-111">Type</span><span class="sxs-lookup"><span data-stu-id="0fbc7-111">Type</span></span>   | <span data-ttu-id="0fbc7-112">Default</span><span class="sxs-lookup"><span data-stu-id="0fbc7-112">Default</span></span> | <span data-ttu-id="0fbc7-113">Description</span><span class="sxs-lookup"><span data-stu-id="0fbc7-113">Description</span></span>                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fbc7-114">Vol</span><span class="sxs-lookup"><span data-stu-id="0fbc7-114">Vol</span></span>      | <span data-ttu-id="0fbc7-115">double</span><span class="sxs-lookup"><span data-stu-id="0fbc7-115">double</span></span> | <span data-ttu-id="0fbc7-116">1.0</span><span class="sxs-lookup"><span data-stu-id="0fbc7-116">1.0</span></span>     | <span data-ttu-id="0fbc7-117">Volume, en pourcentage du volume créé.</span><span class="sxs-lookup"><span data-stu-id="0fbc7-117">Volume, as a percentage of the authored volume.</span></span> <span data-ttu-id="0fbc7-118">Vous pouvez produire des disparitions audio en faisant varier cette valeur de propriété au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="0fbc7-118">You can produce audio fades by varying this property value over time.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0fbc7-119">Notes</span><span class="sxs-lookup"><span data-stu-id="0fbc7-119">Remarks</span></span>

<span data-ttu-id="0fbc7-120">Chaque objet dans une chronologie peut avoir un seul effet d’enveloppe de volume.</span><span class="sxs-lookup"><span data-stu-id="0fbc7-120">Each object in a timeline can have at most one volume envelope effect.</span></span> <span data-ttu-id="0fbc7-121">Dans une composition ou un groupe, l’enveloppe de volume est appliquée en premier, avant tout autre effet audio, quelle que soit sa priorité.</span><span class="sxs-lookup"><span data-stu-id="0fbc7-121">In a composition or a group, the volume envelope is applied first, before any other audio effects, regardless of its priority.</span></span> <span data-ttu-id="0fbc7-122">Dans une source ou une piste, l’effet de volume est appliqué en fonction de sa priorité.</span><span class="sxs-lookup"><span data-stu-id="0fbc7-122">In a source or a track, the volume effect is applied according to its priority.</span></span>

 

 



