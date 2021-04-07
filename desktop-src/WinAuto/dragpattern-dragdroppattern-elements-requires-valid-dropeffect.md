---
title: Les éléments DragPattern/DragDropPattern requièrent un DropEffect valide
description: Les éléments DragPattern/DragDropPattern requièrent un DropEffect valide
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33acda19732e2ebd96182023fce9641012b50d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670977"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a><span data-ttu-id="9fc33-103">Les éléments DragPattern/DragDropPattern requièrent un DropEffect valide</span><span class="sxs-lookup"><span data-stu-id="9fc33-103">DragPattern/DragDropPattern elements requires valid DropEffect</span></span>

## <a name="text"></a><span data-ttu-id="9fc33-104">Texte</span><span class="sxs-lookup"><span data-stu-id="9fc33-104">Text</span></span>

<span data-ttu-id="9fc33-105">Les éléments qui prennent en charge le glisser-déplacer doivent avoir un ensemble’DropEffect’valide</span><span class="sxs-lookup"><span data-stu-id="9fc33-105">Elements that support Drag/Drop should have a valid 'DropEffect' set</span></span>

## <a name="type"></a><span data-ttu-id="9fc33-106">Type</span><span class="sxs-lookup"><span data-stu-id="9fc33-106">Type</span></span>

<span data-ttu-id="9fc33-107">Error</span><span class="sxs-lookup"><span data-stu-id="9fc33-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="9fc33-108">Description</span><span class="sxs-lookup"><span data-stu-id="9fc33-108">Description</span></span>

<span data-ttu-id="9fc33-109">L’élément prend en charge [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) ou [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), mais ne dispose pas d’un jeu de propriétés [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) valide.</span><span class="sxs-lookup"><span data-stu-id="9fc33-109">The element supports either [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) or [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), but does not have a valid [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property set.</span></span>

<span data-ttu-id="9fc33-110">Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran.</span><span class="sxs-lookup"><span data-stu-id="9fc33-110">This issue causes problems for people who rely on a screen-reader.</span></span> <span data-ttu-id="9fc33-111">L’utilisateur ne sera pas en mesure d’indiquer l’effet de cet objet lors de son déplacement.</span><span class="sxs-lookup"><span data-stu-id="9fc33-111">The user will not be able to tell what effect this object has when dragging.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="9fc33-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="9fc33-112">Possible causes</span></span>

-   <span data-ttu-id="9fc33-113">L’élément, ou son parent, n’a pas créé le [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) ou [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) un nom ou une étiquette incorrectement assigné.</span><span class="sxs-lookup"><span data-stu-id="9fc33-113">The element, or its parent, has not created the [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) or [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="9fc33-114">Un développeur ne sait pas que les lecteurs d’écran lisent les DropEffect.</span><span class="sxs-lookup"><span data-stu-id="9fc33-114">A developer is not aware that screen readers read DropEffect(s).</span></span>

 

 




