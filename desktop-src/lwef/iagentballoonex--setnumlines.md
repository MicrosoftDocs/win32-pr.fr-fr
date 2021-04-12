---
title: IAgentBalloonEx SetNumLines
description: IAgentBalloonEx SetNumLines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45c012d0193a0bd21ba203418920b87b2fac81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462375"
---
# <a name="iagentballoonexsetnumlines"></a><span data-ttu-id="24aa5-103">IAgentBalloonEx::SetNumLines</span><span class="sxs-lookup"><span data-stu-id="24aa5-103">IAgentBalloonEx::SetNumLines</span></span>

<span data-ttu-id="24aa5-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="24aa5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

<span data-ttu-id="24aa5-105">Définit le nombre de lignes de sortie de texte qui peuvent être affichées dans la bulle de mot du caractère.</span><span class="sxs-lookup"><span data-stu-id="24aa5-105">Sets the number of lines of text output that can be displayed in the character's word balloon.</span></span>

-   <span data-ttu-id="24aa5-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="24aa5-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="24aa5-107">Retourne E \_ INVALIDARG si le paramètre est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="24aa5-107">Returns E\_INVALIDARG if the parameter is zero.</span></span>

<dl> <dt>

<span data-ttu-id="24aa5-108"><span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*</span><span class="sxs-lookup"><span data-stu-id="24aa5-108"><span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*</span></span>
</dt> <dd>

<span data-ttu-id="24aa5-109">Nombre de lignes à afficher dans la bulle de mot.</span><span class="sxs-lookup"><span data-stu-id="24aa5-109">Number of lines to display in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="24aa5-110">La valeur minimale est 1 et la valeur maximale est 128.</span><span class="sxs-lookup"><span data-stu-id="24aa5-110">The minimum setting is 1 and maximum is 128.</span></span> <span data-ttu-id="24aa5-111">Si le texte spécifié dans la méthode [**Speak**](speak-method.md) ou [**Song**](think-method.md) dépasse la taille de la bulle active, agent fait défiler automatiquement le texte dans l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="24aa5-111">If the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method exceeds the size of the current balloon, Agent automatically scrolls the text in the balloon.</span></span>

<span data-ttu-id="24aa5-112">Cette méthode échoue si le bit de style **SizeToText** Balloon est défini.</span><span class="sxs-lookup"><span data-stu-id="24aa5-112">This method will fail if the **SizeToText** balloon style bit is set.</span></span>

<span data-ttu-id="24aa5-113">Le paramètre par défaut est basé sur les paramètres lorsque le caractère est compilé avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="24aa5-113">The default setting is based on settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="24aa5-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24aa5-114">See Also</span></span>

<span data-ttu-id="24aa5-115">[**IAgentBalloon :: GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx :: getStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx :: SetStyle**](iagentballoonex--setstyle.md)</span><span class="sxs-lookup"><span data-stu-id="24aa5-115">[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx::GetStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md)</span></span>


 

 




