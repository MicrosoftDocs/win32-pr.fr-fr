---
description: Un module de reconnaissance peut trouver plusieurs façons de diviser un échantillon d’encre en segments de reconnaissance. Pour cette raison, le nombre de remplaçants de reconnaissance peut être échelonné, même pour un petit échantillon d’encre.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Segments d’encre et alternatives
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91183f6c9628ea798b66d703a59e44b26049e692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033957"
---
# <a name="ink-segments-and-alternates"></a><span data-ttu-id="cec42-104">Segments d’encre et alternatives</span><span class="sxs-lookup"><span data-stu-id="cec42-104">Ink Segments and Alternates</span></span>

<span data-ttu-id="cec42-105">Un module de reconnaissance peut trouver plusieurs façons de diviser un échantillon d’encre en segments de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="cec42-105">A recognizer may find several ways to break an ink sample into recognition segments.</span></span> <span data-ttu-id="cec42-106">Pour cette raison, le nombre de remplaçants de reconnaissance peut être échelonné, même pour un petit échantillon d’encre.</span><span class="sxs-lookup"><span data-stu-id="cec42-106">Because of this, the number of recognition alternates may be staggering, even for a small ink sample.</span></span>

<span data-ttu-id="cec42-107">Par exemple, « t o g e t h e r » peut générer les résultats suivants :</span><span class="sxs-lookup"><span data-stu-id="cec42-107">For example, "t o g e t h e r" can yield the following results:</span></span>

-   <span data-ttu-id="cec42-108">« pour l’obtenir » (plus de remplacements pour chaque mot)</span><span class="sxs-lookup"><span data-stu-id="cec42-108">"to get her" (plus alternates for each word)</span></span>
-   <span data-ttu-id="cec42-109">« pour rassembler » (plus de remplacements pour chaque mot)</span><span class="sxs-lookup"><span data-stu-id="cec42-109">"to gather" (plus alternates for each word)</span></span>
-   <span data-ttu-id="cec42-110">« TOG Ether » (plus de remplacements pour chaque mot)</span><span class="sxs-lookup"><span data-stu-id="cec42-110">"tog ether" (plus alternates for each word)</span></span>
-   <span data-ttu-id="cec42-111">« TOG » (plus de remplacements pour chaque mot)</span><span class="sxs-lookup"><span data-stu-id="cec42-111">"tog at her" (plus alternates for each word)</span></span>
-   <span data-ttu-id="cec42-112">« ensemble » (plus des alternatives pour le mot)</span><span class="sxs-lookup"><span data-stu-id="cec42-112">"together" (plus alternates for the word)</span></span>

<span data-ttu-id="cec42-113">L’objet [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) prend en charge le stockage efficace des résultats de reconnaissance complets au sein de l’objet [**Ink**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="cec42-113">The [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object supports efficient storage of full recognition results within the [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="cec42-114">L’objet **Ink** mappe la reconnaissance alternative aux traits de l’objet **Ink** et peut également contenir d’autres informations telles que la position de ligne de base, les index de ligne et les plages de langue.</span><span class="sxs-lookup"><span data-stu-id="cec42-114">The **Ink** object maps the recognition alternates to the strokes in the **Ink** object and may also contain other information such as baseline position, line indices, and language ranges.</span></span>

 

 



