---
title: IAgentBalloon GetBackColor
description: IAgentBalloon GetBackColor
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce886c9929892c89b56f162f784dc27a472209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029408"
---
# <a name="iagentballoongetbackcolor"></a><span data-ttu-id="17511-103">IAgentBalloon::GetBackColor</span><span class="sxs-lookup"><span data-stu-id="17511-103">IAgentBalloon::GetBackColor</span></span>

<span data-ttu-id="17511-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="17511-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

<span data-ttu-id="17511-105">Récupère la valeur de la couleur d’arrière-plan affichée dans une bulle de mot.</span><span class="sxs-lookup"><span data-stu-id="17511-105">Retrieves the value for the background color displayed in a word balloon.</span></span>

-   <span data-ttu-id="17511-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="17511-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="17511-107"><span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*</span><span class="sxs-lookup"><span data-stu-id="17511-107"><span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*</span></span>
</dt> <dd>

<span data-ttu-id="17511-108">Adresse d’une variable qui reçoit le paramètre de couleur de l’arrière-plan de l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="17511-108">The address of a variable that receives the color setting for the balloon background.</span></span>

</dd> </dl>

<span data-ttu-id="17511-109">La couleur d’arrière-plan utilisée dans une bulle de mot de caractères est définie dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="17511-109">The background color used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="17511-110">Elle ne peut pas être modifiée par une application.</span><span class="sxs-lookup"><span data-stu-id="17511-110">It cannot be changed by an application.</span></span> <span data-ttu-id="17511-111">Toutefois, l’utilisateur peut modifier la couleur d’arrière-plan des bulles de mot pour tous les caractères par le biais de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="17511-111">However, the user can change the background color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="17511-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17511-112">See Also</span></span>

[<span data-ttu-id="17511-113">**IAgentBalloon::GetForeColor**</span><span class="sxs-lookup"><span data-stu-id="17511-113">**IAgentBalloon::GetForeColor**</span></span>](iagentballoon--getforecolor.md)


 

 




