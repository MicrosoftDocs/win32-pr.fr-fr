---
title: IAgentBalloon GetFontName
description: IAgentBalloon GetFontName
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f29ad981fb4b10249b17e55c92fb286552eedc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380352"
---
# <a name="iagentballoongetfontname"></a><span data-ttu-id="285a9-103">IAgentBalloon::GetFontName</span><span class="sxs-lookup"><span data-stu-id="285a9-103">IAgentBalloon::GetFontName</span></span>

<span data-ttu-id="285a9-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="285a9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

<span data-ttu-id="285a9-105">Récupère la valeur de la police affichée dans une bulle de mot.</span><span class="sxs-lookup"><span data-stu-id="285a9-105">Retrieves the value for the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="285a9-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="285a9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="285a9-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span><span class="sxs-lookup"><span data-stu-id="285a9-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="285a9-108">Adresse d’un BSTR qui reçoit le nom de police affiché dans une bulle de mot.</span><span class="sxs-lookup"><span data-stu-id="285a9-108">The address of a BSTR that receives the font name displayed in a word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="285a9-109">La police par défaut utilisée dans une bulle de mot de caractères est définie dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="285a9-109">The default font used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="285a9-110">Vous pouvez le modifier avec [**IAgentBalloon :: SetFontName**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**).</span><span class="sxs-lookup"><span data-stu-id="285a9-110">You can change it with [**IAgentBalloon::SetFontName**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**).</span></span> <span data-ttu-id="285a9-111">L’utilisateur peut remplacer le paramètre de police pour tous les caractères à l’aide de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="285a9-111">The user can override the font setting for all characters using the Microsoft Agent property sheet.</span></span>

 

 




