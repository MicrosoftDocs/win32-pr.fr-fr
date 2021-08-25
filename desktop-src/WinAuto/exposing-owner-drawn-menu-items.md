---
title: Exposer des éléments de menu Owner-Drawn
description: Exposer des éléments de menu Owner-Drawn
ms.assetid: 93b51cbb-b7b4-4a38-ba69-d6345a269944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84a2630b5227937d4a1c9621360d9fb028676bba03516970f93e314b382035b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860499"
---
# <a name="exposing-owner-drawn-menu-items"></a>Exposer des éléments de menu Owner-Drawn

Les développeurs d’applications peuvent utiliser la structure [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) pour exposer les noms des éléments de menu owner-drawn. En associant cette structure aux données de l’élément de menu owner-drawn, vous n’avez pas besoin d’exposer les éléments de menu avec [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).

Lorsque vous créez un menu owner-drawn, définissez une classe ou une structure pour les données d’élément de menu owner-drawn et créez des instances de cette classe pour chaque élément de menu. Passer un pointeur vers les données de l’élément lors de l’ajout d’éléments au menu.

Pour exposer les noms des éléments de menu, la structure [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) doit être le premier membre de la structure qui définit les données d’élément spécifiques à l’application, comme indiqué dans l’exemple suivant :


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



La structure [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) ne peut pas être membre d’une classe qui contient des fonctions virtuelles. Lorsque le code est compilé, le premier membre de la classe est toujours un pointeur généré par le compilateur vers une table des fonctions virtuelles. Pour contourner ce problème, créez une structure de données d’élément qui contient **MSAAMENUINFO** en tant que premier membre. Le deuxième membre est un pointeur vers une instance de la classe qui définit les données owner-drawn. L’exemple suivant illustre cette technique.


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



Lorsque vous ajoutez des éléments au menu, transmettez un pointeur vers une instance de la structure qui contient [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) pour exposer les noms des éléments de menu.

 

 




