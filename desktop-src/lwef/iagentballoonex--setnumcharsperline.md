---
title: IAgentBalloonEx SetNumCharsPerLine
description: IAgentBalloonEx SetNumCharsPerLine
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a44abe14de6bb1cef631a51b4516d083657016
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310965"
---
# <a name="iagentballoonexsetnumcharsperline"></a><span data-ttu-id="ab4a3-103">IAgentBalloonEx::SetNumCharsPerLine</span><span class="sxs-lookup"><span data-stu-id="ab4a3-103">IAgentBalloonEx::SetNumCharsPerLine</span></span>

<span data-ttu-id="ab4a3-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ab4a3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

<span data-ttu-id="ab4a3-105">Définit le nombre de caractères par ligne qui peuvent être affichés dans la bulle de texte du caractère.</span><span class="sxs-lookup"><span data-stu-id="ab4a3-105">Sets the number of characters per line that can be displayed in the character's word balloon.</span></span>

-   <span data-ttu-id="ab4a3-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="ab4a3-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="ab4a3-107">Retourne E \_ INVALIDARG si le paramètre est inférieur à huit.</span><span class="sxs-lookup"><span data-stu-id="ab4a3-107">Returns E\_INVALIDARG if the parameter is less than eight.</span></span>

<dl> <dt>

<span data-ttu-id="ab4a3-108"><span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*</span><span class="sxs-lookup"><span data-stu-id="ab4a3-108"><span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*</span></span>
</dt> <dd>

<span data-ttu-id="ab4a3-109">Nombre de lignes à afficher dans la bulle de mot.</span><span class="sxs-lookup"><span data-stu-id="ab4a3-109">Number of lines to display in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="ab4a3-110">La valeur minimale est 8 et la valeur maximale est 255.</span><span class="sxs-lookup"><span data-stu-id="ab4a3-110">The minimum setting is 8 and the maximum is 255.</span></span> <span data-ttu-id="ab4a3-111">Si le texte spécifié dans la méthode [**Speak**](speak-method.md) ou [**Song**](think-method.md) dépasse la taille de la bulle active, agent fait défiler automatiquement le texte dans l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="ab4a3-111">If the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method exceeds the size of the current balloon, Agent automatically scrolls the text in the balloon.</span></span>

<span data-ttu-id="ab4a3-112">Le paramètre par défaut est basé sur les paramètres lorsque le caractère est compilé avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="ab4a3-112">The default setting is based on settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab4a3-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab4a3-113">See Also</span></span>

[<span data-ttu-id="ab4a3-114">**IAgentBalloon::GetNumCharsPerLine**</span><span class="sxs-lookup"><span data-stu-id="ab4a3-114">**IAgentBalloon::GetNumCharsPerLine**</span></span>](iagentballoon--getnumcharsperline.md)


 

 




