---
description: 'Prenez en compte les éléments suivants lorsque vous décidez quand et comment utiliser l’objet diviseur dans une application :'
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: Autres considérations relatives aux séparateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e00ebc926dd51efb592304f6015351bdc2790b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203812"
---
# <a name="other-divider-considerations"></a><span data-ttu-id="2470b-103">Autres considérations relatives aux séparateurs</span><span class="sxs-lookup"><span data-stu-id="2470b-103">Other Divider Considerations</span></span>

<span data-ttu-id="2470b-104">Prenez en compte les éléments suivants lorsque vous décidez quand et comment utiliser l’objet [**diviseur**](inkdivider-class.md) dans une application :</span><span class="sxs-lookup"><span data-stu-id="2470b-104">Consider the following when deciding when and how to use the [**Divider**](inkdivider-class.md) object in an application:</span></span>

-   <span data-ttu-id="2470b-105">L’objet [**diviseur**](inkdivider-class.md) est conçu pour séparer les dessins et les blocs d’écriture manuscrite, mais pas pour reconnaître les plus hauts niveaux de structure, tels que les tables ou les colonnes.</span><span class="sxs-lookup"><span data-stu-id="2470b-105">The [**Divider**](inkdivider-class.md) object is designed to separate drawings and blocks of handwriting, but not to recognize higher levels of structure, such as tables or columns.</span></span>
-   <span data-ttu-id="2470b-106">L’objet [**diviseur**](inkdivider-class.md) ne fournit pas d’interfaces spécifiquement pour la correction des résultats de l’analyse de la disposition.</span><span class="sxs-lookup"><span data-stu-id="2470b-106">The [**Divider**](inkdivider-class.md) object does not provide interfaces specifically for correction of results of layout analysis.</span></span>
-   <span data-ttu-id="2470b-107">L’utilisation du délai d’attente et du nombre d’heuristiques de trait pour ajouter ou supprimer plusieurs traits à la fois dans les traits de l’objet de [**séparateur**](inkdivider-class.md) peut améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="2470b-107">The use of timeout and number of stroke heuristics to add or remove multiple strokes at a time from the strokes in the [**Divider**](inkdivider-class.md) object may improve performance.</span></span>

## <a name="reanalysis-considerations"></a><span data-ttu-id="2470b-108">Considérations relatives à la réanalyse</span><span class="sxs-lookup"><span data-stu-id="2470b-108">Reanalysis Considerations</span></span>

<span data-ttu-id="2470b-109">Si vous envisagez d’utiliser l’objet [**diviseur**](inkdivider-class.md) dans une application où l’objet **diviseur** devra peut-être réanalyser de grandes quantités d’encre, gardez les points suivants à l’esprit.</span><span class="sxs-lookup"><span data-stu-id="2470b-109">If you are considering using the [**Divider**](inkdivider-class.md) object in an application where the **Divider** object may have to reanalyze large amounts of ink, keep the following in mind.</span></span>

### <a name="retaining-copies-of-ink-and-strokes"></a><span data-ttu-id="2470b-110">Conservation des copies des encres et des traits</span><span class="sxs-lookup"><span data-stu-id="2470b-110">Retaining Copies of Ink and Strokes</span></span>

<span data-ttu-id="2470b-111">Une application peut conserver des copies d’objets [**Ink**](inkdisp-class.md) et [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) pour les éléments d’application qui peuvent être revisités plus tard dans la session de l’application.</span><span class="sxs-lookup"><span data-stu-id="2470b-111">An application can keep copies of [**Ink**](inkdisp-class.md) and [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) objects for application elements that may be revisited later in the application session.</span></span> <span data-ttu-id="2470b-112">Cela élimine la nécessité de réanalyser l’objet **Ink** si l’utilisateur retourne à l’élément.</span><span class="sxs-lookup"><span data-stu-id="2470b-112">This eliminates the need to reanalyze the **Ink** object if the user returns to the element.</span></span> <span data-ttu-id="2470b-113">Cette approche consiste à déconnecter de la mémoire pour de meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="2470b-113">This approach trades off memory for better performance.</span></span>

### <a name="data-reduction-heuristics"></a><span data-ttu-id="2470b-114">Heuristique de réduction des données</span><span class="sxs-lookup"><span data-stu-id="2470b-114">Data Reduction Heuristics</span></span>

<span data-ttu-id="2470b-115">Vous pouvez enregistrer les résultats d’analyse en tant que données d’application et implémenter des heuristiques pour déterminer quand réanalyser un ensemble de traits.</span><span class="sxs-lookup"><span data-stu-id="2470b-115">You may be able to record the analysis results as application data, and implement heuristics to determine when to reanalyze a set of strokes.</span></span> <span data-ttu-id="2470b-116">Cette pratique réduirait la nécessité de réanalyser toute l’encre dans l’application entre les sessions d’application.</span><span class="sxs-lookup"><span data-stu-id="2470b-116">This practice would reduce the need to reanalyze all the ink in the application between application sessions.</span></span> <span data-ttu-id="2470b-117">Toutefois, il convient de veiller à préserver les limites des éléments structurels ou à réanalyser tous les traits des éléments affectés.</span><span class="sxs-lookup"><span data-stu-id="2470b-117">However, care must be taken to preserve structural element boundaries or to reanalyze all the strokes for affected elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2470b-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2470b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2470b-119">**InkDivider, classe**</span><span class="sxs-lookup"><span data-stu-id="2470b-119">**InkDivider Class**</span></span>](inkdivider-class.md)
</dt> <dt>

<span data-ttu-id="2470b-120">[Classe Microsoft. Ink. diviseur](/previous-versions/ms583616(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="2470b-120">[Microsoft.Ink.Divider Class](/previous-versions/ms583616(v=vs.100))</span></span>
</dt> </dl>

 

 
