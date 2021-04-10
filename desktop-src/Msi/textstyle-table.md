---
description: Le tableau TextStyle répertorie les différents styles de police utilisés dans les contrôles contenant du texte.
ms.assetid: a351e67a-8f51-41bf-9202-56488b870fa7
title: Table TextStyle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9993362228e37f01c0e53683755f7bd1310eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951320"
---
# <a name="textstyle-table"></a><span data-ttu-id="4b4bb-103">Table TextStyle</span><span class="sxs-lookup"><span data-stu-id="4b4bb-103">TextStyle Table</span></span>

<span data-ttu-id="4b4bb-104">Le tableau TextStyle répertorie les différents styles de police utilisés dans les contrôles contenant du texte.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-104">The TextStyle table lists different font styles used in controls having text.</span></span>

<span data-ttu-id="4b4bb-105">La table TextStyle contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-105">The TextStyle table has the following columns.</span></span>



| <span data-ttu-id="4b4bb-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="4b4bb-106">Column</span></span>    | <span data-ttu-id="4b4bb-107">Type</span><span class="sxs-lookup"><span data-stu-id="4b4bb-107">Type</span></span>                               | <span data-ttu-id="4b4bb-108">Clé</span><span class="sxs-lookup"><span data-stu-id="4b4bb-108">Key</span></span> | <span data-ttu-id="4b4bb-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="4b4bb-109">Nullable</span></span> |
|-----------|------------------------------------|-----|----------|
| <span data-ttu-id="4b4bb-110">TextStyle</span><span class="sxs-lookup"><span data-stu-id="4b4bb-110">TextStyle</span></span> | [<span data-ttu-id="4b4bb-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="4b4bb-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="4b4bb-112">O</span><span class="sxs-lookup"><span data-stu-id="4b4bb-112">Y</span></span>   | <span data-ttu-id="4b4bb-113">N</span><span class="sxs-lookup"><span data-stu-id="4b4bb-113">N</span></span>        |
| <span data-ttu-id="4b4bb-114">FaceName</span><span class="sxs-lookup"><span data-stu-id="4b4bb-114">FaceName</span></span>  | [<span data-ttu-id="4b4bb-115">Text</span><span class="sxs-lookup"><span data-stu-id="4b4bb-115">Text</span></span>](text.md)                   | <span data-ttu-id="4b4bb-116">N</span><span class="sxs-lookup"><span data-stu-id="4b4bb-116">N</span></span>   | <span data-ttu-id="4b4bb-117">N</span><span class="sxs-lookup"><span data-stu-id="4b4bb-117">N</span></span>        |
| <span data-ttu-id="4b4bb-118">Taille</span><span class="sxs-lookup"><span data-stu-id="4b4bb-118">Size</span></span>      | [<span data-ttu-id="4b4bb-119">Integer</span><span class="sxs-lookup"><span data-stu-id="4b4bb-119">Integer</span></span>](integer.md)             | <span data-ttu-id="4b4bb-120">N</span><span class="sxs-lookup"><span data-stu-id="4b4bb-120">N</span></span>   | <span data-ttu-id="4b4bb-121">N</span><span class="sxs-lookup"><span data-stu-id="4b4bb-121">N</span></span>        |
| <span data-ttu-id="4b4bb-122">Couleur</span><span class="sxs-lookup"><span data-stu-id="4b4bb-122">Color</span></span>     | [<span data-ttu-id="4b4bb-123">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="4b4bb-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="4b4bb-124">N</span><span class="sxs-lookup"><span data-stu-id="4b4bb-124">N</span></span>   | <span data-ttu-id="4b4bb-125">O</span><span class="sxs-lookup"><span data-stu-id="4b4bb-125">Y</span></span>        |
| <span data-ttu-id="4b4bb-126">StyleBits</span><span class="sxs-lookup"><span data-stu-id="4b4bb-126">StyleBits</span></span> | [<span data-ttu-id="4b4bb-127">Integer</span><span class="sxs-lookup"><span data-stu-id="4b4bb-127">Integer</span></span>](integer.md)             | <span data-ttu-id="4b4bb-128">N</span><span class="sxs-lookup"><span data-stu-id="4b4bb-128">N</span></span>   | <span data-ttu-id="4b4bb-129">O</span><span class="sxs-lookup"><span data-stu-id="4b4bb-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="4b4bb-130">Colonnes</span><span class="sxs-lookup"><span data-stu-id="4b4bb-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="4b4bb-131"><span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>TextStyle</span><span class="sxs-lookup"><span data-stu-id="4b4bb-131"><span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>TextStyle</span></span>
</dt> <dd>

<span data-ttu-id="4b4bb-132">Cette colonne correspond au nom du style de police.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-132">This column is the name of the font style.</span></span> <span data-ttu-id="4b4bb-133">Ce nom peut être incorporé dans la chaîne de texte pour indiquer une modification de style.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-133">This name can be embedded in the text string to indicate a style change.</span></span> <span data-ttu-id="4b4bb-134">Notez que le nom de style de police utilisé dans ce champ ne doit pas se terminer par les caractères suivants : \_ UL.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-134">Note that the font style name used in this field must not end with the characters: \_UL.</span></span> <span data-ttu-id="4b4bb-135">Consultez [Ajout de contrôles et de texte](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="4b4bb-135">See [Adding Controls and Text](adding-controls-and-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b4bb-136"><span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName</span><span class="sxs-lookup"><span data-stu-id="4b4bb-136"><span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName</span></span>
</dt> <dd>

<span data-ttu-id="4b4bb-137">Chaîne qui indique le nom de la police.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-137">A string indicating the name of the font.</span></span> <span data-ttu-id="4b4bb-138">La longueur de la chaîne ne doit pas dépasser 31 caractères.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-138">The string must be no more than 31 characters long.</span></span>

</dd> <dt>

<span data-ttu-id="4b4bb-139"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>Corps</span><span class="sxs-lookup"><span data-stu-id="4b4bb-139"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>Size</span></span>
</dt> <dd>

<span data-ttu-id="4b4bb-140">Taille de la police mesurée en points.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-140">The font size measured in points.</span></span> <span data-ttu-id="4b4bb-141">Il doit s’agir d’un nombre non négatif.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-141">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="4b4bb-142"><span id="Color"></span><span id="color"></span><span id="COLOR"></span>Couleur</span><span class="sxs-lookup"><span data-stu-id="4b4bb-142"><span id="Color"></span><span id="color"></span><span id="COLOR"></span>Color</span></span>
</dt> <dd>

<span data-ttu-id="4b4bb-143">Cette colonne spécifie la couleur de texte affichée par un [contrôle de texte](text-control.md).</span><span class="sxs-lookup"><span data-stu-id="4b4bb-143">This column specifies the text color displayed by a [Text Control](text-control.md).</span></span> <span data-ttu-id="4b4bb-144">Tous les autres types de contrôles utilisent toujours la couleur de texte par défaut.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-144">All other types of controls always use the default text color.</span></span> <span data-ttu-id="4b4bb-145">La valeur placée dans cette colonne doit être calculée à l’aide de la formule suivante : 65536 \* Blue + 256 \* vert + rouge, où Red, Green et Blue se trouvent dans la plage de 0-255.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-145">The value put in this column should be computed using the following formula: 65536 \* blue + 256 \* green + red, where red, green, and blue are each in the range of 0-255.</span></span> <span data-ttu-id="4b4bb-146">La valeur ne doit pas dépasser 16777215, qui est la valeur de blanc.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-146">The value must not exceed 16777215, which is the value for white.</span></span> <span data-ttu-id="4b4bb-147">La valeur est 0 pour le noir, 255 pour rouge, 65280 pour le vert, 16711680 pour bleu et 8421504 pour gris.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-147">The value is 0 for black, 255 for red, 65280 for green, 16711680 for blue and 8421504 for grey.</span></span> <span data-ttu-id="4b4bb-148">Si vous laissez le champ vide, vous spécifiez la couleur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-148">Leaving the field empty specifies the default color.</span></span>

<span data-ttu-id="4b4bb-149">Ne placez pas de [contrôles de texte](text-control.md) transparent par-dessus les bitmaps de couleur.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-149">Do not place transparent [Text controls](text-control.md) on top of colored bitmaps.</span></span> <span data-ttu-id="4b4bb-150">Le texte peut ne pas être visible si l’utilisateur modifie le modèle de couleurs d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-150">The text may not be visible if the user changes the display color scheme.</span></span> <span data-ttu-id="4b4bb-151">Par exemple, le texte peut devenir invisible si l’utilisateur définit le paramètre de contraste élevé pour l’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-151">For example, text may become invisible if the user sets the high contrast parameter for accessibility.</span></span>

</dd> <dt>

<span data-ttu-id="4b4bb-152"><span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits</span><span class="sxs-lookup"><span data-stu-id="4b4bb-152"><span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits</span></span>
</dt> <dd>

<span data-ttu-id="4b4bb-153">Combinaison de bits indiquant la mise en forme du texte.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-153">A combination of bits indicating the formatting for the text.</span></span>

<span data-ttu-id="4b4bb-154">Les bits de style individuels ont les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="4b4bb-154">The individual style bits have the following values.</span></span>



| <span data-ttu-id="4b4bb-155">Constante</span><span class="sxs-lookup"><span data-stu-id="4b4bb-155">Constant</span></span>                             | <span data-ttu-id="4b4bb-156">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="4b4bb-156">Hexadecimal</span></span> | <span data-ttu-id="4b4bb-157">Decimal</span><span class="sxs-lookup"><span data-stu-id="4b4bb-157">Decimal</span></span> | <span data-ttu-id="4b4bb-158">Style</span><span class="sxs-lookup"><span data-stu-id="4b4bb-158">Style</span></span>      |
|--------------------------------------|-------------|---------|------------|
| <span data-ttu-id="4b4bb-159">**msidbTextStyleStyleBitsBold**</span><span class="sxs-lookup"><span data-stu-id="4b4bb-159">**msidbTextStyleStyleBitsBold**</span></span>      | <span data-ttu-id="4b4bb-160">0x001</span><span class="sxs-lookup"><span data-stu-id="4b4bb-160">0x001</span></span>       | <span data-ttu-id="4b4bb-161">1</span><span class="sxs-lookup"><span data-stu-id="4b4bb-161">1</span></span>       | <span data-ttu-id="4b4bb-162">Gras</span><span class="sxs-lookup"><span data-stu-id="4b4bb-162">Bold</span></span>       |
| <span data-ttu-id="4b4bb-163">**msidbTextStyleStyleBitsItalic**</span><span class="sxs-lookup"><span data-stu-id="4b4bb-163">**msidbTextStyleStyleBitsItalic**</span></span>    | <span data-ttu-id="4b4bb-164">0x002</span><span class="sxs-lookup"><span data-stu-id="4b4bb-164">0x002</span></span>       | <span data-ttu-id="4b4bb-165">2</span><span class="sxs-lookup"><span data-stu-id="4b4bb-165">2</span></span>       | <span data-ttu-id="4b4bb-166">Italique</span><span class="sxs-lookup"><span data-stu-id="4b4bb-166">Italic</span></span>     |
| <span data-ttu-id="4b4bb-167">**msidbTextStyleStyleBitsUnderline**</span><span class="sxs-lookup"><span data-stu-id="4b4bb-167">**msidbTextStyleStyleBitsUnderline**</span></span> | <span data-ttu-id="4b4bb-168">0x004</span><span class="sxs-lookup"><span data-stu-id="4b4bb-168">0x004</span></span>       | <span data-ttu-id="4b4bb-169">4</span><span class="sxs-lookup"><span data-stu-id="4b4bb-169">4</span></span>       | <span data-ttu-id="4b4bb-170">Souligner</span><span class="sxs-lookup"><span data-stu-id="4b4bb-170">Underline</span></span>  |
| <span data-ttu-id="4b4bb-171">**msidbTextStyleStyleBitsStrike**</span><span class="sxs-lookup"><span data-stu-id="4b4bb-171">**msidbTextStyleStyleBitsStrike**</span></span>    | <span data-ttu-id="4b4bb-172">0x008</span><span class="sxs-lookup"><span data-stu-id="4b4bb-172">0x008</span></span>       | <span data-ttu-id="4b4bb-173">8</span><span class="sxs-lookup"><span data-stu-id="4b4bb-173">8</span></span>       | <span data-ttu-id="4b4bb-174">Strike</span><span class="sxs-lookup"><span data-stu-id="4b4bb-174">Strike out</span></span> |



 

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="4b4bb-175">Validation</span><span class="sxs-lookup"><span data-stu-id="4b4bb-175">Validation</span></span>

<dl>

[<span data-ttu-id="4b4bb-176">ICE03</span><span class="sxs-lookup"><span data-stu-id="4b4bb-176">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="4b4bb-177">ICE06</span><span class="sxs-lookup"><span data-stu-id="4b4bb-177">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="4b4bb-178">ICE31</span><span class="sxs-lookup"><span data-stu-id="4b4bb-178">ICE31</span></span>](ice31.md)  
[<span data-ttu-id="4b4bb-179">ICE45</span><span class="sxs-lookup"><span data-stu-id="4b4bb-179">ICE45</span></span>](ice45.md)  
</dl>

 

 



