---
title: FirstChildLastChildMismatch
description: FirstChildLastChildMismatch
ms.assetid: 98726C1A-DC43-4FC7-8ECA-628F63D0AFE3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37fedb7e23ce2ac2a7f9c51c9db9e06e59ead515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380127"
---
# <a name="firstchildlastchildmismatch"></a><span data-ttu-id="f1432-103">FirstChildLastChildMismatch</span><span class="sxs-lookup"><span data-stu-id="f1432-103">FirstChildLastChildMismatch</span></span>

## <a name="text"></a><span data-ttu-id="f1432-104">Texte</span><span class="sxs-lookup"><span data-stu-id="f1432-104">Text</span></span>

<span data-ttu-id="f1432-105">Lors de la navigation en appelant {0} à partir du nœud testé, puis en appelant à plusieurs reprises {1} , nous avons terminé à l’enfant suivant : {2} .</span><span class="sxs-lookup"><span data-stu-id="f1432-105">When navigating by calling {0} from the tested node, and then repeatedly calling {1}, we finished at the following child: {2}.</span></span> <span data-ttu-id="f1432-106">Cela ne correspondait pas au résultat de l’appel {3} sur le nœud testé, qui a produit : {4} .</span><span class="sxs-lookup"><span data-stu-id="f1432-106">This did not match the result of calling {3} on the tested node, which yielded: {4}.</span></span> <span data-ttu-id="f1432-107">Au lieu de cela, l’enfant doit signaler comme son parent le nœud de test.</span><span class="sxs-lookup"><span data-stu-id="f1432-107">Instead, the child should report as its parent the testing node.</span></span>

## <a name="type"></a><span data-ttu-id="f1432-108">Type</span><span class="sxs-lookup"><span data-stu-id="f1432-108">Type</span></span>

<span data-ttu-id="f1432-109">Error</span><span class="sxs-lookup"><span data-stu-id="f1432-109">Error</span></span>

## <a name="description"></a><span data-ttu-id="f1432-110">Description</span><span class="sxs-lookup"><span data-stu-id="f1432-110">Description</span></span>

<span data-ttu-id="f1432-111">Un problème est survenu lors de la navigation entre les enfants de l’élément.</span><span class="sxs-lookup"><span data-stu-id="f1432-111">There is a problem when navigating between element’s children.</span></span> <span data-ttu-id="f1432-112">1.</span><span class="sxs-lookup"><span data-stu-id="f1432-112">1.</span></span> <span data-ttu-id="f1432-113">Implémentation d’UI Automation incorrecte ou non valide.</span><span class="sxs-lookup"><span data-stu-id="f1432-113">An incorrect or invalid UI Automation implementation.</span></span>

<span data-ttu-id="f1432-114">Ce problème peut entraîner des problèmes de navigation pour les outils automatisés, car le parcours des éléments peut être erratique et imprévisible.</span><span class="sxs-lookup"><span data-stu-id="f1432-114">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="f1432-115">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="f1432-115">Possible causes</span></span>

<span data-ttu-id="f1432-116">Implémentation d’UI Automation incorrecte ou non valide.</span><span class="sxs-lookup"><span data-stu-id="f1432-116">An incorrect or invalid UI Automation implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1432-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f1432-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1432-118">**IUIAutomationElement::GetCachedParent**</span><span class="sxs-lookup"><span data-stu-id="f1432-118">**IUIAutomationElement::GetCachedParent**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent)
</dt> <dt>

[<span data-ttu-id="f1432-119">**IUIAutomationTreeWalker**</span><span class="sxs-lookup"><span data-stu-id="f1432-119">**IUIAutomationTreeWalker**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)
</dt> </dl>

 

 




