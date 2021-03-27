---
description: Lorsque vous fournissez un aperçu, les instructions suivantes doivent être suivies.
title: Instructions du gestionnaire d’aperçus
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e725d561056e78a88bd9eeabd00d90abda1f0343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866153"
---
# <a name="preview-handler-guidelines"></a><span data-ttu-id="ef27c-103">Instructions du gestionnaire d’aperçus</span><span class="sxs-lookup"><span data-stu-id="ef27c-103">Preview Handler Guidelines</span></span>

<span data-ttu-id="ef27c-104">Lorsque vous fournissez un aperçu, les instructions suivantes doivent être suivies.</span><span class="sxs-lookup"><span data-stu-id="ef27c-104">When you provide a preview, the following guidelines should be followed.</span></span>

-   <span data-ttu-id="ef27c-105">Un aperçu doit contenir une interface utilisateur minimale ; il s’agit simplement d’une version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="ef27c-105">A preview should contain minimal UI—it is simply a preview.</span></span> <span data-ttu-id="ef27c-106">Elle doit afficher uniquement le contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="ef27c-106">It should display only the file content.</span></span> <span data-ttu-id="ef27c-107">Elle ne doit pas afficher de boîtes de dialogue, d’écrans de démarrage, de barres d’outils ou de volets de tâches.</span><span class="sxs-lookup"><span data-stu-id="ef27c-107">It should not display dialogs, splash screens, toolbars, or task panes.</span></span> <span data-ttu-id="ef27c-108">Le volet de lecture est couramment utilisé conjointement avec la recherche pour identifier rapidement un fichier.</span><span class="sxs-lookup"><span data-stu-id="ef27c-108">The reading pane will commonly be used in conjunction with search to quickly identify a file.</span></span> <span data-ttu-id="ef27c-109">Tout ce qui encombre le volet de lecture ou qui dépasse le contenu du fichier ou provoque l’évitement des retards dans l’affichage de l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="ef27c-109">Anything that clutters the reading pane or otherwise detracts from file content or causes delays in preview display should be avoided.</span></span>
-   <span data-ttu-id="ef27c-110">La version préliminaire doit permettre à l’utilisateur de naviguer dans le document.</span><span class="sxs-lookup"><span data-stu-id="ef27c-110">The preview should allow the user to navigate in the document.</span></span> <span data-ttu-id="ef27c-111">L’utilisateur doit également pouvoir sélectionner et copier du texte.</span><span class="sxs-lookup"><span data-stu-id="ef27c-111">The user should also be able to select and copy text.</span></span>
-   <span data-ttu-id="ef27c-112">L’aperçu ne doit pas consommer beaucoup de mémoire, doit consommer un minimum de ressources et doit avoir un temps de démarrage rapide.</span><span class="sxs-lookup"><span data-stu-id="ef27c-112">The preview should not be memory-intensive, should consume minimal resources, and should have a fast startup time.</span></span>
-   <span data-ttu-id="ef27c-113">L’exécution de tous les scripts et macros dans le fichier en cours d’aperçu doit être bloquée à des fins de sécurité et de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="ef27c-113">All script and macros in the file being previewed should be blocked from running for security and privacy purposes.</span></span>
-   <span data-ttu-id="ef27c-114">La version préliminaire doit prendre en charge les accélérateurs de clavier pour la navigation et la sélection, comme pris en charge par l’application.</span><span class="sxs-lookup"><span data-stu-id="ef27c-114">The preview should support keyboard accelerators for navigation and selection as supported by the application.</span></span> <span data-ttu-id="ef27c-115">Il doit également afficher un menu contextuel lorsque l’utilisateur clique avec le bouton droit.</span><span class="sxs-lookup"><span data-stu-id="ef27c-115">It should also display a context menu when right-clicked.</span></span>
-   <span data-ttu-id="ef27c-116">Lorsqu’un fichier est affiché en tant qu’aperçu, l’aperçu ne doit pas verrouiller le fichier lui-même.</span><span class="sxs-lookup"><span data-stu-id="ef27c-116">When a file is displayed as a preview, the preview should not lock the file itself.</span></span> <span data-ttu-id="ef27c-117">Un fichier peut être visualisé et ouvert dans son application associée en même temps.</span><span class="sxs-lookup"><span data-stu-id="ef27c-117">A file can be previewed and opened in its associated application at the same time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef27c-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef27c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef27c-119">Gestionnaires d’aperçus et hôte de l’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="ef27c-119">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="ef27c-120">Génération de gestionnaires d’aperçus</span><span class="sxs-lookup"><span data-stu-id="ef27c-120">Building Preview Handlers</span></span>](building-preview-handlers.md)
</dt> </dl>

 

 



