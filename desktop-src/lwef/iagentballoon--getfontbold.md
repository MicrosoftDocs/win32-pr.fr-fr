---
title: IAgentBalloon GetFontBold
description: IAgentBalloon GetFontBold
ms.assetid: 5a55f771-d68e-4f66-8001-47c141661b06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858f6f42964db1bdd7ae548d308c6f6668b05631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196946"
---
# <a name="iagentballoongetfontbold"></a><span data-ttu-id="049ed-103">IAgentBalloon::GetFontBold</span><span class="sxs-lookup"><span data-stu-id="049ed-103">IAgentBalloon::GetFontBold</span></span>

<span data-ttu-id="049ed-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="049ed-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontBold(
   long * pbFontBold  // address of variable for bold setting for
);                    // font displayed in word balloon 
```

<span data-ttu-id="049ed-105">Indique si la police utilisée dans une bulle de mot est en gras.</span><span class="sxs-lookup"><span data-stu-id="049ed-105">Indicates whether the font used in a word balloon is bold.</span></span>

-   <span data-ttu-id="049ed-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="049ed-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="049ed-107"><span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*</span><span class="sxs-lookup"><span data-stu-id="049ed-107"><span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*</span></span>
</dt> <dd>

<span data-ttu-id="049ed-108">Adresse d’une valeur qui reçoit la valeur **true** si la police est en gras et **false** si elle n’est pas en gras.</span><span class="sxs-lookup"><span data-stu-id="049ed-108">The address of a value that receives **True** if the font is bold and **False** if not bold.</span></span>

</dd> </dl>

<span data-ttu-id="049ed-109">Le style de police utilisé dans une bulle de mot de caractères est défini dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="049ed-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="049ed-110">Elle ne peut pas être modifiée par une application.</span><span class="sxs-lookup"><span data-stu-id="049ed-110">It cannot be changed by an application.</span></span> <span data-ttu-id="049ed-111">Toutefois, l’utilisateur peut remplacer les paramètres de police pour tous les caractères par le biais de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="049ed-111">However, the user can override the font settings for all characters through the Microsoft Agent property sheet.</span></span>

 

 




