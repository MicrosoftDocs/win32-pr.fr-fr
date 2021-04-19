---
description: Implémentation des extensions de menu contextuel
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: Implémentation des extensions de menu contextuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65918f385984355490456cccb626ba297bd3368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518491"
---
# <a name="implementing-context-menu-extensions"></a><span data-ttu-id="69e9a-103">Implémentation des extensions de menu contextuel</span><span class="sxs-lookup"><span data-stu-id="69e9a-103">Implementing Context Menu Extensions</span></span>

<span data-ttu-id="69e9a-104">L’extension d’espace de noms WPD prend en charge les menus contextuels (ou raccourcis) extensibles.</span><span class="sxs-lookup"><span data-stu-id="69e9a-104">The WPD Namespace Extension supports extensible context (or shortcut) menus.</span></span> <span data-ttu-id="69e9a-105">Voici les menus qui s’affichent lorsqu’un utilisateur clique avec le bouton droit sur un objet tel qu’un fichier ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="69e9a-105">These are the menus that appear when a user right-clicks on an object such as a file or a folder.</span></span> <span data-ttu-id="69e9a-106">Certaines applications WPD tirent parti de ces menus extensibles pour prendre en charge les opérations sur le contenu côté appareil (ou les objets qui résident sur l’appareil).</span><span class="sxs-lookup"><span data-stu-id="69e9a-106">Some WPD applications will take advantage of these extensible menus to support operations on device-side content (or objects that reside on the device).</span></span>

<span data-ttu-id="69e9a-107">Les menus contextuels extensibles sont pris en charge par les interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="69e9a-107">Extensible context menus are supported by the interfaces described in the following table.</span></span> <span data-ttu-id="69e9a-108">Pour plus d’informations sur l’une de ces interfaces, consultez le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="69e9a-108">For more information about any of these interfaces, see the Windows SDK.</span></span>



| <span data-ttu-id="69e9a-109">Interface</span><span class="sxs-lookup"><span data-stu-id="69e9a-109">Interface</span></span>           | <span data-ttu-id="69e9a-110">Description</span><span class="sxs-lookup"><span data-stu-id="69e9a-110">Description</span></span>                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69e9a-111">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="69e9a-111">IContextMenu</span></span>        | <span data-ttu-id="69e9a-112">L’interpréteur de commandes de Windows Vista appelle les méthodes dans cette interface pour créer ou fusionner le nouveau menu contextuel avec l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="69e9a-112">The Windows Vista Shell calls the methods in this interface to create or merge the new context menu with the given object.</span></span> |
| <span data-ttu-id="69e9a-113">IDataObject</span><span class="sxs-lookup"><span data-stu-id="69e9a-113">IDataObject</span></span>         | <span data-ttu-id="69e9a-114">Utilisé pour passer le tableau PIDL du menu contextuel au gestionnaire de menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="69e9a-114">Used to pass the context menu's PIDL array to the context menu handler.</span></span>                                                    |
| <span data-ttu-id="69e9a-115">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="69e9a-115">IPropertySetStorage</span></span> | <span data-ttu-id="69e9a-116">Cette interface est utilisée pour récupérer les propriétés WPD pour l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="69e9a-116">This interface is used to retrieve WPD properties for the given object.</span></span>                                                    |
| <span data-ttu-id="69e9a-117">IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="69e9a-117">IPropertyStorage</span></span>    | <span data-ttu-id="69e9a-118">Cette interface est également utilisée pour récupérer les propriétés WPD pour l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="69e9a-118">This interface is also used to retrieve WPD properties for the given object.</span></span>                                               |
| <span data-ttu-id="69e9a-119">IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="69e9a-119">IShellExtInit</span></span>       | <span data-ttu-id="69e9a-120">Initialise les extensions de l’interpréteur de commandes Windows Vista pour le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="69e9a-120">Initializes the Windows Vista Shell extensions for the context menu.</span></span>                                                       |
| <span data-ttu-id="69e9a-121">IStream</span><span class="sxs-lookup"><span data-stu-id="69e9a-121">IStream</span></span>             | <span data-ttu-id="69e9a-122">À fournir.</span><span class="sxs-lookup"><span data-stu-id="69e9a-122">To be supplied.</span></span>                                                                                                            |



 

<span data-ttu-id="69e9a-123">Les menus contextuels pour les API WPD sont implémentés comme n’importe quel autre menu contextuel dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="69e9a-123">Context menus for WPD are implemented like any other context menu in Windows Vista.</span></span> <span data-ttu-id="69e9a-124">Si vous avez déjà implémenté un gestionnaire de menu contextuel, vous pouvez modifier votre code existant afin qu’il prenne en charge le contenu côté appareil.</span><span class="sxs-lookup"><span data-stu-id="69e9a-124">If you've already implemented a context menu handler, you can modify your existing code so that it supports device-side content.</span></span> <span data-ttu-id="69e9a-125">Si vous n’avez jamais créé de gestionnaire de menu contextuel, consultez la rubrique Création de gestionnaires de menu contextuel dans la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="69e9a-125">If you have never created a context menu handler, see the Creating Context Menu Handlers topic in the Windows SDK.</span></span>

<span data-ttu-id="69e9a-126">Les deux points auxquels un gestionnaire de menu contextuel WPD diffère de tout autre gestionnaire se trouvent dans l’inscription du gestionnaire et la prise en charge du contenu côté appareil.</span><span class="sxs-lookup"><span data-stu-id="69e9a-126">The two points at which a WPD context menu handler differs from any other handler is in the handler registration and the support of device-side content.</span></span>

 

 



