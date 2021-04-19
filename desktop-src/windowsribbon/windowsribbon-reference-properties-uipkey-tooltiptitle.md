---
title: UI_PKEY_TooltipTitle
description: Identifie la propriété TooltipTitle de l’interface utilisateur \_ \_ .
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e62fe9ebdb6418f5790e0073e32e81d7f7aba75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513684"
---
# <a name="ui_pkey_tooltiptitle"></a><span data-ttu-id="680bc-103">IU \_ \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="680bc-103">UI\_PKEY\_TooltipTitle</span></span>

<span data-ttu-id="680bc-104">Identifie la propriété TooltipTitle de l’interface utilisateur \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="680bc-104">Identifies the UI\_PKEY\_TooltipTitle property.</span></span>

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="680bc-105">Notes</span><span class="sxs-lookup"><span data-stu-id="680bc-105">Remarks</span></span>

<span data-ttu-id="680bc-106">L’interface utilisateur \_ \_ TooltipTitle est utilisée par une application pour interroger l’info-bulle des onglets, des groupes, des boutons, des éléments de la Galerie et d’autres contrôles du ruban.</span><span class="sxs-lookup"><span data-stu-id="680bc-106">UI\_PKEY\_TooltipTitle is used by an application to query the tooltip of tabs, groups, buttons, gallery items, and other Ribbon controls.</span></span>

<span data-ttu-id="680bc-107">La valeur de la propriété est une chaîne limitée à toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="680bc-107">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="680bc-108">Utilisez la référence de caractère XML UCS (Universal Character Set) `&#xA;` pour spécifier un saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="680bc-108">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="680bc-109">L’alignement à droite n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="680bc-109">Right alignment is not supported.</span></span>

<span data-ttu-id="680bc-110">La longueur maximale de l’interface utilisateur \_ \_ TooltipTitle est illimitée.</span><span class="sxs-lookup"><span data-stu-id="680bc-110">The maximum length of UI\_PKEY\_TooltipTitle is unbounded.</span></span>

<span data-ttu-id="680bc-111">Pour afficher une esperluette dans une info-bulle, échappez la désignation de caractères spéciaux par une double esperluette ( `&&` ), comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="680bc-111">To display an ampersand in a tooltip, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a><span data-ttu-id="680bc-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="680bc-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="680bc-113">Propriétés de la ressource</span><span class="sxs-lookup"><span data-stu-id="680bc-113">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="680bc-114">**Commande. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="680bc-114">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[<span data-ttu-id="680bc-115">IU \_ \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="680bc-115">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




