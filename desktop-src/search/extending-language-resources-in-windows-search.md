---
description: Windows Search utilise des ressources de langage telles que les analyseurs lexicaux et les générateurs de formes dérivées pour scinder le texte dans ses paramètres régionaux natifs lors de la création d’index et du traitement des requêtes.
ms.assetid: 6e8ab091-c22c-4425-b8b9-211d53816304
title: Extension des ressources linguistiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727f5812d0aee370c96d98f1c57dfffcbea5bc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513983"
---
# <a name="extending-language-resources"></a><span data-ttu-id="f1582-103">Extension des ressources linguistiques</span><span class="sxs-lookup"><span data-stu-id="f1582-103">Extending Language Resources</span></span>

<span data-ttu-id="f1582-104">Windows Search utilise des ressources de langage telles que les analyseurs lexicaux et les générateurs de formes dérivées pour scinder le texte dans ses paramètres régionaux natifs lors de la création d’index et du traitement des requêtes.</span><span class="sxs-lookup"><span data-stu-id="f1582-104">Windows Search uses language resources such as word breakers and stemmers to break text in its native locale during index creation and query processing.</span></span> <span data-ttu-id="f1582-105">Microsoft fournit des analyseurs lexicaux et des générateurs de formes dérivées pour plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="f1582-105">Microsoft provides word breakers and stemmers for several languages.</span></span> <span data-ttu-id="f1582-106">Cette section décrit comment implémenter et utiliser des analyseurs lexicaux et des générateurs de formes dérivées personnalisés pour des langues et des paramètres régionaux autres que ceux fournis par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f1582-106">This section describes how to implement and use custom word breakers and stemmers for languages and locales beyond those provided by Microsoft.</span></span>

-   [<span data-ttu-id="f1582-107">Fonctionnement des composants de ressources linguistiques</span><span class="sxs-lookup"><span data-stu-id="f1582-107">Understanding Language Resource Components</span></span>](understanding-language-resource-components.md)
-   [<span data-ttu-id="f1582-108">Implémentation d’un analyseur lexical et du générateur de formes dérivées</span><span class="sxs-lookup"><span data-stu-id="f1582-108">Implementing a Word Breaker and Stemmer</span></span>](implementing-a-word-breaker-and-stemmer.md)
-   [<span data-ttu-id="f1582-109">Considérations linguistiques et Unicode</span><span class="sxs-lookup"><span data-stu-id="f1582-109">Linguistic and Unicode Considerations</span></span>](linguistic-and-unicode-considerations.md)
-   [<span data-ttu-id="f1582-110">Ressources et meilleures pratiques pour la résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="f1582-110">Troubleshooting Language Resources and Best Practices</span></span>](troubleshooting-language-resources.md)

## <a name="additional-resources"></a><span data-ttu-id="f1582-111">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f1582-111">Additional Resources</span></span>

-   <span data-ttu-id="f1582-112">Pour obtenir la liste des lanuages prises en charge par les analyseurs lexicaux, consultez [langues prises en charge par Windows Search](-search-3x-wds-language-support.md).</span><span class="sxs-lookup"><span data-stu-id="f1582-112">For a list of lanuages supported by word breakers, see [Languages Supported by Windows Search](-search-3x-wds-language-support.md).</span></span>
-   <span data-ttu-id="f1582-113">Si vous devez identifier la langue d’un morceau de texte, vous pouvez utiliser la détection automatique de la langue (diagnostic Linux), qui est disponible dans Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f1582-113">If you need to identify the language of a piece of text, you can use Language Auto-Detection (LAD), which is available in Windows 7 and later.</span></span> <span data-ttu-id="f1582-114">Pour plus d’informations, consultez [services linguistiques étendus](../intl/extended-linguistic-services.md) (ELS).</span><span class="sxs-lookup"><span data-stu-id="f1582-114">For more information, see [Extended Linguistic Services](../intl/extended-linguistic-services.md) (ELS).</span></span>
-   <span data-ttu-id="f1582-115">Pour obtenir la documentation de référence applicable, consultez [interfaces de complément de données](-search-data-addins-interfaces-entry-page.md).</span><span class="sxs-lookup"><span data-stu-id="f1582-115">For applicable reference documentation, see [Data Add-in Interfaces](-search-data-addins-interfaces-entry-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1582-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f1582-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1582-117">Gestion de l’index</span><span class="sxs-lookup"><span data-stu-id="f1582-117">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="f1582-118">Interrogation de l’index programmatiquement</span><span class="sxs-lookup"><span data-stu-id="f1582-118">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="f1582-119">Extension de l’index</span><span class="sxs-lookup"><span data-stu-id="f1582-119">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
