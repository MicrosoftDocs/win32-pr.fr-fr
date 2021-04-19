---
title: IAgentPropertySheet SetVisible
description: IAgentPropertySheet SetVisible
ms.assetid: 53520a64-e99f-4d03-aa36-bcbb4547990c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26615f0e5282b399837726c980650abcf12fdb47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511430"
---
# <a name="iagentpropertysheetsetvisible"></a><span data-ttu-id="1561c-103">IAgentPropertySheet :: SetVisible</span><span class="sxs-lookup"><span data-stu-id="1561c-103">IAgentPropertySheet::SetVisible</span></span>

<span data-ttu-id="1561c-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1561c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // property sheet Visible setting 
);
```

<span data-ttu-id="1561c-105">Définit la propriété [**visible**](visible-property.md) pour la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1561c-105">Sets the [**Visible**](visible-property.md) property for the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="1561c-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="1561c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1561c-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="1561c-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="1561c-108">Paramètre de propriété visible.</span><span class="sxs-lookup"><span data-stu-id="1561c-108">Visible property setting.</span></span> <span data-ttu-id="1561c-109">La valeur **true** affiche la feuille de propriétés ; la valeur **false** le masque.</span><span class="sxs-lookup"><span data-stu-id="1561c-109">A value of **True** displays the property sheet; a value of **False** hides it.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="1561c-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1561c-110">See Also</span></span>

[<span data-ttu-id="1561c-111">**IAgentPropertySheet::GetVisible**</span><span class="sxs-lookup"><span data-stu-id="1561c-111">**IAgentPropertySheet::GetVisible**</span></span>](iagentpropertysheet--getvisible.md)


 

 




