---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c08e564b5170d62cf5757536b9e11baec4883c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119864"
---
# <a name="iagentpropertysheetgetpage"></a><span data-ttu-id="8b98d-103">IAgentPropertySheet::GetPage</span><span class="sxs-lookup"><span data-stu-id="8b98d-103">IAgentPropertySheet::GetPage</span></span>

<span data-ttu-id="8b98d-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8b98d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

<span data-ttu-id="8b98d-105">Récupère la page active de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b98d-105">Retrieves the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="8b98d-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8b98d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8b98d-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span><span class="sxs-lookup"><span data-stu-id="8b98d-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span></span>
</dt> <dd>

<span data-ttu-id="8b98d-108">Adresse d’une variable qui reçoit la page actuelle de la feuille de propriétés (dernière page affichée si la fenêtre n’est pas ouverte).</span><span class="sxs-lookup"><span data-stu-id="8b98d-108">Address of a variable that receives the current page of the property sheet (last viewed page if the window is not open).</span></span> <span data-ttu-id="8b98d-109">Le paramètre peut avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8b98d-109">The parameter can be one of the following:</span></span>



|                 | <span data-ttu-id="8b98d-110">Description</span><span class="sxs-lookup"><span data-stu-id="8b98d-110">Description</span></span>            |
|-----------------|------------------------|
| <span data-ttu-id="8b98d-111">**Vocale**</span><span class="sxs-lookup"><span data-stu-id="8b98d-111">**"Speech"**</span></span>    | <span data-ttu-id="8b98d-112">Page d’entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="8b98d-112">The Speech Input page.</span></span> |
| <span data-ttu-id="8b98d-113">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="8b98d-113">**"Output"**</span></span>    | <span data-ttu-id="8b98d-114">Page de sortie.</span><span class="sxs-lookup"><span data-stu-id="8b98d-114">The Output page.</span></span>       |
| <span data-ttu-id="8b98d-115">**Intellectuelle**</span><span class="sxs-lookup"><span data-stu-id="8b98d-115">**"Copyright"**</span></span> | <span data-ttu-id="8b98d-116">Page de copyright.</span><span class="sxs-lookup"><span data-stu-id="8b98d-116">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="8b98d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b98d-117">See Also</span></span>

[<span data-ttu-id="8b98d-118">**IAgentPropertySheet :: SetPage**</span><span class="sxs-lookup"><span data-stu-id="8b98d-118">**IAgentPropertySheet::SetPage**</span></span>](iagentpropertysheet--setpage.md)


 

 




