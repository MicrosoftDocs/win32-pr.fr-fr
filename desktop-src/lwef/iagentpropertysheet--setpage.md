---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86bbacfed445c5266a299495df5c07fd6166d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673769"
---
# <a name="iagentpropertysheetsetpage"></a><span data-ttu-id="851fd-103">IAgentPropertySheet :: SetPage</span><span class="sxs-lookup"><span data-stu-id="851fd-103">IAgentPropertySheet::SetPage</span></span>

<span data-ttu-id="851fd-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="851fd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

<span data-ttu-id="851fd-105">Définit la page active de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="851fd-105">Sets the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="851fd-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="851fd-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="851fd-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span><span class="sxs-lookup"><span data-stu-id="851fd-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span></span>
</dt> <dd>

<span data-ttu-id="851fd-108">BSTR qui définit la page actuelle de la propriété.</span><span class="sxs-lookup"><span data-stu-id="851fd-108">A BSTR that sets the current page of the property.</span></span> <span data-ttu-id="851fd-109">Le paramètre peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="851fd-109">The parameter can be one of the following.</span></span>



|                 |                        |
|-----------------|------------------------|
| <span data-ttu-id="851fd-110">**Vocale**</span><span class="sxs-lookup"><span data-stu-id="851fd-110">**"Speech"**</span></span>    | <span data-ttu-id="851fd-111">Page d’entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="851fd-111">The Speech Input page.</span></span> |
| <span data-ttu-id="851fd-112">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="851fd-112">**"Output"**</span></span>    | <span data-ttu-id="851fd-113">Page de sortie.</span><span class="sxs-lookup"><span data-stu-id="851fd-113">The Output page.</span></span>       |
| <span data-ttu-id="851fd-114">**Intellectuelle**</span><span class="sxs-lookup"><span data-stu-id="851fd-114">**"Copyright"**</span></span> | <span data-ttu-id="851fd-115">Page de copyright.</span><span class="sxs-lookup"><span data-stu-id="851fd-115">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="851fd-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="851fd-116">See Also</span></span>

[<span data-ttu-id="851fd-117">**IAgentPropertySheet::GetPage**</span><span class="sxs-lookup"><span data-stu-id="851fd-117">**IAgentPropertySheet::GetPage**</span></span>](iagentpropertysheet--getpage.md)


 

 




