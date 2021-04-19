---
title: IAgentBalloon GetFontItalic
description: IAgentBalloon GetFontItalic
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c1a0e1e649e325e84d4a78eee087e102e8d1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106536061"
---
# <a name="iagentballoongetfontitalic"></a><span data-ttu-id="8b4b7-103">IAgentBalloon::GetFontItalic</span><span class="sxs-lookup"><span data-stu-id="8b4b7-103">IAgentBalloon::GetFontItalic</span></span>

<span data-ttu-id="8b4b7-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8b4b7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

<span data-ttu-id="8b4b7-105">Indique si la police utilisée dans une bulle de mot est en italique.</span><span class="sxs-lookup"><span data-stu-id="8b4b7-105">Indicates whether the font used in a word balloon is italic.</span></span>

-   <span data-ttu-id="8b4b7-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8b4b7-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8b4b7-107"><span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*</span><span class="sxs-lookup"><span data-stu-id="8b4b7-107"><span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*</span></span>
</dt> <dd>

<span data-ttu-id="8b4b7-108">Adresse d’une valeur qui reçoit la valeur **true** si la police est en italique et **false** si elle n’est pas en italique.</span><span class="sxs-lookup"><span data-stu-id="8b4b7-108">The address of a value that receives **True** if the font is italic and **False** if not italic.</span></span>

</dd> </dl>

<span data-ttu-id="8b4b7-109">Le style de police utilisé dans la bulle de texte d’un caractère est défini dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="8b4b7-109">The font style used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="8b4b7-110">Elle ne peut pas être modifiée par une application.</span><span class="sxs-lookup"><span data-stu-id="8b4b7-110">It cannot be changed by an application.</span></span> <span data-ttu-id="8b4b7-111">Toutefois, l’utilisateur peut remplacer les paramètres de police pour tous les caractères par le biais de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b4b7-111">However, the user can override the font settings for all characters through the Microsoft Agent property sheet.</span></span>

 

 




