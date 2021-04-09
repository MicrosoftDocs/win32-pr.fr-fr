---
title: Comment utiliser des groupes dans un List-View
description: Cette rubrique explique comment créer une instance d’un groupe et l’ajouter à un contrôle List View.
ms.assetid: 8486B9A2-C519-4912-9E88-3BAFCC4D51CF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec47d73c3e8b808eaf1909bdafb015c7eebc37de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103842898"
---
# <a name="how-to-use-groups-in-a-list-view"></a><span data-ttu-id="7b379-103">Comment utiliser des groupes dans un List-View</span><span class="sxs-lookup"><span data-stu-id="7b379-103">How to Use Groups in a List-View</span></span>

<span data-ttu-id="7b379-104">Cette rubrique explique comment créer une instance d’un groupe et l’ajouter à un contrôle List View.</span><span class="sxs-lookup"><span data-stu-id="7b379-104">This topic describes how to create an instance of a group and add it to a list-view control.</span></span> <span data-ttu-id="7b379-105">Le regroupement permet à un utilisateur de réorganiser des listes en groupes d’éléments qui sont répartis visuellement sur la page, à l’aide d’un séparateur horizontal et d’un titre de groupe.</span><span class="sxs-lookup"><span data-stu-id="7b379-105">Grouping allows a user to arrange lists into groups of items that are visually divided on the page, using a horizontal divider and a group title.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7b379-106">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="7b379-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7b379-107">Technologies</span><span class="sxs-lookup"><span data-stu-id="7b379-107">Technologies</span></span>

-   [<span data-ttu-id="7b379-108">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="7b379-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7b379-109">Prérequis</span><span class="sxs-lookup"><span data-stu-id="7b379-109">Prerequisites</span></span>

-   <span data-ttu-id="7b379-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="7b379-110">C/C++</span></span>
-   <span data-ttu-id="7b379-111">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="7b379-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7b379-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="7b379-112">Instructions</span></span>


<span data-ttu-id="7b379-113">Pour utiliser des groupes dans un contrôle List-View, assurez-vous que le contrôle comprend le style de fenêtre [**LVS \_ ALIGNTOP**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7b379-113">To use groups in a list-view control, ensure that the control includes the [**LVS\_ALIGNTOP**](list-view-window-styles.md) window style.</span></span>

<span data-ttu-id="7b379-114">Lorsque vous ajoutez un élément à la liste, vous l’affectez à un groupe en définissant le membre **iGroupId** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) de l’élément sur la valeur du membre **iGroupId** de la structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) du groupe.</span><span class="sxs-lookup"><span data-stu-id="7b379-114">When you add an item to the list, you assign it to a group by setting the **iGroupId** member of the item's [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure to the value of the **iGroupId** member of the groups's [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure.</span></span> <span data-ttu-id="7b379-115">Un élément qui n’est pas assigné à un groupe n’apparaît pas dans la liste lorsque la vue de groupe est activée.</span><span class="sxs-lookup"><span data-stu-id="7b379-115">An item that is not assigned to a group does not appear in the list when group view is enabled.</span></span> <span data-ttu-id="7b379-116">Pour activer ou désactiver la vue de groupe, utilisez la macro [**ListView \_ EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) .</span><span class="sxs-lookup"><span data-stu-id="7b379-116">To enable or disable group view, use the [**ListView\_EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) macro.</span></span>

<span data-ttu-id="7b379-117">L’exemple suivant montre comment créer un groupe avec un en-tête et l’ajouter à un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="7b379-117">The following example shows how to create a group with a header and add it to a list-view control.</span></span>


```C++
    LVGROUP group;

    group.cbSize    = sizeof(LVGROUP);
    group.mask      = LVGF_HEADER | LVGF_GROUPID;
    group.pszHeader = TEXT("Dogs");
    group.iGroupId  = 1;

    ListView_InsertGroup(hWndListView, -1, &group);

```



## <a name="related-topics"></a><span data-ttu-id="7b379-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b379-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b379-119">Référence du contrôle List-View</span><span class="sxs-lookup"><span data-stu-id="7b379-119">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="7b379-120">À propos des contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="7b379-120">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="7b379-121">Utilisation de contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="7b379-121">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




