---
description: Le tableau suivant contient les codes de retour des fonctions API.
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Codes de retour Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15a2fcdc4db5bd2d295b7cd3078ed80d401ce52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514929"
---
# <a name="direct3d-10-return-codes"></a><span data-ttu-id="b5e0e-103">Codes de retour Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="b5e0e-103">Direct3D 10 Return Codes</span></span>

<span data-ttu-id="b5e0e-104">Le tableau suivant contient les codes de retour des fonctions API.</span><span class="sxs-lookup"><span data-stu-id="b5e0e-104">The following table contains return codes from API functions.</span></span>



| <span data-ttu-id="b5e0e-105">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b5e0e-105">HRESULT</span></span>                                         | <span data-ttu-id="b5e0e-106">Description</span><span class="sxs-lookup"><span data-stu-id="b5e0e-106">Description</span></span>                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5e0e-107">\_Fichier d’erreur D3D10 \_ \_ \_ introuvable</span><span class="sxs-lookup"><span data-stu-id="b5e0e-107">D3D10\_ERROR\_FILE\_NOT\_FOUND</span></span>                  | <span data-ttu-id="b5e0e-108">Ce fichier est introuvable.</span><span class="sxs-lookup"><span data-stu-id="b5e0e-108">The file was not found.</span></span>                                                                                                                               |
| <span data-ttu-id="b5e0e-109">\_Erreur D3D10 \_ \_ un trop grand nombre d’objets d' \_ \_ État uniques \_</span><span class="sxs-lookup"><span data-stu-id="b5e0e-109">D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS</span></span> | <span data-ttu-id="b5e0e-110">Le nombre d’instances uniques d’un type particulier d' [objet d’État](d3d10-graphics-programming-guide-api-features-state-objects.md)est trop important.</span><span class="sxs-lookup"><span data-stu-id="b5e0e-110">There are too many unique instances of a particular type of [state object](d3d10-graphics-programming-guide-api-features-state-objects.md).</span></span>          |
| <span data-ttu-id="b5e0e-111">D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="b5e0e-111">D3DERR\_INVALIDCALL</span></span>                             | <span data-ttu-id="b5e0e-112">L’appel de la méthode n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b5e0e-112">The method call is invalid.</span></span> <span data-ttu-id="b5e0e-113">Par exemple, le paramètre d’une méthode peut ne pas être un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="b5e0e-113">For example, a method's parameter may not be a valid pointer.</span></span>                                                             |
| <span data-ttu-id="b5e0e-114">D3DERR \_ WASSTILLDRAWING</span><span class="sxs-lookup"><span data-stu-id="b5e0e-114">D3DERR\_WASSTILLDRAWING</span></span>                         | <span data-ttu-id="b5e0e-115">L’opération blit précédente qui transfère des informations vers ou à partir de cette surface est incomplète.</span><span class="sxs-lookup"><span data-stu-id="b5e0e-115">The previous blit operation that is transferring information to or from this surface is incomplete.</span></span>                                                   |
| <span data-ttu-id="b5e0e-116">E \_ échec</span><span class="sxs-lookup"><span data-stu-id="b5e0e-116">E\_FAIL</span></span>                                         | <span data-ttu-id="b5e0e-117">Tentative de création d’un appareil avec la [couche de débogage](d3d10-graphics-programming-guide-api-features-layers.md) activée et la couche n’est pas installée.</span><span class="sxs-lookup"><span data-stu-id="b5e0e-117">Attempted to create a device with the [debug layer](d3d10-graphics-programming-guide-api-features-layers.md) enabled and the layer is not installed.</span></span> |
| <span data-ttu-id="b5e0e-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b5e0e-118">E\_INVALIDARG</span></span>                                   | <span data-ttu-id="b5e0e-119">Un paramètre non valide a été passé à la fonction retournée.</span><span class="sxs-lookup"><span data-stu-id="b5e0e-119">An invalid parameter was passed to the returning function.</span></span>                                                                                            |
| <span data-ttu-id="b5e0e-120">\_OUTOFMEMORY E</span><span class="sxs-lookup"><span data-stu-id="b5e0e-120">E\_OUTOFMEMORY</span></span>                                  | <span data-ttu-id="b5e0e-121">Direct3D n’a pas pu allouer suffisamment de mémoire pour terminer l’appel.</span><span class="sxs-lookup"><span data-stu-id="b5e0e-121">Direct3D could not allocate sufficient memory to complete the call.</span></span>                                                                                   |
| <span data-ttu-id="b5e0e-122">\_NOTIMPL E</span><span class="sxs-lookup"><span data-stu-id="b5e0e-122">E\_NOTIMPL</span></span>                                      | <span data-ttu-id="b5e0e-123">L’appel de méthode n’est pas implémenté avec la combinaison de paramètres passée.</span><span class="sxs-lookup"><span data-stu-id="b5e0e-123">The method call isn't implemented with the passed parameter combination.</span></span>                                                                              |
| <span data-ttu-id="b5e0e-124">S \_ false</span><span class="sxs-lookup"><span data-stu-id="b5e0e-124">S\_FALSE</span></span>                                        | <span data-ttu-id="b5e0e-125">Autre valeur de réussite, indiquant une saisie semi-automatique réussie mais non standard (la signification précise dépend du contexte).</span><span class="sxs-lookup"><span data-stu-id="b5e0e-125">Alternate success value, indicating a successful but nonstandard completion (the precise meaning depends on context).</span></span>                                 |
| <span data-ttu-id="b5e0e-126">\_OK</span><span class="sxs-lookup"><span data-stu-id="b5e0e-126">S\_OK</span></span>                                           | <span data-ttu-id="b5e0e-127">Aucune erreur ne s'est produite.</span><span class="sxs-lookup"><span data-stu-id="b5e0e-127">No error occurred.</span></span>                                                                                                                                    |



 

<span data-ttu-id="b5e0e-128">Pour écrire du code qui gère les [valeurs HRESULT](../winprog/windows-data-types.md) de façon fiable, utilisez les macros SUCCEEDED (HR) et failed (HR).</span><span class="sxs-lookup"><span data-stu-id="b5e0e-128">To write code that handles [HRESULT values](../winprog/windows-data-types.md) robustly, use the SUCCEEDED(hr) and FAILED(hr) macros.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5e0e-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5e0e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5e0e-130">Référence Direct3D</span><span class="sxs-lookup"><span data-stu-id="b5e0e-130">Direct3D Reference</span></span>](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[<span data-ttu-id="b5e0e-131">Référence pour Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="b5e0e-131">Reference for Direct3D 10</span></span>](d3d10-graphics-reference.md)
</dt> </dl>

 

 
