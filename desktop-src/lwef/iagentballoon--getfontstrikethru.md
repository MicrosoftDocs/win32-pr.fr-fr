---
title: IAgentBalloon GetFontStrikethru
description: IAgentBalloon GetFontStrikethru
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2001ec0125949144843d500f125b3502e94723db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380350"
---
# <a name="iagentballoongetfontstrikethru"></a><span data-ttu-id="a0764-103">IAgentBalloon::GetFontStrikethru</span><span class="sxs-lookup"><span data-stu-id="a0764-103">IAgentBalloon::GetFontStrikethru</span></span>

<span data-ttu-id="a0764-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a0764-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontStrikethru(
   long * pbFontStrikethru  // address of variable for strikethrough setting 
);                          // for font displayed in word balloon 
```

<span data-ttu-id="a0764-105">Indique si la police utilisée dans une bulle de mot a le style barré défini.</span><span class="sxs-lookup"><span data-stu-id="a0764-105">Indicates whether the font used in a word balloon has the strikethrough style set.</span></span>

-   <span data-ttu-id="a0764-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a0764-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a0764-107"><span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*</span><span class="sxs-lookup"><span data-stu-id="a0764-107"><span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*</span></span>
</dt> <dd>

<span data-ttu-id="a0764-108">Adresse d’une valeur qui reçoit la valeur **true** si le style de police barré est défini et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a0764-108">The address of a value that receives **True** if the font strikethrough style is set and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="a0764-109">Le style de police utilisé dans une bulle de mot de caractères est défini dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a0764-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="a0764-110">Elle ne peut pas être modifiée par une application.</span><span class="sxs-lookup"><span data-stu-id="a0764-110">It cannot be changed by an application.</span></span> <span data-ttu-id="a0764-111">Toutefois, l’utilisateur peut remplacer les paramètres de police pour tous les caractères à l’aide de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a0764-111">However, the user can override the font settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




