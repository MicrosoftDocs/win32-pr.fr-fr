---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb1fe6cdf6f667011eb048625349f6905913a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380013"
---
# <a name="iagentpropertysheetgetpage"></a><span data-ttu-id="97e8b-103">IAgentPropertySheet::GetPage</span><span class="sxs-lookup"><span data-stu-id="97e8b-103">IAgentPropertySheet::GetPage</span></span>

<span data-ttu-id="97e8b-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="97e8b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

<span data-ttu-id="97e8b-105">Récupère la page active de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="97e8b-105">Retrieves the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="97e8b-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="97e8b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="97e8b-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span><span class="sxs-lookup"><span data-stu-id="97e8b-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span></span>
</dt> <dd>

<span data-ttu-id="97e8b-108">Adresse d’une variable qui reçoit la page actuelle de la feuille de propriétés (dernière page affichée si la fenêtre n’est pas ouverte).</span><span class="sxs-lookup"><span data-stu-id="97e8b-108">Address of a variable that receives the current page of the property sheet (last viewed page if the window is not open).</span></span> <span data-ttu-id="97e8b-109">Le paramètre peut avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="97e8b-109">The parameter can be one of the following:</span></span>



|                 |                        |
|-----------------|------------------------|
| <span data-ttu-id="97e8b-110">**Vocale**</span><span class="sxs-lookup"><span data-stu-id="97e8b-110">**"Speech"**</span></span>    | <span data-ttu-id="97e8b-111">Page d’entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="97e8b-111">The Speech Input page.</span></span> |
| <span data-ttu-id="97e8b-112">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="97e8b-112">**"Output"**</span></span>    | <span data-ttu-id="97e8b-113">Page de sortie.</span><span class="sxs-lookup"><span data-stu-id="97e8b-113">The Output page.</span></span>       |
| <span data-ttu-id="97e8b-114">**Intellectuelle**</span><span class="sxs-lookup"><span data-stu-id="97e8b-114">**"Copyright"**</span></span> | <span data-ttu-id="97e8b-115">Page de copyright.</span><span class="sxs-lookup"><span data-stu-id="97e8b-115">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="97e8b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97e8b-116">See Also</span></span>

[<span data-ttu-id="97e8b-117">**IAgentPropertySheet :: SetPage**</span><span class="sxs-lookup"><span data-stu-id="97e8b-117">**IAgentPropertySheet::SetPage**</span></span>](iagentpropertysheet--setpage.md)


 

 




