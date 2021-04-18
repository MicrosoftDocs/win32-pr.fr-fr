---
title: Exposer des éléments de menu Owner-Drawn
description: Exposer des éléments de menu Owner-Drawn
ms.assetid: 93b51cbb-b7b4-4a38-ba69-d6345a269944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e79668115cedd5fb6b8c20b0d4df361d6d1d800
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507335"
---
# <a name="exposing-owner-drawn-menu-items"></a><span data-ttu-id="ba6b7-103">Exposer des éléments de menu Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="ba6b7-103">Exposing Owner-Drawn Menu Items</span></span>

<span data-ttu-id="ba6b7-104">Les développeurs d’applications peuvent utiliser la structure [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) pour exposer les noms des éléments de menu owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="ba6b7-104">Application developers can use the [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure to expose the names of owner-drawn menu items.</span></span> <span data-ttu-id="ba6b7-105">En associant cette structure aux données de l’élément de menu owner-drawn, vous n’avez pas besoin d’exposer les éléments de menu avec [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="ba6b7-105">By associating this structure with the owner-drawn menu item data, you do not need to expose the menu items with [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span>

<span data-ttu-id="ba6b7-106">Lorsque vous créez un menu owner-drawn, définissez une classe ou une structure pour les données d’élément de menu owner-drawn et créez des instances de cette classe pour chaque élément de menu.</span><span class="sxs-lookup"><span data-stu-id="ba6b7-106">When creating an owner-drawn menu, define a class or structure for the owner-drawn menu item data and create instances of this class for each menu item.</span></span> <span data-ttu-id="ba6b7-107">Passer un pointeur vers les données de l’élément lors de l’ajout d’éléments au menu.</span><span class="sxs-lookup"><span data-stu-id="ba6b7-107">Pass in a pointer to the item data when adding items to the menu.</span></span>

<span data-ttu-id="ba6b7-108">Pour exposer les noms des éléments de menu, la structure [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) doit être le premier membre de la structure qui définit les données d’élément spécifiques à l’application, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="ba6b7-108">To expose the names of the menu items, the [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure must be the first member of the structure that defines the application-specific item data, as shown in the following example:</span></span>


```C++
// Application-specific owner-drawn menu info struct. Owner-drawn data 
// is a pointer to one of these.
struct MenuEntry
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //   separator item 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //   for separator 
};
```



<span data-ttu-id="ba6b7-109">La structure [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) ne peut pas être membre d’une classe qui contient des fonctions virtuelles.</span><span class="sxs-lookup"><span data-stu-id="ba6b7-109">The [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure cannot be a member in a class that contains virtual functions.</span></span> <span data-ttu-id="ba6b7-110">Lorsque le code est compilé, le premier membre de la classe est toujours un pointeur généré par le compilateur vers une table des fonctions virtuelles.</span><span class="sxs-lookup"><span data-stu-id="ba6b7-110">When the code is compiled, the first member of the class is always a compiler-generated pointer to a table of the virtual functions.</span></span> <span data-ttu-id="ba6b7-111">Pour contourner ce problème, créez une structure de données d’élément qui contient **MSAAMENUINFO** en tant que premier membre.</span><span class="sxs-lookup"><span data-stu-id="ba6b7-111">To work around this problem, create an item data structure that contains **MSAAMENUINFO** as the first member.</span></span> <span data-ttu-id="ba6b7-112">Le deuxième membre est un pointeur vers une instance de la classe qui définit les données owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="ba6b7-112">The second member is a pointer to an instance of the class that defines the owner-drawn data.</span></span> <span data-ttu-id="ba6b7-113">L’exemple suivant illustre cette technique.</span><span class="sxs-lookup"><span data-stu-id="ba6b7-113">The following example demonstrates this technique.</span></span>


```C++
// Application-defined class that contains the owner-drawn data and 
//  virtual functions that operate on that data.  
class MenuEntry
{
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //  separator item. 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //  separator item 
    virtual void m_AnimateIcon();  
    virtual void m_ChangeIconColor();
}

// Application-defined struct that contains MSAAMENUINFO as first 
//  member. Second member points to owner-drawn data. 
struct MenuInfo
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    MenuEntry *pMenuData;      // Points to the owner-drawn data 
}
```



<span data-ttu-id="ba6b7-114">Lorsque vous ajoutez des éléments au menu, transmettez un pointeur vers une instance de la structure qui contient [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) pour exposer les noms des éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="ba6b7-114">When adding items to the menu, pass a pointer to an instance of the structure that contains [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) to expose the names of the menu items.</span></span>

 

 




