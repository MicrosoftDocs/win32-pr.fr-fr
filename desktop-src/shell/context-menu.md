---
description: Cette section décrit la création de menus contextuels (contextuels) et l’implémentation des gestionnaires de menu contextuel (verbe).
title: Menus contextuels (menu contextuel) et gestionnaires de menus contextuels
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 956f3b10-2bc6-4f1f-a6ed-7184f94b545a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 286dd9c860ae79e5124439439da97f206b4aa436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201275"
---
# <a name="shortcut-context-menus-and-shortcut-menu-handlers"></a><span data-ttu-id="42b0e-103">Menus contextuels (menu contextuel) et gestionnaires de menus contextuels</span><span class="sxs-lookup"><span data-stu-id="42b0e-103">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>

<span data-ttu-id="42b0e-104">Cette section décrit la création de menus contextuels (contextuels) et l’implémentation des gestionnaires de menu contextuel (verbe).</span><span class="sxs-lookup"><span data-stu-id="42b0e-104">This section discusses the creation of shortcut (context) menus, and the implementation of shortcut menu (verb) handlers.</span></span>

<span data-ttu-id="42b0e-105">Cette section sur les types de fichiers et les associations de fichiers est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="42b0e-105">This section on file types and file associations is organized as follows:</span></span>

-   [<span data-ttu-id="42b0e-106">Verbes et associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="42b0e-106">Verbs and File Associations</span></span>](fa-verbs.md)
-   [<span data-ttu-id="42b0e-107">Choix d’une méthode de menu contextuel statique ou dynamique</span><span class="sxs-lookup"><span data-stu-id="42b0e-107">Choosing a Static or Dynamic Shortcut Menu Method</span></span>](shortcut-choose-method.md)
-   [<span data-ttu-id="42b0e-108">Meilleures pratiques pour les gestionnaires de menus contextuels et les verbes multiples</span><span class="sxs-lookup"><span data-stu-id="42b0e-108">Best Practices for Shortcut Menu Handlers and Multiple Verbs</span></span>](verbs-best-practices.md)
-   [<span data-ttu-id="42b0e-109">Création de gestionnaires de menu contextuel</span><span class="sxs-lookup"><span data-stu-id="42b0e-109">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
-   [<span data-ttu-id="42b0e-110">Création de menus en cascade statiques</span><span class="sxs-lookup"><span data-stu-id="42b0e-110">Creating Static Cascading Menus</span></span>](creating-static-cascading-menus.md)
-   [<span data-ttu-id="42b0e-111">Comment supprimer et contrôler la visibilité des verbes</span><span class="sxs-lookup"><span data-stu-id="42b0e-111">How to Suppress and Control Verb Visibility</span></span>](how-to-suppress-and-control-visibility.md)
-   [<span data-ttu-id="42b0e-112">Comment utiliser le modèle de sélection de verbe</span><span class="sxs-lookup"><span data-stu-id="42b0e-112">How to Employ the Verb Selection Model</span></span>](how-to-employ-the-verb-selection-model.md)
-   [<span data-ttu-id="42b0e-113">Utilisation des attributs d’élément</span><span class="sxs-lookup"><span data-stu-id="42b0e-113">How to Use Item Attributes</span></span>](how-to-use-item-attributes.md)
-   [<span data-ttu-id="42b0e-114">Comment implémenter des verbes personnalisés pour les dossiers via Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="42b0e-114">How to Implement Custom Verbs for Folders through Desktop.ini</span></span>](how-to-implement-custom-verbs-for-folders-through-desktop-ini.md)
-   [<span data-ttu-id="42b0e-115">Personnalisation d’un menu contextuel à l’aide de verbes dynamiques</span><span class="sxs-lookup"><span data-stu-id="42b0e-115">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
-   [<span data-ttu-id="42b0e-116">Comment implémenter l’interface IContextMenu</span><span class="sxs-lookup"><span data-stu-id="42b0e-116">How to Implement the IContextMenu Interface</span></span>](how-to-implement-the-icontextmenu-interface.md)
-   [<span data-ttu-id="42b0e-117">Référence du menu contextuel</span><span class="sxs-lookup"><span data-stu-id="42b0e-117">Shortcut Menu Reference</span></span>](context-menu-reference.md)

## <a name="additional-resources"></a><span data-ttu-id="42b0e-118">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="42b0e-118">Additional Resources</span></span>

<span data-ttu-id="42b0e-119">Pour en savoir plus sur l’arrière-plan conceptuel, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="42b0e-119">For related conceptual background, see the following topics:</span></span>

-   <span data-ttu-id="42b0e-120">[Présentation des associations de fichiers](fa-intro.md).</span><span class="sxs-lookup"><span data-stu-id="42b0e-120">[Introduction to File Associations](fa-intro.md).</span></span>
-   <span data-ttu-id="42b0e-121">Pour étendre l’interpréteur de commandes avec des gestionnaires de types de fichiers, consultez [création de gestionnaires d’extension de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="42b0e-121">To extend the Shell with file type handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>
-   <span data-ttu-id="42b0e-122">Pour créer un magasin de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](nse-implement.md).</span><span class="sxs-lookup"><span data-stu-id="42b0e-122">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span></span>

<span data-ttu-id="42b0e-123">Pour obtenir des informations de référence connexes documentation, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="42b0e-123">For related reference documenation, see the following topics:</span></span>

-   <span data-ttu-id="42b0e-124">Pour exécuter un verbe sur un élément de Shell, consultez la méthode [**InvokeVerb**](folderitem-invokeverb.md) .</span><span class="sxs-lookup"><span data-stu-id="42b0e-124">To execute a verb on a Shell item, see the [**InvokeVerb**](folderitem-invokeverb.md) method.</span></span>
-   <span data-ttu-id="42b0e-125">Pour récupérer une collection de verbes qui peuvent être exécutés sur un élément de Shell, consultez la méthode [**Verbs**](folderitem-verbs.md) .</span><span class="sxs-lookup"><span data-stu-id="42b0e-125">To retrieve a collection of verbs that can be executed on a Shell item, see the [**Verbs**](folderitem-verbs.md) method.</span></span>
-   <span data-ttu-id="42b0e-126">Pour effectuer une opération sur un fichier spécifié, consultez les fonctions [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .</span><span class="sxs-lookup"><span data-stu-id="42b0e-126">To perform an operation on a specified file, see either the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) functions.</span></span>

 

 



