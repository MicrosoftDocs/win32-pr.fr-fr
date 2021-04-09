---
title: Extensions ADSI
description: Une extension ADSI est un objet COM spécial qui permet à un développeur d’étendre un objet ADSI.
ms.assetid: 3e40e702-089a-4d2a-806c-cd5b29d11bfd
ms.tgt_platform: multiple
keywords:
- Extensions ADSI
- ADSI ADSI, utilisation des extensions
- ADSI des extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3852e64ad282c11ecd17c6b13904738ee7f46a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028575"
---
# <a name="adsi-extensions"></a><span data-ttu-id="02db3-106">Extensions ADSI</span><span class="sxs-lookup"><span data-stu-id="02db3-106">ADSI Extensions</span></span>

<span data-ttu-id="02db3-107">Une extension ADSI est un objet COM spécial qui permet à un développeur d’étendre un objet ADSI.</span><span class="sxs-lookup"><span data-stu-id="02db3-107">An ADSI extension is a special COM object that enable a developer to extend an ADSI object.</span></span> <span data-ttu-id="02db3-108">Chaque extension est associée à une classe spécifiée dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="02db3-108">Each extension is associated with a specified class in the directory.</span></span> <span data-ttu-id="02db3-109">Avec ce modèle d’extension, les développeurs peuvent ajouter des méthodes pour fournir une signification plus dynamique à un objet.</span><span class="sxs-lookup"><span data-stu-id="02db3-109">With this extension model, developers can add methods to give more dynamic meaning to an object.</span></span> <span data-ttu-id="02db3-110">Dans un modèle de programmation d’annuaire traditionnel, l’accès à un objet s’effectue en obtenant et en définissant les attributs de l’objet.</span><span class="sxs-lookup"><span data-stu-id="02db3-110">In a traditional directory programming model, an object is accessed by getting and setting the object attributes.</span></span> <span data-ttu-id="02db3-111">À l’aide des extensions ADSI, vous pouvez ajouter des fonctionnalités à un objet d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="02db3-111">Using ADSI extensions, you can add more features to a directory object.</span></span>

<span data-ttu-id="02db3-112">Cette section aborde les sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="02db3-112">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="02db3-113">Avantages de l’utilisation des extensions ADSI</span><span class="sxs-lookup"><span data-stu-id="02db3-113">Benefits of Using ADSI Extensions</span></span>](benefits-of-using-adsi-extensions.md)
-   [<span data-ttu-id="02db3-114">Architecture d’extension ADSI</span><span class="sxs-lookup"><span data-stu-id="02db3-114">ADSI Extension Architecture</span></span>](adsi-extension-architecture.md)
-   [<span data-ttu-id="02db3-115">Comment ADSI intègre les extensions</span><span class="sxs-lookup"><span data-stu-id="02db3-115">How ADSI Integrates Extensions</span></span>](adsi-and-extensions.md)
-   [<span data-ttu-id="02db3-116">Qu’est-ce qu’un client ?</span><span class="sxs-lookup"><span data-stu-id="02db3-116">What Does a Client See?</span></span>](what-does-a-client-see.md)
-   [<span data-ttu-id="02db3-117">Obtention des interfaces ADSI à partir de votre extension</span><span class="sxs-lookup"><span data-stu-id="02db3-117">Getting ADSI Interfaces From Your Extension</span></span>](getting-adsi-interfaces-from-your-extension.md)
-   [<span data-ttu-id="02db3-118">Bibliothèques de types d’extension ADSI</span><span class="sxs-lookup"><span data-stu-id="02db3-118">ADSI Extension Type Libraries</span></span>](adsi-extension-type-libraries.md)
-   [<span data-ttu-id="02db3-119">Prise en charge de la liaison précoce</span><span class="sxs-lookup"><span data-stu-id="02db3-119">Early Binding Support</span></span>](early-binding-support.md)
-   [<span data-ttu-id="02db3-120">Prise en charge de la liaison tardive</span><span class="sxs-lookup"><span data-stu-id="02db3-120">Late Binding Support</span></span>](late-binding-support.md)
-   [<span data-ttu-id="02db3-121">Interface IADsExtension</span><span class="sxs-lookup"><span data-stu-id="02db3-121">IADsExtension Interface</span></span>](iadsextension-interface.md)
-   [<span data-ttu-id="02db3-122">Prise en charge des interfaces doubles ou de dispatch</span><span class="sxs-lookup"><span data-stu-id="02db3-122">Supporting Dual or Dispatch Interfaces</span></span>](supporting-dual-or-dispatch-interfaces.md)
-   [<span data-ttu-id="02db3-123">Réexaminer les règles d’agrégation COM avec les extensions ADSI</span><span class="sxs-lookup"><span data-stu-id="02db3-123">Revisiting COM Aggregation Rules with ADSI Extensions</span></span>](revisiting-com-aggregation-rules-with-adsi-extensions.md)
-   [<span data-ttu-id="02db3-124">Résolution de plusieurs composants d’agrégation prenant en charge la même interface</span><span class="sxs-lookup"><span data-stu-id="02db3-124">Resolution of Multiple Aggregation Components Supporting the Same Interface</span></span>](resolution-of-multiple-aggregation-components-supporting-the-same-interface.md)
-   [<span data-ttu-id="02db3-125">Résolution des conflits de nom de fonction/propriété dans l’automatisation dans les extensions</span><span class="sxs-lookup"><span data-stu-id="02db3-125">Resolution of Function/Property Name Conflicts in Automation in Extensions</span></span>](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md)

 

 




