---
title: Menus contextuels
description: Menus contextuels
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Windows Media Player Online stores, menus contextuels
- magasins en ligne, menus contextuels
- types 1 magasins en ligne, menus contextuels
- Windows Media Player Online stores, menus contextuels personnalisés
- magasins en ligne, menus contextuels personnalisés
- types 1 magasins en ligne, menus contextuels personnalisés
- menus contextuels
- menus contextuels personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba3ed52b408651607cb1f6dab1a04f53282d3ef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381473"
---
# <a name="context-menus"></a><span data-ttu-id="5ae74-111">Menus contextuels</span><span class="sxs-lookup"><span data-stu-id="5ae74-111">Context Menus</span></span>

<span data-ttu-id="5ae74-112">Les magasins en ligne peuvent fournir des menus contextuels personnalisés.</span><span class="sxs-lookup"><span data-stu-id="5ae74-112">Online stores can provide custom context menus.</span></span> <span data-ttu-id="5ae74-113">Pour ce faire, le plug-in du magasin en ligne implémente la méthode [IWMPContentPartner :: GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) .</span><span class="sxs-lookup"><span data-stu-id="5ae74-113">To do this, the online store plug-in implements the [IWMPContentPartner::GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) method.</span></span> <span data-ttu-id="5ae74-114">Le lecteur Windows Media appelle cette méthode pour fournir des informations sur l’emplacement dans l’interface utilisateur où le menu contextuel s’affiche (où l’utilisateur a cliqué avec le bouton droit).</span><span class="sxs-lookup"><span data-stu-id="5ae74-114">Windows Media Player calls this method to provide information about the location in the user interface where the context menu is displayed (where the user right-clicked).</span></span> <span data-ttu-id="5ae74-115">Le plug-in retourne un tableau de structures [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) qui décrivent chaque élément de menu contextuel, y compris un ID de commande pour chacun.</span><span class="sxs-lookup"><span data-stu-id="5ae74-115">The plug-in returns an array of [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) structures that describe each context menu item, including a command ID for each.</span></span>

<span data-ttu-id="5ae74-116">Une fois que le lecteur Windows Media a récupéré le tableau, le lecteur utilise le tableau pour générer le menu contextuel que l’utilisateur voit.</span><span class="sxs-lookup"><span data-stu-id="5ae74-116">After Windows Media Player has retrieved the array, the Player uses the array to build the context menu the user sees.</span></span> <span data-ttu-id="5ae74-117">Quand l’utilisateur clique sur un élément dans le menu contextuel, le lecteur appelle [IWMPContentPartner :: commande InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), en passant l’ID de commande associé à l’élément de menu par le biais du paramètre *dwCommandID* .</span><span class="sxs-lookup"><span data-stu-id="5ae74-117">When the user clicks an item in the context menu, the Player calls [IWMPContentPartner::InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), passing the command ID associated with the menu item through the *dwCommandID* parameter.</span></span> <span data-ttu-id="5ae74-118">Le lecteur passe également une valeur d’emplacement de bibliothèque et un tableau d’ID qui représente les éléments sur lesquels le menu a été appelé, tel qu’un tableau d’ID de suivi.</span><span class="sxs-lookup"><span data-stu-id="5ae74-118">The Player also passes a library location value and an array of IDs that represents the items the menu was invoked upon, such as an array of track IDs.</span></span> <span data-ttu-id="5ae74-119">À l’aide de ces informations, le plug-in peut démarrer tout processus approprié en réponse au clic de la souris de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5ae74-119">By using this information, the plug-in can start any appropriate process in response to the user's mouse click.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ae74-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ae74-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ae74-121">**À propos des magasins en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="5ae74-121">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




