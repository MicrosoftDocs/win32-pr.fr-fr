---
title: IAgentCharacter GetVisible
description: IAgentCharacter GetVisible
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0593b9b3a193b9d5910888b81b4ecba90469b1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101485"
---
# <a name="iagentcharactergetvisible"></a><span data-ttu-id="2352d-103">IAgentCharacter::GetVisible</span><span class="sxs-lookup"><span data-stu-id="2352d-103">IAgentCharacter::GetVisible</span></span>

<span data-ttu-id="2352d-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2352d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for character Visible setting
);
```

<span data-ttu-id="2352d-105">Détermine si le cadre d’animation du caractère est actuellement visible.</span><span class="sxs-lookup"><span data-stu-id="2352d-105">Determines whether the character's animation frame is currently visible.</span></span>

-   <span data-ttu-id="2352d-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2352d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2352d-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="2352d-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="2352d-108">Adresse d’une variable qui reçoit la **valeur true** si le frame du caractère est visible et **false** s’il est masqué.</span><span class="sxs-lookup"><span data-stu-id="2352d-108">Address of a variable that receives **True** if the character's frame is visible and **False** if hidden.</span></span>

</dd> </dl>

<span data-ttu-id="2352d-109">Vous pouvez utiliser cette méthode pour déterminer si le frame du caractère est actuellement visible.</span><span class="sxs-lookup"><span data-stu-id="2352d-109">You can use this method to determine whether the character's frame is currently visible.</span></span> <span data-ttu-id="2352d-110">Pour rendre un caractère visible, utilisez la méthode [**Show**](/windows/desktop/lwef/iagentcharacter--show) .</span><span class="sxs-lookup"><span data-stu-id="2352d-110">To make a character visible, use the [**Show**](/windows/desktop/lwef/iagentcharacter--show) method.</span></span> <span data-ttu-id="2352d-111">Pour masquer un caractère, utilisez la méthode [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) .</span><span class="sxs-lookup"><span data-stu-id="2352d-111">To hide a character, use the [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) method.</span></span>

 

 