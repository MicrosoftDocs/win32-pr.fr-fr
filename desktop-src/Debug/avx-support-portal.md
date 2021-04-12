---
description: Intel Advanced Vector Extensions (AVX) est une extension de vecteur à virgule flottante 256 bits SIMD de l’architecture Intel. Il comprend des extensions pour les instructions et les ensembles d’registres.
ms.assetid: 76357e08-a53c-4490-b08d-1c26900a3826
title: Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 454c8bd5090463cefa1b0ff3a27ef7a04787db0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392915"
---
# <a name="intel-avx"></a><span data-ttu-id="bf472-104">Intel AVX</span><span class="sxs-lookup"><span data-stu-id="bf472-104">Intel AVX</span></span>

## <a name="purpose"></a><span data-ttu-id="bf472-105">Objectif</span><span class="sxs-lookup"><span data-stu-id="bf472-105">Purpose</span></span>

<span data-ttu-id="bf472-106">Intel Advanced Vector Extensions (AVX) est une extension de vecteur à virgule flottante 256 bits SIMD de l’architecture Intel.</span><span class="sxs-lookup"><span data-stu-id="bf472-106">Intel Advanced Vector Extensions (AVX) is a 256-bit SIMD floating point vector extension of Intel architecture.</span></span> <span data-ttu-id="bf472-107">Il comprend des extensions pour les instructions et les ensembles d’registres.</span><span class="sxs-lookup"><span data-stu-id="bf472-107">It includes extensions to both instruction and register sets.</span></span>

<span data-ttu-id="bf472-108">Microsoft a développé des améliorations de l’API, telles que les fonctions XState, qui permettent aux applications d’accéder aux fonctionnalités et à l’état du processeur étendu et de les manipuler, y compris Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="bf472-108">Microsoft has developed some API enhancements, such as XState functions, that enable applications to access and manipulate extended processor feature information and state, including Intel AVX.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bf472-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="bf472-109">In this section</span></span>



| <span data-ttu-id="bf472-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="bf472-110">Topic</span></span>                                                                     | <span data-ttu-id="bf472-111">Description</span><span class="sxs-lookup"><span data-stu-id="bf472-111">Description</span></span>                                                                                                                                               |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf472-112">Utilisation du contexte XState</span><span class="sxs-lookup"><span data-stu-id="bf472-112">Working with XState Context</span></span>](working-with-xstate-context.md)<br/> | <span data-ttu-id="bf472-113">Ce document contient un exemple qui montre comment utiliser les fonctions de contexte XState pour récupérer et définir des fonctionnalités étendues sur un thread.</span><span class="sxs-lookup"><span data-stu-id="bf472-113">This document contains an example that demonstrates how to use the XState context functions to retrieve and set extended features on a thread.</span></span><br/> |
| [<span data-ttu-id="bf472-114">AVX, fonctions</span><span class="sxs-lookup"><span data-stu-id="bf472-114">AVX Functions</span></span>](avx-functions.md)<br/>                             | <span data-ttu-id="bf472-115">Fonctions Intel AVX</span><span class="sxs-lookup"><span data-stu-id="bf472-115">Intel AVX functions</span></span><br/>                                                                                                                            |



 

## <a name="developer-audience"></a><span data-ttu-id="bf472-116">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="bf472-116">Developer audience</span></span>

<span data-ttu-id="bf472-117">Intel AVX est conçu pour être utilisé par les applications qui utilisent fortement le calcul à virgule flottante et peuvent être vectorisées.</span><span class="sxs-lookup"><span data-stu-id="bf472-117">Intel AVX is designed for use by applications that are strongly floating point compute intensive and can be vectorized.</span></span> <span data-ttu-id="bf472-118">Parmi les exemples d’applications, citons le traitement audio et les codecs audio, les applications d’édition d’images et de vidéos, les logiciels d’analyse et de modélisation des services financiers, ainsi que les logiciels de fabrication et d’ingénierie.</span><span class="sxs-lookup"><span data-stu-id="bf472-118">Example applications include audio processing and audio codecs, image and video editing applications, financial services analysis and modeling software, and manufacturing and engineering software.</span></span>

 

 




