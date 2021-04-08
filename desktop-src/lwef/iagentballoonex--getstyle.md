---
title: IAgentBalloonEx GetStyle
description: IAgentBalloonEx GetStyle
ms.assetid: 7c6a7260-073b-4535-b8e7-a8cae9aae9ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e21ab22a9aa5a85fdbe1bc541f29df75313cdce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840410"
---
# <a name="iagentballoonexgetstyle"></a><span data-ttu-id="b11a5-103">IAgentBalloonEx::GetStyle</span><span class="sxs-lookup"><span data-stu-id="b11a5-103">IAgentBalloonEx::GetStyle</span></span>

<span data-ttu-id="b11a5-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b11a5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetStyle(
   long * plStyle,  // address of style settings
);
```

<span data-ttu-id="b11a5-105">Récupère les paramètres de style de la bulle de texte du caractère.</span><span class="sxs-lookup"><span data-stu-id="b11a5-105">Retrieves the character's word balloon style settings.</span></span>

-   <span data-ttu-id="b11a5-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="b11a5-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b11a5-107"><span id="plStyle"></span><span id="plstyle"></span><span id="PLSTYLE"></span>*plStyle*</span><span class="sxs-lookup"><span data-stu-id="b11a5-107"><span id="plStyle"></span><span id="plstyle"></span><span id="PLSTYLE"></span>*plStyle*</span></span>
</dt> <dd>

<span data-ttu-id="b11a5-108">Paramètres de style pour le mot-bulle, qui peut être une combinaison de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b11a5-108">Style settings for the word balloon, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="b11a5-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="b11a5-109">Value</span></span>                                                                           | <span data-ttu-id="b11a5-110">Description</span><span class="sxs-lookup"><span data-stu-id="b11a5-110">Description</span></span>                                                 |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b11a5-111">const-style de bulle **abrégé non signé** **\_ \_ BALLOONON = 0x00000001 ;**</span><span class="sxs-lookup"><span data-stu-id="b11a5-111">**const unsigned short** **BALLOON\_STYLE\_BALLOONON = 0x00000001;**</span></span><br/> | <span data-ttu-id="b11a5-112">La bulle est prise en charge pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="b11a5-112">The balloon is supported for output.</span></span>                        |
| <span data-ttu-id="b11a5-113">const : style de bulle **abrégé non signé** **\_ \_ SIZETOTEXT = 0x0000002 ;**</span><span class="sxs-lookup"><span data-stu-id="b11a5-113">**const unsigned short** **BALLOON\_STYLE \_SIZETOTEXT = 0x0000002;**</span></span>           | <span data-ttu-id="b11a5-114">La hauteur de la bulle est dimensionnée pour s’adapter à la sortie de texte.</span><span class="sxs-lookup"><span data-stu-id="b11a5-114">The balloon height is sized to accommodate the text output.</span></span> |
| <span data-ttu-id="b11a5-115">const-style de bulle **abrégé non signé** - **\_ \_ Masquer automatiquement = 0x00000004 ;**</span><span class="sxs-lookup"><span data-stu-id="b11a5-115">**const unsigned short** **BALLOON\_STYLE \_AUTOHIDE = 0x00000004;**</span></span>            | <span data-ttu-id="b11a5-116">L’info-bulle est automatiquement masquée.</span><span class="sxs-lookup"><span data-stu-id="b11a5-116">The balloon is automatically hidden.</span></span>                        |
| <span data-ttu-id="b11a5-117">autorythme du style de la bulle **non signée const** **\_ \_ = 0x00000008 ;**</span><span class="sxs-lookup"><span data-stu-id="b11a5-117">**const unsigned short** **BALLOON\_STYLE \_AUTOPACE = 0x00000008;**</span></span>            | <span data-ttu-id="b11a5-118">La sortie de texte est basée sur la vitesse de sortie.</span><span class="sxs-lookup"><span data-stu-id="b11a5-118">The text output is paced based on the output rate.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="b11a5-119">Lorsque le bit de style **BalloonOn** est défini, la bulle de texte s’affiche lorsque la méthode [**Speak**](speak-method.md) ou [**Song**](think-method.md) est utilisée, sauf si l’utilisateur remplace son affichage par le biais de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b11a5-119">When the **BalloonOn** style bit is set, the word balloon appears when the [**Speak**](speak-method.md) or [**Think**](think-method.md) method is used, unless the user overrides its display through the Microsoft Agent property sheet.</span></span> <span data-ttu-id="b11a5-120">Si la valeur n’est pas définie, aucune bulle ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b11a5-120">When not set, no balloon appears.</span></span>

<span data-ttu-id="b11a5-121">Lorsque le bit de style **SizeToText** est défini, le mot bulle redimensionne automatiquement la hauteur de la bulle sur la taille actuelle du texte spécifié dans la méthode [**Speak**](speak-method.md) ou [**Song**](think-method.md) .</span><span class="sxs-lookup"><span data-stu-id="b11a5-121">When the **SizeToText** style bit is set, the word balloon automatically sizes the height of the balloon to the current size of the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method.</span></span> <span data-ttu-id="b11a5-122">Lorsque cette option n’est pas définie, la hauteur de l’info-bulle est basée sur le paramètre de propriété Number of Lines du ballon.</span><span class="sxs-lookup"><span data-stu-id="b11a5-122">When not set, the balloon's height is based on the balloon's number of lines property setting.</span></span> <span data-ttu-id="b11a5-123">Ce bit de style est défini sur 1 et toute tentative d’utilisation de [**IAgentBalloonEx :: SetNumLines**](iagentballoonex--setnumlines.md) génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="b11a5-123">This style bit is set to 1 and an attempt to use [**IAgentBalloonEx::SetNumLines**](iagentballoonex--setnumlines.md) will result in an error.</span></span>

<span data-ttu-id="b11a5-124">Lorsque le bit de style de **masquage** automatique est défini, la bulle de mot se masque automatiquement après un court délai d’attente. Lorsqu’elle n’est pas définie, la bulle s’affiche jusqu’à un nouvel appel [**Speak**](speak-method.md) ou [**Song**](think-method.md) , le caractère est masqué ou l’utilisateur clique ou fait glisser le caractère.</span><span class="sxs-lookup"><span data-stu-id="b11a5-124">When the **AutoHide** style bit is set, the word balloon automatically hides after a short time-out. When not set, the balloon displays until a new [**Speak**](speak-method.md) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="b11a5-125">Lorsque le bit de style de **rythme** automatique est défini, la bulle de mot ajuste la sortie en fonction du taux de sortie actuel, par exemple, un mot à la fois.</span><span class="sxs-lookup"><span data-stu-id="b11a5-125">When the **AutoPace** style bit is set, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="b11a5-126">Lorsque la sortie dépasse la taille de la bulle, le texte précédent est automatiquement défilé.</span><span class="sxs-lookup"><span data-stu-id="b11a5-126">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="b11a5-127">Si la valeur n’est pas définie, tout le texte inclus dans une instruction [**Speak**](speak-method.md) ou [**Song**](think-method.md) s’affiche à la fois.</span><span class="sxs-lookup"><span data-stu-id="b11a5-127">When not set, all text included in a [**Speak**](speak-method.md) or [**Think**](think-method.md) statement displays at once.</span></span>

<span data-ttu-id="b11a5-128">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="b11a5-128">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="b11a5-129">Les valeurs par défaut de ces bits de style sont basées sur les paramètres lorsque le caractère est compilé à l’aide de l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="b11a5-129">The defaults for these style bits are based on the settings when the character is compiled through the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="b11a5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b11a5-130">See Also</span></span>

[<span data-ttu-id="b11a5-131">**IAgentBalloonEx :: SetStyle**</span><span class="sxs-lookup"><span data-stu-id="b11a5-131">**IAgentBalloonEx::SetStyle**</span></span>](iagentballoonex--setstyle.md)


 

 





