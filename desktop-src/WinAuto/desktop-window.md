---
title: Fenêtre du Bureau (référence des éléments d’interface utilisateur MSAA)
description: La fenêtre bureau affiche la vue Liste du Bureau (qui contient des icônes comme Poste de travail) et la barre des tâches qui contient le bouton Démarrer.
ms.assetid: 3668c26e-6462-4219-95d3-507811ed7f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58208b3993964a367d093174d58d705beda23d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379696"
---
# <a name="desktop-window-msaa-ui-element-reference"></a><span data-ttu-id="d37d9-103">Fenêtre du Bureau (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="d37d9-103">Desktop Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="d37d9-104">La fenêtre bureau affiche la vue Liste du Bureau (qui contient des icônes comme Poste de travail) et la barre des tâches qui contient le bouton **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="d37d9-104">The desktop window displays the desktop list view (which contains icons such as My Computer) and the taskbar that contains the **Start** button.</span></span>

<span data-ttu-id="d37d9-105">Cet objet est rarement interrogé par les clients, car l’affichage de liste et la barre des tâches couvrent tout le bureau.</span><span class="sxs-lookup"><span data-stu-id="d37d9-105">This object is rarely queried by clients because the list view and the taskbar cover the entire desktop.</span></span> <span data-ttu-id="d37d9-106">L’objet Desktop est récupéré lorsque vous vous connectez, avant que l’interpréteur de commandes du système d’exploitation affiche le mode liste et la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="d37d9-106">The desktop object is retrieved when you log on, before the operating system shell displays the list view and taskbar.</span></span> <span data-ttu-id="d37d9-107">Dans certains cas, le bureau est obtenu lors de la navigation à partir d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="d37d9-107">In some cases, the desktop is obtained when navigating from other objects.</span></span>

<span data-ttu-id="d37d9-108">Le nom de la classe de fenêtre de la fenêtre du Bureau est « \# 32769 ».</span><span class="sxs-lookup"><span data-stu-id="d37d9-108">The window class name for the desktop window is "\#32769".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="d37d9-109">Méthodes IAccessible</span><span class="sxs-lookup"><span data-stu-id="d37d9-109">IAccessible Methods</span></span>

<span data-ttu-id="d37d9-110">La fenêtre du Bureau prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="d37d9-110">The desktop window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="d37d9-111">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="d37d9-111">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="d37d9-112">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="d37d9-112">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="d37d9-113">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="d37d9-113">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="d37d9-114">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="d37d9-114">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="d37d9-115">Propriétés IAccessible</span><span class="sxs-lookup"><span data-stu-id="d37d9-115">IAccessible Properties</span></span>

<span data-ttu-id="d37d9-116">La fenêtre du Bureau prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="d37d9-116">The desktop window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="d37d9-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="d37d9-117">Property</span></span>                                                                 | <span data-ttu-id="d37d9-118">Commentaires</span><span class="sxs-lookup"><span data-stu-id="d37d9-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d37d9-119">**Obtient \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="d37d9-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="d37d9-120">**Obtient \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="d37d9-120">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="d37d9-121">**Obtient \_ accName**</span><span class="sxs-lookup"><span data-stu-id="d37d9-121">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="d37d9-122">La propriété Name est « Desktop ».</span><span class="sxs-lookup"><span data-stu-id="d37d9-122">The Name property is "Desktop".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="d37d9-123">**Obtient \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="d37d9-123">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="d37d9-124">La propriété de **rôle** est [**client de \_ système \_ de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="d37d9-124">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="d37d9-125">**Obtient \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="d37d9-125">**get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="d37d9-126">**Obtient \_ accState**</span><span class="sxs-lookup"><span data-stu-id="d37d9-126">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="d37d9-127">La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="d37d9-127">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="d37d9-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d37d9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d37d9-129">IAccessible, interface</span><span class="sxs-lookup"><span data-stu-id="d37d9-129">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





