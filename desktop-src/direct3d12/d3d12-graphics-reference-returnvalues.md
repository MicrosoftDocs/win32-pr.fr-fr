---
title: Codes de retour Direct3D 12
description: Voici les codes de retour des fonctions API.
ms.assetid: 5F6CC962-7DB7-489F-82A4-9388313014D3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd04c0c7702f00f1338ce884adc745522390c8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513544"
---
# <a name="direct3d-12-return-codes"></a><span data-ttu-id="706a2-103">Codes de retour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="706a2-103">Direct3D 12 Return Codes</span></span>

<span data-ttu-id="706a2-104">Voici les codes de retour des fonctions API.</span><span class="sxs-lookup"><span data-stu-id="706a2-104">The following are return codes from API functions.</span></span> <span data-ttu-id="706a2-105">Pour plus d’informations sur les codes de retour, consultez [ \_ erreur dxgi](/windows/desktop/direct3ddxgi/dxgi-error).</span><span class="sxs-lookup"><span data-stu-id="706a2-105">For more return codes, see [DXGI\_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).</span></span>



| <span data-ttu-id="706a2-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="706a2-106">HRESULT</span></span>                                                                  | <span data-ttu-id="706a2-107">Description</span><span class="sxs-lookup"><span data-stu-id="706a2-107">Description</span></span>                                                                                                           |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="706a2-108">\_Adaptateur d’erreur D3D12 \_ \_ \_ introuvable</span><span class="sxs-lookup"><span data-stu-id="706a2-108">D3D12\_ERROR\_ADAPTER\_NOT\_FOUND</span></span>                                        | <span data-ttu-id="706a2-109">Le PSO mis en cache spécifié a été créé sur un autre adaptateur et ne peut pas être réutilisé sur l’adaptateur actuel.</span><span class="sxs-lookup"><span data-stu-id="706a2-109">The specified cached PSO was created on a different adapter and cannot be reused on the current adapter.</span></span>          |
| <span data-ttu-id="706a2-110">Incompatibilité de version de pilote d' \_ erreur D3D12 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="706a2-110">D3D12\_ERROR\_DRIVER\_VERSION\_MISMATCH</span></span>                                  | <span data-ttu-id="706a2-111">Le PSO mis en cache spécifié a été créé sur une version de pilote différente et ne peut pas être réutilisé sur l’adaptateur actuel.</span><span class="sxs-lookup"><span data-stu-id="706a2-111">The specified cached PSO was created on a different driver version and cannot be reused on the current adapter.</span></span>  |
| <span data-ttu-id="706a2-112">D3DERR \_ INVALIDCALL (remplacé par une \_ erreur \_ dxgi \_ appel non valide)</span><span class="sxs-lookup"><span data-stu-id="706a2-112">D3DERR\_INVALIDCALL (replaced with DXGI\_ERROR\_INVALID\_CALL)</span></span>           | <span data-ttu-id="706a2-113">L’appel de la méthode n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="706a2-113">The method call is invalid.</span></span> <span data-ttu-id="706a2-114">Par exemple, le paramètre d’une méthode peut ne pas être un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="706a2-114">For example, a method's parameter may not be a valid pointer.</span></span>                             |
| <span data-ttu-id="706a2-115">D3DERR \_ WASSTILLDRAWING (remplacé par l' \_ erreur \_ dxgi \_ \_ dessinait encore)</span><span class="sxs-lookup"><span data-stu-id="706a2-115">D3DERR\_WASSTILLDRAWING (replaced with DXGI\_ERROR\_WAS\_STILL\_DRAWING)</span></span> | <span data-ttu-id="706a2-116">L’opération blit précédente qui transfère des informations vers ou à partir de cette surface est incomplète.</span><span class="sxs-lookup"><span data-stu-id="706a2-116">The previous blit operation that is transferring information to or from this surface is incomplete.</span></span>                   |
| <span data-ttu-id="706a2-117">E \_ échec</span><span class="sxs-lookup"><span data-stu-id="706a2-117">E\_FAIL</span></span>                                                                  | <span data-ttu-id="706a2-118">Tentative de création d’un appareil avec la couche de débogage activée et la couche n’est pas installée.</span><span class="sxs-lookup"><span data-stu-id="706a2-118">Attempted to create a device with the debug layer enabled and the layer is not installed.</span></span>                             |
| <span data-ttu-id="706a2-119">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="706a2-119">E\_INVALIDARG</span></span>                                                            | <span data-ttu-id="706a2-120">Un paramètre non valide a été passé à la fonction retournée.</span><span class="sxs-lookup"><span data-stu-id="706a2-120">An invalid parameter was passed to the returning function.</span></span>                                                             |
| <span data-ttu-id="706a2-121">\_OUTOFMEMORY E</span><span class="sxs-lookup"><span data-stu-id="706a2-121">E\_OUTOFMEMORY</span></span>                                                           | <span data-ttu-id="706a2-122">Direct3D n’a pas pu allouer suffisamment de mémoire pour terminer l’appel.</span><span class="sxs-lookup"><span data-stu-id="706a2-122">Direct3D could not allocate sufficient memory to complete the call.</span></span>                                                   |
| <span data-ttu-id="706a2-123">\_NOTIMPL E</span><span class="sxs-lookup"><span data-stu-id="706a2-123">E\_NOTIMPL</span></span>                                                               | <span data-ttu-id="706a2-124">L’appel de méthode n’est pas implémenté avec la combinaison de paramètres passée.</span><span class="sxs-lookup"><span data-stu-id="706a2-124">The method call isn't implemented with the passed parameter combination.</span></span>                                               |
| <span data-ttu-id="706a2-125">S \_ false</span><span class="sxs-lookup"><span data-stu-id="706a2-125">S\_FALSE</span></span>                                                                 | <span data-ttu-id="706a2-126">Autre valeur de réussite, indiquant une saisie semi-automatique réussie mais non standard (la signification précise dépend du contexte).</span><span class="sxs-lookup"><span data-stu-id="706a2-126">Alternate success value, indicating a successful but nonstandard completion (the precise meaning depends on context).</span></span> |
| <span data-ttu-id="706a2-127">\_OK</span><span class="sxs-lookup"><span data-stu-id="706a2-127">S\_OK</span></span>                                                                    | <span data-ttu-id="706a2-128">Aucune erreur ne s'est produite.</span><span class="sxs-lookup"><span data-stu-id="706a2-128">No error occurred.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="706a2-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="706a2-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="706a2-130">Référence de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="706a2-130">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 