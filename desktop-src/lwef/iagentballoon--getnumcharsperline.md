---
title: IAgentBalloon GetNumCharsPerLine
description: IAgentBalloon GetNumCharsPerLine
ms.assetid: ae0c7fff-8c58-465e-9b4f-3260f7574b57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887167584c46f075bc0696c46b2dde52eb27f8d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029796"
---
# <a name="iagentballoongetnumcharsperline"></a><span data-ttu-id="37181-103">IAgentBalloon::GetNumCharsPerLine</span><span class="sxs-lookup"><span data-stu-id="37181-103">IAgentBalloon::GetNumCharsPerLine</span></span>

<span data-ttu-id="37181-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="37181-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetNumCharsPerLine(
   long * plCharsPerLine  // address of variable for characters per line
);                        // displayed in word balloon
```

<span data-ttu-id="37181-105">Récupère la valeur pour le nombre moyen de caractères par ligne affichée dans une bulle de texte.</span><span class="sxs-lookup"><span data-stu-id="37181-105">Retrieves the value for the average number of characters per line displayed in a word balloon.</span></span>

-   <span data-ttu-id="37181-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="37181-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="37181-107"><span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*</span><span class="sxs-lookup"><span data-stu-id="37181-107"><span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*</span></span>
</dt> <dd>

<span data-ttu-id="37181-108">Adresse d’une variable qui reçoit le nombre de caractères par ligne.</span><span class="sxs-lookup"><span data-stu-id="37181-108">The address of a variable that receives the number of characters per line.</span></span>

</dd> </dl>

<span data-ttu-id="37181-109">Le serveur Microsoft Agent fait défiler automatiquement les lignes affichées pour la sortie parlée dans la bulle de texte.</span><span class="sxs-lookup"><span data-stu-id="37181-109">The Microsoft Agent server automatically scrolls the lines displayed for spoken output in the word balloon.</span></span> <span data-ttu-id="37181-110">Le nombre moyen de caractères par ligne pour la bulle de texte d’un caractère est défini dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="37181-110">The average number of characters per line for a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="37181-111">Elle ne peut pas être modifiée par une application.</span><span class="sxs-lookup"><span data-stu-id="37181-111">It cannot be changed by an application.</span></span>

## <a name="see-also"></a><span data-ttu-id="37181-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37181-112">See Also</span></span>

[<span data-ttu-id="37181-113">**IAgentBalloon::GetNumLines**</span><span class="sxs-lookup"><span data-stu-id="37181-113">**IAgentBalloon::GetNumLines**</span></span>](iagentballoon--getnumlines.md)


 

 




