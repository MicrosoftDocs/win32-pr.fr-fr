---
title: ControlTypeNoExpectedPatternsSupported
description: ControlTypeNoExpectedPatternsSupported
ms.assetid: 2C9CEFEA-8207-47A7-B100-A56CFBFB792D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c40f9f094589b312a033d6bdadf3fbf3b5020b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310161"
---
# <a name="controltypenoexpectedpatternssupported"></a><span data-ttu-id="d7150-103">ControlTypeNoExpectedPatternsSupported</span><span class="sxs-lookup"><span data-stu-id="d7150-103">ControlTypeNoExpectedPatternsSupported</span></span>

## <a name="text"></a><span data-ttu-id="d7150-104">Texte</span><span class="sxs-lookup"><span data-stu-id="d7150-104">Text</span></span>

<span data-ttu-id="d7150-105">L’élément avec un ControlType de {0} doit prendre en charge au moins l’un de ces modèles : {1} mais cet élément ne le fait pas</span><span class="sxs-lookup"><span data-stu-id="d7150-105">Element with a ControlType of {0} should support at least one of these patterns:{1} but this element does not</span></span>

## <a name="type"></a><span data-ttu-id="d7150-106">Type</span><span class="sxs-lookup"><span data-stu-id="d7150-106">Type</span></span>

<span data-ttu-id="d7150-107">Error</span><span class="sxs-lookup"><span data-stu-id="d7150-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="d7150-108">Description</span><span class="sxs-lookup"><span data-stu-id="d7150-108">Description</span></span>

<span data-ttu-id="d7150-109">La prise en charge d’UI Automation de l’élément n’est pas conforme à la spécification UI Automation, car l’élément doit prendre en charge au moins une des listes de modèles de contrôle fournies, mais ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="d7150-109">The element's UI Automation support does not comply with the UI Automation specification because the element should support at least one of the provided list of control patterns, but does not.</span></span> <span data-ttu-id="d7150-110">Par conséquent, cet élément peut ne pas être exposé correctement aux technologies d’assistance, ce qui peut avoir un impact sérieux sur l’expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d7150-110">As a result, this element might not be properly exposed to assistive technologies, which could have a serious impact on user experience.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="d7150-111">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="d7150-111">Possible causes</span></span>

-   <span data-ttu-id="d7150-112">Implémentation d’UI Automation incomplète.</span><span class="sxs-lookup"><span data-stu-id="d7150-112">Incomplete UI Automation implementation.</span></span>
-   <span data-ttu-id="d7150-113">La propriété ControlType n’est pas définie correctement.</span><span class="sxs-lookup"><span data-stu-id="d7150-113">The ControlType property is not set correctly.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7150-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d7150-114">Remarks</span></span>

<span data-ttu-id="d7150-115">AccChecker enregistre ce message d’erreur pour une barre de progression indéterminée.</span><span class="sxs-lookup"><span data-stu-id="d7150-115">AccChecker logs this error message for an indeterminate progress bar.</span></span> <span data-ttu-id="d7150-116">Vous pouvez ignorer ce message et/ou l’ajouter à la liste des suppressions.</span><span class="sxs-lookup"><span data-stu-id="d7150-116">You can ignore this message and/or add it to the suppressions list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7150-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d7150-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7150-118">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d7150-118">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="d7150-119">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="d7150-119">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="d7150-120">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="d7150-120">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




