---
description: Si vous choisissez de le faire, votre application peut fournir ses propres implémentations de module de reconnaissance. Cette section décrit la configuration requise pour la création d’un module de reconnaissance d’application personnalisé pour votre application que vous pouvez utiliser avec l’API de plateforme Tablet PC.
ms.assetid: 502ef3fb-ba45-4f8b-bbd5-19c24e313439
title: Création d’un module de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc71f56dc7095c6c72d18b36c3a12caa493ec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516590"
---
# <a name="creating-a-recognizer"></a><span data-ttu-id="a75a7-104">Création d’un module de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="a75a7-104">Creating a Recognizer</span></span>

<span data-ttu-id="a75a7-105">Si vous choisissez de le faire, votre application peut fournir ses propres implémentations de module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a75a7-105">If you choose to do so, your application can provide its own recognizer implementations.</span></span> <span data-ttu-id="a75a7-106">Cette section décrit la configuration requise pour la création d’un module de reconnaissance d’application personnalisé pour votre application que vous pouvez utiliser avec l’API de plateforme Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="a75a7-106">This section describes the requirements for creating a custom application recognizer for your application that you can use with the Tablet PC Platform API.</span></span>

> [!Note]  
> <span data-ttu-id="a75a7-107">Les programmeurs d’applications personnalisées ne sont pas utilisés par le panneau de saisie Tablet PC ou le journal Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a75a7-107">Custom application recognizers are not used by the Tablet PC Input Panel or Microsoft Windows Journal.</span></span> <span data-ttu-id="a75a7-108">Ces accessoires utilisent uniquement des détecteurs avec lesquels ils ont été testés.</span><span class="sxs-lookup"><span data-stu-id="a75a7-108">These accessories use only recognizers with which they have been tested.</span></span>

 

<span data-ttu-id="a75a7-109">Les sections suivantes détaillent l’implémentation d’un module de reconnaissance personnalisé :</span><span class="sxs-lookup"><span data-stu-id="a75a7-109">The following sections detail the implementation of a custom recognizer:</span></span>

-   [<span data-ttu-id="a75a7-110">Architecture de l’API de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="a75a7-110">Recognition API Architecture</span></span>](recognition-api-architecture.md)
-   <span data-ttu-id="a75a7-111">[API de reconnaissance requises](/previous-versions//ms701664(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a75a7-111">[Required Recognition APIs](/previous-versions//ms701664(v=vs.85))</span></span>
-   [<span data-ttu-id="a75a7-112">HRECOGNIZER et HRECOCONTEXT</span><span class="sxs-lookup"><span data-stu-id="a75a7-112">HRECOGNIZER and HRECOCONTEXT</span></span>](hrecognizer-and-hrecocontext.md)
-   [<span data-ttu-id="a75a7-113">Structure de treillis de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="a75a7-113">Recognizer Lattice Structure</span></span>](recognizer-lattice-structure.md)
-   [<span data-ttu-id="a75a7-114">Inscription de votre DLL de module de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="a75a7-114">Registering Your Recognizer DLL</span></span>](registering-your-recognizer-dll.md)
-   [<span data-ttu-id="a75a7-115">Considérations sur les threads de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="a75a7-115">Recognizer Threading Considerations</span></span>](recognizer-threading-considerations.md)
-   [<span data-ttu-id="a75a7-116">Séquence d’appel classique</span><span class="sxs-lookup"><span data-stu-id="a75a7-116">Typical Calling Sequence</span></span>](typical-calling-sequence.md)
-   [<span data-ttu-id="a75a7-117">Exemple de modèle de DLL de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="a75a7-117">Recognizer DLL Sample Template</span></span>](recognizer-dll-sample-template.md)
-   [<span data-ttu-id="a75a7-118">Valeurs de plage Unicode des mouvements</span><span class="sxs-lookup"><span data-stu-id="a75a7-118">Unicode Range Values of Gestures</span></span>](unicode-range-values-of-gestures.md)
-   [<span data-ttu-id="a75a7-119">API de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="a75a7-119">Recognizer APIs</span></span>](recognizer-apis.md)

 

 
