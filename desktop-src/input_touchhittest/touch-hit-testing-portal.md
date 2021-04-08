---
title: Test d’atteinte tactile
description: Les rubriques de cette section fournissent une vue d’ensemble de la prise en charge du test tactile dans Windows 8.
ms.assetid: bdd7630c-b2d8-4080-a149-efec018f697d
keywords:
- intervention de l'utilisateur
- entrée
- pointeur
- interface tactile
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 8cf6d28badb47a176a6feccf166344003faf1de8
ms.sourcegitcommit: 9e389b8e39616dcef8f7ff4bc53d945179401478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2020
ms.locfileid: "103841854"
---
# <a name="touch-hit-testing"></a><span data-ttu-id="d6682-107">Test d’atteinte tactile</span><span class="sxs-lookup"><span data-stu-id="d6682-107">Touch Hit Testing</span></span>

## <a name="purpose"></a><span data-ttu-id="d6682-108">Objectif</span><span class="sxs-lookup"><span data-stu-id="d6682-108">Purpose</span></span>

<span data-ttu-id="d6682-109">Les rubriques de cette section fournissent une vue d’ensemble de la prise en charge du test tactile dans Windows.</span><span class="sxs-lookup"><span data-stu-id="d6682-109">The topics in this section provide an overview of support for Touch Hit Testing in Windows.</span></span> <span data-ttu-id="d6682-110">Le test d’atteinte tactile vous permet d’identifier une cible d’entrée selon que la zone de contenu d’un élément d’interface utilisateur se trouve dans la zone de contact ou qu’elle inclue le point de contact.</span><span class="sxs-lookup"><span data-stu-id="d6682-110">Touch Hit Testing lets you identify an input target based on whether the content area of a UI element falls within the contact area or includes the contact point.</span></span>

<span data-ttu-id="d6682-111">Le test tactile utilise une géométrie de contact complexe pour l’ensemble de la zone tactile plutôt qu’une seule coordonnée x-y interpolée.</span><span class="sxs-lookup"><span data-stu-id="d6682-111">Touch hit testing uses complex contact geometry for the entire touch area rather than a single interpolated x-y coordinate.</span></span> <span data-ttu-id="d6682-112">L’utilisation de la géométrie de contact entière améliore considérablement la précision et la précision lorsque vous identifiez la cible la plus probable de l’entrée tactile.</span><span class="sxs-lookup"><span data-stu-id="d6682-112">Using the entire contact geometry greatly improves precision and accuracy when you're identifying the most likely target of touch input.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d6682-113">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="d6682-113">In this section</span></span>

| <span data-ttu-id="d6682-114">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d6682-114">Topic</span></span> | <span data-ttu-id="d6682-115">Description</span><span class="sxs-lookup"><span data-stu-id="d6682-115">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="d6682-116">Référence de test de positionnement tactile</span><span class="sxs-lookup"><span data-stu-id="d6682-116">Touch Hit Testing Reference</span></span>](touchhittest-reference.md)<br/> | <span data-ttu-id="d6682-117">Les rubriques de cette section fournissent les spécifications de référence pour le [test d’atteinte tactile](touch-hit-testing-portal.md).</span><span class="sxs-lookup"><span data-stu-id="d6682-117">The topics in this section provide the reference specifications for [Touch Hit Testing](touch-hit-testing-portal.md).</span></span><br/> |

## <a name="developer-audience"></a><span data-ttu-id="d6682-118">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="d6682-118">Developer audience</span></span>

<span data-ttu-id="d6682-119">Les API de test de positionnement tactile sont conçues pour les développeurs qui créent des infrastructures d’interface utilisateur qui offrent une expérience utilisateur cohérente et optimisée pour les applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="d6682-119">The Touch Hit Testing APIs are designed for developers who are building UI frameworks that provide a consistent touch-optimized user experience across desktop applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6682-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6682-120">Related topics</span></span>

[<span data-ttu-id="d6682-121">Interaction de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="d6682-121">User Interaction</span></span>](../user-interaction.md)
