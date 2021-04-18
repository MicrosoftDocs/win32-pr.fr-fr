---
title: Fichier de définition d’apparence
description: Fichier de définition d’apparence
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- Apparences du lecteur Windows Media, fichiers de définition d’apparence
- apparences, fichiers de définition d’apparence
- fichiers pour les apparences, définition d’apparence
- fichiers de définition d’apparence, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd06708a99a15dc9a8266278850c0507007f058
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512264"
---
# <a name="skin-definition-file"></a><span data-ttu-id="890ad-107">Fichier de définition d’apparence</span><span class="sxs-lookup"><span data-stu-id="890ad-107">Skin Definition File</span></span>

<span data-ttu-id="890ad-108">Les fichiers de définition d’apparence contiennent les instructions de base pour ce que fait l’apparence et où d’autres fichiers utilisés par l’apparence peuvent être trouvés.</span><span class="sxs-lookup"><span data-stu-id="890ad-108">Skin definition files contain the basic instructions for what the skin does and where other files used by the skin can be found.</span></span> <span data-ttu-id="890ad-109">Il ne peut y avoir qu’un seul fichier de définition d’apparence pour une apparence, et il a une extension de nom de fichier. WMS.</span><span class="sxs-lookup"><span data-stu-id="890ad-109">There can only be one skin definition file for a skin, and it has a .wms file name extension.</span></span>

<span data-ttu-id="890ad-110">Les instructions contenues dans le fichier de définition d’apparence sont écrites en Extensible Markup Language (XML), qui est semblable à HTML.</span><span class="sxs-lookup"><span data-stu-id="890ad-110">The instructions in the skin definition file are written in Extensible Markup Language (XML), which is similar to HTML.</span></span> <span data-ttu-id="890ad-111">Si vous avez utilisé du code HTML pour créer des pages Web, vous constaterez que le XML vous semble familier.</span><span class="sxs-lookup"><span data-stu-id="890ad-111">If you have used HTML to create webpages, you will find that XML looks familiar.</span></span>

<span data-ttu-id="890ad-112">Le XML dans le fichier de définition d’apparence utilise un ensemble de balises d’élément spéciales pour définir des parties de l’interface utilisateur de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="890ad-112">The XML in the skin definition file uses a set of special element tags to define parts of the skin user interface.</span></span> <span data-ttu-id="890ad-113">Par exemple, l’élément [Button](button-element.md) définit le comportement d’un bouton, son emplacement et son aspect.</span><span class="sxs-lookup"><span data-stu-id="890ad-113">For example, the [BUTTON](button-element.md) element defines how a button will behave, where it will go, and what it will look like.</span></span>

<span data-ttu-id="890ad-114">Chaque balise d’élément a des attributs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="890ad-114">Each element tag has specific attributes.</span></span> <span data-ttu-id="890ad-115">Par exemple, l’élément [Button](button-element.md) a un attribut **image** qui définit l’emplacement où se trouve l’image du bouton.</span><span class="sxs-lookup"><span data-stu-id="890ad-115">For example, the [BUTTON](button-element.md) element has an **image** attribute that defines where the picture for the button can be found.</span></span> <span data-ttu-id="890ad-116">Cela est similaire au code HTML, où l’élément BODY aura un attribut **bgcolor** qui définit la couleur d’arrière-plan de la page html.</span><span class="sxs-lookup"><span data-stu-id="890ad-116">This is similar to HTML, where the BODY element will have a **bgcolor** attribute that defines the background color of the HTML page.</span></span> <span data-ttu-id="890ad-117">Des informations détaillées sur tous les éléments d’apparence et leurs attributs sont incluses dans la section [référence de programmation](skin-programming-reference.md) de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="890ad-117">Detailed information about all skin elements and their attributes is included in the [Skin Programming Reference](skin-programming-reference.md) section.</span></span>

<span data-ttu-id="890ad-118">XML comporte quelques règles simples que vous devez connaître pour créer des apparences.</span><span class="sxs-lookup"><span data-stu-id="890ad-118">XML has a few simple rules that you need to know to create skins.</span></span> <span data-ttu-id="890ad-119">Contrairement au HTML, XML vous oblige à suivre les règles exactement.</span><span class="sxs-lookup"><span data-stu-id="890ad-119">Unlike HTML, XML requires you to follow the rules exactly.</span></span>

## <a name="enclose-elements-with-angle-brackets"></a><span data-ttu-id="890ad-120">Placer les éléments entre crochets pointus</span><span class="sxs-lookup"><span data-stu-id="890ad-120">Enclose Elements with Angle Brackets</span></span>

<span data-ttu-id="890ad-121">Tous les éléments sont encadrés par des crochets pointus ; par exemple, l’élément **Button** est typé comme suit :</span><span class="sxs-lookup"><span data-stu-id="890ad-121">All elements are enclosed by angle brackets; for example, the **BUTTON** element is typed like this:</span></span>


```C++
<BUTTON>

```



<span data-ttu-id="890ad-122">Vous n’avez pas besoin de taper le mot « BUTTON » en majuscules, mais la Convention de saisie des noms d’élément en majuscules est utilisée dans l’exemple de code de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="890ad-122">You do not need to type the word "BUTTON" in all uppercase letters, but the convention of typing element names in all uppercase is used in the example code of this SDK.</span></span>

## <a name="put-attributes-before-the-closing-bracket"></a><span data-ttu-id="890ad-123">Placer les attributs avant le crochet fermant</span><span class="sxs-lookup"><span data-stu-id="890ad-123">Put Attributes Before the Closing Bracket</span></span>

<span data-ttu-id="890ad-124">Tous les attributs d’un élément particulier doivent être inclus avant le Chevron fermant.</span><span class="sxs-lookup"><span data-stu-id="890ad-124">All attributes for a particular element must be included before the closing angle bracket.</span></span> <span data-ttu-id="890ad-125">Un attribut se compose du nom d’attribut suivi d’un signe égal (=) et de la valeur de l’attribut entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="890ad-125">An attribute consists of the attribute name followed by an equal sign (=) and the value of the attribute in quotes.</span></span>


```C++
<BUTTON image="mypic.jpg">

```



<span data-ttu-id="890ad-126">Vous n’avez pas besoin de taper le mot « image » en minuscules, mais la Convention de saisie des noms d’attribut en minuscules est utilisée dans l’exemple de code de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="890ad-126">You do not need to type the word "image" in lowercase, but the convention of typing attribute names in lowercase is used in the example code of this SDK.</span></span> <span data-ttu-id="890ad-127">Notez également que la valeur de l’attribut est placée entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="890ad-127">Also note that the value of the attribute is enclosed in quotation marks.</span></span>

## <a name="opening-and-closing-elements"></a><span data-ttu-id="890ad-128">Éléments d’ouverture et de fermeture</span><span class="sxs-lookup"><span data-stu-id="890ad-128">Opening and Closing Elements</span></span>

<span data-ttu-id="890ad-129">Certains éléments sont regroupés dans un autre élément.</span><span class="sxs-lookup"><span data-stu-id="890ad-129">Some elements are grouped together inside another element.</span></span> <span data-ttu-id="890ad-130">Par exemple, l’élément **BUTTONGROUP** n’a pas beaucoup de sens, sauf si vous utilisez un ou plusieurs éléments **BUTTONELEMENT** avec celui-ci.</span><span class="sxs-lookup"><span data-stu-id="890ad-130">For example, the **BUTTONGROUP** element does not make a lot of sense unless you use one or more **BUTTONELEMENT** elements with it.</span></span> <span data-ttu-id="890ad-131">Pour que le regroupement soit clair, vous devez disposer d’une balise d’ouverture et de fermeture pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="890ad-131">To make the grouping clear, you need to have an opening and closing tag for each element.</span></span> <span data-ttu-id="890ad-132">La balise d’ouverture est simplement le nom de l’élément et tous les attributs associés, entourés par des crochets pointus.</span><span class="sxs-lookup"><span data-stu-id="890ad-132">The opening tag is just the element name and any related attributes, surrounded by angle brackets.</span></span> <span data-ttu-id="890ad-133">La balise de fermeture est le nom de l’élément, précédé d’une barre oblique (/), puis placé entre crochets pointus.</span><span class="sxs-lookup"><span data-stu-id="890ad-133">The closing tag is the element name, preceded by a forward slash (/), and then enclosed by angle brackets.</span></span> <span data-ttu-id="890ad-134">Par exemple, la balise d’ouverture de l’élément **BUTTONGROUP** se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="890ad-134">For example, the **BUTTONGROUP** element opening tag looks like this:</span></span>


```C++
<BUTTONGROUP>

```



<span data-ttu-id="890ad-135">La balise de fermeture **BUTTONGROUP** ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="890ad-135">The closing **BUTTONGROUP** tag looks like this:</span></span>


```C++
</BUTTONGROUP>

```



<span data-ttu-id="890ad-136">Vous devez placer les balises **BUTTONELEMENT** entre les balises d’élément **BUTTONGROUP** d’ouverture et de fermeture.</span><span class="sxs-lookup"><span data-stu-id="890ad-136">You would put the **BUTTONELEMENT** tags between the opening and closing **BUTTONGROUP** element tags.</span></span> <span data-ttu-id="890ad-137">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="890ad-137">For example:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a><span data-ttu-id="890ad-138">Fermeture des éléments</span><span class="sxs-lookup"><span data-stu-id="890ad-138">Closing Off Elements</span></span>

<span data-ttu-id="890ad-139">Si un élément n’a pas d’autres éléments à l’intérieur de celui-ci, vous devez placer une barre oblique à la fin du nom de l’élément juste avant le crochet pointu fermant.</span><span class="sxs-lookup"><span data-stu-id="890ad-139">If an element has no other elements inside it, you must put a forward slash at the end of the element name just before the closing angle bracket.</span></span> <span data-ttu-id="890ad-140">Par exemple, dans le code ci-dessus, chaque élément **BUTTONELEMENT** a une barre oblique pour indiquer qu’il n’y a pas d’autres éléments imbriqués dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="890ad-140">For example, in the code above, each **BUTTONELEMENT** element has a forward slash to indicate that there are no other elements nested within it.</span></span>

<span data-ttu-id="890ad-141">En d’autres termes, vous devez avoir une balise d’élément de fermeture ou fermer votre élément avec une barre oblique.</span><span class="sxs-lookup"><span data-stu-id="890ad-141">In other words, you must either have a closing element tag or close off your element with a forward slash.</span></span>

<span data-ttu-id="890ad-142">Cette erreur est correcte :</span><span class="sxs-lookup"><span data-stu-id="890ad-142">This is correct:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



<span data-ttu-id="890ad-143">Ce n’est pas correct :</span><span class="sxs-lookup"><span data-stu-id="890ad-143">This is not correct:</span></span>


```C++
<BUTTONGROUP/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



<span data-ttu-id="890ad-144">Cela n’est pas non plus correct :</span><span class="sxs-lookup"><span data-stu-id="890ad-144">This is also not correct:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT>
    <BUTTONELEMENT>
</BUTTONGROUP>

```



<span data-ttu-id="890ad-145">La section suivante fournit plus d’informations sur les fichiers de définition d’apparence :</span><span class="sxs-lookup"><span data-stu-id="890ad-145">The following section provides more information about skin definition files:</span></span>

-   [<span data-ttu-id="890ad-146">Structure du fichier de définition d’apparence</span><span class="sxs-lookup"><span data-stu-id="890ad-146">Skin Definition File Structure</span></span>](skin-definition-file-structure.md)

## <a name="related-topics"></a><span data-ttu-id="890ad-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="890ad-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="890ad-148">**Fichiers d’apparence**</span><span class="sxs-lookup"><span data-stu-id="890ad-148">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




