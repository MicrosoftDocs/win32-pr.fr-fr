---
title: Propriété style
description: Propriété style
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d46dd7f7ce0e2fdc16b8b17f9074b1eef30c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310077"
---
# <a name="style-property"></a><span data-ttu-id="c2b5f-103">Propriété style</span><span class="sxs-lookup"><span data-stu-id="c2b5f-103">Style Property</span></span>

<span data-ttu-id="c2b5f-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c2b5f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c2b5f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="c2b5f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c2b5f-106">Retourne ou définit le style de sortie de la bulle de texte du caractère.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-106">Returns or sets the character's word balloon output style.</span></span>

</dd> <dt>

<span data-ttu-id="c2b5f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="c2b5f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c2b5f-108">\*agent. ***Caractères («*** CharacterID \* \* * »). Style Balloon. style* \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="c2b5f-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Balloon.Style** \[ = *Style*\]</span></span>



| <span data-ttu-id="c2b5f-109">Partie</span><span class="sxs-lookup"><span data-stu-id="c2b5f-109">Part</span></span>    | <span data-ttu-id="c2b5f-110">Description</span><span class="sxs-lookup"><span data-stu-id="c2b5f-110">Description</span></span>                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2b5f-111">*Style*</span><span class="sxs-lookup"><span data-stu-id="c2b5f-111">*Style*</span></span> | <span data-ttu-id="c2b5f-112">Entier qui représente le style de sortie de l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-112">An integer that represents the balloon's output style.</span></span> <span data-ttu-id="c2b5f-113">Le paramètre de style est un champ de bits dont les bits correspondent à : Balloon-on (bit 0), taille-to-Text (bit 1), masquage automatique (bit 2), rythme automatique (bit 3), nombre de caractères par ligne (bits 16-23) et nombre de lignes (bits 24-31).</span><span class="sxs-lookup"><span data-stu-id="c2b5f-113">The style setting is a bitfield with bits corresponding to: balloon-on (bit 0), size-to-text (bit 1), auto-hide (bit 2), auto-pace (bit 3), number of characters per lines (bits 16-23), and number of lines (bits 24-31).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2b5f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c2b5f-114">Remarks</span></span>

<span data-ttu-id="c2b5f-115">Lorsque le bit de style Balloon est défini sur 1, la bulle de mot apparaît lorsqu’une méthode [**Speak**](https://www.bing.com/search?q=**Speak**) ou [**Song**](think-method.md) est utilisée, sauf si l’utilisateur remplace ce paramètre dans la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-115">When the balloon-on style bit is set to 1, the word balloon appears when a [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) method is used, unless the user overrides this setting in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="c2b5f-116">Si la valeur est 0, une bulle n’apparaît pas.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-116">When set to 0, a balloon does not appear.</span></span>

<span data-ttu-id="c2b5f-117">Lorsque le bit de style taille-texte a la valeur 1, le mot bulle redimensionne automatiquement la hauteur de l’info-bulle sur la taille actuelle du texte de l’instruction [**Speak**](https://www.bing.com/search?q=**Speak**) ou [**Song**](think-method.md) .</span><span class="sxs-lookup"><span data-stu-id="c2b5f-117">When the size-to-text style bit is set to 1, the word balloon automatically sizes the height of the balloon to the current size of the text for the [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) statement.</span></span> <span data-ttu-id="c2b5f-118">Lorsqu’elle est définie sur 0, la hauteur de l’info-bulle est basée sur le paramètre de propriété [**numberoflines**](numberoflines-property.md) .</span><span class="sxs-lookup"><span data-stu-id="c2b5f-118">When set to 0, the balloon's height is based on the [**NumberOfLines**](numberoflines-property.md) property setting.</span></span> <span data-ttu-id="c2b5f-119">Si ce bit de style est défini sur 1 et que vous tentez de définir la propriété **numberoflines** , l’agent génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-119">If this style bit is set to 1 and you attempt to set the **NumberOfLines** property, Agent raises an error.</span></span>

<span data-ttu-id="c2b5f-120">Lorsque le bit de style à masquage automatique est défini sur 1, la bulle de mot est automatiquement masquée quand la sortie orale est terminée.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-120">When the auto-hide style bit is set to 1, the word balloon automatically hides when spoken output completes.</span></span> <span data-ttu-id="c2b5f-121">Lorsqu’elle est définie sur 0, la bulle reste affichée jusqu’au prochain appel [**Speak**](https://www.bing.com/search?q=**Speak**) ou [**Song**](think-method.md) , que le caractère est masqué ou que l’utilisateur clique sur le caractère ou le fait glisser.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-121">When set to 0, the balloon remains displayed until the next [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="c2b5f-122">Lorsque le bit de style de rythme automatique est défini sur 1, la bulle de mot ajuste la sortie en fonction du taux de sortie actuel, par exemple, un mot à la fois.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-122">When the auto-pace style bit is set to 1, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="c2b5f-123">Lorsque la sortie dépasse la taille de la bulle, le texte précédent est automatiquement défilé.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-123">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="c2b5f-124">Si la valeur est 0, tout le texte inclus dans une instruction [**Speak**](https://www.bing.com/search?q=**Speak**) ou [**Song**](think-method.md) s’affiche à la fois.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-124">When set to 0, all text included in a [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) statement is displayed at once.</span></span>

<span data-ttu-id="c2b5f-125">Pour récupérer uniquement la valeur des quatre bits inférieurs, **et** la valeur retournée par le **style** avec 255.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-125">To retrieve just the value of the bottom four bits, **And** the value returned by **Style** with 255.</span></span> <span data-ttu-id="c2b5f-126">Pour définir une valeur de bit, **ou** la valeur retournée avec la valeur des bits que vous souhaitez définir.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-126">To set a bit value, **Or** the value returned with the value of the bits you want set.</span></span> <span data-ttu-id="c2b5f-127">Pour désactiver un bit, **et** la valeur retournée avec un complément du bit :</span><span class="sxs-lookup"><span data-stu-id="c2b5f-127">To turn a bit off, **And** the value returned with one's complement of the bit:</span></span>


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



<span data-ttu-id="c2b5f-128">La propriété **style** retourne également le nombre de caractères par ligne dans l’octet inférieur du mot supérieur et le nombre de lignes dans l’octet de poids fort du mot supérieur.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-128">The **Style** property also returns the number of characters per line in the lower byte of the upper word and the number of lines in the high byte of the upper word.</span></span> <span data-ttu-id="c2b5f-129">Bien que cette opération puisse être plus facile à lire à l’aide des propriétés [**CharsPerLine**](charsperline-property.md) et [**numberoflines**](numberoflines-property.md), la propriété **style** vous permet également de définir ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-129">While this can be more easily read using the [**CharsPerLine**](charsperline-property.md) and [**NumberOfLines**](numberoflines-property.md)properties, the **Style** property also enables you to set those values.</span></span>

<span data-ttu-id="c2b5f-130">Par exemple, pour modifier le nombre de lignes, effacez les bits 24 à 31 avec une opération **and** logique avant de définir la nouvelle valeur en tant que produit de la nouvelle valeur Times 2 ^ 24, ajouté à la valeur existante de la propriété **style** .</span><span class="sxs-lookup"><span data-stu-id="c2b5f-130">For example, to change the number of lines, clear bits 24 to 31 with a logical **AND** operation before setting the new value as the product of the new value times 2^24, added to the existing value of the **Style** property.</span></span>


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



<span data-ttu-id="c2b5f-131">Pour définir le nombre de caractères par ligne, effacez les bits de 16 à 23 avec une opération **and** logique avant de définir la nouvelle valeur en tant que produit de la nouvelle valeur Times 2 ^ 16, ajouté à la valeur existante de la propriété style.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-131">To set the number of characters per line, clear bits 16 to 23 with a logical **AND** operation before setting the new value as the product of the new value times 2^16, added to the existing value of the Style property.</span></span>


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



<span data-ttu-id="c2b5f-132">La propriété **style** peut être définie même si l’utilisateur a désactivé l’affichage des bulles à l’aide de la feuille de propriétés Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-132">The **Style** property can be set even if the user has disabled balloon display using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="c2b5f-133">Toutefois, les valeurs du nombre de lignes doivent être comprises entre 1 et 128 et le nombre de caractères par ligne doit être compris entre 8 et 255.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-133">However, the values for the number of lines must be between 1 and 128 and the number characters per line must be between 8 and 255.</span></span> <span data-ttu-id="c2b5f-134">Si vous fournissez une valeur non valide pour la propriété **style** , agent génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-134">If you provide an invalid value for the **Style** property, Agent will raise an error.</span></span>

<span data-ttu-id="c2b5f-135">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-135">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="c2b5f-136">Les valeurs par défaut de ces bits de style sont basées sur leurs paramètres lorsque le caractère est compilé avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="c2b5f-136">The defaults for these style bits are based on their settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

 

 




