---
title: Compréhension des problèmes de performances
description: Cette rubrique décrit les problèmes de performances associés à l’utilisation des modèles de contrôle Text et TextRange.
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- clients, comprendre les problèmes de performances
- clients, contrôles textuels
- clients, plages de texte
- clients, modèle de contrôle de texte
- clients, modèle de contrôle TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d8d9b9b6c5cb0ef3ed34c6960e5aeafa623068
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316824"
---
# <a name="understanding-performance-issues"></a><span data-ttu-id="4d1df-108">Compréhension des problèmes de performances</span><span class="sxs-lookup"><span data-stu-id="4d1df-108">Understanding Performance Issues</span></span>

<span data-ttu-id="4d1df-109">Cette rubrique décrit les problèmes de performances associés à l’utilisation des modèles de contrôle [Text et TextRange](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="4d1df-109">This topic describes performance issues associated with using the [Text and TextRange](uiauto-implementingtextandtextrange.md) control patterns.</span></span>


<span data-ttu-id="4d1df-110">Les interfaces [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) et [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) s’appuient sur des appels interprocessus ; elles ne fournissent pas de mécanisme de mise en cache pour améliorer les performances lors de la récupération ou du traitement de contenu textuel.</span><span class="sxs-lookup"><span data-stu-id="4d1df-110">The [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) and [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) interfaces rely on cross-process calls—they do not provide a caching mechanism to improve performance when retrieving or processing textual content.</span></span>

<span data-ttu-id="4d1df-111">Une application cliente peut améliorer les performances à l’aide de la méthode [**IUIAutomationTextRange :: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) pour récupérer des blocs de texte de taille modérée.</span><span class="sxs-lookup"><span data-stu-id="4d1df-111">A client application can improve performance by using the [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) method to retrieve moderately sized blocks of text.</span></span> <span data-ttu-id="4d1df-112">Par exemple, l’utilisation de **gettext** pour récupérer des caractères uniques entraînera un impact sur les performances inter-processus pour chaque caractère, alors que la non-spécification d’une longueur maximale lors de l’appel de **gettext** entraînera un accès inter-processus, mais peut présenter une latence élevée selon la taille de la plage de texte.</span><span class="sxs-lookup"><span data-stu-id="4d1df-112">For example, using **GetText** to retrieve single characters will incur a cross-process performance hit for each character, whereas not specifying a maximum length when calling **GetText** will incur one cross-process hit, but can have high latency depending on the size of the text range.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d1df-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4d1df-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d1df-114">Modèles de contrôle Text et TextRange</span><span class="sxs-lookup"><span data-stu-id="4d1df-114">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="4d1df-115">Prise en charge d’UI Automation pour le contenu textuel</span><span class="sxs-lookup"><span data-stu-id="4d1df-115">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="4d1df-116">Utilisation de contrôles textuels</span><span class="sxs-lookup"><span data-stu-id="4d1df-116">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




