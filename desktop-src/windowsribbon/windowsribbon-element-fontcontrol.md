---
title: Élément FontControl
description: Représente un contrôle de police, qui est un conteneur spécialisé de contrôles individuels dédiés à la manipulation de polices.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- Ruban des fenêtres d’élément FontControl
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa080b58e3a9d53fa044e7dbbb6598d5b7be7c49
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/30/2020
ms.locfileid: "104381754"
---
# <a name="fontcontrol-element"></a><span data-ttu-id="ad8f4-104">Élément FontControl</span><span class="sxs-lookup"><span data-stu-id="ad8f4-104">FontControl element</span></span>

<span data-ttu-id="ad8f4-105">Représente un [contrôle de police](windowsribbon-controls-fontcontrol.md), qui est un conteneur spécialisé de contrôles individuels dédiés à la manipulation de polices.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-105">Represents a [Font Control](windowsribbon-controls-fontcontrol.md), which is a specialized container of individual controls dedicated to font manipulation.</span></span>

## <a name="usage"></a><span data-ttu-id="ad8f4-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="ad8f4-106">Usage</span></span>

``` syntax
<FontControl
  CommandName = "xs:positiveInteger or xs:string"
  FontType = "xs:string"
  IsGrowShrinkButtonGroupVisible = "Boolean"
  IsStrikethroughButtonVisible = "Boolean"
  IsUnderlineButtonVisible = "Boolean"
  IsHighlightButtonVisible = "Boolean"
  ShowVerticalFonts = "Boolean"
  ShowTrueTypeOnly = "Boolean"
  MinimumFontSize = "xs:positiveInteger"
  MaximumFontSize = "xs:positiveInteger"/>
```

## <a name="attributes"></a><span data-ttu-id="ad8f4-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="ad8f4-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad8f4-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="ad8f4-108">Attribute</span></span></th>
<th><span data-ttu-id="ad8f4-109">Type</span><span class="sxs-lookup"><span data-stu-id="ad8f4-109">Type</span></span></th>
<th><span data-ttu-id="ad8f4-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ad8f4-110">Required</span></span></th>
<th><span data-ttu-id="ad8f4-111">Description</span><span class="sxs-lookup"><span data-stu-id="ad8f4-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ad8f4-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="ad8f4-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="ad8f4-113">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="ad8f4-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="ad8f4-114">Non</span><span class="sxs-lookup"><span data-stu-id="ad8f4-114">No</span></span><br/></td>
<td><span data-ttu-id="ad8f4-115">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="ad8f4-116">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="ad8f4-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-117">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="ad8f4-118">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="ad8f4-119">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad8f4-120"><strong>FontType</strong></span><span class="sxs-lookup"><span data-stu-id="ad8f4-120"><strong>FontType</strong></span></span><br/></td>
<td><span data-ttu-id="ad8f4-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="ad8f4-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="ad8f4-122">Non</span><span class="sxs-lookup"><span data-stu-id="ad8f4-122">No</span></span><br/></td>
<td><span data-ttu-id="ad8f4-123">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-123">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="ad8f4-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span><span class="sxs-lookup"><span data-stu-id="ad8f4-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-125">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-125">Default.</span></span> <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> <span data-ttu-id="ad8f4-126">La définition de l’attribut <em>FontType</em> pour <code>FontOnly</code> active les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-126">Setting the <em>FontType</em> attribute to <code>FontOnly</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="ad8f4-127">Zone de liste déroulante <strong>famille de polices</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-127"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="ad8f4-128">Zone de liste déroulante <strong>taille de police</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-128"><strong>Font Size</strong> combo box.</span></span></li>
<li><p><span data-ttu-id="ad8f4-129">Boutons bascule <strong>gras</strong>, <strong>italique</strong>, <strong>souligné</strong>et <strong>barré</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-129"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="ad8f4-130">Les boutons de bascule <strong>barré</strong> et <strong>souligné</strong> s’affichent par défaut, mais peuvent être masqués en définissant les attributs <em>IsStrikethroughButtonVisible</em> et <em>IsUnderlineButtonVisible</em> sur <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-130">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="ad8f4-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span><span class="sxs-lookup"><span data-stu-id="ad8f4-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> <span data-ttu-id="ad8f4-132">La définition de l’attribut <em>FontType</em> pour <code>FontWithColor</code> active les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-132">Setting the <em>FontType</em> attribute to <code>FontWithColor</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="ad8f4-133">Zone de liste déroulante <strong>famille de polices</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-133"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="ad8f4-134">Zone de liste déroulante <strong>taille de police</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-134"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="ad8f4-135"><strong>Agrandir la police</strong> et <strong>réduire</strong> la taille de police de police des boutons d’incrémentation et de décrémentation.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-135"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="ad8f4-136">Boutons bascule <strong>gras</strong>, <strong>italique</strong>, <strong>souligné</strong>et <strong>barré</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-136"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="ad8f4-137">Les boutons de bascule <strong>barré</strong> et <strong>souligné</strong> s’affichent par défaut, mais peuvent être masqués en définissant les attributs <em>IsStrikethroughButtonVisible</em> et <em>IsUnderlineButtonVisible</em> sur <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-137">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="ad8f4-138">Sélecteur de couleurs de <strong>couleur du texte</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-138"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="ad8f4-139">Sélecteur de couleurs de <strong>couleur de mise en surbrillance du texte</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-139"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="ad8f4-140">Ce contrôle est masqué par défaut, mais il peut être affiché en affectant à l’attribut <em>IsHighlightButtonVisible</em> la valeur <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-140">This control is hidden by default but can be displayed by setting the <em>IsHighlightButtonVisible</em> attribute to <code>true</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="ad8f4-141"><dt><span></span><span></span><strong></strong> (RichFont)</span><span class="sxs-lookup"><span data-stu-id="ad8f4-141"><dt><span></span><span></span><strong></strong> (RichFont)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> <span data-ttu-id="ad8f4-142">La définition de l’attribut <em>FontType</em> pour <code>RichFont</code> active les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-142">Setting the <em>FontType</em> attribute to <code>RichFont</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="ad8f4-143">Zone de liste déroulante <strong>famille de polices</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-143"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="ad8f4-144">Zone de liste déroulante <strong>taille de police</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-144"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="ad8f4-145"><strong>Agrandir la police</strong> et <strong>réduire</strong> la taille de police de police des boutons d’incrémentation et de décrémentation.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-145"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="ad8f4-146">Boutons bascule <strong>gras</strong>, <strong>italique</strong>, <strong>souligné</strong>et <strong>barré</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-146"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="ad8f4-147">Les boutons de bascule <strong>barré</strong> et <strong>souligné</strong> s’affichent par défaut et ne peuvent pas être masqués en définissant les attributs <em>IsStrikethroughButtonVisible</em> et <em>IsUnderlineButtonVisible</em> sur <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-147">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default and cannot be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="ad8f4-148">Sélecteur de couleurs de <strong>couleur du texte</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-148"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="ad8f4-149">Sélecteur de couleurs de <strong>couleur de mise en surbrillance du texte</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-149"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="ad8f4-150">Ce contrôle s’affiche par défaut et ne peut pas être masqué en affectant à l’attribut <em>IsHighlightButtonVisible</em> la valeur <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-150">This control is displayed by default and cannot be hidden by setting the <em>IsHighlightButtonVisible</em> attribute to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="ad8f4-151">Boutons bascule en <strong>indice</strong> et en <strong>exposant</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-151"><strong>Subscript</strong> and <strong>Superscript</strong> toggle buttons.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ad8f4-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span><span class="sxs-lookup"><span data-stu-id="ad8f4-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span></span><br/></td>
<td><span data-ttu-id="ad8f4-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="ad8f4-153">Boolean</span></span><br/></td>
<td><span data-ttu-id="ad8f4-154">Non</span><span class="sxs-lookup"><span data-stu-id="ad8f4-154">No</span></span><br/></td>
<td><span data-ttu-id="ad8f4-155"><strong>Windows 8 et versions ultérieures</strong></span><span class="sxs-lookup"><span data-stu-id="ad8f4-155"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="ad8f4-156">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-156">Restricted to one of the following values:</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ad8f4-157">Les boutons agrandir/rétrécir ne sont jamais affichés dans le <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-157">The Grow/Shrink buttons are never displayed in the <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="ad8f4-158">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-158">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-159">Valeur par défaut lorsque la valeur de <em>FontType</em> est égale à <code>FontWithColor</code> ou <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-159">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="ad8f4-160"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="ad8f4-160"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-161">Valeur par défaut lorsque la valeur de <em>FontType</em> est égale à <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-161">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad8f4-162"><strong>IsHighlightButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="ad8f4-162"><strong>IsHighlightButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="ad8f4-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="ad8f4-163">Boolean</span></span><br/></td>
<td><span data-ttu-id="ad8f4-164">Non</span><span class="sxs-lookup"><span data-stu-id="ad8f4-164">No</span></span><br/></td>
<td><span data-ttu-id="ad8f4-165">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-165">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ad8f4-166">La mise en surbrillance des couleurs n’est disponible qu’à partir d’un <strong>FontControl</strong> lorsque la valeur de l’attribut <em>FontType</em> est égale à <code>FontWithColor</code> ou <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-166">Color highlighting is available only from a <strong>FontControl</strong> when the value of the <em>FontType</em> attribute equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="ad8f4-167">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-167">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-168">Valeur par défaut lorsque la valeur de <em>FontType</em> est égale à <code>FontWithColor</code> ou <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-168">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> <span data-ttu-id="ad8f4-169">Valide uniquement lorsque la valeur de <em>FontType</em> est égale à <code>FontWithColor</code> ou <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-169">Valid only when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="ad8f4-170"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="ad8f4-170"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-171">Valeur par défaut lorsque la valeur de <em>FontType</em> est égale à <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-171">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> <span data-ttu-id="ad8f4-172">Valide uniquement lorsque la valeur de <em>FontType</em> est égale à <code>FontOnly</code> ou <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-172">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ad8f4-173"><strong>IsStrikethroughButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="ad8f4-173"><strong>IsStrikethroughButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="ad8f4-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="ad8f4-174">Boolean</span></span><br/></td>
<td><span data-ttu-id="ad8f4-175">Non</span><span class="sxs-lookup"><span data-stu-id="ad8f4-175">No</span></span><br/></td>
<td><span data-ttu-id="ad8f4-176">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-176">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="ad8f4-177">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-177">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-178">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-178">Default.</span></span> <br/> </dd> <span data-ttu-id="ad8f4-179"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="ad8f4-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-180">Valide uniquement lorsque la valeur de <em>FontType</em> est égale à <code>FontOnly</code> ou <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-180">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad8f4-181"><strong>IsUnderlineButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="ad8f4-181"><strong>IsUnderlineButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="ad8f4-182">Boolean</span><span class="sxs-lookup"><span data-stu-id="ad8f4-182">Boolean</span></span><br/></td>
<td><span data-ttu-id="ad8f4-183">Non</span><span class="sxs-lookup"><span data-stu-id="ad8f4-183">No</span></span><br/></td>
<td><span data-ttu-id="ad8f4-184">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-184">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="ad8f4-185">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-185">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-186">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-186">Default.</span></span> <br/> </dd> <span data-ttu-id="ad8f4-187"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="ad8f4-187"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-188">Valide uniquement lorsque la valeur de <em>FontType</em> est égale à <code>FontOnly</code> ou <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-188">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ad8f4-189"><strong>MaximumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="ad8f4-189"><strong>MaximumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="ad8f4-190">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="ad8f4-190">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="ad8f4-191">Non</span><span class="sxs-lookup"><span data-stu-id="ad8f4-191">No</span></span><br/></td>
<td><span data-ttu-id="ad8f4-192">Taille maximale en points à afficher.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-192">The maximum point size to display.</span></span><br/> <br/><span data-ttu-id="ad8f4-193">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="ad8f4-193">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-194">Valeur entière comprise entre 1 et 9999 inclus.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-194">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="ad8f4-195">La valeur par défaut est <strong>9999</strong>.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-195">Default is <strong>9999</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad8f4-196"><strong>MinimumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="ad8f4-196"><strong>MinimumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="ad8f4-197">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="ad8f4-197">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="ad8f4-198">Non</span><span class="sxs-lookup"><span data-stu-id="ad8f4-198">No</span></span><br/></td>
<td><span data-ttu-id="ad8f4-199">Taille minimale du point à afficher.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-199">The minimum point size to display.</span></span><br/> <br/><span data-ttu-id="ad8f4-200">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="ad8f4-200">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-201">Valeur entière comprise entre 1 et 9999 inclus.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-201">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="ad8f4-202">La valeur par défaut est <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-202">Default is <strong>1</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ad8f4-203"><strong>ShowTrueTypeOnly</strong></span><span class="sxs-lookup"><span data-stu-id="ad8f4-203"><strong>ShowTrueTypeOnly</strong></span></span><br/></td>
<td><span data-ttu-id="ad8f4-204">Boolean</span><span class="sxs-lookup"><span data-stu-id="ad8f4-204">Boolean</span></span><br/></td>
<td><span data-ttu-id="ad8f4-205">Non</span><span class="sxs-lookup"><span data-stu-id="ad8f4-205">No</span></span><br/></td>
<td><span data-ttu-id="ad8f4-206">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-206">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="ad8f4-207">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-207">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-208">Affiche uniquement les polices TrueType et OpenType.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-208">Displays TrueType and OpenType fonts only.</span></span> <br/> </dd> <span data-ttu-id="ad8f4-209"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="ad8f4-209"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-210">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-210">Default.</span></span> <span data-ttu-id="ad8f4-211">Aucune restriction n’est placée sur le type de polices affichées.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-211">No restriction is placed on the type of fonts displayed.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad8f4-212"><strong>ShowVerticalFonts</strong></span><span class="sxs-lookup"><span data-stu-id="ad8f4-212"><strong>ShowVerticalFonts</strong></span></span><br/></td>
<td><span data-ttu-id="ad8f4-213">Boolean</span><span class="sxs-lookup"><span data-stu-id="ad8f4-213">Boolean</span></span><br/></td>
<td><span data-ttu-id="ad8f4-214">Non</span><span class="sxs-lookup"><span data-stu-id="ad8f4-214">No</span></span><br/></td>
<td><span data-ttu-id="ad8f4-215">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-215">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ad8f4-216">Les polices verticales sont précédées d’un symbole @ dans la liste des <strong>familles de polices</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-216">Vertical fonts are preceded by an @ symbol in the <strong>Font family</strong> list.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="ad8f4-217">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="ad8f4-217">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-218">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-218">Default.</span></span> <span data-ttu-id="ad8f4-219">Affiche les polices verticales qui sont définies pour s' <strong>Afficher</strong> dans le panneau de configuration <strong>polices</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-219">Displays the vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span> <br/> </dd> <span data-ttu-id="ad8f4-220"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="ad8f4-220"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="ad8f4-221">Permet à une application qui ne prend pas en charge le texte vertical de masquer les polices verticales qui sont définies pour s' <strong>Afficher</strong> dans le panneau de configuration <strong>polices</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-221">Allows an application that does not support vertical text to hide any vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ad8f4-222">Dans Windows Vista, le panneau de configuration des <strong>polices</strong> n’offre pas de fonctionnalité d' <strong>affichage</strong> ou de <strong>masquage</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-222">In Windows Vista, the <strong>Fonts</strong> control panel does not offer <strong>Show</strong> or <strong>Hide</strong> functionality.</span></span> <span data-ttu-id="ad8f4-223">Dans ce cas, l’attribut <em>ShowVerticalFonts</em> doit avoir la valeur <code>False</code> .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-223">In this case, the <em>ShowVerticalFonts</em> attribute must be set to <code>False</code>.</span></span>
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="ad8f4-224">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ad8f4-224">Child elements</span></span>

<span data-ttu-id="ad8f4-225">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-225">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ad8f4-226">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ad8f4-226">Parent elements</span></span>



| <span data-ttu-id="ad8f4-227">Élément</span><span class="sxs-lookup"><span data-stu-id="ad8f4-227">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="ad8f4-228">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="ad8f4-228">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/> |
| [<span data-ttu-id="ad8f4-229">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="ad8f4-229">**Group**</span></span>](windowsribbon-element-group.md)<br/>               |
| [<span data-ttu-id="ad8f4-230">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="ad8f4-230">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="ad8f4-231">Notes</span><span class="sxs-lookup"><span data-stu-id="ad8f4-231">Remarks</span></span>

<span data-ttu-id="ad8f4-232">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-232">Optional.</span></span>

<span data-ttu-id="ad8f4-233">Peut se produire au plus une fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md)ou [**MenuGroup**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-233">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), or [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="ad8f4-234">Les attributs de commande **FontControl** déclarés dans le balisage, tels que [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), sont substitués par les attributs des contrôles individuels qui composent le **FontControl**.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-234">Any **FontControl** Command attributes declared in markup, such as [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), are overridden by the attributes of the individual controls that comprise the **FontControl**.</span></span>

<span data-ttu-id="ad8f4-235">Toute tentative de sélection d’un échantillon de couleur dans le sélecteur de couleurs d’un [contrôle de police](windowsribbon-controls-fontcontrol.md) peut entraîner une violation d’accès si aucun gestionnaire de commandes n’est associé au contrôle.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-235">Any attempt to select a color swatch from the color picker of a [Font Control](windowsribbon-controls-fontcontrol.md) may result in an access violation if no Command handler is associated with the control.</span></span>

## <a name="examples"></a><span data-ttu-id="ad8f4-236">Exemples</span><span class="sxs-lookup"><span data-stu-id="ad8f4-236">Examples</span></span>

<span data-ttu-id="ad8f4-237">L’exemple suivant illustre le balisage de base pour les trois types de [contrôle de police](windowsribbon-controls-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="ad8f4-237">The following example demonstrates the basic markup for the three types of [Font Control](windowsribbon-controls-fontcontrol.md).</span></span>

<span data-ttu-id="ad8f4-238">Cette section de code montre les déclarations de commande **FontControl** , chacune avec une déclaration de conteneur de [**groupe**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-238">This section of code shows the **FontControl** Command declarations, each with a [**Group**](windowsribbon-element-group.md) container declaration.</span></span>


```XML
<!-- A FontOnly FontControl -->
<Command Name="cmdFontOnlyGroup"
         Symbol="cmdFontOnlyGroup"
         Comment="FontOnlyGroup"
         Id="50001"
         LabelTitle="FontOnly"/>
<Command Name="cmdFontOnly"
         Symbol="cmdFontOnly"
         Comment="FontOnly"
         Id="50010"/>

<!-- A FontWithColor FontControl -->
<Command Name="cmdFontWithColorGroup"
         Symbol="cmdFontWithColorGroup"
         Comment="FontWithColorGroup"
         Id="50002"
         LabelTitle="FontWithColor"/>
<Command Name="cmdFontWithColor"
         Symbol="cmdFontWithColor"
         Comment="FontWithColor"
         Id="50020"/>

<!-- A RichFont FontControl -->
<Command Name="cmdRichFontGroup"
         Symbol="cmdRichFontGroup"
         Comment="RichFontGroup"
         Id="50003"
         LabelTitle="RichFont"
         Keytip="ZF"/>
<Command Name="cmdRichFont"
         Symbol="cmdRichFont"
         Comment="RichFont"
         Id="50030"
         Keytip="RF"
         LabelTitle="test"
         TooltipTitle="test"/>
```



<span data-ttu-id="ad8f4-239">Cette section de code montre les déclarations de contrôle **FontControl** où chaque **FontControl** et [**groupe**](windowsribbon-element-group.md) est déclaré dans un seul onglet.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-239">This section of code shows the **FontControl** control declarations where each **FontControl** and [**Group**](windowsribbon-element-group.md) is declared in a single Tab.</span></span>


```XML
<Tab CommandName="cmdTab1">
  <Group CommandName="cmdFontOnlyGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontOnly"
                 FontType="FontOnly"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdFontWithColorGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontWithColor"
                 FontType="FontWithColor"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 IsHighlightButtonVisible="true"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdRichFontGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdRichFont"
                 FontType="RichFont"
                 IsHighlightButtonVisible="true"
                 IsUnderlineButtonVisible="true"
                 IsStrikethroughButtonVisible="true"
                 ShowVerticalFonts="true"
                 MinimumFontSize="15"/>
  </Group>
```



## <a name="element-information"></a><span data-ttu-id="ad8f4-240">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ad8f4-240">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="ad8f4-241">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad8f4-241">Minimum supported system</span></span><br/> | <span data-ttu-id="ad8f4-242">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ad8f4-242">Windows 7</span></span> |
| <span data-ttu-id="ad8f4-243">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="ad8f4-243">Can be empty</span></span>                        | <span data-ttu-id="ad8f4-244">Oui</span><span class="sxs-lookup"><span data-stu-id="ad8f4-244">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="ad8f4-245">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad8f4-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad8f4-246">Contrôle de contrôle de police</span><span class="sxs-lookup"><span data-stu-id="ad8f4-246">Font Control control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="ad8f4-247">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="ad8f4-247">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="ad8f4-248">Exemple FontControl</span><span class="sxs-lookup"><span data-stu-id="ad8f4-248">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





