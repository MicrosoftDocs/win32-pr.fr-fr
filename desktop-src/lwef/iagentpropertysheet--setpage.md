---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b84f9b9d5f74170644488cc2049376ecf409997
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120744"
---
# <a name="iagentpropertysheetsetpage"></a><span data-ttu-id="5a441-103">IAgentPropertySheet :: SetPage</span><span class="sxs-lookup"><span data-stu-id="5a441-103">IAgentPropertySheet::SetPage</span></span>

<span data-ttu-id="5a441-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5a441-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

<span data-ttu-id="5a441-105">Définit la page active de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5a441-105">Sets the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="5a441-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="5a441-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5a441-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span><span class="sxs-lookup"><span data-stu-id="5a441-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span></span>
</dt> <dd>

<span data-ttu-id="5a441-108">BSTR qui définit la page actuelle de la propriété.</span><span class="sxs-lookup"><span data-stu-id="5a441-108">A BSTR that sets the current page of the property.</span></span> <span data-ttu-id="5a441-109">Le paramètre peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5a441-109">The parameter can be one of the following.</span></span>



|                 | <span data-ttu-id="5a441-110">Description</span><span class="sxs-lookup"><span data-stu-id="5a441-110">Description</span></span>            |
|-----------------|------------------------|
| <span data-ttu-id="5a441-111">**Vocale**</span><span class="sxs-lookup"><span data-stu-id="5a441-111">**"Speech"**</span></span>    | <span data-ttu-id="5a441-112">Page d’entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="5a441-112">The Speech Input page.</span></span> |
| <span data-ttu-id="5a441-113">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="5a441-113">**"Output"**</span></span>    | <span data-ttu-id="5a441-114">Page de sortie.</span><span class="sxs-lookup"><span data-stu-id="5a441-114">The Output page.</span></span>       |
| <span data-ttu-id="5a441-115">**Intellectuelle**</span><span class="sxs-lookup"><span data-stu-id="5a441-115">**"Copyright"**</span></span> | <span data-ttu-id="5a441-116">Page de copyright.</span><span class="sxs-lookup"><span data-stu-id="5a441-116">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="5a441-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a441-117">See Also</span></span>

[<span data-ttu-id="5a441-118">**IAgentPropertySheet::GetPage**</span><span class="sxs-lookup"><span data-stu-id="5a441-118">**IAgentPropertySheet::GetPage**</span></span>](iagentpropertysheet--getpage.md)


 

 




