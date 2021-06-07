---
title: Référence du modèle objet VML
description: Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c387935119babc73442e9b8f307672925bdf71d3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444820"
---
# <a name="vml-object-model-reference"></a><span data-ttu-id="9d026-104">Référence du modèle objet VML</span><span class="sxs-lookup"><span data-stu-id="9d026-104">VML Object Model Reference</span></span>

<span data-ttu-id="9d026-105">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9d026-105">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9d026-106">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9d026-106">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9d026-107">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="9d026-107">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9d026-108">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="9d026-108">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9d026-109">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9d026-109">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9d026-110">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9d026-110">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9d026-111">Dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="9d026-111">In this topic:</span></span>

-   [<span data-ttu-id="9d026-112">Introduction</span><span class="sxs-lookup"><span data-stu-id="9d026-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="9d026-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="9d026-113">Example</span></span>](#example)
-   [<span data-ttu-id="9d026-114">Configuration de VML</span><span class="sxs-lookup"><span data-stu-id="9d026-114">Setting up VML</span></span>](#setting-up-vml)
-   [<span data-ttu-id="9d026-115">Informations de référence sur VML OM</span><span class="sxs-lookup"><span data-stu-id="9d026-115">VML OM Reference</span></span>](#vml-om-reference)
    -   [<span data-ttu-id="9d026-116">Élément Shape</span><span class="sxs-lookup"><span data-stu-id="9d026-116">Shape element</span></span>](#shape-element)
-   [<span data-ttu-id="9d026-117">Sous-éléments de l’élément Shape</span><span class="sxs-lookup"><span data-stu-id="9d026-117">Subelements of the Shape Element</span></span>](#subelements-of-the-shape-element)
    -   [<span data-ttu-id="9d026-118">Élément d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="9d026-118">Background element</span></span>](#background-element)
    -   [<span data-ttu-id="9d026-119">Élément extrusion</span><span class="sxs-lookup"><span data-stu-id="9d026-119">Extrusion element</span></span>](#extrusion-element)
    -   [<span data-ttu-id="9d026-120">Fill, élément</span><span class="sxs-lookup"><span data-stu-id="9d026-120">Fill element</span></span>](#fill-element)
    -   [<span data-ttu-id="9d026-121">élément Group</span><span class="sxs-lookup"><span data-stu-id="9d026-121">Group element</span></span>](#group-element)
    -   [<span data-ttu-id="9d026-122">Élément ImageData</span><span class="sxs-lookup"><span data-stu-id="9d026-122">Imagedata element</span></span>](#imagedata-element)
    -   [<span data-ttu-id="9d026-123">Élément Path</span><span class="sxs-lookup"><span data-stu-id="9d026-123">Path element</span></span>](#path-element)
    -   [<span data-ttu-id="9d026-124">Élément Shadow</span><span class="sxs-lookup"><span data-stu-id="9d026-124">Shadow element</span></span>](#shadow-element)
    -   [<span data-ttu-id="9d026-125">Élément Skew</span><span class="sxs-lookup"><span data-stu-id="9d026-125">Skew element</span></span>](#skew-element)
    -   [<span data-ttu-id="9d026-126">Stroke, élément</span><span class="sxs-lookup"><span data-stu-id="9d026-126">Stroke element</span></span>](#stroke-element)
    -   [<span data-ttu-id="9d026-127">Élément TextPath</span><span class="sxs-lookup"><span data-stu-id="9d026-127">TextPath element</span></span>](#textpath-element)
-   [<span data-ttu-id="9d026-128">Types de données utilisés dans le modèle d’objet VML</span><span class="sxs-lookup"><span data-stu-id="9d026-128">Data Types Used in the VML Object Model</span></span>](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a><span data-ttu-id="9d026-129">Introduction</span><span class="sxs-lookup"><span data-stu-id="9d026-129">Introduction</span></span>

<span data-ttu-id="9d026-130">[Langage VML (VML)](https://www.w3.org/TR/NOTE-datetime.html) est un langage textuel qui utilise [XML](https://www.w3.org/TR/REC-xml.mdl) pour étendre le code HTML en vue d’afficher des informations graphiques vectorielles.</span><span class="sxs-lookup"><span data-stu-id="9d026-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) is a text-based language that uses [XML](https://www.w3.org/TR/REC-xml.mdl) to extend HTML for the purpose of displaying vector graphic information.</span></span> <span data-ttu-id="9d026-131">Le Document Object Model VML (DOM) définit une interface de programmation pour la manipulation des éléments de document.</span><span class="sxs-lookup"><span data-stu-id="9d026-131">The VML Document Object Model (DOM) defines a programmatic interface for the manipulation of the document elements.</span></span> <span data-ttu-id="9d026-132">Cela permet à l’utilisateur de créer et de modifier dynamiquement des graphiques vectoriels via une interface de plateforme et une interface indépendante du langage.</span><span class="sxs-lookup"><span data-stu-id="9d026-132">This enables the user to dynamically create and modify vector graphics through a platform- and language-neutral interface.</span></span> <span data-ttu-id="9d026-133">Le DOM VML est conforme à la spécification [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) .</span><span class="sxs-lookup"><span data-stu-id="9d026-133">The VML DOM conforms to the [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specification.</span></span>

<span data-ttu-id="9d026-134">VML utilise l’élément [Shape](#shape-element) comme bloc de construction de base pour les images vectorielles.</span><span class="sxs-lookup"><span data-stu-id="9d026-134">VML uses the [Shape](#shape-element) element as the basic building block for vector graphic images.</span></span> <span data-ttu-id="9d026-135">Une fois qu’une forme est créée, vous pouvez modifier la forme par le biais des attributs ou des sous-éléments attachés.</span><span class="sxs-lookup"><span data-stu-id="9d026-135">Once a shape is created, you can modify the shape through attributes or by attached subelements.</span></span> <span data-ttu-id="9d026-136">Par exemple, pour modifier la couleur d’une forme, assignez une valeur de couleur à l’attribut **FillColor** .</span><span class="sxs-lookup"><span data-stu-id="9d026-136">For example, to change the color of a shape, assign a color value to the **FillColor** attribute.</span></span>


```HTML
myshape.fillcolor = "red"
```



<span data-ttu-id="9d026-137">Plusieurs des attributs d’une forme sont également des sous- [éléments](/windows) et ont leurs propres attributs, y compris les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9d026-137">Several of the attributes of a shape are also [subelements](/windows) and have their own attributes, including the following:</span></span>

-   [<span data-ttu-id="9d026-138">Contexte</span><span class="sxs-lookup"><span data-stu-id="9d026-138">Background</span></span>](#background-element)
-   [<span data-ttu-id="9d026-139">Extrusion</span><span class="sxs-lookup"><span data-stu-id="9d026-139">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="9d026-140">Remplir</span><span class="sxs-lookup"><span data-stu-id="9d026-140">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="9d026-141">Groupe</span><span class="sxs-lookup"><span data-stu-id="9d026-141">Group</span></span>](#group-element)
-   [<span data-ttu-id="9d026-142">Imagedata</span><span class="sxs-lookup"><span data-stu-id="9d026-142">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="9d026-143">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9d026-143">Path</span></span>](#path-element)
-   [<span data-ttu-id="9d026-144">Shadow</span><span class="sxs-lookup"><span data-stu-id="9d026-144">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="9d026-145">Appliquez</span><span class="sxs-lookup"><span data-stu-id="9d026-145">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="9d026-146">Stroke</span><span class="sxs-lookup"><span data-stu-id="9d026-146">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="9d026-147">TextPath</span><span class="sxs-lookup"><span data-stu-id="9d026-147">TextPath</span></span>](#textpath-element)

<span data-ttu-id="9d026-148">VML OM utilise plusieurs [types de données](/windows) pour définir des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9d026-148">The VML OM uses several [data types](/windows) to define parameters.</span></span> <span data-ttu-id="9d026-149">Les types de données précédés de « VG » sont des énumérations et celles précédées de « IVg » sont des objets.</span><span class="sxs-lookup"><span data-stu-id="9d026-149">Datatypes prefixed with "Vg" are enumerations and those prefixed with "IVg" are objects.</span></span> <span data-ttu-id="9d026-150">Cliquez ici pour obtenir une liste.</span><span class="sxs-lookup"><span data-stu-id="9d026-150">Click here for a list.</span></span> <span data-ttu-id="9d026-151">Les types de données mineurs sont répertoriés avec des paramètres spécifiques.</span><span class="sxs-lookup"><span data-stu-id="9d026-151">Minor datatypes are listed with specific parameters.</span></span>

## <a name="example"></a><span data-ttu-id="9d026-152">Exemple</span><span class="sxs-lookup"><span data-stu-id="9d026-152">Example</span></span>

<span data-ttu-id="9d026-153">Le code VBScript suivant montre comment créer une forme simple :</span><span class="sxs-lookup"><span data-stu-id="9d026-153">The following VBScript code shows how to create a simple shape:</span></span>


```HTML
        Set MyRect = Document.CreateElement("v:Rect")
        Set R = MyDiv.AppendChild(MyRect)
        R.Style.Position = "absolute"
        R.Style.Width = 20
        R.Style.Height = 20
        R.Style.Top = 50
        R.Style.Left = 50
        R.FillColor = "red"
```



<span data-ttu-id="9d026-154">Dans l’exemple ci-dessus, une forme est créée à l’aide de la méthode Document Object Model **createElement**.</span><span class="sxs-lookup"><span data-stu-id="9d026-154">In the above example, a shape is created by using the Document Object Model method **CreateElement**.</span></span> <span data-ttu-id="9d026-155">La forme est une forme Rect prédéfinie VML.</span><span class="sxs-lookup"><span data-stu-id="9d026-155">The shape is a VML predefined Rect shape.</span></span> <span data-ttu-id="9d026-156">Même si l’objet existe, il ne peut pas faire partie du document tant qu’il n’est pas attaché au document.</span><span class="sxs-lookup"><span data-stu-id="9d026-156">Even though the object exists, it cannot be part of the document until it is attached to the document.</span></span> <span data-ttu-id="9d026-157">À l’aide de la méthode **AppendChild** , le Rect est devenu l’enfant d’un élément **div** appelé MyDiv.</span><span class="sxs-lookup"><span data-stu-id="9d026-157">Using the **AppendChild** method, the Rect is made a child of a **DIV** element called MyDiv.</span></span> <span data-ttu-id="9d026-158">Quelques attributs de style minimum (**position**, **largeur**, **hauteur**, **haut**, **gauche**) sont définis pour attribuer une taille spécifique à la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-158">A few minimum style attributes (**Position**, **Width**, **Height**, **Top**, **Left**) are set to give the shape a specific size.</span></span> <span data-ttu-id="9d026-159">Enfin, une couleur est assignée avec l’attribut **FillColor** .</span><span class="sxs-lookup"><span data-stu-id="9d026-159">Finally, a color is assigned with the **FillColor** attribute.</span></span> <span data-ttu-id="9d026-160">Notez que vous pouvez utiliser n’importe quel langage de script ou n’importe quel langage pouvant fonctionner avec des interfaces Document Object Model.</span><span class="sxs-lookup"><span data-stu-id="9d026-160">Note that any scripting language or any language that can work with Document Object Model interfaces can be used.</span></span>

## <a name="setting-up-vml"></a><span data-ttu-id="9d026-161">Configuration de VML</span><span class="sxs-lookup"><span data-stu-id="9d026-161">Setting up VML</span></span>

<span data-ttu-id="9d026-162">L’une des implémentations de VML est par le biais de Microsoft Internet Explorer 5,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9d026-162">One implementation of VML is through Microsoft Internet Explorer 5.0 or greater.</span></span> <span data-ttu-id="9d026-163">Pour configurer correctement l’objet de rendu dans une page Web, les ajouts suivants doivent être effectués :</span><span class="sxs-lookup"><span data-stu-id="9d026-163">To set up the rendering object correctly in a Web page, the following additions must be made:</span></span>

1.  <span data-ttu-id="9d026-164">Le schéma doit être configuré dans le</span><span class="sxs-lookup"><span data-stu-id="9d026-164">The schema must be set up in the initial</span></span> <HTML> <span data-ttu-id="9d026-165">comme suit :</span><span class="sxs-lookup"><span data-stu-id="9d026-165">tag as follows:</span></span>
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  <span data-ttu-id="9d026-166">Le comportement de rendu doit faire partie du style du document :</span><span class="sxs-lookup"><span data-stu-id="9d026-166">The rendering behavior must be part of the document's style:</span></span>
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

<span data-ttu-id="9d026-167">L’exemple suivant montre un exemple de page Web HTML configuré correctement pour VML montrant la création dynamique d’une forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-167">The following shows a sample HTML Web page set up correctly for VML showing the dynamic creation of a shape.</span></span>


```HTML
<HTML xmlns:v="urn:schemas-microsoft-com:vml">
<HEAD>
<STYLE>
v\:* { behavior: url(#default#VML); display:inline-block}
</STYLE>
<TITLE>VML Sample</TITLE>
</HEAD>
<BODY>
<DIV id="MyDiv"></DIV>
<SCRIPT ID="MYSCRIPT" LANGUAGE="VBScript">
<!--
Set MyRect = Document.CreateElement("v:Rect")
Set R = MyDiv.AppendChild(MyRect)
R.Style.Position = "absolute"
R.Style.Width = 20
R.Style.Height = 20
R.Style.Top = 50
R.Style.Left = 50
R.FillColor = "red"
-->
</SCRIPT>
</BODY>
</HTML>
```



<span data-ttu-id="9d026-168">Notez que dans les versions bêta, une balise d’objet ActiveX et un style de comportement différent étaient requis.</span><span class="sxs-lookup"><span data-stu-id="9d026-168">Note that in beta versions, an ActiveX object tag and a different behavior style was required.</span></span>

## <a name="vml-om-reference"></a><span data-ttu-id="9d026-169">Informations de référence sur VML OM</span><span class="sxs-lookup"><span data-stu-id="9d026-169">VML OM Reference</span></span>

<span data-ttu-id="9d026-170">Cette référence définit l’élément de [forme](#shape-element) , les sous- [éléments](/windows)et les [types de données](/windows) utilisés par le modèle objet de Vml.</span><span class="sxs-lookup"><span data-stu-id="9d026-170">This reference defines the [Shape](#shape-element) element, [subelements](/windows), and [data types](/windows) that are used by the object model of VML.</span></span>

### <a name="shape-element"></a><span data-ttu-id="9d026-171">Élément Shape</span><span class="sxs-lookup"><span data-stu-id="9d026-171">Shape element</span></span>

<span data-ttu-id="9d026-172">Les formes sont les blocs de construction des images graphiques définies par langage VML (VML).</span><span class="sxs-lookup"><span data-stu-id="9d026-172">Shapes are the building blocks of graphical images defined by Vector Markup Language (VML).</span></span> <span data-ttu-id="9d026-173">La forme est l’élément de niveau supérieur et plusieurs sous-éléments permettent de définir la nature de chaque forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-173">The shape is the top-level element and several subelements help define the nature of each shape.</span></span>

<span data-ttu-id="9d026-174">VML fournit des formes prédéfinies :</span><span class="sxs-lookup"><span data-stu-id="9d026-174">VML provides predefined shapes:</span></span>

<span data-ttu-id="9d026-175">**Attributs de forme**</span><span class="sxs-lookup"><span data-stu-id="9d026-175">**Shape Attributes**</span></span>

-   <span data-ttu-id="9d026-176">**Arc**</span><span class="sxs-lookup"><span data-stu-id="9d026-176">**Arc**</span></span>
-   <span data-ttu-id="9d026-177">**Apprendre**</span><span class="sxs-lookup"><span data-stu-id="9d026-177">**Curve**</span></span>
-   <span data-ttu-id="9d026-178">**Ligne**</span><span class="sxs-lookup"><span data-stu-id="9d026-178">**Line**</span></span>
-   <span data-ttu-id="9d026-179">**Polyligne**</span><span class="sxs-lookup"><span data-stu-id="9d026-179">**PolyLine**</span></span>
-   <span data-ttu-id="9d026-180">**Rect**</span><span class="sxs-lookup"><span data-stu-id="9d026-180">**Rect**</span></span>
-   <span data-ttu-id="9d026-181">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="9d026-181">**RoundRect**</span></span>



|   <span data-ttu-id="9d026-182">Sous-élément</span><span class="sxs-lookup"><span data-stu-id="9d026-182">Subelement</span></span>           |    <span data-ttu-id="9d026-183">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-183">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d026-184">Ajustement</span><span class="sxs-lookup"><span data-stu-id="9d026-184">Adj</span></span>          | <span data-ttu-id="9d026-185">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-185">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span></span> <span data-ttu-id="9d026-186">Liste délimitée par des virgules de nombres qui correspondent aux paramètres des formules de repère qui définissent le chemin d’accès de la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-186">A comma-delimited list of numbers that are the parameters for the guide formulas that define the path of the shape.</span></span> <span data-ttu-id="9d026-187">Les valeurs peuvent être omises pour permettre l’utilisation des valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d026-187">Values may be omitted to allow for using defaults.</span></span> <span data-ttu-id="9d026-188">Il peut y avoir jusqu’à 8 valeurs d’ajustement.</span><span class="sxs-lookup"><span data-stu-id="9d026-188">There can be up to 8 adjustment values.</span></span>                                                                                                   |
| <span data-ttu-id="9d026-189">Alt</span><span class="sxs-lookup"><span data-stu-id="9d026-189">Alt</span></span>          | <span data-ttu-id="9d026-190">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="9d026-190">String.</span></span> <span data-ttu-id="9d026-191">Texte de remplacement associé à Shape.</span><span class="sxs-lookup"><span data-stu-id="9d026-191">Alternative text associated with shape.</span></span> <span data-ttu-id="9d026-192">Utilisé pour l’exploration non graphique.</span><span class="sxs-lookup"><span data-stu-id="9d026-192">Used for non-graphical browsing.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9d026-193">Bouton</span><span class="sxs-lookup"><span data-stu-id="9d026-193">Button</span></span>       | <span data-ttu-id="9d026-194">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-194">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d026-195">Affiche le comportement du bouton sur clic.</span><span class="sxs-lookup"><span data-stu-id="9d026-195">Displays button behavior on click.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9d026-196">BWMode</span><span class="sxs-lookup"><span data-stu-id="9d026-196">BWMode</span></span>       | <span data-ttu-id="9d026-197">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-197">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="9d026-198">Détermine le mode de rendu de la forme en noir et blanc dans les applications, ou lorsqu’elle est imprimée sur des imprimantes noir et blanc.</span><span class="sxs-lookup"><span data-stu-id="9d026-198">Determines how shape will render in black-and-white view in apps or when printed to black-and-white printers.</span></span> <span data-ttu-id="9d026-199">Les valeurs sont les suivantes : **couleur**, **auto**, **nuances de gris**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **noir**, **blanc**, **dédessiné**.</span><span class="sxs-lookup"><span data-stu-id="9d026-199">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="9d026-200">Valeur par défaut : **auto**.</span><span class="sxs-lookup"><span data-stu-id="9d026-200">Default: **Auto**.</span></span> |
| <span data-ttu-id="9d026-201">BWNormal</span><span class="sxs-lookup"><span data-stu-id="9d026-201">BWNormal</span></span>     | <span data-ttu-id="9d026-202">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="9d026-202">VgBlackWhiteMode.</span></span> <span data-ttu-id="9d026-203">Quand BWMode est auto, cette propriété est consultée pour savoir comment afficher la forme en noir et blanc normal.</span><span class="sxs-lookup"><span data-stu-id="9d026-203">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span> <span data-ttu-id="9d026-204">Les valeurs sont les suivantes : **couleur**, **auto**, **nuances de gris**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **noir**, **blanc**, **dédessiné**.</span><span class="sxs-lookup"><span data-stu-id="9d026-204">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="9d026-205">Valeur par défaut : **auto**.</span><span class="sxs-lookup"><span data-stu-id="9d026-205">Default: **Auto**.</span></span>                                                |
| <span data-ttu-id="9d026-206">BWPure</span><span class="sxs-lookup"><span data-stu-id="9d026-206">BWPure</span></span>       | <span data-ttu-id="9d026-207">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="9d026-207">VgBlackWhiteMode.</span></span> <span data-ttu-id="9d026-208">Quand BWMode est auto, cette propriété est consultée pour savoir comment afficher la forme dans les e/s pures.</span><span class="sxs-lookup"><span data-stu-id="9d026-208">When BWMode is Auto, this property is consulted for how to render the shape in pure B/W.</span></span> <span data-ttu-id="9d026-209">Les valeurs sont les suivantes : **couleur**, **auto**, **nuances de gris**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **noir**, **blanc**, **dédessiné**.</span><span class="sxs-lookup"><span data-stu-id="9d026-209">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="9d026-210">Valeur par défaut : **auto**.</span><span class="sxs-lookup"><span data-stu-id="9d026-210">Default: **Auto**.</span></span>                                                              |
| <span data-ttu-id="9d026-211">ChildShapes</span><span class="sxs-lookup"><span data-stu-id="9d026-211">ChildShapes</span></span>  | <span data-ttu-id="9d026-212">IVgGroupShapes.</span><span class="sxs-lookup"><span data-stu-id="9d026-212">IVgGroupShapes.</span></span> <span data-ttu-id="9d026-213">Collection d’autres formes de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="9d026-213">A collection of other shapes in this group.</span></span> <span data-ttu-id="9d026-214">Cette collection prend en charge les méthodes de longueur et d’élément standard.</span><span class="sxs-lookup"><span data-stu-id="9d026-214">This collection supports the standard Length and Item methods.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9d026-215">Chromakey</span><span class="sxs-lookup"><span data-stu-id="9d026-215">Chromakey</span></span>    | <span data-ttu-id="9d026-216">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-216">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9d026-217">Valeur de couleur qui est transparente et qui affiche tout ce qui se trouve derrière la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-217">A color value that will be transparent and show anything behind the shape.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="9d026-218">Control1</span><span class="sxs-lookup"><span data-stu-id="9d026-218">Control1</span></span>     | <span data-ttu-id="9d026-219">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-219">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d026-220">Point de contrôle pour la courbe.</span><span class="sxs-lookup"><span data-stu-id="9d026-220">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9d026-221">Control2</span><span class="sxs-lookup"><span data-stu-id="9d026-221">Control2</span></span>     | <span data-ttu-id="9d026-222">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-222">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d026-223">Point de contrôle pour la courbe.</span><span class="sxs-lookup"><span data-stu-id="9d026-223">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9d026-224">CoordOrigin</span><span class="sxs-lookup"><span data-stu-id="9d026-224">CoordOrigin</span></span>  | <span data-ttu-id="9d026-225">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md) Coordonnées situées dans le coin supérieur gauche du rectangle de conteneur.</span><span class="sxs-lookup"><span data-stu-id="9d026-225">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) The coordinates at the top left corner of the container rectangle.</span></span> <span data-ttu-id="9d026-226">Plage comprise entre 0 et l’infini.</span><span class="sxs-lookup"><span data-stu-id="9d026-226">Range from 0 to infinity.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="9d026-227">CoordSize</span><span class="sxs-lookup"><span data-stu-id="9d026-227">CoordSize</span></span>    | <span data-ttu-id="9d026-228">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-228">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d026-229">Largeur et hauteur de l’espace de coordonnées à l’intérieur du rectangle de référence de cette forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-229">The width and height of the coordinate space inside the reference rectangle of this shape.</span></span> <span data-ttu-id="9d026-230">S’il n’est pas spécifié, il est identique à la largeur et à la hauteur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="9d026-230">If it is not specified, it is the same as the width and height of the rectangle.</span></span> <span data-ttu-id="9d026-231">Plage comprise entre 0 et l’infini.</span><span class="sxs-lookup"><span data-stu-id="9d026-231">Range from 0 to infinity.</span></span> <span data-ttu-id="9d026-232">Valeur par défaut : « 1000, 1000 ».</span><span class="sxs-lookup"><span data-stu-id="9d026-232">Default: "1000,1000".</span></span>                                                                                               |
| <span data-ttu-id="9d026-233">EndAngle</span><span class="sxs-lookup"><span data-stu-id="9d026-233">EndAngle</span></span>     | <span data-ttu-id="9d026-234">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-234">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="9d026-235">Angle de fin de la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-235">End angle of shape.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="9d026-236">Extrusion</span><span class="sxs-lookup"><span data-stu-id="9d026-236">Extrusion</span></span>    | <span data-ttu-id="9d026-237">IVgExtrusion.</span><span class="sxs-lookup"><span data-stu-id="9d026-237">IVgExtrusion.</span></span> <span data-ttu-id="9d026-238">Spécifie la valeur de l’objet d’extrusion pour cette forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-238">Specifies the Extrusion object value for this shape.</span></span> <span data-ttu-id="9d026-239">Pour plus d’informations, consultez l’élément [extrusion](msdn-online-vml-extrusion-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9d026-239">See the [Extrusion](msdn-online-vml-extrusion-element.md) element for details.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="9d026-240">Remplir</span><span class="sxs-lookup"><span data-stu-id="9d026-240">Fill</span></span>         | <span data-ttu-id="9d026-241">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="9d026-241">VgFillFormat.</span></span> <span data-ttu-id="9d026-242">Spécifie la valeur de remplissage de cette forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-242">Specifies the fill value for this shape.</span></span> <span data-ttu-id="9d026-243">Pour plus d’informations, consultez l’élément [Fill](msdn-online-vml-fill-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9d026-243">See the [Fill](msdn-online-vml-fill-element.md) element for more details.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="9d026-244">FillColor</span><span class="sxs-lookup"><span data-stu-id="9d026-244">FillColor</span></span>    | <span data-ttu-id="9d026-245">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-245">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9d026-246">Couleur principale du pinceau à utiliser pour remplir le tracé de cette forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-246">The primary color of the brush to use to fill the path of this shape.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9d026-247">Spécifié</span><span class="sxs-lookup"><span data-stu-id="9d026-247">Filled</span></span>       | <span data-ttu-id="9d026-248">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-248">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d026-249">Si la valeur est true, le chemin d’accès qui définit la forme est rempli.</span><span class="sxs-lookup"><span data-stu-id="9d026-249">If True, the path defining the shape will be filled.</span></span> <span data-ttu-id="9d026-250">Par défaut, il est rempli à l’aide d’une couleur unie, sauf s’il existe un sous-élément Fill qui spécifie des propriétés de remplissage plus complexes.</span><span class="sxs-lookup"><span data-stu-id="9d026-250">By default, it will be filled using a solid color unless there is a Fill subelement that specifies more complex fill properties.</span></span> <span data-ttu-id="9d026-251">Si la valeur est false, le remplissage est transparent.</span><span class="sxs-lookup"><span data-stu-id="9d026-251">If False, the fill is transparent.</span></span>                                                                                                           |
| <span data-ttu-id="9d026-252">Livre</span><span class="sxs-lookup"><span data-stu-id="9d026-252">Flip</span></span>         | <span data-ttu-id="9d026-253">VgFlipOrientation.</span><span class="sxs-lookup"><span data-stu-id="9d026-253">VgFlipOrientation.</span></span> <span data-ttu-id="9d026-254">Les valeurs sont les suivantes : X XY YX</span><span class="sxs-lookup"><span data-stu-id="9d026-254">Values are: X Y XY YX</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="9d026-255">ForceDash</span><span class="sxs-lookup"><span data-stu-id="9d026-255">ForceDash</span></span>    | <span data-ttu-id="9d026-256">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-256">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d026-257">Indique qu’un contour en pointillés doit être rendu lorsqu’il n’y a aucune ligne et aucun remplissage pour une forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-257">Indication that a dashed outline should be rendered when there is no line and no fill for a shape.</span></span> <span data-ttu-id="9d026-258">Ce comportement est généralement utile pour rendre les formes invisibles visibles dans la modification des applications afin qu’elles puissent être sélectionnées et exploitées, par exemple dans une image interactive.</span><span class="sxs-lookup"><span data-stu-id="9d026-258">This behavior is generally useful for making invisible shapes visible in editing applications so they can be selected and operated on, such as in an image map.</span></span>                                                                 |
| <span data-ttu-id="9d026-259">Formules</span><span class="sxs-lookup"><span data-stu-id="9d026-259">Formulas</span></span>     | <span data-ttu-id="9d026-260">IVgFormulas.</span><span class="sxs-lookup"><span data-stu-id="9d026-260">IVgFormulas.</span></span> <span data-ttu-id="9d026-261">Tableau de formules qui définit une forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-261">An array of formulas that defines a shape.</span></span>                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="9d026-262">Du</span><span class="sxs-lookup"><span data-stu-id="9d026-262">From</span></span>         | <span data-ttu-id="9d026-263">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-263">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d026-264">Point de départ de la ligne.</span><span class="sxs-lookup"><span data-stu-id="9d026-264">Starting point of line.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="9d026-265">HRef</span><span class="sxs-lookup"><span data-stu-id="9d026-265">HRef</span></span>         | <span data-ttu-id="9d026-266">[Chaîne](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-266">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-267">URL à laquelle accéder si l’utilisateur clique sur cette forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-267">The URL to jump to if this shape is clicked.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9d026-268">ImageData</span><span class="sxs-lookup"><span data-stu-id="9d026-268">ImageData</span></span>    | <span data-ttu-id="9d026-269">IVgImageData.</span><span class="sxs-lookup"><span data-stu-id="9d026-269">IVgImageData.</span></span> <span data-ttu-id="9d026-270">Informations d’image si la forme est une image.</span><span class="sxs-lookup"><span data-stu-id="9d026-270">Image information if the shape is a picture.</span></span> <span data-ttu-id="9d026-271">Pour plus d’informations, consultez l’élément ImageData.</span><span class="sxs-lookup"><span data-stu-id="9d026-271">See the ImageData element for more information.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9d026-272">OnEd</span><span class="sxs-lookup"><span data-stu-id="9d026-272">OnEd</span></span>         | <span data-ttu-id="9d026-273">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-273">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d026-274">Masque tous les descripteurs à l’exception des poignées en haut à gauche et en bas à droite, comme dans les poignées pour un segment de ligne droite.</span><span class="sxs-lookup"><span data-stu-id="9d026-274">Hides all handles except the top left and bottom right, as in the handles for a straight line segment.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="9d026-275">Opacity</span><span class="sxs-lookup"><span data-stu-id="9d026-275">Opacity</span></span>      | <span data-ttu-id="9d026-276">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-276">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="9d026-277">Opacité de la forme entière.</span><span class="sxs-lookup"><span data-stu-id="9d026-277">The opacity of the entire shape.</span></span> <span data-ttu-id="9d026-278">Nombre compris entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="9d026-278">A number between 0.0 and 1.0.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9d026-279">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9d026-279">Path</span></span>         | <span data-ttu-id="9d026-280">IVgPath.</span><span class="sxs-lookup"><span data-stu-id="9d026-280">IVgPath.</span></span> <span data-ttu-id="9d026-281">Chaîne contenant les commandes qui définissent le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="9d026-281">A string containing the commands that define the path.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9d026-282">Points</span><span class="sxs-lookup"><span data-stu-id="9d026-282">Points</span></span>       | <span data-ttu-id="9d026-283">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-283">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span></span> <span data-ttu-id="9d026-284">Collection de points définissant une forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-284">A collection of points defining a shape.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="9d026-285">Impression</span><span class="sxs-lookup"><span data-stu-id="9d026-285">Print</span></span>        | <span data-ttu-id="9d026-286">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-286">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d026-287">Si la valeur est true, cette forme est destinée à être imprimée.</span><span class="sxs-lookup"><span data-stu-id="9d026-287">If True, this shape is meant to be printed.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9d026-288">Rotation</span><span class="sxs-lookup"><span data-stu-id="9d026-288">Rotation</span></span>     | <span data-ttu-id="9d026-289">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-289">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="9d026-290">Définit la rotation de la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-290">Sets rotation of shape.</span></span> <span data-ttu-id="9d026-291">La valeur est propagée au style de forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-291">Value is propagated to the shape style.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="9d026-292">Scale</span><span class="sxs-lookup"><span data-stu-id="9d026-292">Scale</span></span>        | <span data-ttu-id="9d026-293">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-293">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d026-294">Échelle de la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-294">Scale of shape.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9d026-295">Shadow</span><span class="sxs-lookup"><span data-stu-id="9d026-295">Shadow</span></span>       | <span data-ttu-id="9d026-296">IVgShadow.</span><span class="sxs-lookup"><span data-stu-id="9d026-296">IVgShadow.</span></span> <span data-ttu-id="9d026-297">Spécifie l’ombre de cette forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-297">Specifies the shadow for this shape.</span></span> <span data-ttu-id="9d026-298">Pour plus d’informations, consultez l’élément [Shadow](msdn-online-vml-shadow-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9d026-298">See the [Shadow](msdn-online-vml-shadow-element.md) element for details.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9d026-299">Arborescence</span><span class="sxs-lookup"><span data-stu-id="9d026-299">Spt</span></span>          | <span data-ttu-id="9d026-300">Réservé.</span><span class="sxs-lookup"><span data-stu-id="9d026-300">Reserved.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9d026-301">StartAngle</span><span class="sxs-lookup"><span data-stu-id="9d026-301">StartAngle</span></span>   | <span data-ttu-id="9d026-302">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-302">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="9d026-303">Angle de début de la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-303">Start angle of shape.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9d026-304">Trait</span><span class="sxs-lookup"><span data-stu-id="9d026-304">Stroke</span></span>       | <span data-ttu-id="9d026-305">VgStrokeFormat.</span><span class="sxs-lookup"><span data-stu-id="9d026-305">VgStrokeFormat.</span></span> <span data-ttu-id="9d026-306">Pour plus d’informations, consultez élément Stroke.</span><span class="sxs-lookup"><span data-stu-id="9d026-306">See Stroke element for details.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9d026-307">StrokeColor</span><span class="sxs-lookup"><span data-stu-id="9d026-307">StrokeColor</span></span>  | <span data-ttu-id="9d026-308">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-308">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9d026-309">Couleur principale du pinceau à utiliser pour rayer le tracé de cette forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-309">The primary color of the brush to use to stroke the path of this shape.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="9d026-310">Rayé</span><span class="sxs-lookup"><span data-stu-id="9d026-310">Stroked</span></span>      | <span data-ttu-id="9d026-311">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-311">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d026-312">Si la valeur est true, le chemin d’accès qui définit la forme est rayé.</span><span class="sxs-lookup"><span data-stu-id="9d026-312">If True, the path defining the shape will be stroked.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9d026-313">StrokeWeight</span><span class="sxs-lookup"><span data-stu-id="9d026-313">StrokeWeight</span></span> | <span data-ttu-id="9d026-314">[VGLength](msdn-online-vml-vglength.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-314">[VGLength](msdn-online-vml-vglength.md).</span></span> <span data-ttu-id="9d026-315">Largeur du pinceau à utiliser pour rayer le tracé.</span><span class="sxs-lookup"><span data-stu-id="9d026-315">The width of the brush to use to stroke the path.</span></span> <span data-ttu-id="9d026-316">Les plages sont comprises entre 0 et 1584.</span><span class="sxs-lookup"><span data-stu-id="9d026-316">Ranges between 0 and 1584.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9d026-317">TextPath</span><span class="sxs-lookup"><span data-stu-id="9d026-317">TextPath</span></span>     | <span data-ttu-id="9d026-318">IVgTextPath.</span><span class="sxs-lookup"><span data-stu-id="9d026-318">IVgTextPath.</span></span> <span data-ttu-id="9d026-319">Spécifie l’objet TextPath de la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-319">Specifies the TextPath object of the shape.</span></span> <span data-ttu-id="9d026-320">Pour plus d’informations, consultez l’élément [TextPath](msdn-online-vml-textpath-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9d026-320">See the [TextPath](msdn-online-vml-textpath-element.md) element for more information.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="9d026-321">À</span><span class="sxs-lookup"><span data-stu-id="9d026-321">To</span></span>           | <span data-ttu-id="9d026-322">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-322">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d026-323">Point de terminaison de la ligne.</span><span class="sxs-lookup"><span data-stu-id="9d026-323">End point of line.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9d026-324">Type</span><span class="sxs-lookup"><span data-stu-id="9d026-324">Type</span></span>         | <span data-ttu-id="9d026-325">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="9d026-325">String.</span></span> <span data-ttu-id="9d026-326">Type de forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-326">Type of shape.</span></span>                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a><span data-ttu-id="9d026-327">Sous-éléments de l’élément Shape</span><span class="sxs-lookup"><span data-stu-id="9d026-327">Subelements of the Shape Element</span></span>

<span data-ttu-id="9d026-328">Les sous-éléments suivants font partie du modèle d’objet VML.</span><span class="sxs-lookup"><span data-stu-id="9d026-328">The following subelements are part of the VML object model.</span></span>

-   [<span data-ttu-id="9d026-329">Contexte</span><span class="sxs-lookup"><span data-stu-id="9d026-329">Background</span></span>](#background-element)
-   [<span data-ttu-id="9d026-330">Extrusion</span><span class="sxs-lookup"><span data-stu-id="9d026-330">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="9d026-331">Remplir</span><span class="sxs-lookup"><span data-stu-id="9d026-331">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="9d026-332">Groupe</span><span class="sxs-lookup"><span data-stu-id="9d026-332">Group</span></span>](#group-element)
-   [<span data-ttu-id="9d026-333">Imagedata</span><span class="sxs-lookup"><span data-stu-id="9d026-333">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="9d026-334">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9d026-334">Path</span></span>](#path-element)
-   [<span data-ttu-id="9d026-335">Shadow</span><span class="sxs-lookup"><span data-stu-id="9d026-335">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="9d026-336">Appliquez</span><span class="sxs-lookup"><span data-stu-id="9d026-336">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="9d026-337">Stroke</span><span class="sxs-lookup"><span data-stu-id="9d026-337">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="9d026-338">TextPath</span><span class="sxs-lookup"><span data-stu-id="9d026-338">TextPath</span></span>](#textpath-element)

### <a name="background-element"></a><span data-ttu-id="9d026-339">Élément d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="9d026-339">Background element</span></span>

<span data-ttu-id="9d026-340">Décrit le remplissage de l’arrière-plan d’une page à l’aide des remplissages VML.</span><span class="sxs-lookup"><span data-stu-id="9d026-340">Describes the fill of the background of a page using VML fills.</span></span>


|   <span data-ttu-id="9d026-341">Attribut</span><span class="sxs-lookup"><span data-stu-id="9d026-341">Attribute</span></span>        |   <span data-ttu-id="9d026-342">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-342">Description</span></span>                                                                                                                                                                                      |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d026-343">BWMode</span><span class="sxs-lookup"><span data-stu-id="9d026-343">BWMode</span></span>    | <span data-ttu-id="9d026-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="9d026-345">Détermine la façon dont la forme s’affiche dans une vue en noir et blanc dans des applications ou à l’impression.</span><span class="sxs-lookup"><span data-stu-id="9d026-345">Determines how shape will render in black-and-white view in applications or when printed.</span></span>                                     |
| <span data-ttu-id="9d026-346">BWNormal</span><span class="sxs-lookup"><span data-stu-id="9d026-346">BWNormal</span></span>  | <span data-ttu-id="9d026-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="9d026-348">Quand BWMode est auto, cette propriété est consultée pour savoir comment afficher la forme en noir et blanc normal.</span><span class="sxs-lookup"><span data-stu-id="9d026-348">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span>                        |
| <span data-ttu-id="9d026-349">BWPure</span><span class="sxs-lookup"><span data-stu-id="9d026-349">BWPure</span></span>    | <span data-ttu-id="9d026-350">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-350">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="9d026-351">Quand BWMode est auto, cette propriété est consultée pour savoir comment afficher la forme en noir et blanc pur.</span><span class="sxs-lookup"><span data-stu-id="9d026-351">When BWMode is Auto, this property is consulted for how to render the shape in pure black and white.</span></span>                          |
| <span data-ttu-id="9d026-352">Remplir</span><span class="sxs-lookup"><span data-stu-id="9d026-352">Fill</span></span>      | <span data-ttu-id="9d026-353">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="9d026-353">VgFillFormat.</span></span> <span data-ttu-id="9d026-354">Spécifie le remplissage de cette forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-354">Specifies the fill for this shape.</span></span> <span data-ttu-id="9d026-355">Pour plus d’informations, consultez l’élément [Fill](msdn-online-vml-fill-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9d026-355">See [Fill](msdn-online-vml-fill-element.md) element for more information.</span></span>                                                             |
| <span data-ttu-id="9d026-356">FillColor</span><span class="sxs-lookup"><span data-stu-id="9d026-356">FillColor</span></span> | <span data-ttu-id="9d026-357">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-357">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9d026-358">Couleur principale du pinceau à utiliser pour remplir le tracé de cette forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-358">The primary color of the brush to use to fill the path of this shape.</span></span> <span data-ttu-id="9d026-359">Doublon de la valeur de couleur dans l’élément Fill.</span><span class="sxs-lookup"><span data-stu-id="9d026-359">Duplicate of the Color value in the Fill element.</span></span> <span data-ttu-id="9d026-360">La valeur par défaut est blanc.</span><span class="sxs-lookup"><span data-stu-id="9d026-360">The default is white.</span></span> |



 

### <a name="extrusion-element"></a><span data-ttu-id="9d026-361">Élément extrusion</span><span class="sxs-lookup"><span data-stu-id="9d026-361">Extrusion element</span></span>

<span data-ttu-id="9d026-362">Décrit une extrusion 3D de la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-362">Describes a 3-D extrusion of the shape.</span></span>

<span data-ttu-id="9d026-363">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="9d026-363">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-364">AutoRotationCenter</span><span class="sxs-lookup"><span data-stu-id="9d026-364">AutoRotationCenter</span></span></td>
<td><span data-ttu-id="9d026-365"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-365"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d026-366">Si la valeur est true, le centre de rotation du groupe d’objets 3D (en fait, il n’y a qu’un seul objet dans le groupe) est déterminé automatiquement comme étant le centre du groupe ; dans le cas contraire, il est déterminé par les paramètres RotationCenter, qui sont une fraction de la forme avec 0, 0, le centre.</span><span class="sxs-lookup"><span data-stu-id="9d026-366">If True, the center of rotation of the group of 3-D objects (in fact there is only ever one object in the group) is determined automatically to be the center of the group; otherwise it is determined by the RotationCenter parameters, which are a fraction of the shape with 0,0,0 being the center.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-367">Profondeur</span><span class="sxs-lookup"><span data-stu-id="9d026-367">BackDepth</span></span></td>
<td><span data-ttu-id="9d026-368"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-368"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span></span> <span data-ttu-id="9d026-369">Quantité d’extrusion vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="9d026-369">Amount of backward extrusion.</span></span> <span data-ttu-id="9d026-370">Est compris entre 0 et 32767.</span><span class="sxs-lookup"><span data-stu-id="9d026-370">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-371">Luminosité</span><span class="sxs-lookup"><span data-stu-id="9d026-371">Brightness</span></span></td>
<td><span data-ttu-id="9d026-372"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-372"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="9d026-373">Luminosité globale de la scène.</span><span class="sxs-lookup"><span data-stu-id="9d026-373">Overall brightness of the scene.</span></span> <span data-ttu-id="9d026-374">La valeur par défaut est &quot; 20 000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d026-374">Default is &quot;20,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-375">Couleur</span><span class="sxs-lookup"><span data-stu-id="9d026-375">Color</span></span></td>
<td><span data-ttu-id="9d026-376"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-376"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="9d026-377">Couleur de l’extrusion.</span><span class="sxs-lookup"><span data-stu-id="9d026-377">The color of the extrusion.</span></span> <span data-ttu-id="9d026-378">Utilisé uniquement si ColorMode est personnalisé.</span><span class="sxs-lookup"><span data-stu-id="9d026-378">Only used if ColorMode is Custom.</span></span> <span data-ttu-id="9d026-379">Dans le cas contraire, définit automatiquement la couleur de l’effet d’extrusion sur la même valeur que FillColor.</span><span class="sxs-lookup"><span data-stu-id="9d026-379">Otherwise, Auto sets the extrusion effect color to the same as FillColor.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-380">ColorMode</span><span class="sxs-lookup"><span data-stu-id="9d026-380">ColorMode</span></span></td>
<td><span data-ttu-id="9d026-381">Vg3DColorMode.</span><span class="sxs-lookup"><span data-stu-id="9d026-381">Vg3DColorMode.</span></span> <span data-ttu-id="9d026-382">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-382">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-383">Auto (par défaut)</span><span class="sxs-lookup"><span data-stu-id="9d026-383">Auto (default)</span></span></li>
<li><span data-ttu-id="9d026-384">Custom</span><span class="sxs-lookup"><span data-stu-id="9d026-384">Custom</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-385">Diffusion</span><span class="sxs-lookup"><span data-stu-id="9d026-385">Diffusity</span></span></td>
<td><span data-ttu-id="9d026-386"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-386"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="9d026-387">Rapport entre l’incident et la lumière diffuse.</span><span class="sxs-lookup"><span data-stu-id="9d026-387">The ratio of incident to diffusely reflected light.</span></span> <span data-ttu-id="9d026-388">Les valeurs inférieures à 1,0 sont normales, mais les valeurs supérieures à un peuvent générer des effets intéressants.</span><span class="sxs-lookup"><span data-stu-id="9d026-388">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-389">Edge</span><span class="sxs-lookup"><span data-stu-id="9d026-389">Edge</span></span></td>
<td><span data-ttu-id="9d026-390"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-390"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="9d026-391">Définit la taille d’un bord biseauté arrondi simulé.</span><span class="sxs-lookup"><span data-stu-id="9d026-391">Sets the size of a simulated rounded beveled edge.</span></span> <span data-ttu-id="9d026-392">Est compris entre 0 et 32767 dans la valeur de type virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="9d026-392">Ranges from 0 to 32767 in floating point pts.</span></span> <span data-ttu-id="9d026-393">La valeur par défaut est &quot; 1PT &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d026-393">Default is &quot;1pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-394">Facette</span><span class="sxs-lookup"><span data-stu-id="9d026-394">Facet</span></span></td>
<td><span data-ttu-id="9d026-395"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-395"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="9d026-396">Définit la facette de la scène.</span><span class="sxs-lookup"><span data-stu-id="9d026-396">Sets the facet of the scene.</span></span> <span data-ttu-id="9d026-397">La valeur par défaut est &quot; 30 000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d026-397">Default is &quot;30,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-398">ForeDepth</span><span class="sxs-lookup"><span data-stu-id="9d026-398">ForeDepth</span></span></td>
<td><span data-ttu-id="9d026-399"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-399"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="9d026-400">Quantité d’extrusion vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="9d026-400">Amount of forward extrusion.</span></span> <span data-ttu-id="9d026-401">Est compris entre 0 et 32767.</span><span class="sxs-lookup"><span data-stu-id="9d026-401">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-402">LightFace</span><span class="sxs-lookup"><span data-stu-id="9d026-402">LightFace</span></span></td>
<td><span data-ttu-id="9d026-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d026-404">Determimes si la face avant de l’objet répond aux modifications de l’éclairage 3D, par exemple quand un objet pivote.</span><span class="sxs-lookup"><span data-stu-id="9d026-404">Determimes whether the front face of the object will respond to changes in the 3-D lighting, e.g., when an object rotates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-405">LightHarsh</span><span class="sxs-lookup"><span data-stu-id="9d026-405">LightHarsh</span></span></td>
<td><span data-ttu-id="9d026-406"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-406"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d026-407">Éclairage sévère de la source de lumière principale.</span><span class="sxs-lookup"><span data-stu-id="9d026-407">Harsh lighting for the primary light source.</span></span> <span data-ttu-id="9d026-408">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="9d026-408">Default is False.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-409">LightHarsh2</span><span class="sxs-lookup"><span data-stu-id="9d026-409">LightHarsh2</span></span></td>
<td><span data-ttu-id="9d026-410"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-410"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d026-411">Éclairage sévère de la source de lumière secondaire.</span><span class="sxs-lookup"><span data-stu-id="9d026-411">Harsh lighting for the secondary light source.</span></span> <span data-ttu-id="9d026-412">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="9d026-412">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-413">LightLevel</span><span class="sxs-lookup"><span data-stu-id="9d026-413">LightLevel</span></span></td>
<td><span data-ttu-id="9d026-414"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-414"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="9d026-415">Intensité de la source de lumière principale.</span><span class="sxs-lookup"><span data-stu-id="9d026-415">Intensity of the primary light source.</span></span> <span data-ttu-id="9d026-416">La valeur par défaut est &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d026-416">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-417">LightLevel2</span><span class="sxs-lookup"><span data-stu-id="9d026-417">LightLevel2</span></span></td>
<td><span data-ttu-id="9d026-418"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-418"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="9d026-419">Intensité de la source de lumière secondaire.</span><span class="sxs-lookup"><span data-stu-id="9d026-419">Intensity of the secondary light source.</span></span> <span data-ttu-id="9d026-420">La valeur par défaut est &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d026-420">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-421">LightPosition</span><span class="sxs-lookup"><span data-stu-id="9d026-421">LightPosition</span></span></td>
<td><span data-ttu-id="9d026-422">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="9d026-422">Vector3D.</span></span> <span data-ttu-id="9d026-423">Position de la source de lumière principale.</span><span class="sxs-lookup"><span data-stu-id="9d026-423">Position of the primary light source.</span></span> <span data-ttu-id="9d026-424">La valeur par défaut est &quot; 50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d026-424">Default is &quot;50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-425">LightPosition2</span><span class="sxs-lookup"><span data-stu-id="9d026-425">LightPosition2</span></span></td>
<td><span data-ttu-id="9d026-426">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="9d026-426">Vector3D.</span></span> <span data-ttu-id="9d026-427">Position de la source de lumière secondaire.</span><span class="sxs-lookup"><span data-stu-id="9d026-427">Position of the secondary light source.</span></span> <span data-ttu-id="9d026-428">La valeur par défaut est &quot; -50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d026-428">Default is &quot;-50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-429">LockRotationCenter</span><span class="sxs-lookup"><span data-stu-id="9d026-429">LockRotationCenter</span></span></td>
<td><span data-ttu-id="9d026-430"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-430"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d026-431">&quot;Lockrotationcenter &quot; signifie que la rotation du groupe est définie par l’angle de rotation [1] degrés autour de l’axe y sur la page suivie de l’angle de rotation [0] degrés sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="9d026-431">&quot;Lockrotationcenter&quot; means that the rotation of the group is defined to be by rotation-angle[1] degrees about the y-axis on the page followed by rotation-angle[0] degrees about the x-axis.</span></span> <span data-ttu-id="9d026-432">Quand LockRotationCenter a la valeur false, la rotation est définie en tant que degrés d’orientation-angle sur le vecteur défini par l’orientation.</span><span class="sxs-lookup"><span data-stu-id="9d026-432">When LockRotationCenter is False, the rotation is defined to be by orientation-angle degrees about the vector defined by orientation.</span></span> <span data-ttu-id="9d026-433">Par exemple, lockrotationcenter = false OrientationAngle = 45 orientation = (0, 1, 0) équivaut à lockrotationcenter = true RotationAngle = (0, 45).</span><span class="sxs-lookup"><span data-stu-id="9d026-433">So, for example, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) is equivalent to lockrotationcenter=true rotationangle=(0,45).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-434">Métallique</span><span class="sxs-lookup"><span data-stu-id="9d026-434">Metal</span></span></td>
<td><span data-ttu-id="9d026-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d026-436">Fait en sorte que la lumière réfléchie modèle éclairé soit la couleur matérielle au lieu de la couleur de la source de lumière, ce qui rend l’objet plus métallique.</span><span class="sxs-lookup"><span data-stu-id="9d026-436">Causes specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-437">Activé</span><span class="sxs-lookup"><span data-stu-id="9d026-437">On</span></span></td>
<td><span data-ttu-id="9d026-438"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-438"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d026-439">Active et désactive l’affichage de l’effet de l’extrusion.</span><span class="sxs-lookup"><span data-stu-id="9d026-439">Turns the display of the extrusion effect on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-440">Orientation</span><span class="sxs-lookup"><span data-stu-id="9d026-440">Orientation</span></span></td>
<td><span data-ttu-id="9d026-441">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="9d026-441">Vector3D.</span></span> <span data-ttu-id="9d026-442">Orientation de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="9d026-442">Orientation of the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-443">OrientationAngle</span><span class="sxs-lookup"><span data-stu-id="9d026-443">OrientationAngle</span></span></td>
<td><span data-ttu-id="9d026-444"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-444"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="9d026-445">Angle entre l’orientation de l’appareil photo et le plan XY.</span><span class="sxs-lookup"><span data-stu-id="9d026-445">Angle between the orientation of the camera and the xy plane.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-446">Verticale</span><span class="sxs-lookup"><span data-stu-id="9d026-446">Plane</span></span></td>
<td><span data-ttu-id="9d026-447">Vg3DExtrudePlane.</span><span class="sxs-lookup"><span data-stu-id="9d026-447">Vg3DExtrudePlane.</span></span> <span data-ttu-id="9d026-448">Autorise l’extrusion des plans orthogonals au plan de l’écran.</span><span class="sxs-lookup"><span data-stu-id="9d026-448">Allows extrusion from planes orthogonal to the screen plane.</span></span> <span data-ttu-id="9d026-449">Requiert la spécification de ForeDepth et de l’effet de profondeur pour les unités de dessin au lieu de EMU.</span><span class="sxs-lookup"><span data-stu-id="9d026-449">Requires ForeDepth and BackDepth to be specified in drawing units instead of emus.</span></span> <span data-ttu-id="9d026-450">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-450">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-451">XY</span><span class="sxs-lookup"><span data-stu-id="9d026-451">XY</span></span></li>
<li><span data-ttu-id="9d026-452">ZX</span><span class="sxs-lookup"><span data-stu-id="9d026-452">ZX</span></span></li>
<li><span data-ttu-id="9d026-453">YZ</span><span class="sxs-lookup"><span data-stu-id="9d026-453">YZ</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-454">Rendu</span><span class="sxs-lookup"><span data-stu-id="9d026-454">Render</span></span></td>
<td><span data-ttu-id="9d026-455">Vg3DRenderMode.</span><span class="sxs-lookup"><span data-stu-id="9d026-455">Vg3DRenderMode.</span></span> <span data-ttu-id="9d026-456">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-456">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-457">Unie (par défaut)</span><span class="sxs-lookup"><span data-stu-id="9d026-457">Solid (default)</span></span></li>
<li><span data-ttu-id="9d026-458">WireFrame</span><span class="sxs-lookup"><span data-stu-id="9d026-458">WireFrame</span></span></li>
<li><span data-ttu-id="9d026-459">BoundingCube</span><span class="sxs-lookup"><span data-stu-id="9d026-459">BoundingCube</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-460">RotationAngle</span><span class="sxs-lookup"><span data-stu-id="9d026-460">RotationAngle</span></span></td>
<td><span data-ttu-id="9d026-461"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-461"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d026-462">AngleX, AngleY ou AngleZ est contrôlé par l’attribut ShapeRotation.</span><span class="sxs-lookup"><span data-stu-id="9d026-462">AngleX, AngleY, or AngleZ is controlled by the ShapeRotation attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-463">RotationCenter</span><span class="sxs-lookup"><span data-stu-id="9d026-463">RotationCenter</span></span></td>
<td><span data-ttu-id="9d026-464">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="9d026-464">Vector3D.</span></span> <span data-ttu-id="9d026-465">Centre de rotation.</span><span class="sxs-lookup"><span data-stu-id="9d026-465">Center of rotation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-466">Éclat</span><span class="sxs-lookup"><span data-stu-id="9d026-466">Shininess</span></span></td>
<td><span data-ttu-id="9d026-467"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-467"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="9d026-468">Détermine la façon dont la réflexion spéculaire concentrée ou répartie est.</span><span class="sxs-lookup"><span data-stu-id="9d026-468">Determines how concentrated or spread out specular reflection is.</span></span> <span data-ttu-id="9d026-469">Une valeur élevée est comprendra de 8 à 10 et se traduirait par un miroir, et une valeur basse serait de 2 à 3 et sequinedrait des vêtements de ré.</span><span class="sxs-lookup"><span data-stu-id="9d026-469">A high value would be 8 to 10 and would approximate a mirror, and a low value would be 2 to 3 and would approximate sequined clothing.</span></span> <span data-ttu-id="9d026-470">Les valeurs 3 à 7 sont recommandées.</span><span class="sxs-lookup"><span data-stu-id="9d026-470">Values of 3 to 7 are recommended.</span></span> <span data-ttu-id="9d026-471">Des valeurs élevées reflètent les sources de lumière de repérage.</span><span class="sxs-lookup"><span data-stu-id="9d026-471">High values will reflect pinpoint light sources.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-472">SkewAmt</span><span class="sxs-lookup"><span data-stu-id="9d026-472">SkewAmt</span></span></td>
<td><span data-ttu-id="9d026-473"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-473"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span></span> <span data-ttu-id="9d026-474">Si le type est Parallel, l’attribut détermine la quantité d’inclinaison.</span><span class="sxs-lookup"><span data-stu-id="9d026-474">If Type is Parallel, attribute determines the amount of skew.</span></span> <span data-ttu-id="9d026-475">Est compris entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="9d026-475">Ranges from 0 to 100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-476">SkewAngle</span><span class="sxs-lookup"><span data-stu-id="9d026-476">SkewAngle</span></span></td>
<td><span data-ttu-id="9d026-477"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-477"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="9d026-478">Si le type est Parallel, l’attribut détermine le degré d’inclinaison.</span><span class="sxs-lookup"><span data-stu-id="9d026-478">If Type is Parallel, attribute determines the degree of skew.</span></span> <span data-ttu-id="9d026-479">La valeur par défaut est &quot; -45 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d026-479">Default is &quot;-45&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-480">Specularity</span><span class="sxs-lookup"><span data-stu-id="9d026-480">Specularity</span></span></td>
<td><span data-ttu-id="9d026-481"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-481"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="9d026-482">Rapport entre l’incident et le modèle éclairé de lumière réfléchie.</span><span class="sxs-lookup"><span data-stu-id="9d026-482">The ratio of incident to specularly reflected light.</span></span> <span data-ttu-id="9d026-483">Les valeurs inférieures à 1,0 sont normales, mais les valeurs supérieures à un peuvent générer des effets intéressants.</span><span class="sxs-lookup"><span data-stu-id="9d026-483">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-484">Type</span><span class="sxs-lookup"><span data-stu-id="9d026-484">Type</span></span></td>
<td><span data-ttu-id="9d026-485">VgExtrusionType.</span><span class="sxs-lookup"><span data-stu-id="9d026-485">VgExtrusionType.</span></span> <span data-ttu-id="9d026-486">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-486">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-487">Parallèle (par défaut)</span><span class="sxs-lookup"><span data-stu-id="9d026-487">Parallel (default)</span></span></li>
<li><span data-ttu-id="9d026-488">Perspective</span><span class="sxs-lookup"><span data-stu-id="9d026-488">Perspective</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-489">Point</span><span class="sxs-lookup"><span data-stu-id="9d026-489">Viewpoint</span></span></td>
<td><span data-ttu-id="9d026-490">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="9d026-490">Vector3D.</span></span> <span data-ttu-id="9d026-491">Point à partir duquel la scène est affichée.</span><span class="sxs-lookup"><span data-stu-id="9d026-491">The point where the scene is being viewed from.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-492">ViewpointOrigin</span><span class="sxs-lookup"><span data-stu-id="9d026-492">ViewpointOrigin</span></span></td>
<td><span data-ttu-id="9d026-493"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-493"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d026-494">Peut avoir des valeurs comprises entre 0,5 et-0,5 pour positionner l’origine du point de vue dans le cadre englobant de la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-494">Can have values from 0.5 to -0.5 to position the origin of the viewpoint within the shape bounding box.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a><span data-ttu-id="9d026-495">Fill, élément</span><span class="sxs-lookup"><span data-stu-id="9d026-495">Fill element</span></span>

<span data-ttu-id="9d026-496">Décrit comment remplir un tracé pour obtenir des remplissages plus complexes qu’une couleur unie.</span><span class="sxs-lookup"><span data-stu-id="9d026-496">Describes how a path should be filled for fills more complex than a solid color.</span></span>

<span data-ttu-id="9d026-497">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="9d026-497">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-498">AlignShape</span><span class="sxs-lookup"><span data-stu-id="9d026-498">AlignShape</span></span></td>
<td><span data-ttu-id="9d026-499"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-499"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d026-500">Alignez l’image avec la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-500">Align the image with the shape.</span></span> <span data-ttu-id="9d026-501">Si la valeur est false, l’image est alignée avec la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9d026-501">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-502">Angle</span><span class="sxs-lookup"><span data-stu-id="9d026-502">Angle</span></span></td>
<td><span data-ttu-id="9d026-503"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-503"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="9d026-504">Angle de rotation du dégradé.</span><span class="sxs-lookup"><span data-stu-id="9d026-504">The angle along which the gradient goes.</span></span> <span data-ttu-id="9d026-505">0 degré est le long de l’axe horizontal de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="9d026-505">0 degrees is along the horizontal axis from left to right.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-506">Aspect</span><span class="sxs-lookup"><span data-stu-id="9d026-506">Aspect</span></span></td>
<td><span data-ttu-id="9d026-507"><strong>VgAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-507"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="9d026-508">L’attribut ImageSize est ajusté pour conserver l’aspect de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-508">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="9d026-509">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="9d026-509">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d026-510">Value</span><span class="sxs-lookup"><span data-stu-id="9d026-510">Value</span></span></th>
<th><span data-ttu-id="9d026-511">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-511">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-512">Ignorer</span><span class="sxs-lookup"><span data-stu-id="9d026-512">Ignore</span></span></td>
<td><span data-ttu-id="9d026-513">Ignorer les problèmes d’aspect.</span><span class="sxs-lookup"><span data-stu-id="9d026-513">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-514">Au moins</span><span class="sxs-lookup"><span data-stu-id="9d026-514">AtLeast</span></span></td>
<td><span data-ttu-id="9d026-515">L’image est au moins aussi grande que la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-515">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-516">AtMost</span><span class="sxs-lookup"><span data-stu-id="9d026-516">AtMost</span></span></td>
<td><span data-ttu-id="9d026-517">L’image n’est pas plus grande que la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-517">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-518">Couleur</span><span class="sxs-lookup"><span data-stu-id="9d026-518">Color</span></span></td>
<td><span data-ttu-id="9d026-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> Couleur de remplissage principale.</span><span class="sxs-lookup"><span data-stu-id="9d026-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> The main fill color.</span></span> <span data-ttu-id="9d026-520">Identique à l’attribut FillColor dans Shape.</span><span class="sxs-lookup"><span data-stu-id="9d026-520">Same as FillColor attribute in shape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-521">Couleur2</span><span class="sxs-lookup"><span data-stu-id="9d026-521">Color2</span></span></td>
<td><span data-ttu-id="9d026-522"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-522"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="9d026-523">Couleur secondaire d’un remplissage lorsque le type d’image est Pattern ou un remplissage dégradé.</span><span class="sxs-lookup"><span data-stu-id="9d026-523">The secondary color for a fill when image type is Pattern or a gradient fill.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-524">Couleurs</span><span class="sxs-lookup"><span data-stu-id="9d026-524">Colors</span></span></td>
<td><span data-ttu-id="9d026-525"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-525"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span></span> <span data-ttu-id="9d026-526">Les couleurs intermédiaires dans le dégradé et leurs positions relatives le long du dégradé, par exemple &quot; 30% de rouge, 70% bleu, 90% vert &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d026-526">Intermediate colors in the gradient and their relative positions along the gradient, e.g., &quot;30% red, 70% blue, 90% green&quot;.</span></span> <span data-ttu-id="9d026-527">La couleur primaire (attribut Color dans Shape) est 0% et la couleur secondaire (attribut Color2) est 100%.</span><span class="sxs-lookup"><span data-stu-id="9d026-527">Primary color (Color attribute in shape) is 0% and secondary color (Color2 attribute) is 100%.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-528">Priorité</span><span class="sxs-lookup"><span data-stu-id="9d026-528">Focus</span></span></td>
<td><span data-ttu-id="9d026-529"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-529"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span></span> <span data-ttu-id="9d026-530">Point focal pour le remplissage dégradé linéaire.</span><span class="sxs-lookup"><span data-stu-id="9d026-530">Focal point for linear gradient fill.</span></span> <span data-ttu-id="9d026-531">Les valeurs sont comprises entre-100 et + 100.</span><span class="sxs-lookup"><span data-stu-id="9d026-531">Values go from -100 to +100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-532">FocusPosition</span><span class="sxs-lookup"><span data-stu-id="9d026-532">FocusPosition</span></span></td>
<td><span data-ttu-id="9d026-533"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-533"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d026-534">Position du rectangle le plus profond pour les dégradés radiaux.</span><span class="sxs-lookup"><span data-stu-id="9d026-534">Position of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="9d026-535">Le vecteur est une fraction (0,0-1,0) de la largeur et de la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-535">The vector is a fraction (0.0 - 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-536">FocusSize</span><span class="sxs-lookup"><span data-stu-id="9d026-536">FocusSize</span></span></td>
<td><span data-ttu-id="9d026-537"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a> Taille du rectangle le plus profond pour les dégradés radiaux.</span><span class="sxs-lookup"><span data-stu-id="9d026-537"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Size of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="9d026-538">Le vecteur est une fraction (0,0 à 1,0) de la largeur et de la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-538">The vector is a fraction (0.0 to 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-539">Méthode</span><span class="sxs-lookup"><span data-stu-id="9d026-539">Method</span></span></td>
<td><span data-ttu-id="9d026-540">VgSigmaType.</span><span class="sxs-lookup"><span data-stu-id="9d026-540">VgSigmaType.</span></span> <span data-ttu-id="9d026-541">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="9d026-541">Values include:</span></span>
<ul>
<li><span data-ttu-id="9d026-542">Aucun</span><span class="sxs-lookup"><span data-stu-id="9d026-542">None</span></span></li>
<li><span data-ttu-id="9d026-543">Linéaire</span><span class="sxs-lookup"><span data-stu-id="9d026-543">Linear</span></span></li>
<li><span data-ttu-id="9d026-544">Sigma</span><span class="sxs-lookup"><span data-stu-id="9d026-544">Sigma</span></span></li>
<li><span data-ttu-id="9d026-545">Quelconque</span><span class="sxs-lookup"><span data-stu-id="9d026-545">Any</span></span></li>
</ul>
<p><span data-ttu-id="9d026-546">La valeur par défaut est Sigma.</span><span class="sxs-lookup"><span data-stu-id="9d026-546">Default is Sigma.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-547">Activé</span><span class="sxs-lookup"><span data-stu-id="9d026-547">On</span></span></td>
<td><span data-ttu-id="9d026-548"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-548"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d026-549">Active l’affichage du remplissage.</span><span class="sxs-lookup"><span data-stu-id="9d026-549">Turns fill display on.</span></span> <span data-ttu-id="9d026-550">Identique à l’attribut Fill dans Shape.</span><span class="sxs-lookup"><span data-stu-id="9d026-550">Same as Fill attribute in shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-551">Opacity</span><span class="sxs-lookup"><span data-stu-id="9d026-551">Opacity</span></span></td>
<td><span data-ttu-id="9d026-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="9d026-553">Opacité du remplissage.</span><span class="sxs-lookup"><span data-stu-id="9d026-553">Opacity of the fill.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-554">Opacity2</span><span class="sxs-lookup"><span data-stu-id="9d026-554">Opacity2</span></span></td>
<td><span data-ttu-id="9d026-555"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-555"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="9d026-556">Opacité secondaire pour les dégradés.</span><span class="sxs-lookup"><span data-stu-id="9d026-556">The secondary opacity for gradients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-557">Origine</span><span class="sxs-lookup"><span data-stu-id="9d026-557">Origin</span></span></td>
<td><span data-ttu-id="9d026-558"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-558"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d026-559">Point relatif au coin supérieur gauche de l’image qui est traité comme l’origine de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-559">Point relative to upper left corner of the image that is treated as the origin of the image.</span></span> <span data-ttu-id="9d026-560">La valeur par défaut est le centre de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-560">Default is the center of the image.</span></span> <span data-ttu-id="9d026-561">Le vecteur est une fraction (de 0,0 à 1,0) de la largeur et de la hauteur de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-561">The vector is a fraction (from 0.0 to 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-562">Position</span><span class="sxs-lookup"><span data-stu-id="9d026-562">Position</span></span></td>
<td><span data-ttu-id="9d026-563"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-563"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d026-564">Point dans le rectangle de référence de la forme pour positionner l’origine de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-564">Point in the reference rectangle of the shape to position the origin of the image.</span></span> <span data-ttu-id="9d026-565">La valeur par défaut est le centre du rectangle de conteneur.</span><span class="sxs-lookup"><span data-stu-id="9d026-565">Default is the center of the container rectangle.</span></span> <span data-ttu-id="9d026-566">Le vecteur est une fraction (0,0-1,0) de la largeur et de la hauteur de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-566">The vector is a fraction (0.0 - 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-567">Taille</span><span class="sxs-lookup"><span data-stu-id="9d026-567">Size</span></span></td>
<td><span data-ttu-id="9d026-568"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-568"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d026-569">Taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-569">The size of the image.</span></span> <span data-ttu-id="9d026-570">La valeur par défaut est la taille en pixels de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-570">Default is pixel size of the image.</span></span> <span data-ttu-id="9d026-571">Peut être spécifié en coordonnées absolues ou en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="9d026-571">May be specified in absolute coordinates or percentage.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-572">Source</span><span class="sxs-lookup"><span data-stu-id="9d026-572">Src</span></span></td>
<td><span data-ttu-id="9d026-573"><a href="#data-types-used-in-the-vml-object-model">Chaîne</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-573"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="9d026-574">URL vers une image à charger pour les remplissages d’image et de motif.</span><span class="sxs-lookup"><span data-stu-id="9d026-574">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="9d026-575">Cet attribut doit toujours être présent et pointer vers des données d’image valides pour qu’une image s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9d026-575">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-576">Type</span><span class="sxs-lookup"><span data-stu-id="9d026-576">Type</span></span></td>
<td><span data-ttu-id="9d026-577">VgFillType.</span><span class="sxs-lookup"><span data-stu-id="9d026-577">VgFillType.</span></span> <span data-ttu-id="9d026-578">qui peut être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="9d026-578">May be one of the following types:</span></span>
<ul>
<li><span data-ttu-id="9d026-579">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="9d026-579">Background</span></span></li>
<li><span data-ttu-id="9d026-580">Frame</span><span class="sxs-lookup"><span data-stu-id="9d026-580">Frame</span></span></li>
<li><span data-ttu-id="9d026-581">Dégradé</span><span class="sxs-lookup"><span data-stu-id="9d026-581">Gradient</span></span></li>
<li><span data-ttu-id="9d026-582">GradientCenter</span><span class="sxs-lookup"><span data-stu-id="9d026-582">GradientCenter</span></span></li>
<li><span data-ttu-id="9d026-583">GradientRadial</span><span class="sxs-lookup"><span data-stu-id="9d026-583">GradientRadial</span></span></li>
<li><span data-ttu-id="9d026-584">GradientTitle</span><span class="sxs-lookup"><span data-stu-id="9d026-584">GradientTitle</span></span></li>
<li><span data-ttu-id="9d026-585">GradientUnscaled</span><span class="sxs-lookup"><span data-stu-id="9d026-585">GradientUnscaled</span></span></li>
<li><span data-ttu-id="9d026-586">Modèle</span><span class="sxs-lookup"><span data-stu-id="9d026-586">Pattern</span></span></li>
<li><span data-ttu-id="9d026-587">Unie</span><span class="sxs-lookup"><span data-stu-id="9d026-587">Solid</span></span></li>
<li><span data-ttu-id="9d026-588">Tile</span><span class="sxs-lookup"><span data-stu-id="9d026-588">Tile</span></span></li>
</ul>
<span data-ttu-id="9d026-589">Les mosaïques, les modèles et les frames requièrent que les attributs d’image soient fournis.</span><span class="sxs-lookup"><span data-stu-id="9d026-589">Tile, Pattern, and Frame require the image attributes to be supplied.</span></span> <span data-ttu-id="9d026-590">Les attributs gradient et GradientRadial requièrent que les attributs de dégradé soient fournis.</span><span class="sxs-lookup"><span data-stu-id="9d026-590">Gradient and GradientRadial require the gradient attributes to be supplied.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a><span data-ttu-id="9d026-591">élément Group</span><span class="sxs-lookup"><span data-stu-id="9d026-591">Group element</span></span>

<span data-ttu-id="9d026-592">Un groupe est une collection de formes individuelles qui peuvent être positionnées et transformées en une unité.</span><span class="sxs-lookup"><span data-stu-id="9d026-592">A group is a collection of individual shapes that can be positioned and transformed as a unit.</span></span>



|   <span data-ttu-id="9d026-593">Attribut</span><span class="sxs-lookup"><span data-stu-id="9d026-593">Attribute</span></span>        |   <span data-ttu-id="9d026-594">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-594">Description</span></span>                                                                                                                                                                                      |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d026-595">Élément</span><span class="sxs-lookup"><span data-stu-id="9d026-595">Item</span></span>   | <span data-ttu-id="9d026-596">[IVgShape](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-596">[IVgShape](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-597">Élément spécifié dans le tableau de formes.</span><span class="sxs-lookup"><span data-stu-id="9d026-597">Specified item in the array of shapes.</span></span> |
| <span data-ttu-id="9d026-598">Longueur</span><span class="sxs-lookup"><span data-stu-id="9d026-598">Length</span></span> | <span data-ttu-id="9d026-599">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-599">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-600">Nombre de formes dans ce groupe.</span><span class="sxs-lookup"><span data-stu-id="9d026-600">Number of shapes in this group.</span></span>         |



 

### <a name="imagedata-element"></a><span data-ttu-id="9d026-601">Élément ImageData</span><span class="sxs-lookup"><span data-stu-id="9d026-601">Imagedata element</span></span>

<span data-ttu-id="9d026-602">Décrit une image à afficher en haut d’une forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-602">Describes a picture to be rendered on top of a shape.</span></span>



|   <span data-ttu-id="9d026-603">Attribut</span><span class="sxs-lookup"><span data-stu-id="9d026-603">Attribute</span></span>        |   <span data-ttu-id="9d026-604">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-604">Description</span></span>                                                                                                                                                                                      |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d026-605">Anticrénelage</span><span class="sxs-lookup"><span data-stu-id="9d026-605">BiLevel</span></span>     | <span data-ttu-id="9d026-606">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-606">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d026-607">Affichez l’image dans deux couleurs uniquement (généralement en noir et blanc).</span><span class="sxs-lookup"><span data-stu-id="9d026-607">Display picture in only two colors (usually black and white).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="9d026-608">BlackLevel</span><span class="sxs-lookup"><span data-stu-id="9d026-608">BlackLevel</span></span>  | <span data-ttu-id="9d026-609">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-609">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="9d026-610">Permet de définir le niveau de manière à ce que les noirs apparaissent comme des véritables noirs et que toutes les autres couleurs soient visibles en tant que nuances au-dessus du noir.</span><span class="sxs-lookup"><span data-stu-id="9d026-610">Allows adjustment to set the level so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="9d026-611">Chromakey</span><span class="sxs-lookup"><span data-stu-id="9d026-611">Chromakey</span></span>   | <span data-ttu-id="9d026-612">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-612">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9d026-613">Couleur transparente de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-613">Transparent color of picture.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="9d026-614">CropBottom</span><span class="sxs-lookup"><span data-stu-id="9d026-614">CropBottom</span></span>  | <span data-ttu-id="9d026-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-616">Distance de rognage à partir du bas de l’image exprimée sous la forme d’un pourcentage de la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-616">Crop distance from bottom of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="9d026-617">CropLeft</span><span class="sxs-lookup"><span data-stu-id="9d026-617">CropLeft</span></span>    | <span data-ttu-id="9d026-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-619">Distance de rognage à partir du bord gauche de l’image exprimée sous la forme d’une fraction de la taille de l’image (de 0,0 à 1,0).</span><span class="sxs-lookup"><span data-stu-id="9d026-619">Crop distance from left edge of picture expressed as a fraction of picture size (from 0.0 to 1.0).</span></span> <span data-ttu-id="9d026-620">Toutefois, « out-recadrage » est pris en charge et, par conséquent, les valeurs inférieures à 0 et supérieures à 1 sont prises en charge ; par exemple,-5, 20 découpent les limites 25X la taille de l’image avec 4/5 d’un côté de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-620">However, "out-cropping" is supported and thus values of less than 0 and greater than 1 are supported; e.g., -5, 20 would out-crop the bounds 25X the picture size with 4/5 on one side of the picture.</span></span> |
| <span data-ttu-id="9d026-621">CropRight</span><span class="sxs-lookup"><span data-stu-id="9d026-621">CropRight</span></span>   | <span data-ttu-id="9d026-622">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-622">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-623">Distance de rognage à partir de la droite de l’image exprimée sous la forme d’un pourcentage de la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-623">Crop distance from right of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="9d026-624">CropTop</span><span class="sxs-lookup"><span data-stu-id="9d026-624">CropTop</span></span>     | <span data-ttu-id="9d026-625">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-625">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-626">Distance de rognage à partir du haut de l’image exprimée sous la forme d’un pourcentage de la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-626">Crop distance from top of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="9d026-627">EmbossColor</span><span class="sxs-lookup"><span data-stu-id="9d026-627">EmbossColor</span></span> | <span data-ttu-id="9d026-628">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-628">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9d026-629">Il s’agit d’un pourcentage de la couleur de l’ombre pour créer un effet d’image en relief.</span><span class="sxs-lookup"><span data-stu-id="9d026-629">This is set to a percentage of the shadow color to create an embossed picture effect.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="9d026-630">Maîtrise</span><span class="sxs-lookup"><span data-stu-id="9d026-630">Gain</span></span>        | <span data-ttu-id="9d026-631">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-631">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-632">Ajuste l’intensité de toutes les couleurs.</span><span class="sxs-lookup"><span data-stu-id="9d026-632">Adjusts the intensity of all colors.</span></span> <span data-ttu-id="9d026-633">Définit essentiellement le degré de luminosité du blanc.</span><span class="sxs-lookup"><span data-stu-id="9d026-633">Essentially sets how bright white will be.</span></span> <span data-ttu-id="9d026-634">Est compris entre 0 et 32767.</span><span class="sxs-lookup"><span data-stu-id="9d026-634">Ranges from 0 to 32767.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="9d026-635">Gamma</span><span class="sxs-lookup"><span data-stu-id="9d026-635">Gamma</span></span>       | <span data-ttu-id="9d026-636">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-636">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="9d026-637">Correction gamma.</span><span class="sxs-lookup"><span data-stu-id="9d026-637">Gamma correction.</span></span> <span data-ttu-id="9d026-638">L’amélioration de l’image donne une image plus contrastée.</span><span class="sxs-lookup"><span data-stu-id="9d026-638">Increasing it gives an image more contrast.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="9d026-639">Nuances de gris</span><span class="sxs-lookup"><span data-stu-id="9d026-639">GrayScale</span></span>   | <span data-ttu-id="9d026-640">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-640">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d026-641">Affichez l’image en nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="9d026-641">Display picture in grayscale colors.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9d026-642">Source</span><span class="sxs-lookup"><span data-stu-id="9d026-642">Src</span></span>         | <span data-ttu-id="9d026-643">[Chaîne](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-643">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-644">URL vers une image à charger pour les remplissages d’image et de motif.</span><span class="sxs-lookup"><span data-stu-id="9d026-644">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="9d026-645">Cet attribut doit toujours être présent et pointer vers des données d’image valides pour qu’une image s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9d026-645">This attribute must always be present and point to valid image data for a picture to appear.</span></span>                                                                                                                                                           |



 

### <a name="path-element"></a><span data-ttu-id="9d026-646">Élément Path</span><span class="sxs-lookup"><span data-stu-id="9d026-646">Path element</span></span>

<span data-ttu-id="9d026-647">Définit le chemin d’accès qui compose la forme, à l’aide d’une chaîne qui contient un ensemble complet de commandes de « mouvement du stylet ».</span><span class="sxs-lookup"><span data-stu-id="9d026-647">Defines the path that makes up the shape, using a string that contains a rich set of "pen movement" commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-648">Limo</span><span class="sxs-lookup"><span data-stu-id="9d026-648">Limo</span></span></td>
<td><span data-ttu-id="9d026-649"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-649"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span></span> <span data-ttu-id="9d026-650">Définit le point d’étirement de la forme ; par exemple, pour une forme Giraffe, le point Limo serait sur le cou. par conséquent, lorsque la forme est redimensionnée, le cou est étiré et le reste de la forme conserve ses dimensions.</span><span class="sxs-lookup"><span data-stu-id="9d026-650">Defines the point where the shape is stretched; e.g., for a giraffe shape, the limo point would be on the neck so when the shape is resized, the neck will stretch and the rest of the shape will maintain its dimensions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-651">TextBoxRect</span><span class="sxs-lookup"><span data-stu-id="9d026-651">TextBoxRect</span></span></td>
<td><span data-ttu-id="9d026-652"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-652"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span></span> <span data-ttu-id="9d026-653">Tableau contenant les rectangles qui définissent l’emplacement où le texte doit être placé.</span><span class="sxs-lookup"><span data-stu-id="9d026-653">Array containing the rectangles that define where text should go.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-654">V</span><span class="sxs-lookup"><span data-stu-id="9d026-654">V</span></span></td>
<td><span data-ttu-id="9d026-655"><a href="#data-types-used-in-the-vml-object-model">Chaîne</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-655"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="9d026-656">Correspond à l’attribut v de la balise Path.</span><span class="sxs-lookup"><span data-stu-id="9d026-656">Matches the v attribute on the Path tag.</span></span> <span data-ttu-id="9d026-657">Notez que le chemin d’accès peut correspondre à un attribut ou à un élément de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="9d026-657">Note that path may correspond to Path attribute or element.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-658">Value</span><span class="sxs-lookup"><span data-stu-id="9d026-658">Value</span></span></td>
<td><span data-ttu-id="9d026-659"><a href="#data-types-used-in-the-vml-object-model">Chaîne</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-659"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="9d026-660">Représentation textuelle des commandes qui définissent le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="9d026-660">A text representation of the commands that define the path.</span></span> <span data-ttu-id="9d026-661">Les valeurs de coordonnée X ou y peuvent être une référence à une formule dans le formulaire &quot; @# &quot; où # est le nombre ordinal de la formule, par exemple, &quot; @2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d026-661">X or y-coordinate values can be a reference to a formula in the form &quot;@#&quot; where # is the formula's ordinal number, e.g., &quot;@2&quot;.</span></span> <span data-ttu-id="9d026-662">Cette chaîne d’attribut est constituée d’un ensemble complet de commandes, notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-662">This attribute string is made up of a rich set of commands including the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d026-663">Commande</span><span class="sxs-lookup"><span data-stu-id="9d026-663">Command</span></span></th>
<th><span data-ttu-id="9d026-664">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-664">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-665">AE (angleellipseto)</span><span class="sxs-lookup"><span data-stu-id="9d026-665">ae (angleellipseto)</span></span></td>
<td><span data-ttu-id="9d026-666"><strong>Centre</strong>(x, y) <strong>taille</strong>(w, h), angle de <strong>début</strong>, <strong>angle de fin</strong></span><span class="sxs-lookup"><span data-stu-id="9d026-666"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span></span><br/> <span data-ttu-id="9d026-667">Dessinez un segment d’une ellipse.</span><span class="sxs-lookup"><span data-stu-id="9d026-667">Draw a segment of an ellipse.</span></span> <span data-ttu-id="9d026-668">Une ligne droite est dessinée à partir du point actuel jusqu’au point de départ du segment.</span><span class="sxs-lookup"><span data-stu-id="9d026-668">A straight line is drawn from the current point to the start point of the segment.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-669">Al (angleelipse)</span><span class="sxs-lookup"><span data-stu-id="9d026-669">al (angleelipse)</span></span></td>
<td><span data-ttu-id="9d026-670">Identique à AE, sauf qu’il existe un m implicite vers le point de départ du segment.</span><span class="sxs-lookup"><span data-stu-id="9d026-670">Same as ae except that there is an implied m to the starting point of the segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-671">AR (ARC)</span><span class="sxs-lookup"><span data-stu-id="9d026-671">ar (arc)</span></span></td>
<td><span data-ttu-id="9d026-672">Identique à.</span><span class="sxs-lookup"><span data-stu-id="9d026-672">Same as at.</span></span> <span data-ttu-id="9d026-673">Toutefois, un nouveau sous-tracé est démarré par un m implicite jusqu’au point de départ de l’arc.</span><span class="sxs-lookup"><span data-stu-id="9d026-673">However, a new subpath is started by an implied m to the start point of the arc.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-674">à (ArcTo)</span><span class="sxs-lookup"><span data-stu-id="9d026-674">at (arcto)</span></span></td>
<td><span data-ttu-id="9d026-675"><strong>end</strong> <strong>gauche</strong>, <strong>haut</strong>, <strong>droite</strong>, <strong>bas</strong>, <strong>début</strong>(x, y) (x, y)</span><span class="sxs-lookup"><span data-stu-id="9d026-675"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="9d026-676">Les quatre premières valeurs définissent le cadre englobant d’une ellipse.</span><span class="sxs-lookup"><span data-stu-id="9d026-676">The first four values define the bounding box of an ellipse.</span></span> <span data-ttu-id="9d026-677">Les quatre derniers définissent deux vecteurs radials.</span><span class="sxs-lookup"><span data-stu-id="9d026-677">The last four define two radial vectors.</span></span> <span data-ttu-id="9d026-678">Un segment de l’ellipse est dessiné qui commence à l’angle défini par le vecteur de démarrage RADIUS et se termine à l’angle défini par le vecteur de fin.</span><span class="sxs-lookup"><span data-stu-id="9d026-678">A segment of the ellipse is drawn that starts at the angle defined by the start radius vector and ends at the angle defined by the end vector.</span></span> <span data-ttu-id="9d026-679">Une ligne droite est dessinée à partir du point actuel jusqu’au début de l’arc. L’arc est toujours dessiné dans le sens inverse des aiguilles d’une passe.</span><span class="sxs-lookup"><span data-stu-id="9d026-679">A straight line is drawn from the current point to the start of the arc. The arc is always drawn in a counterclockwise direction.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-680">c (curveTo)</span><span class="sxs-lookup"><span data-stu-id="9d026-680">c (curveto)</span></span></td>
<td><span data-ttu-id="9d026-681"><strong>Control1</strong>(x, y) <strong>Control2</strong>(x, y) <strong>à</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="9d026-681"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong>(x,y)</span></span> <br/> <span data-ttu-id="9d026-682">Dessinez une courbe de Bézier cubique à partir du point actuel jusqu’à la coordonnée donnée par les deux derniers paramètres, les points de contrôle donnés par les quatre premiers paramètres.</span><span class="sxs-lookup"><span data-stu-id="9d026-682">Draw a cubic bezier curve from the current point to the coordinate given by the final two parameters, the control points given by the first four parameters.</span></span> <span data-ttu-id="9d026-683">Le point actuel devient le point de terminaison de la courbe de Bézier.</span><span class="sxs-lookup"><span data-stu-id="9d026-683">The current point becomes the endpoint of the bezier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-684">e (fin)</span><span class="sxs-lookup"><span data-stu-id="9d026-684">e (end)</span></span></td>
<td><span data-ttu-id="9d026-685">Terminer l’ensemble de sous-chemins en cours.</span><span class="sxs-lookup"><span data-stu-id="9d026-685">End the current set of subpaths.</span></span> <span data-ttu-id="9d026-686">Un ensemble donné de sous-chemins (délimités par fin) est rempli à l’aide de eofill.</span><span class="sxs-lookup"><span data-stu-id="9d026-686">A given set of subpaths (as delimited by end) are filled using eofill.</span></span> <span data-ttu-id="9d026-687">Les ensembles de sous-tracés suivants sont remplis indépendamment et superposés sur ceux qui existent déjà.</span><span class="sxs-lookup"><span data-stu-id="9d026-687">Subsequent sets of subpaths are filled independently and superimposed on existing ones.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-688">l (LineTo)</span><span class="sxs-lookup"><span data-stu-id="9d026-688">l (lineto)</span></span></td>
<td><span data-ttu-id="9d026-689">x, y</span><span class="sxs-lookup"><span data-stu-id="9d026-689">x,y</span></span><br/> <span data-ttu-id="9d026-690">Dessine une ligne du point actuel jusqu’à la coordonnée x, y donnée, qui devient le nouveau point actuel.</span><span class="sxs-lookup"><span data-stu-id="9d026-690">Draw a line from the current point to the given x,y-coordinate, which becomes the new current point.</span></span> <span data-ttu-id="9d026-691">Des paires de coordonnées supplémentaires peuvent être spécifiées pour former une polyligne, par exemple &quot; l 10, 13, 45, 27, 89,-12 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d026-691">Additional coordinate pairs may be specified to form a polyline, e.g., &quot;l 10,13,45,27,89,-12&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-692">m (MoveTo)</span><span class="sxs-lookup"><span data-stu-id="9d026-692">m (moveto)</span></span></td>
<td><span data-ttu-id="9d026-693">x, y</span><span class="sxs-lookup"><span data-stu-id="9d026-693">x,y</span></span><br/> <span data-ttu-id="9d026-694">Démarre un nouveau sous-tracé à la coordonnée x, y donnée.</span><span class="sxs-lookup"><span data-stu-id="9d026-694">Start a new subpath at the given x,y-coordinate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-695">NF (NoFill)</span><span class="sxs-lookup"><span data-stu-id="9d026-695">nf (nofill)</span></span></td>
<td><span data-ttu-id="9d026-696">L’ensemble actuel de sous-chemins (délimité par fin) n’est pas rempli.</span><span class="sxs-lookup"><span data-stu-id="9d026-696">The current set of subpaths (delimited by end) will not be filled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-697">NS (noStroke)</span><span class="sxs-lookup"><span data-stu-id="9d026-697">ns (nostroke)</span></span></td>
<td><span data-ttu-id="9d026-698">L’ensemble actuel de sous-chemins (délimité par fin) n’est pas rayé.</span><span class="sxs-lookup"><span data-stu-id="9d026-698">The current set of subpaths (delimited by end) will not be stroked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-699">QB (quadraticbezier)</span><span class="sxs-lookup"><span data-stu-id="9d026-699">qb (quadraticbezier)</span></span></td>
<td><span data-ttu-id="9d026-700">(<strong>ControlPoint</strong>(x, y)) \*,<strong>end</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="9d026-700">(<strong>controlpoint</strong>(x, y))\*,<strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="9d026-701">Définit une ou plusieurs courbes de Bézier quadratiques au moyen de points de contrôle et d’un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="9d026-701">Defines one or more quadratic bezier curves by means of control points and an endpoint.</span></span> <span data-ttu-id="9d026-702">Les points intermédiaires (sur la courbe) sont obtenus par interpolation entre des points de contrôle successifs similaires aux polices TrueType.</span><span class="sxs-lookup"><span data-stu-id="9d026-702">Intermediate (on-curve) points are obtained by interpolation between successive control points similar to TrueType fonts.</span></span> <span data-ttu-id="9d026-703">Le sous-tracé n’a pas besoin d’être un début, auquel cas le sous-tracé est fermé et le dernier point définit le point de départ.</span><span class="sxs-lookup"><span data-stu-id="9d026-703">The subpath need not be a start, in which case the subpath is closed and the last point defines the start point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-704">qx (ellipticalquadrantx)</span><span class="sxs-lookup"><span data-stu-id="9d026-704">qx (ellipticalquadrantx)</span></span></td>
<td><span data-ttu-id="9d026-705"><strong>fin</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="9d026-705"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="9d026-706">Un quart d’ellipse est dessiné du point actuel au point de terminaison donné.</span><span class="sxs-lookup"><span data-stu-id="9d026-706">A quarter ellipse is drawn from the current point to the given endpoint.</span></span> <span data-ttu-id="9d026-707">Le segment elliptique est initialement tangent à une ligne parallèle à l’axe x ; autrement dit, le segment démarre horizontalement.</span><span class="sxs-lookup"><span data-stu-id="9d026-707">The elliptical segment is initially tangential to a line parallel to the x-axis; i.e., the segment starts out horizontal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-708">qy (ellipticalquadranty)</span><span class="sxs-lookup"><span data-stu-id="9d026-708">qy (ellipticalquadranty)</span></span></td>
<td><span data-ttu-id="9d026-709"><strong>fin</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="9d026-709"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="9d026-710">Identique à qx, à ceci près que le segment elliptique est initialement tangent à une ligne parallèle à l’axe y ; autrement dit, le segment démarre verticalement.</span><span class="sxs-lookup"><span data-stu-id="9d026-710">Same as qx except that the elliptical segment is initially tangential to a line parallel to the y-axis; i.e., the segment starts out vertical.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-711">r (rlineto)</span><span class="sxs-lookup"><span data-stu-id="9d026-711">r (rlineto)</span></span></td>
<td><span data-ttu-id="9d026-712">x, y</span><span class="sxs-lookup"><span data-stu-id="9d026-712">x,y</span></span> <br/> <span data-ttu-id="9d026-713">Dessinez une ligne du point actuel vers la coordonnée relative (CPX + x, cpy + y).</span><span class="sxs-lookup"><span data-stu-id="9d026-713">Draw a line from the current point to the relative coordinate (cpx + x, cpy + y).</span></span> <span data-ttu-id="9d026-714">Si des paires de coordonnées supplémentaires sont fournies, chaque nouveau point est calculé par rapport au dernier.</span><span class="sxs-lookup"><span data-stu-id="9d026-714">If additional coordinate pairs are given, each new point is computed relative to the last one.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-715">t (rmoveto)</span><span class="sxs-lookup"><span data-stu-id="9d026-715">t (rmoveto)</span></span></td>
<td><span data-ttu-id="9d026-716">x, y</span><span class="sxs-lookup"><span data-stu-id="9d026-716">x,y</span></span><br/> <span data-ttu-id="9d026-717">Démarrez un nouveau sous-chemin d’accès aux coordonnées relatives (CPX + x, cpy + y) où CPX, cpy correspond à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="9d026-717">Start a new subpath at the relative coordinates ( cpx + x, cpy + y) where cpx, cpy is the current position.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-718">v (curveTo)</span><span class="sxs-lookup"><span data-stu-id="9d026-718">v (curveto)</span></span></td>
<td><span data-ttu-id="9d026-719"><strong>Control1</strong>(x, y) <strong>Control2</strong>(x, y) <strong>à</strong> (x, y)</span><span class="sxs-lookup"><span data-stu-id="9d026-719"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong> (x,y)</span></span> <br/> <span data-ttu-id="9d026-720">Courbe de Bézier cubique utilisant les coordonnées données relatives au point actuel.</span><span class="sxs-lookup"><span data-stu-id="9d026-720">Cubic bezier curve using the given coordinates relative to the current point.</span></span> <span data-ttu-id="9d026-721">Tous les points sont calculés par rapport au même point de départ.</span><span class="sxs-lookup"><span data-stu-id="9d026-721">All the points are computed relative to the same starting point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-722">WA (clockwisearcto)</span><span class="sxs-lookup"><span data-stu-id="9d026-722">wa (clockwisearcto)</span></span></td>
<td><span data-ttu-id="9d026-723">Identique à, mais l’arc est dessiné dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="9d026-723">Same as at but the arc is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-724">WR (clockwisearc)</span><span class="sxs-lookup"><span data-stu-id="9d026-724">wr (clockwisearc)</span></span></td>
<td><span data-ttu-id="9d026-725">Identique à AR mais est dessiné dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="9d026-725">Same as ar but is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-726">x (fermer)</span><span class="sxs-lookup"><span data-stu-id="9d026-726">x (close)</span></span></td>
<td><span data-ttu-id="9d026-727">Fermer le sous-tracé en cours en dessinant une ligne droite à partir du point actuel sur le point MoveTo d’origine.</span><span class="sxs-lookup"><span data-stu-id="9d026-727">Close the current subpath by drawing a straight line from the current point to the original moveto point.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a><span data-ttu-id="9d026-728">Élément Shadow</span><span class="sxs-lookup"><span data-stu-id="9d026-728">Shadow element</span></span>

<span data-ttu-id="9d026-729">Décrit un effet d’ombrage sur une forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-729">Describes a shadow effect on a shape.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-730">Couleur</span><span class="sxs-lookup"><span data-stu-id="9d026-730">Color</span></span></td>
<td><span data-ttu-id="9d026-731"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-731"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="9d026-732">Couleur de l’ombre principale.</span><span class="sxs-lookup"><span data-stu-id="9d026-732">Color of the primary shadow.</span></span> <span data-ttu-id="9d026-733">La valeur par défaut est RVB (128128128)</span><span class="sxs-lookup"><span data-stu-id="9d026-733">Default is RGB(128,128,128)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-734">Couleur2</span><span class="sxs-lookup"><span data-stu-id="9d026-734">Color2</span></span></td>
<td><span data-ttu-id="9d026-735"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-735"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="9d026-736">Couleur de la deuxième ombre, ou mise en surbrillance dans une ombre de relief ou d’empreinte.</span><span class="sxs-lookup"><span data-stu-id="9d026-736">Color of the second shadow, or highlight in an embossed or engraved shadow.</span></span> <span data-ttu-id="9d026-737">La valeur par défaut est RVB (203203203).</span><span class="sxs-lookup"><span data-stu-id="9d026-737">Default is RGB(203,203,203).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-738">Matrice</span><span class="sxs-lookup"><span data-stu-id="9d026-738">Matrix</span></span></td>
<td><span data-ttu-id="9d026-739"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-739"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span></span> <span data-ttu-id="9d026-740">Matrice de transformation de perspective au format &quot; Sxx, SXY, syx, SYY, PX, py &quot; [s = Scale, p = perspective].</span><span class="sxs-lookup"><span data-stu-id="9d026-740">A perspective transform matrix in the form, &quot;sxx,sxy,syx,syy,px,py&quot; [s=scale, p=perspective].</span></span> <span data-ttu-id="9d026-741">Les éléments s spécifient la façon dont l’ombre doit être mise à l’échelle par rapport à la forme, et les éléments p spécifient la façon dont l’ombre doit être faussée par rapport à la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-741">The s items specify how the shadow should scale with respect to the shape, and the p items specify how the shadow should skew with respect to the shape.</span></span> <span data-ttu-id="9d026-742">Par exemple, la matrice suivante redimensionne la forme d’un facteur de 2 et l’incline par un facteur de 4 dans toutes les directions :</span><span class="sxs-lookup"><span data-stu-id="9d026-742">For example, the following matrix resizes the shape by a factor of 2 and skews it by a factor of 4 in all directions:</span></span> <br/> <span data-ttu-id="9d026-743">&quot;2, 2, 2, 2, 4, 4&quot;</span><span class="sxs-lookup"><span data-stu-id="9d026-743">&quot;2,2,2,2,4,4&quot;</span></span><br/> <span data-ttu-id="9d026-744">Cette matrice est utilisée uniquement si le type de l’ombre est défini sur perspective.</span><span class="sxs-lookup"><span data-stu-id="9d026-744">This matrix is only used if the type of the shadow is set to perspective.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-745">Masquée</span><span class="sxs-lookup"><span data-stu-id="9d026-745">Obscured</span></span></td>
<td><span data-ttu-id="9d026-746"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-746"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d026-747">L’ombre peut être consultée si aucun remplissage n’est présent sur la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-747">The shadow can be seen through if there is no fill on the shape.</span></span> <span data-ttu-id="9d026-748">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="9d026-748">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-749">Offset</span><span class="sxs-lookup"><span data-stu-id="9d026-749">Offset</span></span></td>
<td><span data-ttu-id="9d026-750"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-750"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span></span> <span data-ttu-id="9d026-751">Quantité de décalage x, y à partir de l’emplacement de la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-751">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="9d026-752">La valeur par défaut est &quot; 2pt, 2pt &quot; .</span><span class="sxs-lookup"><span data-stu-id="9d026-752">Default is &quot;2pt,2pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-753">Offset2</span><span class="sxs-lookup"><span data-stu-id="9d026-753">Offset2</span></span></td>
<td><span data-ttu-id="9d026-754"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-754"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d026-755">Nombre de décalages x, y à partir de l’emplacement de la forme ?.</span><span class="sxs-lookup"><span data-stu-id="9d026-755">Amount of x,y second offset from the shape?s location.</span></span> <span data-ttu-id="9d026-756">Les valeurs sont soit une mesure absolue, soit une valeur fractionnaire de forme (-0,5 à + 0,5).</span><span class="sxs-lookup"><span data-stu-id="9d026-756">Values are either an absolute measurement, or a fractional value of shape (-0.5 to +0.5).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-757">Activé</span><span class="sxs-lookup"><span data-stu-id="9d026-757">On</span></span></td>
<td><span data-ttu-id="9d026-758"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-758"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d026-759">Active ou désactive l’affichage de l’ombre.</span><span class="sxs-lookup"><span data-stu-id="9d026-759">Turns the display of the shadow on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-760">Opacity</span><span class="sxs-lookup"><span data-stu-id="9d026-760">Opacity</span></span></td>
<td><span data-ttu-id="9d026-761"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-761"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="9d026-762">Opacité de l’effet d’ombre.</span><span class="sxs-lookup"><span data-stu-id="9d026-762">Opacity of the shadow effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-763">Origine</span><span class="sxs-lookup"><span data-stu-id="9d026-763">Origin</span></span></td>
<td><span data-ttu-id="9d026-764"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a> Paire de valeurs fractionnaires de forme comprise entre-0,5 et + 0,5.</span><span class="sxs-lookup"><span data-stu-id="9d026-764"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> A pair of fractional values of shape from -0.5 to +0.5.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-765">Type</span><span class="sxs-lookup"><span data-stu-id="9d026-765">Type</span></span></td>
<td><span data-ttu-id="9d026-766"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-766"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span></span> <span data-ttu-id="9d026-767">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-767">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-768">Unique (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="9d026-768">Single (default)</span></span></li>
<li><span data-ttu-id="9d026-769">Double</span><span class="sxs-lookup"><span data-stu-id="9d026-769">Double</span></span></li>
<li><span data-ttu-id="9d026-770">Perspective</span><span class="sxs-lookup"><span data-stu-id="9d026-770">Perspective</span></span></li>
<li><span data-ttu-id="9d026-771">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="9d026-771">ShapeRelative</span></span></li>
<li><span data-ttu-id="9d026-772">DrawingRelative</span><span class="sxs-lookup"><span data-stu-id="9d026-772">DrawingRelative</span></span></li>
<li><span data-ttu-id="9d026-773">Relief</span><span class="sxs-lookup"><span data-stu-id="9d026-773">Emboss</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a><span data-ttu-id="9d026-774">Élément Skew</span><span class="sxs-lookup"><span data-stu-id="9d026-774">Skew element</span></span>

<span data-ttu-id="9d026-775">Décrit un effet d’inclinaison de perspective sur une forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-775">Describes a perspective skew effect on a shape.</span></span> <span data-ttu-id="9d026-776">L’inclinaison est appliquée aux données de graphique vectoriel, et non aux données d’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-776">The skew is applied to vector graphic data, not image data.</span></span>



|   <span data-ttu-id="9d026-777">Attribut</span><span class="sxs-lookup"><span data-stu-id="9d026-777">Attribute</span></span>        |   <span data-ttu-id="9d026-778">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-778">Description</span></span>                                                                                                                                                                                      |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d026-779">Matrice</span><span class="sxs-lookup"><span data-stu-id="9d026-779">Matrix</span></span> | <span data-ttu-id="9d026-780">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-780">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-781">Matrice de transformation de perspective sous la forme «Sxx, SXY, syx, SYY, PX, py « \[ s = Scale, p = perspective \] .</span><span class="sxs-lookup"><span data-stu-id="9d026-781">A perspective transform matrix in the form, "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective\].</span></span> <span data-ttu-id="9d026-782">Si le décalage est en unités absolues alors que PX, py sont en unités UME ^-1 ; Sinon, il s’agit d’une fraction inverse de la taille de la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-782">If offset is in absolute units then px,py are in emu ^ -1 units; otherwise they are an inverse fraction of shape size.</span></span> |
| <span data-ttu-id="9d026-783">Offset</span><span class="sxs-lookup"><span data-stu-id="9d026-783">Offset</span></span> | <span data-ttu-id="9d026-784">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-784">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-785">Quantité de décalage x, y à partir de l’emplacement de la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-785">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="9d026-786">La valeur par défaut est « 2pt, 2pt ».</span><span class="sxs-lookup"><span data-stu-id="9d026-786">Default is "2pt,2pt".</span></span>                                                                                                                                                   |
| <span data-ttu-id="9d026-787">Activé</span><span class="sxs-lookup"><span data-stu-id="9d026-787">On</span></span>     | <span data-ttu-id="9d026-788">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-788">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d026-789">Active ou désactive l’affichage de l’inclinaison.</span><span class="sxs-lookup"><span data-stu-id="9d026-789">Turns the display of the skew on or off.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="9d026-790">Origine</span><span class="sxs-lookup"><span data-stu-id="9d026-790">Origin</span></span> | <span data-ttu-id="9d026-791">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-791">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d026-792">Paire de valeurs fractionnaires de forme comprise entre-0,5 et + 0,5.</span><span class="sxs-lookup"><span data-stu-id="9d026-792">A pair of fractional values of shape from -0.5 to +0.5.</span></span>                                                                                                                                                                     |



 

### <a name="stroke-element"></a><span data-ttu-id="9d026-793">Stroke, élément</span><span class="sxs-lookup"><span data-stu-id="9d026-793">Stroke element</span></span>

<span data-ttu-id="9d026-794">Décrit comment dessiner le tracé si un point au-delà d’une ligne pleine avec une couleur unie est souhaité.</span><span class="sxs-lookup"><span data-stu-id="9d026-794">Describes how to draw the path if something beyond a solid line with a solid color is desired.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-795">Couleur</span><span class="sxs-lookup"><span data-stu-id="9d026-795">Color</span></span></td>
<td><span data-ttu-id="9d026-796"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-796"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d026-797">Couleur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="9d026-797">The color of the line.</span></span> <span data-ttu-id="9d026-798">Identique à l’attribut StrokeColor dans Shape mais le remplace.</span><span class="sxs-lookup"><span data-stu-id="9d026-798">Same as StrokeColor attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-799">Couleur2</span><span class="sxs-lookup"><span data-stu-id="9d026-799">Color2</span></span></td>
<td><span data-ttu-id="9d026-800"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-800"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="9d026-801">Couleur secondaire.</span><span class="sxs-lookup"><span data-stu-id="9d026-801">Secondary color.</span></span> <span data-ttu-id="9d026-802">Utilisé quand FillType est un modèle.</span><span class="sxs-lookup"><span data-stu-id="9d026-802">Used when FillType is Pattern.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-803">DashStyle</span><span class="sxs-lookup"><span data-stu-id="9d026-803">DashStyle</span></span></td>
<td><span data-ttu-id="9d026-804"><strong>VgLineDashStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-804"><strong>VgLineDashStyle</strong>.</span></span> <span data-ttu-id="9d026-805">Format du style des tirets.</span><span class="sxs-lookup"><span data-stu-id="9d026-805">Dash style format.</span></span> <span data-ttu-id="9d026-806">Peut être une valeur spécifique ou une séquence de nombres avec un modèle de tiret défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9d026-806">May be a specific value or a sequence of numbers with a user-defined dash pattern.</span></span> <span data-ttu-id="9d026-807">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-807">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-808">Unie (par défaut)</span><span class="sxs-lookup"><span data-stu-id="9d026-808">Solid (default)</span></span></li>
<li><span data-ttu-id="9d026-809">ShortDash</span><span class="sxs-lookup"><span data-stu-id="9d026-809">ShortDash</span></span></li>
<li><span data-ttu-id="9d026-810">ShortDot</span><span class="sxs-lookup"><span data-stu-id="9d026-810">ShortDot</span></span></li>
<li><span data-ttu-id="9d026-811">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="9d026-811">ShortDashDot</span></span></li>
<li><span data-ttu-id="9d026-812">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="9d026-812">ShortDashDotDot</span></span></li>
<li><span data-ttu-id="9d026-813">Points</span><span class="sxs-lookup"><span data-stu-id="9d026-813">Dot</span></span></li>
<li><span data-ttu-id="9d026-814">Tiret</span><span class="sxs-lookup"><span data-stu-id="9d026-814">Dash</span></span></li>
<li><span data-ttu-id="9d026-815">Tiret-point</span><span class="sxs-lookup"><span data-stu-id="9d026-815">DashDot</span></span></li>
<li><span data-ttu-id="9d026-816">LongDash</span><span class="sxs-lookup"><span data-stu-id="9d026-816">LongDash</span></span></li>
<li><span data-ttu-id="9d026-817">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="9d026-817">LongDashDot</span></span></li>
<li><span data-ttu-id="9d026-818">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="9d026-818">LongDashDotDot</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-819">EndArrow</span><span class="sxs-lookup"><span data-stu-id="9d026-819">EndArrow</span></span></td>
<td><span data-ttu-id="9d026-820"><strong>VgArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-820"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="9d026-821">Pointe de flèche pour la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="9d026-821">Arrowhead for the end of the line.</span></span> <span data-ttu-id="9d026-822">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-822">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-823">Aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="9d026-823">None (default)</span></span></li>
<li><span data-ttu-id="9d026-824">Bloquer</span><span class="sxs-lookup"><span data-stu-id="9d026-824">Block</span></span></li>
<li><span data-ttu-id="9d026-825">Classique</span><span class="sxs-lookup"><span data-stu-id="9d026-825">Classic</span></span></li>
<li><span data-ttu-id="9d026-826">Losange</span><span class="sxs-lookup"><span data-stu-id="9d026-826">Diamond</span></span></li>
<li><span data-ttu-id="9d026-827">Ovale</span><span class="sxs-lookup"><span data-stu-id="9d026-827">Oval</span></span></li>
<li><span data-ttu-id="9d026-828">Ouvrir</span><span class="sxs-lookup"><span data-stu-id="9d026-828">Open</span></span></li>
<li><span data-ttu-id="9d026-829">Chevron</span><span class="sxs-lookup"><span data-stu-id="9d026-829">Chevron</span></span></li>
<li><span data-ttu-id="9d026-830">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="9d026-830">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-831">EndArrowLength</span><span class="sxs-lookup"><span data-stu-id="9d026-831">EndArrowLength</span></span></td>
<td><span data-ttu-id="9d026-832"><strong>VgArrowHeadLength</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-832"><strong>VgArrowHeadLength</strong>.</span></span> <span data-ttu-id="9d026-833">Longueur de la flèche pour la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="9d026-833">Arrowhead length for the end of the line.</span></span> <span data-ttu-id="9d026-834">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-834">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-835">Court</span><span class="sxs-lookup"><span data-stu-id="9d026-835">Short</span></span></li>
<li><span data-ttu-id="9d026-836">Moyenne (par défaut)</span><span class="sxs-lookup"><span data-stu-id="9d026-836">Medium (default)</span></span></li>
<li><span data-ttu-id="9d026-837">Long</span><span class="sxs-lookup"><span data-stu-id="9d026-837">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-838">EndArrowWidth</span><span class="sxs-lookup"><span data-stu-id="9d026-838">EndArrowWidth</span></span></td>
<td><span data-ttu-id="9d026-839"><strong>VgArrowheadWidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-839"><strong>VgArrowheadWidth</strong>.</span></span> <span data-ttu-id="9d026-840">Largeur de la flèche pour la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="9d026-840">Arrowhead width for the end of the line.</span></span> <span data-ttu-id="9d026-841">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-841">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-842">Restreindre</span><span class="sxs-lookup"><span data-stu-id="9d026-842">Narrow</span></span></li>
<li><span data-ttu-id="9d026-843">Moyenne (par défaut)</span><span class="sxs-lookup"><span data-stu-id="9d026-843">Medium (default)</span></span></li>
<li><span data-ttu-id="9d026-844">Large</span><span class="sxs-lookup"><span data-stu-id="9d026-844">Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-845">Extrem</span><span class="sxs-lookup"><span data-stu-id="9d026-845">EndCap</span></span></td>
<td><span data-ttu-id="9d026-846"><strong>VgLineEndCapStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-846"><strong>VgLineEndCapStyle</strong>.</span></span> <span data-ttu-id="9d026-847">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-847">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-848">À deux dimensions</span><span class="sxs-lookup"><span data-stu-id="9d026-848">Flat</span></span></li>
<li><span data-ttu-id="9d026-849">Carré</span><span class="sxs-lookup"><span data-stu-id="9d026-849">Square</span></span></li>
<li><span data-ttu-id="9d026-850">Round</span><span class="sxs-lookup"><span data-stu-id="9d026-850">Round</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-851">FillType</span><span class="sxs-lookup"><span data-stu-id="9d026-851">FillType</span></span></td>
<td><span data-ttu-id="9d026-852"><strong>VgLineFillType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-852"><strong>VgLineFillType</strong>.</span></span> <span data-ttu-id="9d026-853">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-853">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-854">Unie (par défaut)</span><span class="sxs-lookup"><span data-stu-id="9d026-854">Solid (default)</span></span></li>
<li><span data-ttu-id="9d026-855">Tile</span><span class="sxs-lookup"><span data-stu-id="9d026-855">Tile</span></span></li>
<li><span data-ttu-id="9d026-856">Modèle</span><span class="sxs-lookup"><span data-stu-id="9d026-856">Pattern</span></span></li>
<li><span data-ttu-id="9d026-857">Frame</span><span class="sxs-lookup"><span data-stu-id="9d026-857">Frame</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-858">ImageAlignShape</span><span class="sxs-lookup"><span data-stu-id="9d026-858">ImageAlignShape</span></span></td>
<td><span data-ttu-id="9d026-859"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-859"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d026-860">Alignez l’image avec la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-860">Align the image with the shape.</span></span> <span data-ttu-id="9d026-861">Si la valeur est false, l’image est alignée avec la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9d026-861">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-862">ImageAspect</span><span class="sxs-lookup"><span data-stu-id="9d026-862">ImageAspect</span></span></td>
<td><span data-ttu-id="9d026-863"><strong>VgAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-863"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="9d026-864">L’attribut ImageSize est ajusté pour conserver l’aspect de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-864">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="9d026-865">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="9d026-865">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d026-866">Value</span><span class="sxs-lookup"><span data-stu-id="9d026-866">Value</span></span></th>
<th><span data-ttu-id="9d026-867">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-867">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-868">Ignorer</span><span class="sxs-lookup"><span data-stu-id="9d026-868">Ignore</span></span></td>
<td><span data-ttu-id="9d026-869">Ignorer les problèmes d’aspect.</span><span class="sxs-lookup"><span data-stu-id="9d026-869">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-870">Au moins</span><span class="sxs-lookup"><span data-stu-id="9d026-870">AtLeast</span></span></td>
<td><span data-ttu-id="9d026-871">L’image est au moins aussi grande que la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-871">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-872">AtMost</span><span class="sxs-lookup"><span data-stu-id="9d026-872">AtMost</span></span></td>
<td><span data-ttu-id="9d026-873">L’image n’est pas plus grande que la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-873">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-874">ImageSize</span><span class="sxs-lookup"><span data-stu-id="9d026-874">ImageSize</span></span></td>
<td><span data-ttu-id="9d026-875"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-875"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9d026-876">Taille de l’image avec laquelle former le pinceau.</span><span class="sxs-lookup"><span data-stu-id="9d026-876">Size of the image to form the brush with.</span></span> <span data-ttu-id="9d026-877">La valeur par défaut est la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="9d026-877">Default is the size of the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-878">JoinStyle</span><span class="sxs-lookup"><span data-stu-id="9d026-878">JoinStyle</span></span></td>
<td><span data-ttu-id="9d026-879"><strong>VgLineJoinStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-879"><strong>VgLineJoinStyle</strong>.</span></span> <span data-ttu-id="9d026-880">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-880">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-881">Round (joint arrondi)</span><span class="sxs-lookup"><span data-stu-id="9d026-881">Round (rounded joint)</span></span></li>
<li><span data-ttu-id="9d026-882">Biseau (joint biseauté)</span><span class="sxs-lookup"><span data-stu-id="9d026-882">Bevel (beveled joint)</span></span></li>
<li><span data-ttu-id="9d026-883">Mitre (articulation à onglet)</span><span class="sxs-lookup"><span data-stu-id="9d026-883">Miter (miter joint)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-884">LineStyle</span><span class="sxs-lookup"><span data-stu-id="9d026-884">LineStyle</span></span></td>
<td><span data-ttu-id="9d026-885"><strong>VgLineStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-885"><strong>VgLineStyle</strong>.</span></span> <span data-ttu-id="9d026-886">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-886">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-887">Unique</span><span class="sxs-lookup"><span data-stu-id="9d026-887">Single</span></span></li>
<li><span data-ttu-id="9d026-888">ThinThin (1:1:1)</span><span class="sxs-lookup"><span data-stu-id="9d026-888">ThinThin (1:1:1)</span></span></li>
<li><span data-ttu-id="9d026-889">ThinThick (1:1:2)</span><span class="sxs-lookup"><span data-stu-id="9d026-889">ThinThick (1:1:2)</span></span></li>
<li><span data-ttu-id="9d026-890">ThickThin (2:1:1)</span><span class="sxs-lookup"><span data-stu-id="9d026-890">ThickThin (2:1:1)</span></span></li>
<li><span data-ttu-id="9d026-891">ThickBetweenThin (1:1:2:1:1)</span><span class="sxs-lookup"><span data-stu-id="9d026-891">ThickBetweenThin (1:1:2:1:1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-892">MiterLimit</span><span class="sxs-lookup"><span data-stu-id="9d026-892">MiterLimit</span></span></td>
<td><span data-ttu-id="9d026-893"><a href="msdn-online-vml-vglength.md">Longueur</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-893"><a href="msdn-online-vml-vglength.md">Length</a>.</span></span> <span data-ttu-id="9d026-894">Distance maximale entre le point interne et le point externe d’une jointure.</span><span class="sxs-lookup"><span data-stu-id="9d026-894">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="9d026-895">Ce nombre est un multiple de l’épaisseur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="9d026-895">This number is a multiple of the thickness of the line.</span></span> <span data-ttu-id="9d026-896">Est compris entre 0 et 32 767.</span><span class="sxs-lookup"><span data-stu-id="9d026-896">Ranges from 0 to 32,767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-897">Activé</span><span class="sxs-lookup"><span data-stu-id="9d026-897">On</span></span></td>
<td><span data-ttu-id="9d026-898"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-898"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9d026-899">Active ou désactive l’affichage de la ligne.</span><span class="sxs-lookup"><span data-stu-id="9d026-899">Turns the display of the line on and off.</span></span> <span data-ttu-id="9d026-900">Identique à l’attribut Stroke dans Shape, mais le remplace.</span><span class="sxs-lookup"><span data-stu-id="9d026-900">Same as Stroke attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-901">Opacity</span><span class="sxs-lookup"><span data-stu-id="9d026-901">Opacity</span></span></td>
<td><span data-ttu-id="9d026-902"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-902"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="9d026-903">Opacité du trait.</span><span class="sxs-lookup"><span data-stu-id="9d026-903">Opacity of the stroke.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-904">Source</span><span class="sxs-lookup"><span data-stu-id="9d026-904">Src</span></span></td>
<td><span data-ttu-id="9d026-905">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="9d026-905">String.</span></span> <span data-ttu-id="9d026-906">URL vers une image à charger pour les remplissages d’image et de motif.</span><span class="sxs-lookup"><span data-stu-id="9d026-906">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="9d026-907">Cet attribut doit toujours être présent et pointer vers des données d’image valides pour qu’une image s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9d026-907">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-908">StartArrow</span><span class="sxs-lookup"><span data-stu-id="9d026-908">StartArrow</span></span></td>
<td><span data-ttu-id="9d026-909"><strong>VgArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-909"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="9d026-910">Pointe de flèche pour le début de la ligne.</span><span class="sxs-lookup"><span data-stu-id="9d026-910">Arrowhead for the start of the line.</span></span> <span data-ttu-id="9d026-911">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-911">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-912">Aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="9d026-912">None (default)</span></span></li>
<li><span data-ttu-id="9d026-913">Bloquer</span><span class="sxs-lookup"><span data-stu-id="9d026-913">Block</span></span></li>
<li><span data-ttu-id="9d026-914">Classique</span><span class="sxs-lookup"><span data-stu-id="9d026-914">Classic</span></span></li>
<li><span data-ttu-id="9d026-915">Losange</span><span class="sxs-lookup"><span data-stu-id="9d026-915">Diamond</span></span></li>
<li><span data-ttu-id="9d026-916">Ovale</span><span class="sxs-lookup"><span data-stu-id="9d026-916">Oval</span></span></li>
<li><span data-ttu-id="9d026-917">Ouvrir</span><span class="sxs-lookup"><span data-stu-id="9d026-917">Open</span></span></li>
<li><span data-ttu-id="9d026-918">Chevron</span><span class="sxs-lookup"><span data-stu-id="9d026-918">Chevron</span></span></li>
<li><span data-ttu-id="9d026-919">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="9d026-919">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-920">StartArrowLength</span><span class="sxs-lookup"><span data-stu-id="9d026-920">StartArrowLength</span></span></td>
<td><span data-ttu-id="9d026-921">VgArrowHeadLength.</span><span class="sxs-lookup"><span data-stu-id="9d026-921">VgArrowHeadLength.</span></span> <span data-ttu-id="9d026-922">Longueur de la flèche pour le début de la ligne.</span><span class="sxs-lookup"><span data-stu-id="9d026-922">Arrowhead length for the start of the line.</span></span> <span data-ttu-id="9d026-923">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-923">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-924">Court</span><span class="sxs-lookup"><span data-stu-id="9d026-924">Short</span></span></li>
<li><span data-ttu-id="9d026-925">Moyenne (par défaut)</span><span class="sxs-lookup"><span data-stu-id="9d026-925">Medium (default)</span></span></li>
<li><span data-ttu-id="9d026-926">Long</span><span class="sxs-lookup"><span data-stu-id="9d026-926">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-927">StartArrowWidth</span><span class="sxs-lookup"><span data-stu-id="9d026-927">StartArrowWidth</span></span></td>
<td><span data-ttu-id="9d026-928">VgArrowheadWidth.</span><span class="sxs-lookup"><span data-stu-id="9d026-928">VgArrowheadWidth.</span></span> <span data-ttu-id="9d026-929">Largeur de la flèche pour le début de la ligne.</span><span class="sxs-lookup"><span data-stu-id="9d026-929">Arrowhead width for the start of the line.</span></span> <span data-ttu-id="9d026-930">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-930">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-931">Étroit moyen (par défaut) large</span><span class="sxs-lookup"><span data-stu-id="9d026-931">Narrow Medium (default) Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-932">Poids</span><span class="sxs-lookup"><span data-stu-id="9d026-932">Weight</span></span></td>
<td><span data-ttu-id="9d026-933"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-933"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="9d026-934">Largeur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="9d026-934">Width of line.</span></span> <span data-ttu-id="9d026-935">Est compris entre 0 et 1584.</span><span class="sxs-lookup"><span data-stu-id="9d026-935">Ranges from 0 to 1584.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="9d026-936">L’attribut DashStyle permet à l’utilisateur de spécifier un modèle de tirets personnalisé.</span><span class="sxs-lookup"><span data-stu-id="9d026-936">The DashStyle attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="9d026-937">Cette opération s’effectue à l’aide d’une série de nombres.</span><span class="sxs-lookup"><span data-stu-id="9d026-937">This is done using a series of numbers.</span></span> <span data-ttu-id="9d026-938">Les styles de tirets sont définis en termes de longueur du tiret (partie dessinée du trait) et de la longueur de l’espace entre les tirets.</span><span class="sxs-lookup"><span data-stu-id="9d026-938">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="9d026-939">Les longueurs sont relatives à la largeur de la ligne ; une longueur de &quot; 1 &quot; est égale à la largeur de ligne.</span><span class="sxs-lookup"><span data-stu-id="9d026-939">The lengths are relative to the line width; a length of &quot;1&quot; is equal to the line width.</span></span> <span data-ttu-id="9d026-940">Le style d’extrémité est appliqué à chaque tiret. les styles de flèche ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="9d026-940">The EndCap style is applied to each dash, arrow styles are not.</span></span> <span data-ttu-id="9d026-941">La chaîne définit d’abord la longueur du tiret, puis la longueur de l’espace.</span><span class="sxs-lookup"><span data-stu-id="9d026-941">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="9d026-942">Cela peut être répété pour former des styles de tiret complexes.</span><span class="sxs-lookup"><span data-stu-id="9d026-942">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="9d026-943">La chaîne doit toujours contenir une paire de nombres ; Si elle contient un nombre impair de nombres, la dernière peut être ignorée.</span><span class="sxs-lookup"><span data-stu-id="9d026-943">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span> <span data-ttu-id="9d026-944">Le tableau suivant répertorie des valeurs typiques et une description de l’effet prévu.</span><span class="sxs-lookup"><span data-stu-id="9d026-944">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="9d026-945">&quot;0 &quot; signifie un point qui doit être quatre symétrique (avec des extrémités arrondies, il doit s’agir d’un cercle).</span><span class="sxs-lookup"><span data-stu-id="9d026-945">&quot;0&quot; implies a dot that should be fourfold symmetrical (with round endcaps it should be a circle).</span></span> <span data-ttu-id="9d026-946">Si l’extrémité de la ligne est plate, une visionneuse doit choisir un tiret de système d’exploitation intégré si possible (c’est-à-dire un point rapide à dessiner).</span><span class="sxs-lookup"><span data-stu-id="9d026-946">If the line endcap is Flat, a viewer should choose a built-in operating system dash where possible (i.e., something that is fast to draw).</span></span> <span data-ttu-id="9d026-947">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="9d026-947">The following shows some examples.</span></span>
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-948">&quot;2 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9d026-948">&quot;2 2&quot;</span></span></td>
<td><span data-ttu-id="9d026-949">des tirets courts (chaque tiret et l’espace entre deux fois la largeur de la ligne)</span><span class="sxs-lookup"><span data-stu-id="9d026-949">short-dashes (each dash and the space in between is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-950">&quot;1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9d026-950">&quot;1 2&quot;</span></span></td>
<td><span data-ttu-id="9d026-951">point (chaque tiret correspond à la largeur de la ligne, tandis que chaque espace est deux fois plus large que la largeur de la ligne)</span><span class="sxs-lookup"><span data-stu-id="9d026-951">dot (each dash is the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-952">&quot;4 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9d026-952">&quot;4 2&quot;</span></span></td>
<td><span data-ttu-id="9d026-953">Dash (chaque tiret correspond à quatre fois la largeur de la ligne, tandis que chaque espace est deux fois plus large que la largeur de la ligne)</span><span class="sxs-lookup"><span data-stu-id="9d026-953">dash (each dash is four times the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-954">&quot;8 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9d026-954">&quot;8 2&quot;</span></span></td>
<td><span data-ttu-id="9d026-955">long tiret</span><span class="sxs-lookup"><span data-stu-id="9d026-955">long-dash</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-956">&quot;4 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9d026-956">&quot;4 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="9d026-957">tiret-point</span><span class="sxs-lookup"><span data-stu-id="9d026-957">dash dot</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-958">&quot;8 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9d026-958">&quot;8 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="9d026-959">long-tiret-point</span><span class="sxs-lookup"><span data-stu-id="9d026-959">long-dash dot</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-960">&quot;8 2 1 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9d026-960">&quot;8 2 1 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="9d026-961">point-tiret long</span><span class="sxs-lookup"><span data-stu-id="9d026-961">long-dash dot dot</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a><span data-ttu-id="9d026-962">Élément TextPath</span><span class="sxs-lookup"><span data-stu-id="9d026-962">TextPath element</span></span>

<span data-ttu-id="9d026-963">Décrit un tracé vectoriel basé sur les données de texte, la police et les styles fournis.</span><span class="sxs-lookup"><span data-stu-id="9d026-963">Describes a vector path based on the text data, font, and styles supplied.</span></span> <span data-ttu-id="9d026-964">Le chemin d’accès du texte est déformé pour se conformer à un élément de **chemin d’accès** , s’il est fourni.</span><span class="sxs-lookup"><span data-stu-id="9d026-964">The text path is warped to conform to a **Path** element if supplied.</span></span>



|   <span data-ttu-id="9d026-965">Attribut</span><span class="sxs-lookup"><span data-stu-id="9d026-965">Attribute</span></span>        |   <span data-ttu-id="9d026-966">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-966">Description</span></span>                                                                                                                                                                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d026-967">FitPath</span><span class="sxs-lookup"><span data-stu-id="9d026-967">FitPath</span></span>  | <span data-ttu-id="9d026-968">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-968">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d026-969">Dimensionne le texte pour remplir le tracé sur lequel il se trouve.</span><span class="sxs-lookup"><span data-stu-id="9d026-969">Sizes the text to fill the path it lies out on.</span></span>                                 |
| <span data-ttu-id="9d026-970">FitShape</span><span class="sxs-lookup"><span data-stu-id="9d026-970">FitShape</span></span> | <span data-ttu-id="9d026-971">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-971">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d026-972">Étire le tracé du texte vers les bords de la zone de forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-972">Stretches the text path out to the edges of the shape box.</span></span>                      |
| <span data-ttu-id="9d026-973">Activé</span><span class="sxs-lookup"><span data-stu-id="9d026-973">On</span></span>       | <span data-ttu-id="9d026-974">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-974">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d026-975">Détermine si les chemins d’accès aux caractères sont affichés ou non.</span><span class="sxs-lookup"><span data-stu-id="9d026-975">Determines whether the character paths are displayed or not.</span></span>                    |
| <span data-ttu-id="9d026-976">String</span><span class="sxs-lookup"><span data-stu-id="9d026-976">String</span></span>   | <span data-ttu-id="9d026-977">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="9d026-977">String.</span></span> <span data-ttu-id="9d026-978">Texte à afficher sous la forme d’un tracé de texte.</span><span class="sxs-lookup"><span data-stu-id="9d026-978">The text to render as a text path.</span></span>                                                                                    |
| <span data-ttu-id="9d026-979">SupprEspace</span><span class="sxs-lookup"><span data-stu-id="9d026-979">Trim</span></span>     | <span data-ttu-id="9d026-980">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-980">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d026-981">Supprime tout espace supplémentaire réservé pour les jambages ascendants et descendants s’il n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="9d026-981">Removes any additional space reserved for ascenders and descenders if not used.</span></span> |
| <span data-ttu-id="9d026-982">Cadencé</span><span class="sxs-lookup"><span data-stu-id="9d026-982">XScale</span></span>   | <span data-ttu-id="9d026-983">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-983">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d026-984">Utilisez une mesure x droite au lieu de mesurer le long du tracé.</span><span class="sxs-lookup"><span data-stu-id="9d026-984">Use straight x measurement instead of measuring along the path.</span></span>                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a><span data-ttu-id="9d026-985">Types de données utilisés dans le modèle d’objet VML</span><span class="sxs-lookup"><span data-stu-id="9d026-985">Data Types Used in the VML Object Model</span></span>

<span data-ttu-id="9d026-986">Les types de données suivants sont utilisés par le modèle objet VML.</span><span class="sxs-lookup"><span data-stu-id="9d026-986">The following data types are used by the VML Object Model.</span></span>

-   [<span data-ttu-id="9d026-987">Double</span><span class="sxs-lookup"><span data-stu-id="9d026-987">Double</span></span>](/windows)
-   [<span data-ttu-id="9d026-988">Fixe</span><span class="sxs-lookup"><span data-stu-id="9d026-988">Fixed</span></span>](/windows)
-   [<span data-ttu-id="9d026-989">Integer</span><span class="sxs-lookup"><span data-stu-id="9d026-989">Integer</span></span>](/windows)
-   [<span data-ttu-id="9d026-990">IVgAdjustments</span><span class="sxs-lookup"><span data-stu-id="9d026-990">IVgAdjustments</span></span>](/windows)
-   [<span data-ttu-id="9d026-991">IVgColor</span><span class="sxs-lookup"><span data-stu-id="9d026-991">IVgColor</span></span>](/windows)
-   [<span data-ttu-id="9d026-992">IVgEquation</span><span class="sxs-lookup"><span data-stu-id="9d026-992">IVgEquation</span></span>](/windows)
-   [<span data-ttu-id="9d026-993">IVgFixedRectangle</span><span class="sxs-lookup"><span data-stu-id="9d026-993">IVgFixedRectangle</span></span>](/windows)
-   [<span data-ttu-id="9d026-994">IVgFixedRectangleArray</span><span class="sxs-lookup"><span data-stu-id="9d026-994">IVgFixedRectangleArray</span></span>](/windows)
-   [<span data-ttu-id="9d026-995">IVgFormula</span><span class="sxs-lookup"><span data-stu-id="9d026-995">IVgFormula</span></span>](/windows)
-   [<span data-ttu-id="9d026-996">IVgFormulas</span><span class="sxs-lookup"><span data-stu-id="9d026-996">IVgFormulas</span></span>](/windows)
-   [<span data-ttu-id="9d026-997">IVgGradientColorArray</span><span class="sxs-lookup"><span data-stu-id="9d026-997">IVgGradientColorArray</span></span>](/windows)
-   [<span data-ttu-id="9d026-998">IVgPoints</span><span class="sxs-lookup"><span data-stu-id="9d026-998">IVgPoints</span></span>](/windows)
-   [<span data-ttu-id="9d026-999">IVgSkewMatrix</span><span class="sxs-lookup"><span data-stu-id="9d026-999">IVgSkewMatrix</span></span>](/windows)
-   [<span data-ttu-id="9d026-1000">IVgSkewOffset</span><span class="sxs-lookup"><span data-stu-id="9d026-1000">IVgSkewOffset</span></span>](/windows)
-   [<span data-ttu-id="9d026-1001">IVgVector2D</span><span class="sxs-lookup"><span data-stu-id="9d026-1001">IVgVector2D</span></span>](/windows)
-   [<span data-ttu-id="9d026-1002">IVgVector3D</span><span class="sxs-lookup"><span data-stu-id="9d026-1002">IVgVector3D</span></span>](/windows)
-   [<span data-ttu-id="9d026-1003">Durée</span><span class="sxs-lookup"><span data-stu-id="9d026-1003">Length</span></span>](/windows)
-   <span data-ttu-id="9d026-1004">[Unité](/windows) :</span><span class="sxs-lookup"><span data-stu-id="9d026-1004">[Measure](/windows)</span></span>
-   [<span data-ttu-id="9d026-1005">Chaîne</span><span class="sxs-lookup"><span data-stu-id="9d026-1005">String</span></span>](/windows)
-   [<span data-ttu-id="9d026-1006">VgBlackWhiteMode</span><span class="sxs-lookup"><span data-stu-id="9d026-1006">VgBlackWhiteMode</span></span>](/windows)
-   [<span data-ttu-id="9d026-1007">VgFraction</span><span class="sxs-lookup"><span data-stu-id="9d026-1007">VgFraction</span></span>](/windows)
-   [<span data-ttu-id="9d026-1008">VgTriState</span><span class="sxs-lookup"><span data-stu-id="9d026-1008">VgTriState</span></span>](/windows)

<span data-ttu-id="9d026-1009">**Double (type de données)**</span><span class="sxs-lookup"><span data-stu-id="9d026-1009">**Double data type**</span></span>

<span data-ttu-id="9d026-1010">Entier double précision avec une plage comprise entre-Infinity et Infinity.</span><span class="sxs-lookup"><span data-stu-id="9d026-1010">A double precision integer with range from -infinity to infinity.</span></span>

<span data-ttu-id="9d026-1011">**Type de données fixe**</span><span class="sxs-lookup"><span data-stu-id="9d026-1011">**Fixed data type**</span></span>

<span data-ttu-id="9d026-1012">Nombre à virgule flottante avec une plage comprise entre-32 766,0 et 32 766,0.</span><span class="sxs-lookup"><span data-stu-id="9d026-1012">Floating point number with range from -32,766.0 to 32,766.0.</span></span>

<span data-ttu-id="9d026-1013">**Integer (type de données)**</span><span class="sxs-lookup"><span data-stu-id="9d026-1013">**Integer data type**</span></span>

<span data-ttu-id="9d026-1014">Entier compris entre-Infinity et Infinity.</span><span class="sxs-lookup"><span data-stu-id="9d026-1014">An integer with a range from -infinity to infinity.</span></span>

<span data-ttu-id="9d026-1015">**Type de données IVgAdjustments**</span><span class="sxs-lookup"><span data-stu-id="9d026-1015">**IVgAdjustments data type**</span></span>

<span data-ttu-id="9d026-1016">Collection d’ajustements d’une forme qui peut être utilisée pour modifier les dimensions d’une forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-1016">Collection of adjustments to a shape that can be used to change the dimensions of a shape.</span></span> <span data-ttu-id="9d026-1017">Les ajustements peuvent être utilisés en tant qu’espaces réservés temporaires ou pour une raison quelconque, vous pouvez utiliser des variables.</span><span class="sxs-lookup"><span data-stu-id="9d026-1017">Adjustments can be used as temporary placeholders or for any reason you would use variables.</span></span> <span data-ttu-id="9d026-1018">La collection ne contient que 8 ajustements.</span><span class="sxs-lookup"><span data-stu-id="9d026-1018">There are only 8 adjustments in the collection.</span></span>



| <span data-ttu-id="9d026-1019">Attribut</span><span class="sxs-lookup"><span data-stu-id="9d026-1019">Attribute</span></span> | <span data-ttu-id="9d026-1020">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-1020">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d026-1021">Exists</span><span class="sxs-lookup"><span data-stu-id="9d026-1021">Exists</span></span>     | <span data-ttu-id="9d026-1022">[IVgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-1022">[IVgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9d026-1023">Détermine si un ajustement spécifié existe.</span><span class="sxs-lookup"><span data-stu-id="9d026-1023">Determines whether a specified adjustment exists.</span></span> <span data-ttu-id="9d026-1024">Notez qu’un index doit être utilisé ; en d’autres cas, Exists (Item) doit être utilisé pour récupérer l’existence d’un élément.</span><span class="sxs-lookup"><span data-stu-id="9d026-1024">Note that an index must be used; that is, exists( item ) must be used to retrieve the existence of an item.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="9d026-1025">Élément</span><span class="sxs-lookup"><span data-stu-id="9d026-1025">Item</span></span>       | <span data-ttu-id="9d026-1026">[Long](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1026">[Long](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1027">Tableau d’ajustements indexés de 0 à 7.</span><span class="sxs-lookup"><span data-stu-id="9d026-1027">Array of adjustments indexed from 0 to 7.</span></span> <span data-ttu-id="9d026-1028">Notez que les ajustements peuvent être spécifiés pour SPARC. autrement dit, les valeurs de tableau intermédiaire ne peuvent pas toujours être remplies.</span><span class="sxs-lookup"><span data-stu-id="9d026-1028">Note that adjustments may be sparcely specified; that is, intermediate array values may not always be filled.</span></span> <span data-ttu-id="9d026-1029">Par exemple, les éléments 1, 3 et 5 peuvent avoir des valeurs pour une longueur de 3, avec l’élément (0), l’élément (2) et l’élément (4) spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9d026-1029">For example, item 1, 3, and 5 could have values for a length of 3, with item(0), item(2), and item(4) specified.</span></span> <span data-ttu-id="9d026-1030">Pour voir si un élément existe, utilisez l’attribut exists.</span><span class="sxs-lookup"><span data-stu-id="9d026-1030">To see if an item exists, use the Exists attribute.</span></span> |
| <span data-ttu-id="9d026-1031">Longueur</span><span class="sxs-lookup"><span data-stu-id="9d026-1031">Length</span></span>     | <span data-ttu-id="9d026-1032">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1032">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1033">Nombre d’ajustements.</span><span class="sxs-lookup"><span data-stu-id="9d026-1033">Number of adjustments.</span></span> <span data-ttu-id="9d026-1034">Ne peut pas être supérieur à 8.</span><span class="sxs-lookup"><span data-stu-id="9d026-1034">Can be no greater than 8.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="9d026-1035">Value</span><span class="sxs-lookup"><span data-stu-id="9d026-1035">Value</span></span>      | <span data-ttu-id="9d026-1036">[Chaîne](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1036">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1037">Représentation textuelle des valeurs numériques, avec des virgules entre chaque nombre.</span><span class="sxs-lookup"><span data-stu-id="9d026-1037">Text representation of numeric values, with commas between each number.</span></span>                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="9d026-1038">**IVgColor**</span><span class="sxs-lookup"><span data-stu-id="9d026-1038">**IVgColor**</span></span>

<span data-ttu-id="9d026-1039">Spécifie une couleur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1039">Specifies a color.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d026-1040">Attributs</span><span class="sxs-lookup"><span data-stu-id="9d026-1040">Attributes</span></span></th>
<th><span data-ttu-id="9d026-1041">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-1041">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-1042">RGB</span><span class="sxs-lookup"><span data-stu-id="9d026-1042">RGB</span></span></td>
<td><span data-ttu-id="9d026-1043"><strong>VgRGBType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1043"><strong>VgRGBType</strong>.</span></span> <span data-ttu-id="9d026-1044">Valeur RVB (longue) de la couleur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1044">RGB value (Long) of the color.</span></span> <span data-ttu-id="9d026-1045">Valide uniquement si le type est RVB.</span><span class="sxs-lookup"><span data-stu-id="9d026-1045">Only valid if Type is RGB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1046">R</span><span class="sxs-lookup"><span data-stu-id="9d026-1046">R</span></span></td>
<td><span data-ttu-id="9d026-1047"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1047"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="9d026-1048">Composant rouge de la couleur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1048">Red component of the color.</span></span> <span data-ttu-id="9d026-1049">Peut être compris entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="9d026-1049">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1050">G</span><span class="sxs-lookup"><span data-stu-id="9d026-1050">G</span></span></td>
<td><span data-ttu-id="9d026-1051"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1051"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="9d026-1052">Composant vert de la couleur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1052">Green component of the color.</span></span> <span data-ttu-id="9d026-1053">Peut être compris entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="9d026-1053">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1054">B</span><span class="sxs-lookup"><span data-stu-id="9d026-1054">B</span></span></td>
<td><span data-ttu-id="9d026-1055"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1055"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="9d026-1056">Composant bleu de la couleur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1056">Blue component of the color.</span></span> <span data-ttu-id="9d026-1057">Peut être compris entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="9d026-1057">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1058">String</span><span class="sxs-lookup"><span data-stu-id="9d026-1058">String</span></span></td>
<td><span data-ttu-id="9d026-1059"><a href="#data-types-used-in-the-vml-object-model">Chaîne</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1059"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="9d026-1060">Représentation textuelle de la couleur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1060">Text representation of the color.</span></span> <span data-ttu-id="9d026-1061">Les types de couleur nommés suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="9d026-1061">The following named color types are supported:</span></span>
<ul>
<li><span data-ttu-id="9d026-1062">Noir (#000000)</span><span class="sxs-lookup"><span data-stu-id="9d026-1062">Black (#000000)</span></span></li>
<li><span data-ttu-id="9d026-1063">Silver (#C0C0C0)</span><span class="sxs-lookup"><span data-stu-id="9d026-1063">Silver (#C0C0C0)</span></span></li>
<li><span data-ttu-id="9d026-1064">Gris (#808080)</span><span class="sxs-lookup"><span data-stu-id="9d026-1064">Gray (#808080)</span></span></li>
<li><span data-ttu-id="9d026-1065">Blanc (#FFFFFF)</span><span class="sxs-lookup"><span data-stu-id="9d026-1065">White (#FFFFFF)</span></span></li>
<li><span data-ttu-id="9d026-1066">Marron (#800000)</span><span class="sxs-lookup"><span data-stu-id="9d026-1066">Maroon (#800000)</span></span></li>
<li><span data-ttu-id="9d026-1067">Rouge (#FF0000)</span><span class="sxs-lookup"><span data-stu-id="9d026-1067">Red (#FF0000)</span></span></li>
<li><span data-ttu-id="9d026-1068">Violet (#800080)</span><span class="sxs-lookup"><span data-stu-id="9d026-1068">Purple (#800080)</span></span></li>
<li><span data-ttu-id="9d026-1069">Fuchsia (#FF00FF)</span><span class="sxs-lookup"><span data-stu-id="9d026-1069">Fuchsia (#FF00FF)</span></span></li>
<li><span data-ttu-id="9d026-1070">Vert (#008000)</span><span class="sxs-lookup"><span data-stu-id="9d026-1070">Green (#008000)</span></span></li>
<li><span data-ttu-id="9d026-1071">Chaux (#00FF00)</span><span class="sxs-lookup"><span data-stu-id="9d026-1071">Lime (#00FF00)</span></span></li>
<li><span data-ttu-id="9d026-1072">Vert olive (#808000)</span><span class="sxs-lookup"><span data-stu-id="9d026-1072">Olive (#808000)</span></span></li>
<li><span data-ttu-id="9d026-1073">Jaune (#FFFF00)</span><span class="sxs-lookup"><span data-stu-id="9d026-1073">Yellow (#FFFF00)</span></span></li>
<li><span data-ttu-id="9d026-1074">Bleu marine (#000080)</span><span class="sxs-lookup"><span data-stu-id="9d026-1074">Navy (#000080)</span></span></li>
<li><span data-ttu-id="9d026-1075">Bleu (#0000FF)</span><span class="sxs-lookup"><span data-stu-id="9d026-1075">Blue (#0000FF)</span></span></li>
<li><span data-ttu-id="9d026-1076">Bleu-vert (#008080)</span><span class="sxs-lookup"><span data-stu-id="9d026-1076">Teal (#008080)</span></span></li>
<li><span data-ttu-id="9d026-1077">Aqua (#00FFFF)</span><span class="sxs-lookup"><span data-stu-id="9d026-1077">Aqua (#00FFFF)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1078">Type</span><span class="sxs-lookup"><span data-stu-id="9d026-1078">Type</span></span></td>
<td><span data-ttu-id="9d026-1079"><strong>VgColorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1079"><strong>VgColorType</strong>.</span></span> <span data-ttu-id="9d026-1080">Type de couleur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1080">Type of color.</span></span> <span data-ttu-id="9d026-1081">L’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="9d026-1081">One of the following types:</span></span>
<ul>
<li><span data-ttu-id="9d026-1082">Mixte</span><span class="sxs-lookup"><span data-stu-id="9d026-1082">Mixed</span></span></li>
<li><span data-ttu-id="9d026-1083">named</span><span class="sxs-lookup"><span data-stu-id="9d026-1083">Named</span></span></li>
<li><span data-ttu-id="9d026-1084">RGB</span><span class="sxs-lookup"><span data-stu-id="9d026-1084">RGB</span></span></li>
<li><span data-ttu-id="9d026-1085">Schéma</span><span class="sxs-lookup"><span data-stu-id="9d026-1085">Scheme</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9d026-1086">**IVgEquation**</span><span class="sxs-lookup"><span data-stu-id="9d026-1086">**IVgEquation**</span></span>

<span data-ttu-id="9d026-1087">Équations utilisées pour les formules.</span><span class="sxs-lookup"><span data-stu-id="9d026-1087">Equations used for formulas.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-1088">Opération</span><span class="sxs-lookup"><span data-stu-id="9d026-1088">Operation</span></span></td>
<td><span data-ttu-id="9d026-1089"><strong>VgEquationOperationType</strong> Nom de l’opération à effectuer sur les paramètres.</span><span class="sxs-lookup"><span data-stu-id="9d026-1089"><strong>VgEquationOperationType</strong> Name of operation to perform on the parameters.</span></span> <span data-ttu-id="9d026-1090">Les opérations suivantes peuvent être utilisées dans une équation :</span><span class="sxs-lookup"><span data-stu-id="9d026-1090">The following operations can be used in an equation:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d026-1091">Opération</span><span class="sxs-lookup"><span data-stu-id="9d026-1091">Operation</span></span></th>
<th><span data-ttu-id="9d026-1092">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-1092">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-1093">Abs</span><span class="sxs-lookup"><span data-stu-id="9d026-1093">Abs</span></span></td>
<td><span data-ttu-id="9d026-1094">Valeur absolue.</span><span class="sxs-lookup"><span data-stu-id="9d026-1094">Absolute value.</span></span> <br/> <span data-ttu-id="9d026-1095"><strong>ABS</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="9d026-1095"><strong>abs</strong>(v)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1096">Atan2</span><span class="sxs-lookup"><span data-stu-id="9d026-1096">Atan2</span></span></td>
<td><span data-ttu-id="9d026-1097">Arithmétique polaire--résultats en unités FD (degrés multiplié par 65536).</span><span class="sxs-lookup"><span data-stu-id="9d026-1097">Polar arithmetic--results in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="9d026-1098"><strong>atan2</strong>(P1, v)</span><span class="sxs-lookup"><span data-stu-id="9d026-1098"><strong>atan2</strong>(p1,v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1099">Cos</span><span class="sxs-lookup"><span data-stu-id="9d026-1099">Cos</span></span></td>
<td><span data-ttu-id="9d026-1100">Cosinus, argument en unités FD (degrés multiplié par 65536).</span><span class="sxs-lookup"><span data-stu-id="9d026-1100">Cosine, argument in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="9d026-1101">v \* <strong>COS</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="9d026-1101">v \* <strong>cos</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1102">Cosatan2</span><span class="sxs-lookup"><span data-stu-id="9d026-1102">Cosatan2</span></span></td>
<td><span data-ttu-id="9d026-1103">Préserve la précision complète dans le calcul intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="9d026-1103">Preserves full accuracy in intermediate calculation.</span></span><br/> <span data-ttu-id="9d026-1104">v \* <strong>cos (atan2 (</strong> P2, P1 <strong>))</strong></span><span class="sxs-lookup"><span data-stu-id="9d026-1104">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1105">Ellipse</span><span class="sxs-lookup"><span data-stu-id="9d026-1105">Ellipse</span></span></td>
<td><span data-ttu-id="9d026-1106">Ellipse</span><span class="sxs-lookup"><span data-stu-id="9d026-1106">Ellipse</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1107">Si</span><span class="sxs-lookup"><span data-stu-id="9d026-1107">If</span></span></td>
<td><span data-ttu-id="9d026-1108">Test de condition if.</span><span class="sxs-lookup"><span data-stu-id="9d026-1108">If Condition test.</span></span> <span data-ttu-id="9d026-1109">v > 0 <strong>?</strong></span><span class="sxs-lookup"><span data-stu-id="9d026-1109">v > 0 <strong>?</strong></span></span> <span data-ttu-id="9d026-1110">P1 : P2</span><span class="sxs-lookup"><span data-stu-id="9d026-1110">p1 : p2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1111">Max</span><span class="sxs-lookup"><span data-stu-id="9d026-1111">Max</span></span></td>
<td><span data-ttu-id="9d026-1112">Valeur la plus grande de deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="9d026-1112">The greater of two values.</span></span> <br/> <span data-ttu-id="9d026-1113"><strong>Max</strong>(v, P1)</span><span class="sxs-lookup"><span data-stu-id="9d026-1113"><strong>max</strong>(v,p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1114">ExtracChaîne</span><span class="sxs-lookup"><span data-stu-id="9d026-1114">Mid</span></span></td>
<td><span data-ttu-id="9d026-1115">Moyenne (v + P1)/2</span><span class="sxs-lookup"><span data-stu-id="9d026-1115">Average ( v + p1)/2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1116">Min</span><span class="sxs-lookup"><span data-stu-id="9d026-1116">Min</span></span></td>
<td><span data-ttu-id="9d026-1117">La plus petite des deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="9d026-1117">The lesser of two values.</span></span> <span data-ttu-id="9d026-1118"><strong>min</strong>(v, P1)</span><span class="sxs-lookup"><span data-stu-id="9d026-1118"><strong>min</strong>(v,p1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1119">Mod</span><span class="sxs-lookup"><span data-stu-id="9d026-1119">Mod</span></span></td>
<td><span data-ttu-id="9d026-1120">Modulo.</span><span class="sxs-lookup"><span data-stu-id="9d026-1120">Modulus.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1121">Produit</span><span class="sxs-lookup"><span data-stu-id="9d026-1121">Product</span></span></td>
<td><span data-ttu-id="9d026-1122">Utilisé pour la multiplication et la Division.</span><span class="sxs-lookup"><span data-stu-id="9d026-1122">Used for multiplication and division.</span></span> <span data-ttu-id="9d026-1123">v \* P1/P2</span><span class="sxs-lookup"><span data-stu-id="9d026-1123">v \* p1 / p2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1124">Sin</span><span class="sxs-lookup"><span data-stu-id="9d026-1124">Sin</span></span></td>
<td><span data-ttu-id="9d026-1125">Sinus, argument en unités FD (degrés multiplié par 65536).</span><span class="sxs-lookup"><span data-stu-id="9d026-1125">Sine, argument in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="9d026-1126">v \* <strong>Sin</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="9d026-1126">v \* <strong>sin</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1127">Sinatan2</span><span class="sxs-lookup"><span data-stu-id="9d026-1127">Sinatan2</span></span></td>
<td><span data-ttu-id="9d026-1128">Préserve la précision complète dans le calcul intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="9d026-1128">Preserves full accuracy in intermediate calculation.</span></span> <span data-ttu-id="9d026-1129">v \* <strong>Sin</strong>(<strong>atan2</strong>(P2, P1))</span><span class="sxs-lookup"><span data-stu-id="9d026-1129">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1130">Sqrt</span><span class="sxs-lookup"><span data-stu-id="9d026-1130">Sqrt</span></span></td>
<td><span data-ttu-id="9d026-1131">Le résultat est positif et arrondit à la valeur inférieure.</span><span class="sxs-lookup"><span data-stu-id="9d026-1131">Result is positive and rounds down.</span></span> <br/> <span data-ttu-id="9d026-1132"><strong>sqrt</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="9d026-1132"><strong>sqrt</strong>(v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1133">Sum</span><span class="sxs-lookup"><span data-stu-id="9d026-1133">Sum</span></span></td>
<td><span data-ttu-id="9d026-1134">Utilisé pour l’addition et la soustraction.</span><span class="sxs-lookup"><span data-stu-id="9d026-1134">Used for addition and subtraction.</span></span><br/> <span data-ttu-id="9d026-1135">v + P1 P2</span><span class="sxs-lookup"><span data-stu-id="9d026-1135">v + p1 p2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1136">Sumangle</span><span class="sxs-lookup"><span data-stu-id="9d026-1136">Sumangle</span></span></td>
<td><span data-ttu-id="9d026-1137">Angle existant (mis à l’échelle par 65536), où P1 et P2 sont exprimés en degrés.</span><span class="sxs-lookup"><span data-stu-id="9d026-1137">Existing angle (scaled by 65536), where p1 and p2 are in degrees.</span></span><br/> <span data-ttu-id="9d026-1138">v + P1 \* 65536 + P2 \* 65536</span><span class="sxs-lookup"><span data-stu-id="9d026-1138">v + p1 \* 65536 + p2 \* 65536</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1139">Tan</span><span class="sxs-lookup"><span data-stu-id="9d026-1139">Tan</span></span></td>
<td><span data-ttu-id="9d026-1140">Tangente, l’argument est en unités FD (degrés multiplié par 65536).</span><span class="sxs-lookup"><span data-stu-id="9d026-1140">Tangent, argument is in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="9d026-1141">v \* Tan (P1)</span><span class="sxs-lookup"><span data-stu-id="9d026-1141">v \* tan( p1 )</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1142">Val</span><span class="sxs-lookup"><span data-stu-id="9d026-1142">Val</span></span></td>
<td><span data-ttu-id="9d026-1143">Définit une valeur de repère à partir d’une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1143">Defines a guide value from some other value.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1144">Param1</span><span class="sxs-lookup"><span data-stu-id="9d026-1144">Param1</span></span></td>
<td><span data-ttu-id="9d026-1145"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1145"><strong>Integer</strong>.</span></span> <span data-ttu-id="9d026-1146">Premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="9d026-1146">The first parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1147">Paramtype1</span><span class="sxs-lookup"><span data-stu-id="9d026-1147">Paramtype1</span></span></td>
<td><span data-ttu-id="9d026-1148"><strong>VgFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1148"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="9d026-1149">Type du premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="9d026-1149">The type of the first parameter.</span></span> <span data-ttu-id="9d026-1150">Les valeurs suivantes sont admises :</span><span class="sxs-lookup"><span data-stu-id="9d026-1150">The following values are supported:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d026-1151">Type</span><span class="sxs-lookup"><span data-stu-id="9d026-1151">Type</span></span></th>
<th><span data-ttu-id="9d026-1152">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-1152">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-1153">Value</span><span class="sxs-lookup"><span data-stu-id="9d026-1153">Value</span></span></td>
<td><span data-ttu-id="9d026-1154">Le paramètre est une valeur simple.</span><span class="sxs-lookup"><span data-stu-id="9d026-1154">Parameter is simple value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1155">AdjustmentReference</span><span class="sxs-lookup"><span data-stu-id="9d026-1155">AdjustmentReference</span></span></td>
<td><span data-ttu-id="9d026-1156">Le paramètre est une référence à un ajustement.</span><span class="sxs-lookup"><span data-stu-id="9d026-1156">Parameter is a reference to an adjustment.</span></span> <span data-ttu-id="9d026-1157">Par exemple, si le premier paramètre est 1, la valeur du premier ajustement sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="9d026-1157">For example, if the first parameter is 1, then the value of the first adjustment will be used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1158">FormulaReference</span><span class="sxs-lookup"><span data-stu-id="9d026-1158">FormulaReference</span></span></td>
<td><span data-ttu-id="9d026-1159">Le paramètre est le résultat d’une référence au résultat d’une formule précédente.</span><span class="sxs-lookup"><span data-stu-id="9d026-1159">Parameter is the result of a reference to the result of a previous formula.</span></span> <span data-ttu-id="9d026-1160">Par exemple, si le premier paramètre a la valeur 2, le résultat de la formule 2 sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="9d026-1160">For example, if the first parameter is 2, then the result of formula 2 will be used.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1161">Param2</span><span class="sxs-lookup"><span data-stu-id="9d026-1161">Param2</span></span></td>
<td><span data-ttu-id="9d026-1162"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1162"><strong>Integer</strong>.</span></span> <span data-ttu-id="9d026-1163">Deuxième paramètre.</span><span class="sxs-lookup"><span data-stu-id="9d026-1163">The second parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1164">Paramtype2</span><span class="sxs-lookup"><span data-stu-id="9d026-1164">Paramtype2</span></span></td>
<td><span data-ttu-id="9d026-1165"><strong>VgFormulaParamType</strong> Type de paramètre 2.</span><span class="sxs-lookup"><span data-stu-id="9d026-1165"><strong>VgFormulaParamType</strong> The type of parameter 2.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1166">Val</span><span class="sxs-lookup"><span data-stu-id="9d026-1166">Val</span></span></td>
<td><span data-ttu-id="9d026-1167"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1167"><strong>Integer</strong>.</span></span> <span data-ttu-id="9d026-1168">Résultat.</span><span class="sxs-lookup"><span data-stu-id="9d026-1168">The result.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1169">Valtype2</span><span class="sxs-lookup"><span data-stu-id="9d026-1169">Valtype2</span></span></td>
<td><span data-ttu-id="9d026-1170"><strong>VgFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1170"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="9d026-1171">Type du résultat.</span><span class="sxs-lookup"><span data-stu-id="9d026-1171">The type of the result.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9d026-1172">**IVgFixedRectangle**</span><span class="sxs-lookup"><span data-stu-id="9d026-1172">**IVgFixedRectangle**</span></span>

<span data-ttu-id="9d026-1173">Spécifie un rectangle fixe.</span><span class="sxs-lookup"><span data-stu-id="9d026-1173">Specifies a fixed rectangle.</span></span>



| <span data-ttu-id="9d026-1174">Attribut</span><span class="sxs-lookup"><span data-stu-id="9d026-1174">Attribute</span></span> | <span data-ttu-id="9d026-1175">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-1175">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d026-1176">Value</span><span class="sxs-lookup"><span data-stu-id="9d026-1176">Value</span></span>      | <span data-ttu-id="9d026-1177">[Chaîne](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1177">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1178">Valeur de texte spécifiant le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="9d026-1178">Text value specifying the path.</span></span>         |
| <span data-ttu-id="9d026-1179">Gauche</span><span class="sxs-lookup"><span data-stu-id="9d026-1179">Left</span></span>       | <span data-ttu-id="9d026-1180">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1180">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1181">Coordonnée la plus à gauche du rectangle.</span><span class="sxs-lookup"><span data-stu-id="9d026-1181">Leftmost coordinate of the rectangle.</span></span>   |
| <span data-ttu-id="9d026-1182">Haut</span><span class="sxs-lookup"><span data-stu-id="9d026-1182">Top</span></span>        | <span data-ttu-id="9d026-1183">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1183">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1184">Coordonnée la plus grande du rectangle.</span><span class="sxs-lookup"><span data-stu-id="9d026-1184">Topmost coordinate of the rectangle.</span></span>    |
| <span data-ttu-id="9d026-1185">Right</span><span class="sxs-lookup"><span data-stu-id="9d026-1185">Right</span></span>      | <span data-ttu-id="9d026-1186">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1186">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1187">Coordonnée la plus à droite du rectangle.</span><span class="sxs-lookup"><span data-stu-id="9d026-1187">Rightmost coordinate of the rectangle.</span></span>  |
| <span data-ttu-id="9d026-1188">Bas</span><span class="sxs-lookup"><span data-stu-id="9d026-1188">Bottom</span></span>     | <span data-ttu-id="9d026-1189">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1189">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1190">Coordonnée la plus basse du rectangle.</span><span class="sxs-lookup"><span data-stu-id="9d026-1190">Bottommost coordinate of the rectangle.</span></span> |



 

<span data-ttu-id="9d026-1191">**IVgFixedRectangleArray**</span><span class="sxs-lookup"><span data-stu-id="9d026-1191">**IVgFixedRectangleArray**</span></span>

<span data-ttu-id="9d026-1192">Tableau de rectangles fixes.</span><span class="sxs-lookup"><span data-stu-id="9d026-1192">Array of fixed rectangles.</span></span>



| <span data-ttu-id="9d026-1193">Attribut</span><span class="sxs-lookup"><span data-stu-id="9d026-1193">Attribute</span></span> | <span data-ttu-id="9d026-1194">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-1194">Description</span></span>                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d026-1195">Value</span><span class="sxs-lookup"><span data-stu-id="9d026-1195">Value</span></span>      | <span data-ttu-id="9d026-1196">[Chaîne](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1196">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1197">Représentation textuelle d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="9d026-1197">Text representation of array.</span></span>                           |
| <span data-ttu-id="9d026-1198">Longueur</span><span class="sxs-lookup"><span data-stu-id="9d026-1198">Length</span></span>     | <span data-ttu-id="9d026-1199">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1199">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1200">Nombre de rectangles dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="9d026-1200">Number of rectangles in this array.</span></span>                    |
| <span data-ttu-id="9d026-1201">Élément</span><span class="sxs-lookup"><span data-stu-id="9d026-1201">Item</span></span>       | <span data-ttu-id="9d026-1202">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1202">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1203">Objet Rectangle à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="9d026-1203">The rectangle object at the specified index.</span></span> |



 

<span data-ttu-id="9d026-1204">Type de données **IVgFormula**</span><span class="sxs-lookup"><span data-stu-id="9d026-1204">**IVgFormula** data type</span></span>

<span data-ttu-id="9d026-1205">Définitions des formules qui peuvent varier le tracé d’une forme ou être utilisées à d’autres fins de calcul.</span><span class="sxs-lookup"><span data-stu-id="9d026-1205">Definitions for formulas that can vary the path of a shape or be used for other calculation purposes.</span></span> <span data-ttu-id="9d026-1206">Les formules peuvent être basées sur l’attribut **Adj** d’une forme, ce qui peut changer.</span><span class="sxs-lookup"><span data-stu-id="9d026-1206">Formulas can be based on the **Adj** attribute of a shape, which can change.</span></span> <span data-ttu-id="9d026-1207">Les formules peuvent également faire référence à d’autres formules.</span><span class="sxs-lookup"><span data-stu-id="9d026-1207">Formulas can reference other formulas as well.</span></span>



| <span data-ttu-id="9d026-1208">Attribut</span><span class="sxs-lookup"><span data-stu-id="9d026-1208">Attribute</span></span>| <span data-ttu-id="9d026-1209">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-1209">Description</span></span>                                           |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d026-1210">Eqn</span><span class="sxs-lookup"><span data-stu-id="9d026-1210">Eqn</span></span>        | <span data-ttu-id="9d026-1211">[IVgEquation](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1211">[IVgEquation](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1212">Chaque formule définit une valeur unique comme résultat de l’évaluation de l’expression.</span><span class="sxs-lookup"><span data-stu-id="9d026-1212">Each formula defines a single value as the result of the evaluation of the expression.</span></span> <span data-ttu-id="9d026-1213">L’expression est définie par cet attribut et présente la forme générale d’une opération suivie de jusqu’à trois arguments, qui peuvent être des valeurs d’ajustement (par exemple, \# 2), des résultats de formules antérieures (par exemple, @2 ), des nombres fixes ou des valeurs prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="9d026-1213">The expression is defined by this attribute and has the general form of an operation followed by up to three arguments, which may be adjustment values (e.g., \#2), the results of earlier formulas (e.g., @2), fixed numbers, or predefined values.</span></span> |



 

<span data-ttu-id="9d026-1214">**Type de données IVgFormulas**</span><span class="sxs-lookup"><span data-stu-id="9d026-1214">**IVgFormulas data type**</span></span>

<span data-ttu-id="9d026-1215">Collection d’objets de formule.</span><span class="sxs-lookup"><span data-stu-id="9d026-1215">A collection of formula objects.</span></span>



| <span data-ttu-id="9d026-1216">Attribut</span><span class="sxs-lookup"><span data-stu-id="9d026-1216">Attribute</span></span> | <span data-ttu-id="9d026-1217">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-1217">Description</span></span>                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d026-1218">Longueur</span><span class="sxs-lookup"><span data-stu-id="9d026-1218">Length</span></span>     | <span data-ttu-id="9d026-1219">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1219">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1220">Nombre d’objets de formule dans la collection.</span><span class="sxs-lookup"><span data-stu-id="9d026-1220">Number of formula objects in collection.</span></span>                                                |
| <span data-ttu-id="9d026-1221">Élément</span><span class="sxs-lookup"><span data-stu-id="9d026-1221">Item</span></span>       | <span data-ttu-id="9d026-1222">[IVgFormula](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1222">[IVgFormula](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1223">Formule spécifique.</span><span class="sxs-lookup"><span data-stu-id="9d026-1223">A specific formula.</span></span> <span data-ttu-id="9d026-1224">Notez que le tableau de formules peut être hérité de le type de forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-1224">Note that the formula array may be inherited fom the shape type.</span></span> |



 

<span data-ttu-id="9d026-1225">**IVgGradientColorArray**</span><span class="sxs-lookup"><span data-stu-id="9d026-1225">**IVgGradientColorArray**</span></span>

<span data-ttu-id="9d026-1226">Tableau de couleurs qui définissent un dégradé (plage de couleurs fusionnée).</span><span class="sxs-lookup"><span data-stu-id="9d026-1226">An array of colors that define a gradient (blended range of colors).</span></span>



| <span data-ttu-id="9d026-1227">Attribut</span><span class="sxs-lookup"><span data-stu-id="9d026-1227">Attribute</span></span> | <span data-ttu-id="9d026-1228">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-1228">Description</span></span>                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d026-1229">Value</span><span class="sxs-lookup"><span data-stu-id="9d026-1229">Value</span></span>      | <span data-ttu-id="9d026-1230">[Chaîne](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1230">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1231">Spécifie le tableau de couleurs ; par exemple, «Red. 2 ; vert. 4 ; noir. 7»</span><span class="sxs-lookup"><span data-stu-id="9d026-1231">Specifies the array of colors; for example, "red .2; green .4; black .7"</span></span> |
| <span data-ttu-id="9d026-1232">Longueur</span><span class="sxs-lookup"><span data-stu-id="9d026-1232">Length</span></span>     | <span data-ttu-id="9d026-1233">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1233">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1234">Nombre de couleurs dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="9d026-1234">Number of colors in the array.</span></span>                                          |



 



| <span data-ttu-id="9d026-1235">Méthode</span><span class="sxs-lookup"><span data-stu-id="9d026-1235">Method</span></span>     | <span data-ttu-id="9d026-1236">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-1236">Description</span></span>                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d026-1237">AddColor</span><span class="sxs-lookup"><span data-stu-id="9d026-1237">AddColor</span></span>    | <span data-ttu-id="9d026-1238">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-1238">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="9d026-1239">Ajoute une nouvelle couleur au point de terminaison spécifié par fraction.</span><span class="sxs-lookup"><span data-stu-id="9d026-1239">Adds new color at endpoint specified by fraction.</span></span> <span data-ttu-id="9d026-1240">La nouvelle couleur est blanche par défaut et est la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9d026-1240">The new color is white by default and is the return value.</span></span> <span data-ttu-id="9d026-1241">La couleur peut ensuite être modifiée par référence.</span><span class="sxs-lookup"><span data-stu-id="9d026-1241">The color can then be changed by reference.</span></span> |
| <span data-ttu-id="9d026-1242">RemoveColor</span><span class="sxs-lookup"><span data-stu-id="9d026-1242">RemoveColor</span></span> | <span data-ttu-id="9d026-1243">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-1243">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="9d026-1244">Supprime une couleur au point de terminaison spécifié par fraction.</span><span class="sxs-lookup"><span data-stu-id="9d026-1244">Removes a color at endpoint specified by fraction.</span></span> <span data-ttu-id="9d026-1245">Remarque : si 0,0 ou 1,0 n’existe pas, il est implicite et le blanc de couleur est utilisé à ce stade.</span><span class="sxs-lookup"><span data-stu-id="9d026-1245">Note: if 0.0 or 1.0 does not exist, it is implied and the color white is used at that point.</span></span>          |



 

<span data-ttu-id="9d026-1246">**Type de données IVgPoints**</span><span class="sxs-lookup"><span data-stu-id="9d026-1246">**IVgPoints datatype**</span></span>

<span data-ttu-id="9d026-1247">Tableau de points qui définissent une forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-1247">Array of points that define a shape.</span></span>



| <span data-ttu-id="9d026-1248">Attribut</span><span class="sxs-lookup"><span data-stu-id="9d026-1248">Attribute</span></span> | <span data-ttu-id="9d026-1249">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-1249">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d026-1250">Value</span><span class="sxs-lookup"><span data-stu-id="9d026-1250">Value</span></span>      | <span data-ttu-id="9d026-1251">[Chaîne](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1251">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1252">Représentation textuelle d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="9d026-1252">Text representation of array.</span></span>           |
| <span data-ttu-id="9d026-1253">Longueur</span><span class="sxs-lookup"><span data-stu-id="9d026-1253">Length</span></span>     | <span data-ttu-id="9d026-1254">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1254">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9d026-1255">Nombre de points dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="9d026-1255">Number of points in this array.</span></span>        |
| <span data-ttu-id="9d026-1256">Élément</span><span class="sxs-lookup"><span data-stu-id="9d026-1256">Item</span></span>       | <span data-ttu-id="9d026-1257">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9d026-1257">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9d026-1258">Point au niveau de l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="9d026-1258">The point at the specified index.</span></span> |



 

<span data-ttu-id="9d026-1259">**Type de données IVgSkewMatrix**</span><span class="sxs-lookup"><span data-stu-id="9d026-1259">**IVgSkewMatrix datatype**</span></span>

<span data-ttu-id="9d026-1260">Matrice utilisée pour incliner des formes, une matrice de transformation de perspective sous la forme "*Sxx, SXY, syx, SYY, PX, py* " \[ *s* = Scale, *p* = perspective \] .</span><span class="sxs-lookup"><span data-stu-id="9d026-1260">A matrix used for skewing shapes, a perspective transform matrix in the form, "*sxx,sxy,syx,syy,px,py* " \[*s* =scale, *p* =perspective\].</span></span> <span data-ttu-id="9d026-1261">Si le décalage est en unités absolues, alors *PX, py* sont en unités UME ^-1 ; Sinon, il s’agit d’une fraction inverse de la taille de la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-1261">If offset is in absolute units, then *px,py* are in emu ^-1 units; otherwise they are an inverse fraction of shape size.</span></span>



| <span data-ttu-id="9d026-1262">Attribut</span><span class="sxs-lookup"><span data-stu-id="9d026-1262">Attribute</span></span>   | <span data-ttu-id="9d026-1263">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-1263">Description</span></span>                                         |
|--------------|-----------------------------------------------------|
| <span data-ttu-id="9d026-1264">XtoX</span><span class="sxs-lookup"><span data-stu-id="9d026-1264">XtoX</span></span>         | <span data-ttu-id="9d026-1265">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1265">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="9d026-1266">YtoX</span><span class="sxs-lookup"><span data-stu-id="9d026-1266">YtoX</span></span>         | <span data-ttu-id="9d026-1267">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1267">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="9d026-1268">XtoY</span><span class="sxs-lookup"><span data-stu-id="9d026-1268">XtoY</span></span>         | <span data-ttu-id="9d026-1269">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1269">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="9d026-1270">YtoY</span><span class="sxs-lookup"><span data-stu-id="9d026-1270">YtoY</span></span>         | <span data-ttu-id="9d026-1271">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1271">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="9d026-1272">PerspectiveX</span><span class="sxs-lookup"><span data-stu-id="9d026-1272">PerspectiveX</span></span> | <span data-ttu-id="9d026-1273">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1273">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="9d026-1274">Perspective</span><span class="sxs-lookup"><span data-stu-id="9d026-1274">PerspectiveY</span></span> | <span data-ttu-id="9d026-1275">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9d026-1275">[Double](#data-types-used-in-the-vml-object-model).</span></span> |



 

<span data-ttu-id="9d026-1276">**IVgSkewOffset**</span><span class="sxs-lookup"><span data-stu-id="9d026-1276">**IVgSkewOffset**</span></span>

<span data-ttu-id="9d026-1277">Spécifie le décalage de l’inclinaison.</span><span class="sxs-lookup"><span data-stu-id="9d026-1277">Specifies the offset of the skew.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d026-1278">Attributs</span><span class="sxs-lookup"><span data-stu-id="9d026-1278">Attributes</span></span></th>
<th><span data-ttu-id="9d026-1279">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-1279">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-1280">Value</span><span class="sxs-lookup"><span data-stu-id="9d026-1280">Value</span></span></td>
<td><span data-ttu-id="9d026-1281"><a href="#data-types-used-in-the-vml-object-model">Chaîne</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1281"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="9d026-1282">Représentation textuelle du décalage.</span><span class="sxs-lookup"><span data-stu-id="9d026-1282">Text representation of offset.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1283">X</span><span class="sxs-lookup"><span data-stu-id="9d026-1283">X</span></span></td>
<td><span data-ttu-id="9d026-1284"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1284"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9d026-1285">Composant X.</span><span class="sxs-lookup"><span data-stu-id="9d026-1285">X component.</span></span> <span data-ttu-id="9d026-1286">Pourcentage ou mesure.</span><span class="sxs-lookup"><span data-stu-id="9d026-1286">Percentage or measure.</span></span> <span data-ttu-id="9d026-1287">Si aucune unité n’est présente, le type ShapeRelative est implicite ; Sinon, le type absolu est implicite.</span><span class="sxs-lookup"><span data-stu-id="9d026-1287">If no units, then ShapeRelative type is implied; otherwise Absolute type is implied.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1288">Y</span><span class="sxs-lookup"><span data-stu-id="9d026-1288">Y</span></span></td>
<td><span data-ttu-id="9d026-1289"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1289"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9d026-1290">Composant Y.</span><span class="sxs-lookup"><span data-stu-id="9d026-1290">Y component.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1291">Type</span><span class="sxs-lookup"><span data-stu-id="9d026-1291">Type</span></span></td>
<td><span data-ttu-id="9d026-1292"><strong>VgSkewTransformType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1292"><strong>VgSkewTransformType</strong>.</span></span> <span data-ttu-id="9d026-1293">Spécifie le type de transformation.</span><span class="sxs-lookup"><span data-stu-id="9d026-1293">Specifies the type of transformation.</span></span> <span data-ttu-id="9d026-1294">Les valeurs valides sont les points d’entier compris entre-Infinity et Infinity.</span><span class="sxs-lookup"><span data-stu-id="9d026-1294">Valid values are integer points ranging between -infinity and infinity.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d026-1295">Type</span><span class="sxs-lookup"><span data-stu-id="9d026-1295">Type</span></span></th>
<th><span data-ttu-id="9d026-1296">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-1296">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-1297">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="9d026-1297">ShapeRelative</span></span></td>
<td><span data-ttu-id="9d026-1298">Les valeurs du décalage sont des pourcentages (proportions) de la taille de la forme d’origine ; par exemple, une valeur de 0,5 signifie un décalage de la moitié de la taille de la forme.</span><span class="sxs-lookup"><span data-stu-id="9d026-1298">The values of the offset are percentages (ratios) of the original shape's size; e.g., a value of 0.5 means an offset half the size of the shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1299">Absolu</span><span class="sxs-lookup"><span data-stu-id="9d026-1299">Absolute</span></span></td>
<td><span data-ttu-id="9d026-1300">Les valeurs sont des unités absolues.</span><span class="sxs-lookup"><span data-stu-id="9d026-1300">The values are absolute units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9d026-1301">**Type de données IVgVector2D**</span><span class="sxs-lookup"><span data-stu-id="9d026-1301">**IVgVector2D data type**</span></span>

<span data-ttu-id="9d026-1302">Spécifie un vecteur à deux dimensions constitué de deux nombres **doubles** .</span><span class="sxs-lookup"><span data-stu-id="9d026-1302">Specifies a two-dimensional vector consisting of two **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d026-1303">Attributs</span><span class="sxs-lookup"><span data-stu-id="9d026-1303">Attributes</span></span></th>
<th><span data-ttu-id="9d026-1304">Description</span><span class="sxs-lookup"><span data-stu-id="9d026-1304">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-1305">Value</span><span class="sxs-lookup"><span data-stu-id="9d026-1305">Value</span></span></td>
<td><span data-ttu-id="9d026-1306"><strong>Chaîne</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1306"><strong>String</strong>.</span></span> <span data-ttu-id="9d026-1307">Représentation textuelle des deux nombres vectorisés séparés par un espace.</span><span class="sxs-lookup"><span data-stu-id="9d026-1307">Text representation of both vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1308">X</span><span class="sxs-lookup"><span data-stu-id="9d026-1308">X</span></span></td>
<td><span data-ttu-id="9d026-1309"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1309"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9d026-1310">Composant X de ce vecteur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1310">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1311">Y</span><span class="sxs-lookup"><span data-stu-id="9d026-1311">Y</span></span></td>
<td><span data-ttu-id="9d026-1312"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1312"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9d026-1313">Composant Y de ce vecteur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1313">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1314">Type</span><span class="sxs-lookup"><span data-stu-id="9d026-1314">Type</span></span></td>
<td><span data-ttu-id="9d026-1315"><strong>VgVectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1315"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="9d026-1316">Unités attendues pour ce vecteur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1316">Expected units for this vector.</span></span> <span data-ttu-id="9d026-1317">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-1317">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-1318">Mesure</span><span class="sxs-lookup"><span data-stu-id="9d026-1318">Measure</span></span></li>
<li><span data-ttu-id="9d026-1319">Longueur</span><span class="sxs-lookup"><span data-stu-id="9d026-1319">Length</span></span></li>
<li><span data-ttu-id="9d026-1320">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="9d026-1320">AngleInDegrees</span></span></li>
<li><span data-ttu-id="9d026-1321">Fraction</span><span class="sxs-lookup"><span data-stu-id="9d026-1321">Fraction</span></span></li>
<li><span data-ttu-id="9d026-1322">Nombre entier de pourcentage</span><span class="sxs-lookup"><span data-stu-id="9d026-1322">Number Percentage Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9d026-1323">**Type de données IVgVector3D**</span><span class="sxs-lookup"><span data-stu-id="9d026-1323">**IVgVector3D data type**</span></span>

<span data-ttu-id="9d026-1324">Spécifie un vecteur à trois dimensions composé de trois nombres **doubles** .</span><span class="sxs-lookup"><span data-stu-id="9d026-1324">Specifies a three-dimensional vector consisting of three **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d026-1325">Value</span><span class="sxs-lookup"><span data-stu-id="9d026-1325">Value</span></span></td>
<td><span data-ttu-id="9d026-1326"><strong>Chaîne</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1326"><strong>String</strong>.</span></span> <span data-ttu-id="9d026-1327">Représentation textuelle de trois nombres vectorisés séparés par un espace.</span><span class="sxs-lookup"><span data-stu-id="9d026-1327">Text representation of three vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1328">X</span><span class="sxs-lookup"><span data-stu-id="9d026-1328">X</span></span></td>
<td><span data-ttu-id="9d026-1329"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1329"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9d026-1330">Composant X de ce vecteur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1330">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1331">Y</span><span class="sxs-lookup"><span data-stu-id="9d026-1331">Y</span></span></td>
<td><span data-ttu-id="9d026-1332"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1332"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9d026-1333">Composant Y de ce vecteur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1333">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d026-1334">Z</span><span class="sxs-lookup"><span data-stu-id="9d026-1334">Z</span></span></td>
<td><span data-ttu-id="9d026-1335"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1335"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9d026-1336">Composant Z de ce vecteur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1336">Z component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d026-1337">Type</span><span class="sxs-lookup"><span data-stu-id="9d026-1337">Type</span></span></td>
<td><span data-ttu-id="9d026-1338"><strong>VgVectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d026-1338"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="9d026-1339">Unités attendues pour ce vecteur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1339">Expected units for this vector.</span></span> <span data-ttu-id="9d026-1340">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-1340">Values are:</span></span>
<ul>
<li><span data-ttu-id="9d026-1341">Mesure</span><span class="sxs-lookup"><span data-stu-id="9d026-1341">Measure</span></span></li>
<li><span data-ttu-id="9d026-1342">Longueur</span><span class="sxs-lookup"><span data-stu-id="9d026-1342">Length</span></span></li>
<li><span data-ttu-id="9d026-1343">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="9d026-1343">AngleInDegrees</span></span></li>
<li><span data-ttu-id="9d026-1344">Fraction</span><span class="sxs-lookup"><span data-stu-id="9d026-1344">Fraction</span></span></li>
<li><span data-ttu-id="9d026-1345">Nombre</span><span class="sxs-lookup"><span data-stu-id="9d026-1345">Number</span></span></li>
<li><span data-ttu-id="9d026-1346">Pourcentage</span><span class="sxs-lookup"><span data-stu-id="9d026-1346">Percentage</span></span></li>
<li><span data-ttu-id="9d026-1347">Integer</span><span class="sxs-lookup"><span data-stu-id="9d026-1347">Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9d026-1348">**Type de données de longueur**</span><span class="sxs-lookup"><span data-stu-id="9d026-1348">**Length data type**</span></span>

<span data-ttu-id="9d026-1349">Nombre à virgule flottante avec une plage comprise entre 0 et l’infini.</span><span class="sxs-lookup"><span data-stu-id="9d026-1349">A floating point number with a range from 0 to infinity.</span></span>

<span data-ttu-id="9d026-1350">**Type de données Measure**</span><span class="sxs-lookup"><span data-stu-id="9d026-1350">**Measure data type**</span></span>

<span data-ttu-id="9d026-1351">Nombre à virgule flottante de-Infinity à Infinity.</span><span class="sxs-lookup"><span data-stu-id="9d026-1351">A floating point number from -infinity to infinity.</span></span>

<span data-ttu-id="9d026-1352">**Type de données String**</span><span class="sxs-lookup"><span data-stu-id="9d026-1352">**String data type**</span></span>

<span data-ttu-id="9d026-1353">Données de caractères de n’importe quelle longueur.</span><span class="sxs-lookup"><span data-stu-id="9d026-1353">Character data of any length.</span></span>

<span data-ttu-id="9d026-1354">**VgBlackWhiteMode**</span><span class="sxs-lookup"><span data-stu-id="9d026-1354">**VgBlackWhiteMode**</span></span>

<span data-ttu-id="9d026-1355">Mode de rendu pour le noir et le blanc.</span><span class="sxs-lookup"><span data-stu-id="9d026-1355">Rendering mode for black and white.</span></span> <span data-ttu-id="9d026-1356">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d026-1356">Possible values are:</span></span>

-   <span data-ttu-id="9d026-1357">**Couleur**</span><span class="sxs-lookup"><span data-stu-id="9d026-1357">**Color**</span></span>
-   <span data-ttu-id="9d026-1358">**Automatique**</span><span class="sxs-lookup"><span data-stu-id="9d026-1358">**Auto**</span></span>
-   <span data-ttu-id="9d026-1359">**Semble**</span><span class="sxs-lookup"><span data-stu-id="9d026-1359">**GrayScale**</span></span>
-   <span data-ttu-id="9d026-1360">**LightGrayScale**</span><span class="sxs-lookup"><span data-stu-id="9d026-1360">**LightGrayScale**</span></span>
-   <span data-ttu-id="9d026-1361">**InverseGray**</span><span class="sxs-lookup"><span data-stu-id="9d026-1361">**InverseGray**</span></span>
-   <span data-ttu-id="9d026-1362">**GrayOutline**</span><span class="sxs-lookup"><span data-stu-id="9d026-1362">**GrayOutline**</span></span>
-   <span data-ttu-id="9d026-1363">**BlackTextAndLines**</span><span class="sxs-lookup"><span data-stu-id="9d026-1363">**BlackTextAndLines**</span></span>
-   <span data-ttu-id="9d026-1364">**HighContrast**</span><span class="sxs-lookup"><span data-stu-id="9d026-1364">**HighContrast**</span></span>
-   <span data-ttu-id="9d026-1365">**Noir**</span><span class="sxs-lookup"><span data-stu-id="9d026-1365">**Black**</span></span>
-   <span data-ttu-id="9d026-1366">**Blancs**</span><span class="sxs-lookup"><span data-stu-id="9d026-1366">**White**</span></span>
-   <span data-ttu-id="9d026-1367">**Dédessiné**</span><span class="sxs-lookup"><span data-stu-id="9d026-1367">**Undrawn**</span></span>

<span data-ttu-id="9d026-1368">**Type de données VgFraction**</span><span class="sxs-lookup"><span data-stu-id="9d026-1368">**VgFraction data type**</span></span>

<span data-ttu-id="9d026-1369">Nombre à virgule flottante avec une plage comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="9d026-1369">Floating point number with range from 0.0 to 1.0.</span></span> <span data-ttu-id="9d026-1370">Les fractions peuvent également être spécifiées sous la forme d’un pourcentage. par exemple, « 50% ».</span><span class="sxs-lookup"><span data-stu-id="9d026-1370">Fractions can also be specified as a percentage; e.g., "50%".</span></span>

<span data-ttu-id="9d026-1371">**Type de données VgTriState**</span><span class="sxs-lookup"><span data-stu-id="9d026-1371">**VgTriState datatype**</span></span>

<span data-ttu-id="9d026-1372">Énumération utilisée pour les valeurs qui peuvent être de l’un des trois États suivants :</span><span class="sxs-lookup"><span data-stu-id="9d026-1372">Enumeration used for values that can be one of three states:</span></span>

-   <span data-ttu-id="9d026-1373">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="9d026-1373">**TRUE**</span></span>
-   <span data-ttu-id="9d026-1374">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="9d026-1374">**FALSE**</span></span>
-   <span data-ttu-id="9d026-1375">**CONDITIONS MIXTES**</span><span class="sxs-lookup"><span data-stu-id="9d026-1375">**MIXED**</span></span>