---
title: IAgentBalloon GetNumLines
description: IAgentBalloon GetNumLines
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d66c18d75af77a2559efc86f775710fb32e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380349"
---
# <a name="iagentballoongetnumlines"></a><span data-ttu-id="c5a26-103">IAgentBalloon::GetNumLines</span><span class="sxs-lookup"><span data-stu-id="c5a26-103">IAgentBalloon::GetNumLines</span></span>

<span data-ttu-id="c5a26-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c5a26-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetNumLines(
   long * pcLines  // address of variable for number of lines 
);                  // displayed in word balloon
```

<span data-ttu-id="c5a26-105">Récupère la valeur du nombre de lignes affichées dans une bulle de texte.</span><span class="sxs-lookup"><span data-stu-id="c5a26-105">Retrieves the value of the number of lines displayed in a word balloon.</span></span>

-   <span data-ttu-id="c5a26-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="c5a26-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c5a26-107"><span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*</span><span class="sxs-lookup"><span data-stu-id="c5a26-107"><span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*</span></span>
</dt> <dd>

<span data-ttu-id="c5a26-108">Adresse d’une variable qui reçoit le nombre de lignes affichées.</span><span class="sxs-lookup"><span data-stu-id="c5a26-108">The address of a variable that receives the number of lines displayed.</span></span>

</dd> </dl>

<span data-ttu-id="c5a26-109">Le serveur Microsoft Agent fait défiler automatiquement les lignes affichées pour la sortie parlée dans la bulle de texte.</span><span class="sxs-lookup"><span data-stu-id="c5a26-109">The Microsoft Agent server automatically scrolls the lines displayed for spoken output in the word balloon.</span></span> <span data-ttu-id="c5a26-110">Le nombre de lignes pour une bulle de mot de caractères est défini dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="c5a26-110">The number of lines for a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="c5a26-111">Elle ne peut pas être modifiée par une application.</span><span class="sxs-lookup"><span data-stu-id="c5a26-111">It cannot be changed by an application.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5a26-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5a26-112">See Also</span></span>

[<span data-ttu-id="c5a26-113">**IAgentBalloon::GetNumCharsPerLine**</span><span class="sxs-lookup"><span data-stu-id="c5a26-113">**IAgentBalloon::GetNumCharsPerLine**</span></span>](iagentballoon--getnumcharsperline.md)


 

 




