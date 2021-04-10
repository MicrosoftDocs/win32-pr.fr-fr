---
title: Comment ajouter un élément à un contrôle header
description: Cette rubrique montre comment ajouter un élément à un contrôle header.
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cf020c95a9dfe06bb06370533fdfd9416ddfef
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941493"
---
# <a name="how-to-add-an-item-to-a-header-control"></a><span data-ttu-id="ade98-103">Comment ajouter un élément à un contrôle header</span><span class="sxs-lookup"><span data-stu-id="ade98-103">How to Add an Item to a Header Control</span></span>

<span data-ttu-id="ade98-104">Cette rubrique montre comment ajouter un élément à un contrôle header.</span><span class="sxs-lookup"><span data-stu-id="ade98-104">This topic demonstrates how to add an item to a header control.</span></span> <span data-ttu-id="ade98-105">Un contrôle header contient généralement plusieurs éléments d’en-tête qui définissent les colonnes du contrôle.</span><span class="sxs-lookup"><span data-stu-id="ade98-105">A header control typically has several header items that define the columns of the control.</span></span> <span data-ttu-id="ade98-106">Vous pouvez ajouter un élément à un contrôle header en envoyant le message [**HDM \_ INSERTITEM**](hdm-insertitem.md) au contrôle.</span><span class="sxs-lookup"><span data-stu-id="ade98-106">You can add an item to a header control by sending the [**HDM\_INSERTITEM**](hdm-insertitem.md) message to the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ade98-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="ade98-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ade98-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="ade98-108">Technologies</span></span>

-   [<span data-ttu-id="ade98-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="ade98-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ade98-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="ade98-110">Prerequisites</span></span>

-   <span data-ttu-id="ade98-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="ade98-111">C/C++</span></span>
-   <span data-ttu-id="ade98-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="ade98-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ade98-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="ade98-113">Instructions</span></span>


<span data-ttu-id="ade98-114">Utilisez le message [**HDM \_ INSERTITEM**](hdm-insertitem.md) pour ajouter un élément au contrôle header.</span><span class="sxs-lookup"><span data-stu-id="ade98-114">Use the [**HDM\_INSERTITEM**](hdm-insertitem.md) message to add an item to the header control.</span></span> <span data-ttu-id="ade98-115">Le message doit inclure l’adresse d’une structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) .</span><span class="sxs-lookup"><span data-stu-id="ade98-115">The message must include the address of an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure.</span></span> <span data-ttu-id="ade98-116">Cette structure définit les propriétés de l’élément d’en-tête, qui peut inclure une chaîne, une image bitmap, une taille initiale et une valeur 32 bits définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="ade98-116">This structure defines the properties of the header item, which can include a string, a bitmapped image, an initial size, and an application-defined 32-bit value.</span></span>

<span data-ttu-id="ade98-117">L’exemple suivant illustre l’utilisation du message [**HDM \_ INSERTITEM**](hdm-insertitem.md) et de la structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) pour ajouter un élément à un contrôle header.</span><span class="sxs-lookup"><span data-stu-id="ade98-117">The following example illustrates how to use the [**HDM\_INSERTITEM**](hdm-insertitem.md) message and the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure to add an item to a header control.</span></span> <span data-ttu-id="ade98-118">Le nouvel élément est constitué d’une chaîne qui est alignée à gauche dans le rectangle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ade98-118">The new item consists of a string that is left-justified within the item rectangle.</span></span>



```C++
// DoInsertItem - inserts an item into a header control. 
// Returns the index of the new item. 
// hwndHeader - handle to the header control. 
// iInsertAfter - index of the previous item. 
// nWidth - width of the new item. 
// lpsz - address of the item string. 
int DoInsertItem(HWND hwndHeader, int iInsertAfter, 
    int nWidth, LPTSTR lpsz) 
{ 
    HDITEM hdi; 
    int index; 
 
    hdi.mask = HDI_TEXT | HDI_FORMAT | HDI_WIDTH; 
    hdi.cxy = nWidth; 
    hdi.pszText = lpsz; 
    hdi.cchTextMax = sizeof(hdi.pszText)/sizeof(hdi.pszText[0]); 
    hdi.fmt = HDF_LEFT | HDF_STRING; 
 
    index = SendMessage(hwndHeader, HDM_INSERTITEM, 
        (WPARAM) iInsertAfter, (LPARAM) &hdi); 
 
    return index; 
}
```



## <a name="related-topics"></a><span data-ttu-id="ade98-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ade98-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ade98-120">À propos des contrôles Header</span><span class="sxs-lookup"><span data-stu-id="ade98-120">About Header Controls</span></span>](header-controls.md)
</dt> <dt>

[<span data-ttu-id="ade98-121">Référence de contrôle header</span><span class="sxs-lookup"><span data-stu-id="ade98-121">Header Control Reference</span></span>](bumper-header-control-header-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ade98-122">Utilisation des contrôles Header</span><span class="sxs-lookup"><span data-stu-id="ade98-122">Using Header Controls</span></span>](using-header-controls.md)
</dt> </dl>

 

 




