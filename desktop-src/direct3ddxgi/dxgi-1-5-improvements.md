---
description: Les fonctionnalités suivantes ont été ajoutées à Microsoft DirectX Graphics infrastructure (DXGI) 1,5 pour la prise en charge de la spécification et de la duplication des formats de sortie plus flexibles.
ms.assetid: DD7401E1-9991-48D8-AD23-4D34238EA4AF
title: Améliorations de DXGI 1,5
ms.topic: article
ms.date: 03/05/2021
ms.openlocfilehash: 58df3ef78781437ee033530a2ed2179bb9a132d8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104321746"
---
# <a name="dxgi-15-improvements"></a><span data-ttu-id="cba98-103">Améliorations de DXGI 1,5</span><span class="sxs-lookup"><span data-stu-id="cba98-103">DXGI 1.5 Improvements</span></span>

<span data-ttu-id="cba98-104">Les fonctionnalités suivantes ont été ajoutées à Microsoft DirectX Graphics infrastructure (DXGI) 1,5 pour la prise en charge de la spécification et de la duplication des formats de sortie plus flexibles.</span><span class="sxs-lookup"><span data-stu-id="cba98-104">The following functionality has been added to Microsoft DirectX Graphics Infrastructure (DXGI) 1.5, to support more flexible specifying and duplication of output formats.</span></span>

## <a name="high-dynamic-range-and-wide-color-gamut"></a><span data-ttu-id="cba98-105">Plage dynamique élevée et gamme de couleurs étendue</span><span class="sxs-lookup"><span data-stu-id="cba98-105">High Dynamic Range and Wide Color Gamut</span></span>

<span data-ttu-id="cba98-106">Reportez-vous à [utilisation de DirectX avec des affichages à plage dynamique élevée et couleur avancée](../direct3darticles/high-dynamic-range.md).</span><span class="sxs-lookup"><span data-stu-id="cba98-106">Refer to [Using DirectX with high dynamic range displays and advanced color](../direct3darticles/high-dynamic-range.md).</span></span>

## <a name="variable-refresh-rate-displays"></a><span data-ttu-id="cba98-107">Affichage du taux d’actualisation des variables</span><span class="sxs-lookup"><span data-stu-id="cba98-107">Variable refresh rate displays</span></span>

<span data-ttu-id="cba98-108">Reportez-vous à [taux d’actualisation des variables affiche](variable-refresh-rate-displays.md).</span><span class="sxs-lookup"><span data-stu-id="cba98-108">Refer to [Variable refresh rate displays](variable-refresh-rate-displays.md).</span></span>

## <a name="duplicating-output"></a><span data-ttu-id="cba98-109">Duplication de la sortie</span><span class="sxs-lookup"><span data-stu-id="cba98-109">Duplicating output</span></span>

<span data-ttu-id="cba98-110">Une seule interface, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), avec une seule méthode, [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), a été ajoutée à DXGI 1,5 pour fournir une version plus flexible et plus performante de la méthode [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) d’origine.</span><span class="sxs-lookup"><span data-stu-id="cba98-110">A single interface, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), with a single method, [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), has been added to DXGI 1.5 to provide a more flexible and higher performance version of the original [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) method.</span></span> <span data-ttu-id="cba98-111">**DuplicateOutput1** permet de spécifier une liste de formats pris en charge pour les surfaces plein écran qui peuvent être retournées par l’objet [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) et permet la capture de contenu HDR et WCG.</span><span class="sxs-lookup"><span data-stu-id="cba98-111">**DuplicateOutput1** allows specifying a list of supported formats for fullscreen surfaces that can be returned by the [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) object, and enables capturing HDR and WCG content.</span></span>

## <a name="offering-and-reclaiming-resources"></a><span data-ttu-id="cba98-112">Offre et récupération des ressources</span><span class="sxs-lookup"><span data-stu-id="cba98-112">Offering and Reclaiming Resources</span></span>

<span data-ttu-id="cba98-113">Les méthodes mises à jour [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) et [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) ont été ajoutées à une nouvelle interface, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), pour permettre la libération de la mémoire en plus de l’abandon des ressources.</span><span class="sxs-lookup"><span data-stu-id="cba98-113">Updated methods [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) and [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) have been added to a new interface, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), to allow de-committing of memory in addition to discarding resources.</span></span> <span data-ttu-id="cba98-114">Si vous optez pour la nouvelle option d' [**\_ indicateur de ressource dxgi proposer la \_ \_ \_ \_ dévalidation**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) , les nouveaux résultats de la récupération doivent être correctement gérés.</span><span class="sxs-lookup"><span data-stu-id="cba98-114">Opting in to the new [**DXGI\_OFFER\_RESOURCE\_FLAG\_ALLOW\_DECOMMIT**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) flag means the new reclaim results must be properly handled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cba98-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cba98-115">Related topics</span></span>

[<span data-ttu-id="cba98-116">Guide de programmation pour DXGI</span><span class="sxs-lookup"><span data-stu-id="cba98-116">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
