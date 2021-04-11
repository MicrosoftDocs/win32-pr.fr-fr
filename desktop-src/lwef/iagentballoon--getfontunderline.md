---
title: IAgentBalloon GetFontUnderline
description: IAgentBalloon GetFontUnderline
ms.assetid: 19886e94-8095-4650-bd88-34ea9d96ddaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5acf35453209679dc96c85b3017fbe76b19d53b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029797"
---
# <a name="iagentballoongetfontunderline"></a><span data-ttu-id="21ff7-103">IAgentBalloon::GetFontUnderline</span><span class="sxs-lookup"><span data-stu-id="21ff7-103">IAgentBalloon::GetFontUnderline</span></span>

<span data-ttu-id="21ff7-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="21ff7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontUnderline(
   long * pbFontUnderline  // address of variable for underline setting
);                         // for font displayed in word balloon 
```

<span data-ttu-id="21ff7-105">Indique si la police utilisée dans une bulle de mot a le style de soulignement défini.</span><span class="sxs-lookup"><span data-stu-id="21ff7-105">Indicates whether the font used in a word balloon has the underline style set.</span></span>

-   <span data-ttu-id="21ff7-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="21ff7-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="21ff7-107"><span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbFontUnderline*</span><span class="sxs-lookup"><span data-stu-id="21ff7-107"><span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbFontUnderline*</span></span>
</dt> <dd>

<span data-ttu-id="21ff7-108">Adresse d’une valeur qui reçoit **true** si le style de soulignement de police est défini et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="21ff7-108">The address of a value that receives **True** if the font underline style is set and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="21ff7-109">Le style de police utilisé dans une bulle de mot de caractères est défini dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="21ff7-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="21ff7-110">Elle ne peut pas être modifiée par une application.</span><span class="sxs-lookup"><span data-stu-id="21ff7-110">It cannot be changed by an application.</span></span> <span data-ttu-id="21ff7-111">Toutefois, l’utilisateur peut remplacer les paramètres de police pour tous les caractères à l’aide de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="21ff7-111">However, the user can override the font settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




