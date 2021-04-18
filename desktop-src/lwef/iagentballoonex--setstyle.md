---
title: IAgentBalloonEx SetStyle
description: IAgentBalloonEx SetStyle
ms.assetid: 5be569b7-8a2d-437b-b5db-401af343bc78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d942cc8adaf454a7c5f1cd299581f917560c00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511858"
---
# <a name="iagentballoonexsetstyle"></a><span data-ttu-id="e24a8-103">IAgentBalloonEx :: SetStyle</span><span class="sxs-lookup"><span data-stu-id="e24a8-103">IAgentBalloonEx::SetStyle</span></span>

<span data-ttu-id="e24a8-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e24a8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetStyle(
   long lStyle,  // style settings
);
```

<span data-ttu-id="e24a8-105">Récupère les paramètres de style de la bulle de texte du caractère.</span><span class="sxs-lookup"><span data-stu-id="e24a8-105">Retrieves the character's word balloon style settings.</span></span>

-   <span data-ttu-id="e24a8-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="e24a8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e24a8-107"><span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*</span><span class="sxs-lookup"><span data-stu-id="e24a8-107"><span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*</span></span>
</dt> <dd>

<span data-ttu-id="e24a8-108">Paramètres de style pour le mot-bulle, qui peut être une combinaison de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e24a8-108">Style settings for the word balloon, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="e24a8-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="e24a8-109">Value</span></span>                                                                            | <span data-ttu-id="e24a8-110">Description</span><span class="sxs-lookup"><span data-stu-id="e24a8-110">Description</span></span>                                                 |
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="e24a8-111">const-style de bulle **abrégé non signé** **\_ \_ BALLOONON = 0x00000001 ;**</span><span class="sxs-lookup"><span data-stu-id="e24a8-111">**const unsigned short** **BALLOON\_STYLE\_BALLOONON = 0x00000001;**</span></span><br/>  | <span data-ttu-id="e24a8-112">La bulle est prise en charge pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="e24a8-112">The balloon is supported for output.</span></span>                        |
| <span data-ttu-id="e24a8-113">const : style de bulle **abrégé non signé** **\_ \_ SIZETOTEXT = 0x0000002 ;**</span><span class="sxs-lookup"><span data-stu-id="e24a8-113">**const unsigned short** **BALLOON\_STYLE \_SIZETOTEXT = 0x0000002;**</span></span><br/> | <span data-ttu-id="e24a8-114">La hauteur de la bulle est dimensionnée pour s’adapter à la sortie de texte.</span><span class="sxs-lookup"><span data-stu-id="e24a8-114">The balloon height is sized to accommodate the text output.</span></span> |
| <span data-ttu-id="e24a8-115">const-style de bulle **abrégé non signé** - **\_ \_ Masquer automatiquement = 0x00000004 ;**</span><span class="sxs-lookup"><span data-stu-id="e24a8-115">**const unsigned short** **BALLOON\_STYLE \_AUTOHIDE = 0x00000004;**</span></span><br/>  | <span data-ttu-id="e24a8-116">L’info-bulle est automatiquement masquée.</span><span class="sxs-lookup"><span data-stu-id="e24a8-116">The balloon is automatically hidden.</span></span>                        |
| <span data-ttu-id="e24a8-117">autorythme du style de la bulle **non signée const** **\_ \_ = 0x00000008 ;**</span><span class="sxs-lookup"><span data-stu-id="e24a8-117">**const unsigned short** **BALLOON\_STYLE \_AUTOPACE = 0x00000008;**</span></span><br/>  | <span data-ttu-id="e24a8-118">La sortie de texte est basée sur la vitesse de sortie.</span><span class="sxs-lookup"><span data-stu-id="e24a8-118">The text output is paced based on the output rate.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="e24a8-119">Lorsque le bit de style **BalloonOn** est défini, la bulle de mot apparaît lorsque la méthode [**Speak**](speak-method.md) ou [**Song**](think-method.md) est utilisée, sauf si l’utilisateur remplace son affichage dans la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e24a8-119">When the **BalloonOn** style bit is set, the word balloon appears when the [**Speak**](speak-method.md) or [**Think**](think-method.md) method is used, unless the user overrides its display in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="e24a8-120">Si la valeur n’est pas définie, aucune bulle ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e24a8-120">When not set, no balloon appears.</span></span>

<span data-ttu-id="e24a8-121">Lorsque le bit de style **SizeToText** est défini, le mot bulle redimensionne automatiquement la hauteur de la bulle sur la taille actuelle du texte spécifié dans la méthode [**Speak**](speak-method.md) ou [**Song**](think-method.md) .</span><span class="sxs-lookup"><span data-stu-id="e24a8-121">When the **SizeToText** style bit is set, the word balloon automatically sizes the height of the balloon to the current size of the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method.</span></span> <span data-ttu-id="e24a8-122">Lorsque cette option n’est pas définie, la hauteur de l’info-bulle est basée sur le paramètre de propriété Number of Lines du ballon.</span><span class="sxs-lookup"><span data-stu-id="e24a8-122">When not set, the balloon's height is based on the balloon's number of lines property setting.</span></span> <span data-ttu-id="e24a8-123">Ce bit de style est défini sur 1 et toute tentative d’utilisation de [**IAgentBalloonEx :: SetNumLines**](iagentballoonex--setnumlines.md) génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="e24a8-123">This style bit is set to 1 and an attempt to use [**IAgentBalloonEx::SetNumLines**](iagentballoonex--setnumlines.md) will result in an error.</span></span>

<span data-ttu-id="e24a8-124">Lorsque le bit de style de **masquage** automatique est défini, la bulle de mot est automatiquement masquée après un délai d’expiration courts.</span><span class="sxs-lookup"><span data-stu-id="e24a8-124">When the **AutoHide** style bit is set, the word balloon automatically hides after a short timeout.</span></span> <span data-ttu-id="e24a8-125">Lorsqu’elle n’est pas définie, la bulle s’affiche jusqu’à un nouvel appel [**Speak**](speak-method.md) ou [**Song**](think-method.md) , le caractère est masqué ou l’utilisateur clique ou fait glisser le caractère.</span><span class="sxs-lookup"><span data-stu-id="e24a8-125">When not set, the balloon displays until a new [**Speak**](speak-method.md) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="e24a8-126">Lorsque le bit de style de **rythme** automatique est défini, la bulle de mot ajuste la sortie en fonction du taux de sortie actuel, par exemple, un mot à la fois.</span><span class="sxs-lookup"><span data-stu-id="e24a8-126">When the **AutoPace** style bit is set, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="e24a8-127">Lorsque la sortie dépasse la taille de la bulle, le texte précédent est automatiquement défilé.</span><span class="sxs-lookup"><span data-stu-id="e24a8-127">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="e24a8-128">Si la valeur n’est pas définie, tout le texte inclus dans une instruction [**Speak**](speak-method.md) ou [**Song**](think-method.md) s’affiche à la fois.</span><span class="sxs-lookup"><span data-stu-id="e24a8-128">When not set, all text included in a [**Speak**](speak-method.md) or [**Think**](think-method.md) statement displays at once.</span></span>

<span data-ttu-id="e24a8-129">La propriété style de l’info-bulle peut être définie même si l’utilisateur a désactivé l’affichage de l’info-bulle à l’aide de la feuille de propriétés Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e24a8-129">The Balloon's style property can be set even if the user has disabled display of the Balloon using the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="e24a8-130">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="e24a8-130">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="e24a8-131">Les valeurs par défaut de ces bits de style sont basées sur leurs paramètres lorsque le caractère est compilé avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e24a8-131">The defaults for these style bits are based on their settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="e24a8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e24a8-132">See Also</span></span>

[<span data-ttu-id="e24a8-133">**IAgentBalloonEx::GetStyle**</span><span class="sxs-lookup"><span data-stu-id="e24a8-133">**IAgentBalloonEx::GetStyle**</span></span>](iagentballoonex--getstyle.md)


 

 





