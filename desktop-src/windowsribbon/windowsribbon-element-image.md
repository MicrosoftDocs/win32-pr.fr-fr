---
title: Élément image (infrastructure de ruban Windows)
description: Représente une image.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Ruban des fenêtres d’élément d’image
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe0b9afb51697d50de9cb80886cf829b90c81262
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442890"
---
# <a name="image-element"></a><span data-ttu-id="0fd52-104">Élément Image</span><span class="sxs-lookup"><span data-stu-id="0fd52-104">Image element</span></span>

<span data-ttu-id="0fd52-105">Représente une image.</span><span class="sxs-lookup"><span data-stu-id="0fd52-105">Represents an image.</span></span>

## <a name="usage"></a><span data-ttu-id="0fd52-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="0fd52-106">Usage</span></span>

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
```

## <a name="attributes"></a><span data-ttu-id="0fd52-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="0fd52-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0fd52-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="0fd52-108">Attribute</span></span></th>
<th><span data-ttu-id="0fd52-109">Type</span><span class="sxs-lookup"><span data-stu-id="0fd52-109">Type</span></span></th>
<th><span data-ttu-id="0fd52-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0fd52-110">Required</span></span></th>
<th><span data-ttu-id="0fd52-111">Description</span><span class="sxs-lookup"><span data-stu-id="0fd52-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0fd52-112"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="0fd52-112"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="0fd52-113">XS : positiveInteger Union XS : String</span><span class="sxs-lookup"><span data-stu-id="0fd52-113">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="0fd52-114">Non</span><span class="sxs-lookup"><span data-stu-id="0fd52-114">No</span></span><br/></td>
<td><span data-ttu-id="0fd52-115">ID de ressource unique.</span><span class="sxs-lookup"><span data-stu-id="0fd52-115">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="0fd52-116">
<dt><span></span><span></span><strong></strong> (Union de XS : positiveInteger et XS : String)</span><span class="sxs-lookup"><span data-stu-id="0fd52-116">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0fd52-117">Valeur entière comprise entre 2 et 59999, inclusive, ou 0X2 et 0xea5f en hexadécimal, inclus.</span><span class="sxs-lookup"><span data-stu-id="0fd52-117">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="0fd52-118">La longueur maximale est de 10 caractères, y compris des zéros non significatifs facultatifs.</span><span class="sxs-lookup"><span data-stu-id="0fd52-118">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0fd52-119"><strong>MinDPI</strong></span><span class="sxs-lookup"><span data-stu-id="0fd52-119"><strong>MinDPI</strong></span></span><br/></td>
<td><span data-ttu-id="0fd52-120">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="0fd52-120">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="0fd52-121">Non</span><span class="sxs-lookup"><span data-stu-id="0fd52-121">No</span></span><br/></td>
<td><span data-ttu-id="0fd52-122"><dt><span></span><span></span><strong></strong> (XS : positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="0fd52-122"><dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="0fd52-123">Toute séquence de chiffres avec une valeur minimale de 96.</span><span class="sxs-lookup"><span data-stu-id="0fd52-123">Any sequence of digits with a minimum value of 96.</span></span> <br/> <span data-ttu-id="0fd52-124">Si MinDPI est omis, la valeur par défaut est 96.</span><span class="sxs-lookup"><span data-stu-id="0fd52-124">If MinDPI is omitted, the default value is 96.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0fd52-125"><strong>Source</strong></span><span class="sxs-lookup"><span data-stu-id="0fd52-125"><strong>Source</strong></span></span><br/></td>
<td><span data-ttu-id="0fd52-126">xs:anyURI</span><span class="sxs-lookup"><span data-stu-id="0fd52-126">xs:anyURI</span></span><br/></td>
<td><span data-ttu-id="0fd52-127">Non</span><span class="sxs-lookup"><span data-stu-id="0fd52-127">No</span></span><br/></td>
<td><span data-ttu-id="0fd52-128"><dt><span></span><span></span><strong></strong> (XS : anyURI)</span><span class="sxs-lookup"><span data-stu-id="0fd52-128"><dt><span></span><span></span><strong></strong> (xs:anyURI)</span></span><br/> </dt> <dd> <span data-ttu-id="0fd52-129">Séquence de caractères qui représente un URI.</span><span class="sxs-lookup"><span data-stu-id="0fd52-129">Any sequence of characters that represents a URI.</span></span> <span data-ttu-id="0fd52-130">La valeur de l’URI est un chemin d’accès absolu ou relatif (au fichier de balisage du ruban) à une ressource image de type BMP.</span><span class="sxs-lookup"><span data-stu-id="0fd52-130">The URI value is an absolute or relative (to the Ribbon markup file) path to an image resource of type BMP.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0fd52-131"><strong>Symbole</strong></span><span class="sxs-lookup"><span data-stu-id="0fd52-131"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="0fd52-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="0fd52-132">xs:string</span></span><br/></td>
<td><span data-ttu-id="0fd52-133">Non</span><span class="sxs-lookup"><span data-stu-id="0fd52-133">No</span></span><br/></td>
<td><span data-ttu-id="0fd52-134">Symbole de ressource pour l’image.</span><span class="sxs-lookup"><span data-stu-id="0fd52-134">The resource symbol for the image.</span></span><br/> <br/><span data-ttu-id="0fd52-135">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="0fd52-135">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0fd52-136">Chaîne composée d’une lettre ou d’un trait de soulignement suivi d’une séquence de lettres, de chiffres ou de traits de soulignement, avec un maximum de 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="0fd52-136">A string composed of a letter or underscore followed by any sequence of letters, digits, or underscores up to a maximum of 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="0fd52-137">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0fd52-137">Child elements</span></span>



| <span data-ttu-id="0fd52-138">Élément</span><span class="sxs-lookup"><span data-stu-id="0fd52-138">Element</span></span>                                                               | <span data-ttu-id="0fd52-139">Description</span><span class="sxs-lookup"><span data-stu-id="0fd52-139">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="0fd52-140">**Image. source**</span><span class="sxs-lookup"><span data-stu-id="0fd52-140">**Image.Source**</span></span>](windowsribbon-element-image-source.md)<br/> | <span data-ttu-id="0fd52-141">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="0fd52-141">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="0fd52-142">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0fd52-142">Parent elements</span></span>



| <span data-ttu-id="0fd52-143">Élément</span><span class="sxs-lookup"><span data-stu-id="0fd52-143">Element</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0fd52-144">**Commande. LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="0fd52-144">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [<span data-ttu-id="0fd52-145">**Commande. LargeImages**</span><span class="sxs-lookup"><span data-stu-id="0fd52-145">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         |
| [<span data-ttu-id="0fd52-146">**Commande. SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="0fd52-146">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [<span data-ttu-id="0fd52-147">**Commande. SmallImages**</span><span class="sxs-lookup"><span data-stu-id="0fd52-147">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a><span data-ttu-id="0fd52-148">Remarques</span><span class="sxs-lookup"><span data-stu-id="0fd52-148">Remarks</span></span>

<span data-ttu-id="0fd52-149">facultatif.</span><span class="sxs-lookup"><span data-stu-id="0fd52-149">Optional.</span></span>

<span data-ttu-id="0fd52-150">Peut se produire une ou plusieurs fois pour chaque élément [**Command. SmallImages**](windowsribbon-element-command-smallimages.md), [**Command. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command. LargeImages**](windowsribbon-element-command-largeimages.md)ou [**Command. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd52-150">May occur one or more times for each [**Command.SmallImages**](windowsribbon-element-command-smallimages.md), [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command.LargeImages**](windowsribbon-element-command-largeimages.md), or [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) element.</span></span>

<span data-ttu-id="0fd52-151">Lorsqu’une collection de ressources d’image conçues pour prendre en charge des paramètres de points par pouce (dpi) spécifiques est fournie à l’infrastructure du ruban via un ensemble d’éléments d' **image** , l’infrastructure utilise l' **image** avec une valeur d’attribut *MinDPI* qui correspond au paramètre PPP d’écran actuel.</span><span class="sxs-lookup"><span data-stu-id="0fd52-151">When a collection of image resources that are designed to support specific screen dots per inch (dpi) settings is supplied to the Ribbon framework through a set of **Image** elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>

<span data-ttu-id="0fd52-152">Si aucun élément **image** n’est déclaré avec une valeur *MinDPI* qui correspond au paramètre PPP d’écran actuel, l’infrastructure sélectionne l' **image** qui a la valeur *MinDPI* la plus proche inférieure au paramètre PPP d’écran actuel et met à l’échelle la ressource d’image.</span><span class="sxs-lookup"><span data-stu-id="0fd52-152">If no **Image** element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="0fd52-153">Sinon, si aucun élément **image** n’est déclaré avec une valeur d’attribut *MinDPI* inférieure au paramètre PPP d’écran actuel, le Framework choisit la valeur *MinDPI* la plus proche supérieure au paramètre PPP d’écran actuel et met à l’échelle la ressource d’image.</span><span class="sxs-lookup"><span data-stu-id="0fd52-153">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

## <a name="examples"></a><span data-ttu-id="0fd52-154">Exemples</span><span class="sxs-lookup"><span data-stu-id="0fd52-154">Examples</span></span>

<span data-ttu-id="0fd52-155">L’exemple de code suivant montre le balisage requis pour déclarer, via un ensemble d’éléments **image** , une collection de ressources d’image conçues pour prendre en charge quatre paramètres de résolution d’écran spécifiques.</span><span class="sxs-lookup"><span data-stu-id="0fd52-155">The following code example shows the markup required to declare, through a set of **Image** elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span>


```XML
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">res/sizeAndColor_96.bmp</Image>
    <Image Id="252" MinDPI="120">res/sizeAndColor_120.bmp</Image>
    <Image Id="253" MinDPI="144">res/sizeAndColor_144.bmp</Image>
    <Image Id="254" MinDPI="192">res/sizeAndColor_192.bmp</Image>
  </Command.LargeImages>
</Command>
```



## <a name="element-information"></a><span data-ttu-id="0fd52-156">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0fd52-156">Element information</span></span>

* <span data-ttu-id="0fd52-157">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="0fd52-157">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="0fd52-158">**Peut être vide**: non</span><span class="sxs-lookup"><span data-stu-id="0fd52-158">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="0fd52-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fd52-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd52-160">Spécification des ressources d’image du ruban</span><span class="sxs-lookup"><span data-stu-id="0fd52-160">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 





