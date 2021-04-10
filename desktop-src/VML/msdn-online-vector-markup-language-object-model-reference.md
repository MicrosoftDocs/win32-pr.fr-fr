---
title: Référence du modèle objet VML
description: Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889c977260548c26bbfd8196160e4537ccb8895d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031763"
---
# <a name="vml-object-model-reference"></a><span data-ttu-id="3ec7a-104">Référence du modèle objet VML</span><span class="sxs-lookup"><span data-stu-id="3ec7a-104">VML Object Model Reference</span></span>

<span data-ttu-id="3ec7a-105">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-105">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3ec7a-106">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-106">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3ec7a-107">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-107">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3ec7a-108">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-108">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3ec7a-109">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-109">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3ec7a-110">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-110">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3ec7a-111">Dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-111">In this topic:</span></span>

-   [<span data-ttu-id="3ec7a-112">Introduction</span><span class="sxs-lookup"><span data-stu-id="3ec7a-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="3ec7a-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="3ec7a-113">Example</span></span>](#example)
-   [<span data-ttu-id="3ec7a-114">Configuration de VML</span><span class="sxs-lookup"><span data-stu-id="3ec7a-114">Setting up VML</span></span>](#setting-up-vml)
-   [<span data-ttu-id="3ec7a-115">Informations de référence sur VML OM</span><span class="sxs-lookup"><span data-stu-id="3ec7a-115">VML OM Reference</span></span>](#vml-om-reference)
    -   [<span data-ttu-id="3ec7a-116">Élément Shape</span><span class="sxs-lookup"><span data-stu-id="3ec7a-116">Shape element</span></span>](#shape-element)
-   [<span data-ttu-id="3ec7a-117">Sous-éléments de l’élément Shape</span><span class="sxs-lookup"><span data-stu-id="3ec7a-117">Subelements of the Shape Element</span></span>](#subelements-of-the-shape-element)
    -   [<span data-ttu-id="3ec7a-118">Élément d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="3ec7a-118">Background element</span></span>](#background-element)
    -   [<span data-ttu-id="3ec7a-119">Élément extrusion</span><span class="sxs-lookup"><span data-stu-id="3ec7a-119">Extrusion element</span></span>](#extrusion-element)
    -   [<span data-ttu-id="3ec7a-120">Fill, élément</span><span class="sxs-lookup"><span data-stu-id="3ec7a-120">Fill element</span></span>](#fill-element)
    -   [<span data-ttu-id="3ec7a-121">élément Group</span><span class="sxs-lookup"><span data-stu-id="3ec7a-121">Group element</span></span>](#group-element)
    -   [<span data-ttu-id="3ec7a-122">Élément ImageData</span><span class="sxs-lookup"><span data-stu-id="3ec7a-122">Imagedata element</span></span>](#imagedata-element)
    -   [<span data-ttu-id="3ec7a-123">Élément Path</span><span class="sxs-lookup"><span data-stu-id="3ec7a-123">Path element</span></span>](#path-element)
    -   [<span data-ttu-id="3ec7a-124">Élément Shadow</span><span class="sxs-lookup"><span data-stu-id="3ec7a-124">Shadow element</span></span>](#shadow-element)
    -   [<span data-ttu-id="3ec7a-125">Élément Skew</span><span class="sxs-lookup"><span data-stu-id="3ec7a-125">Skew element</span></span>](#skew-element)
    -   [<span data-ttu-id="3ec7a-126">Stroke, élément</span><span class="sxs-lookup"><span data-stu-id="3ec7a-126">Stroke element</span></span>](#stroke-element)
    -   [<span data-ttu-id="3ec7a-127">Élément TextPath</span><span class="sxs-lookup"><span data-stu-id="3ec7a-127">TextPath element</span></span>](#textpath-element)
-   [<span data-ttu-id="3ec7a-128">Types de données utilisés dans le modèle d’objet VML</span><span class="sxs-lookup"><span data-stu-id="3ec7a-128">Data Types Used in the VML Object Model</span></span>](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a><span data-ttu-id="3ec7a-129">Introduction</span><span class="sxs-lookup"><span data-stu-id="3ec7a-129">Introduction</span></span>

<span data-ttu-id="3ec7a-130">[Langage VML (VML)](https://www.w3.org/TR/NOTE-datetime.html) est un langage textuel qui utilise [XML](https://www.w3.org/TR/REC-xml.mdl) pour étendre le code HTML en vue d’afficher des informations graphiques vectorielles.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) is a text-based language that uses [XML](https://www.w3.org/TR/REC-xml.mdl) to extend HTML for the purpose of displaying vector graphic information.</span></span> <span data-ttu-id="3ec7a-131">Le Document Object Model VML (DOM) définit une interface de programmation pour la manipulation des éléments de document.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-131">The VML Document Object Model (DOM) defines a programmatic interface for the manipulation of the document elements.</span></span> <span data-ttu-id="3ec7a-132">Cela permet à l’utilisateur de créer et de modifier dynamiquement des graphiques vectoriels via une interface de plateforme et une interface indépendante du langage.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-132">This enables the user to dynamically create and modify vector graphics through a platform- and language-neutral interface.</span></span> <span data-ttu-id="3ec7a-133">Le DOM VML est conforme à la spécification [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-133">The VML DOM conforms to the [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specification.</span></span>

<span data-ttu-id="3ec7a-134">VML utilise l’élément [Shape](#shape-element) comme bloc de construction de base pour les images vectorielles.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-134">VML uses the [Shape](#shape-element) element as the basic building block for vector graphic images.</span></span> <span data-ttu-id="3ec7a-135">Une fois qu’une forme est créée, vous pouvez modifier la forme par le biais des attributs ou des sous-éléments attachés.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-135">Once a shape is created, you can modify the shape through attributes or by attached subelements.</span></span> <span data-ttu-id="3ec7a-136">Par exemple, pour modifier la couleur d’une forme, assignez une valeur de couleur à l’attribut **FillColor** .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-136">For example, to change the color of a shape, assign a color value to the **FillColor** attribute.</span></span>


```HTML
myshape.fillcolor = "red"
```



<span data-ttu-id="3ec7a-137">Plusieurs des attributs d’une forme sont également des sous- [éléments](/windows) et ont leurs propres attributs, y compris les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-137">Several of the attributes of a shape are also [subelements](/windows) and have their own attributes, including the following:</span></span>

-   [<span data-ttu-id="3ec7a-138">Contexte</span><span class="sxs-lookup"><span data-stu-id="3ec7a-138">Background</span></span>](#background-element)
-   [<span data-ttu-id="3ec7a-139">Extrusion</span><span class="sxs-lookup"><span data-stu-id="3ec7a-139">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="3ec7a-140">Complète</span><span class="sxs-lookup"><span data-stu-id="3ec7a-140">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="3ec7a-141">Groupe</span><span class="sxs-lookup"><span data-stu-id="3ec7a-141">Group</span></span>](#group-element)
-   [<span data-ttu-id="3ec7a-142">Imagedata</span><span class="sxs-lookup"><span data-stu-id="3ec7a-142">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="3ec7a-143">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3ec7a-143">Path</span></span>](#path-element)
-   [<span data-ttu-id="3ec7a-144">Shadow</span><span class="sxs-lookup"><span data-stu-id="3ec7a-144">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="3ec7a-145">Appliquez</span><span class="sxs-lookup"><span data-stu-id="3ec7a-145">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="3ec7a-146">Stroke</span><span class="sxs-lookup"><span data-stu-id="3ec7a-146">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="3ec7a-147">TextPath</span><span class="sxs-lookup"><span data-stu-id="3ec7a-147">TextPath</span></span>](#textpath-element)

<span data-ttu-id="3ec7a-148">VML OM utilise plusieurs [types de données](/windows) pour définir des paramètres.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-148">The VML OM uses several [data types](/windows) to define parameters.</span></span> <span data-ttu-id="3ec7a-149">Les types de données précédés de « VG » sont des énumérations et celles précédées de « IVg » sont des objets.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-149">Datatypes prefixed with "Vg" are enumerations and those prefixed with "IVg" are objects.</span></span> <span data-ttu-id="3ec7a-150">Cliquez ici pour obtenir une liste.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-150">Click here for a list.</span></span> <span data-ttu-id="3ec7a-151">Les types de données mineurs sont répertoriés avec des paramètres spécifiques.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-151">Minor datatypes are listed with specific parameters.</span></span>

## <a name="example"></a><span data-ttu-id="3ec7a-152">Exemple</span><span class="sxs-lookup"><span data-stu-id="3ec7a-152">Example</span></span>

<span data-ttu-id="3ec7a-153">Le code VBScript suivant montre comment créer une forme simple :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-153">The following VBScript code shows how to create a simple shape:</span></span>


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



<span data-ttu-id="3ec7a-154">Dans l’exemple ci-dessus, une forme est créée à l’aide de la méthode Document Object Model **createElement**.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-154">In the above example, a shape is created by using the Document Object Model method **CreateElement**.</span></span> <span data-ttu-id="3ec7a-155">La forme est une forme Rect prédéfinie VML.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-155">The shape is a VML predefined Rect shape.</span></span> <span data-ttu-id="3ec7a-156">Même si l’objet existe, il ne peut pas faire partie du document tant qu’il n’est pas attaché au document.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-156">Even though the object exists, it cannot be part of the document until it is attached to the document.</span></span> <span data-ttu-id="3ec7a-157">À l’aide de la méthode **AppendChild** , le Rect est devenu l’enfant d’un élément **div** appelé MyDiv.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-157">Using the **AppendChild** method, the Rect is made a child of a **DIV** element called MyDiv.</span></span> <span data-ttu-id="3ec7a-158">Quelques attributs de style minimum (**position**, **largeur**, **hauteur**, **haut**, **gauche**) sont définis pour attribuer une taille spécifique à la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-158">A few minimum style attributes (**Position**, **Width**, **Height**, **Top**, **Left**) are set to give the shape a specific size.</span></span> <span data-ttu-id="3ec7a-159">Enfin, une couleur est assignée avec l’attribut **FillColor** .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-159">Finally, a color is assigned with the **FillColor** attribute.</span></span> <span data-ttu-id="3ec7a-160">Notez que vous pouvez utiliser n’importe quel langage de script ou n’importe quel langage pouvant fonctionner avec des interfaces Document Object Model.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-160">Note that any scripting language or any language that can work with Document Object Model interfaces can be used.</span></span>

## <a name="setting-up-vml"></a><span data-ttu-id="3ec7a-161">Configuration de VML</span><span class="sxs-lookup"><span data-stu-id="3ec7a-161">Setting up VML</span></span>

<span data-ttu-id="3ec7a-162">L’une des implémentations de VML est par le biais de Microsoft Internet Explorer 5,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-162">One implementation of VML is through Microsoft Internet Explorer 5.0 or greater.</span></span> <span data-ttu-id="3ec7a-163">Pour configurer correctement l’objet de rendu dans une page Web, les ajouts suivants doivent être effectués :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-163">To set up the rendering object correctly in a Web page, the following additions must be made:</span></span>

1.  <span data-ttu-id="3ec7a-164">Le schéma doit être configuré dans le</span><span class="sxs-lookup"><span data-stu-id="3ec7a-164">The schema must be set up in the initial</span></span> <HTML> <span data-ttu-id="3ec7a-165">comme suit :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-165">tag as follows:</span></span>
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  <span data-ttu-id="3ec7a-166">Le comportement de rendu doit faire partie du style du document :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-166">The rendering behavior must be part of the document's style:</span></span>
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

<span data-ttu-id="3ec7a-167">L’exemple suivant montre un exemple de page Web HTML configuré correctement pour VML montrant la création dynamique d’une forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-167">The following shows a sample HTML Web page set up correctly for VML showing the dynamic creation of a shape.</span></span>


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



<span data-ttu-id="3ec7a-168">Notez que dans les versions bêta, une balise d’objet ActiveX et un style de comportement différent étaient requis.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-168">Note that in beta versions, an ActiveX object tag and a different behavior style was required.</span></span>

## <a name="vml-om-reference"></a><span data-ttu-id="3ec7a-169">Informations de référence sur VML OM</span><span class="sxs-lookup"><span data-stu-id="3ec7a-169">VML OM Reference</span></span>

<span data-ttu-id="3ec7a-170">Cette référence définit l’élément de [forme](#shape-element) , les sous- [éléments](/windows)et les [types de données](/windows) utilisés par le modèle objet de Vml.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-170">This reference defines the [Shape](#shape-element) element, [subelements](/windows), and [data types](/windows) that are used by the object model of VML.</span></span>

### <a name="shape-element"></a><span data-ttu-id="3ec7a-171">Élément Shape</span><span class="sxs-lookup"><span data-stu-id="3ec7a-171">Shape element</span></span>

<span data-ttu-id="3ec7a-172">Les formes sont les blocs de construction des images graphiques définies par langage VML (VML).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-172">Shapes are the building blocks of graphical images defined by Vector Markup Language (VML).</span></span> <span data-ttu-id="3ec7a-173">La forme est l’élément de niveau supérieur et plusieurs sous-éléments permettent de définir la nature de chaque forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-173">The shape is the top-level element and several subelements help define the nature of each shape.</span></span>

<span data-ttu-id="3ec7a-174">VML fournit des formes prédéfinies :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-174">VML provides predefined shapes:</span></span>

<span data-ttu-id="3ec7a-175">**Attributs de forme**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-175">**Shape Attributes**</span></span>

-   <span data-ttu-id="3ec7a-176">**Arc**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-176">**Arc**</span></span>
-   <span data-ttu-id="3ec7a-177">**Apprendre**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-177">**Curve**</span></span>
-   <span data-ttu-id="3ec7a-178">**Ligne**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-178">**Line**</span></span>
-   <span data-ttu-id="3ec7a-179">**Polyligne**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-179">**PolyLine**</span></span>
-   <span data-ttu-id="3ec7a-180">**Rect**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-180">**Rect**</span></span>
-   <span data-ttu-id="3ec7a-181">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-181">**RoundRect**</span></span>



|              |                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec7a-182">Ajustement</span><span class="sxs-lookup"><span data-stu-id="3ec7a-182">Adj</span></span>          | <span data-ttu-id="3ec7a-183">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-183">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span></span> <span data-ttu-id="3ec7a-184">Liste délimitée par des virgules de nombres qui correspondent aux paramètres des formules de repère qui définissent le chemin d’accès de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-184">A comma-delimited list of numbers that are the parameters for the guide formulas that define the path of the shape.</span></span> <span data-ttu-id="3ec7a-185">Les valeurs peuvent être omises pour permettre l’utilisation des valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-185">Values may be omitted to allow for using defaults.</span></span> <span data-ttu-id="3ec7a-186">Il peut y avoir jusqu’à 8 valeurs d’ajustement.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-186">There can be up to 8 adjustment values.</span></span>                                                                                                   |
| <span data-ttu-id="3ec7a-187">Alt</span><span class="sxs-lookup"><span data-stu-id="3ec7a-187">Alt</span></span>          | <span data-ttu-id="3ec7a-188">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-188">String.</span></span> <span data-ttu-id="3ec7a-189">Texte de remplacement associé à Shape.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-189">Alternative text associated with shape.</span></span> <span data-ttu-id="3ec7a-190">Utilisé pour l’exploration non graphique.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-190">Used for non-graphical browsing.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3ec7a-191">Bouton</span><span class="sxs-lookup"><span data-stu-id="3ec7a-191">Button</span></span>       | <span data-ttu-id="3ec7a-192">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-192">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="3ec7a-193">Affiche le comportement du bouton sur clic.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-193">Displays button behavior on click.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3ec7a-194">BWMode</span><span class="sxs-lookup"><span data-stu-id="3ec7a-194">BWMode</span></span>       | <span data-ttu-id="3ec7a-195">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-195">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="3ec7a-196">Détermine le mode de rendu de la forme en noir et blanc dans les applications, ou lorsqu’elle est imprimée sur des imprimantes noir et blanc.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-196">Determines how shape will render in black-and-white view in apps or when printed to black-and-white printers.</span></span> <span data-ttu-id="3ec7a-197">Les valeurs sont les suivantes : **couleur**, **auto**, **nuances de gris**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **noir**, **blanc**, **dédessiné**.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-197">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="3ec7a-198">Valeur par défaut : **auto**.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-198">Default: **Auto**.</span></span> |
| <span data-ttu-id="3ec7a-199">BWNormal</span><span class="sxs-lookup"><span data-stu-id="3ec7a-199">BWNormal</span></span>     | <span data-ttu-id="3ec7a-200">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-200">VgBlackWhiteMode.</span></span> <span data-ttu-id="3ec7a-201">Quand BWMode est auto, cette propriété est consultée pour savoir comment afficher la forme en noir et blanc normal.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-201">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span> <span data-ttu-id="3ec7a-202">Les valeurs sont les suivantes : **couleur**, **auto**, **nuances de gris**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **noir**, **blanc**, **dédessiné**.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-202">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="3ec7a-203">Valeur par défaut : **auto**.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-203">Default: **Auto**.</span></span>                                                |
| <span data-ttu-id="3ec7a-204">BWPure</span><span class="sxs-lookup"><span data-stu-id="3ec7a-204">BWPure</span></span>       | <span data-ttu-id="3ec7a-205">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-205">VgBlackWhiteMode.</span></span> <span data-ttu-id="3ec7a-206">Quand BWMode est auto, cette propriété est consultée pour savoir comment afficher la forme dans les e/s pures.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-206">When BWMode is Auto, this property is consulted for how to render the shape in pure B/W.</span></span> <span data-ttu-id="3ec7a-207">Les valeurs sont les suivantes : **couleur**, **auto**, **nuances de gris**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **noir**, **blanc**, **dédessiné**.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-207">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="3ec7a-208">Valeur par défaut : **auto**.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-208">Default: **Auto**.</span></span>                                                              |
| <span data-ttu-id="3ec7a-209">ChildShapes</span><span class="sxs-lookup"><span data-stu-id="3ec7a-209">ChildShapes</span></span>  | <span data-ttu-id="3ec7a-210">IVgGroupShapes.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-210">IVgGroupShapes.</span></span> <span data-ttu-id="3ec7a-211">Collection d’autres formes de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-211">A collection of other shapes in this group.</span></span> <span data-ttu-id="3ec7a-212">Cette collection prend en charge les méthodes de longueur et d’élément standard.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-212">This collection supports the standard Length and Item methods.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="3ec7a-213">Chromakey</span><span class="sxs-lookup"><span data-stu-id="3ec7a-213">Chromakey</span></span>    | <span data-ttu-id="3ec7a-214">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-214">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="3ec7a-215">Valeur de couleur qui est transparente et qui affiche tout ce qui se trouve derrière la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-215">A color value that will be transparent and show anything behind the shape.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3ec7a-216">Control1</span><span class="sxs-lookup"><span data-stu-id="3ec7a-216">Control1</span></span>     | <span data-ttu-id="3ec7a-217">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-217">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="3ec7a-218">Point de contrôle pour la courbe.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-218">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3ec7a-219">Control2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-219">Control2</span></span>     | <span data-ttu-id="3ec7a-220">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-220">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="3ec7a-221">Point de contrôle pour la courbe.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-221">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3ec7a-222">CoordOrigin</span><span class="sxs-lookup"><span data-stu-id="3ec7a-222">CoordOrigin</span></span>  | <span data-ttu-id="3ec7a-223">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md) Coordonnées situées dans le coin supérieur gauche du rectangle de conteneur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-223">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) The coordinates at the top left corner of the container rectangle.</span></span> <span data-ttu-id="3ec7a-224">Plage comprise entre 0 et l’infini.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-224">Range from 0 to infinity.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="3ec7a-225">CoordSize</span><span class="sxs-lookup"><span data-stu-id="3ec7a-225">CoordSize</span></span>    | <span data-ttu-id="3ec7a-226">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-226">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="3ec7a-227">Largeur et hauteur de l’espace de coordonnées à l’intérieur du rectangle de référence de cette forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-227">The width and height of the coordinate space inside the reference rectangle of this shape.</span></span> <span data-ttu-id="3ec7a-228">S’il n’est pas spécifié, il est identique à la largeur et à la hauteur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-228">If it is not specified, it is the same as the width and height of the rectangle.</span></span> <span data-ttu-id="3ec7a-229">Plage comprise entre 0 et l’infini.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-229">Range from 0 to infinity.</span></span> <span data-ttu-id="3ec7a-230">Valeur par défaut : « 1000, 1000 ».</span><span class="sxs-lookup"><span data-stu-id="3ec7a-230">Default: "1000,1000".</span></span>                                                                                               |
| <span data-ttu-id="3ec7a-231">EndAngle</span><span class="sxs-lookup"><span data-stu-id="3ec7a-231">EndAngle</span></span>     | <span data-ttu-id="3ec7a-232">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-232">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="3ec7a-233">Angle de fin de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-233">End angle of shape.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3ec7a-234">Extrusion</span><span class="sxs-lookup"><span data-stu-id="3ec7a-234">Extrusion</span></span>    | <span data-ttu-id="3ec7a-235">IVgExtrusion.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-235">IVgExtrusion.</span></span> <span data-ttu-id="3ec7a-236">Spécifie la valeur de l’objet d’extrusion pour cette forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-236">Specifies the Extrusion object value for this shape.</span></span> <span data-ttu-id="3ec7a-237">Pour plus d’informations, consultez l’élément [extrusion](msdn-online-vml-extrusion-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-237">See the [Extrusion](msdn-online-vml-extrusion-element.md) element for details.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="3ec7a-238">Fill</span><span class="sxs-lookup"><span data-stu-id="3ec7a-238">Fill</span></span>         | <span data-ttu-id="3ec7a-239">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-239">VgFillFormat.</span></span> <span data-ttu-id="3ec7a-240">Spécifie la valeur de remplissage de cette forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-240">Specifies the fill value for this shape.</span></span> <span data-ttu-id="3ec7a-241">Pour plus d’informations, consultez l’élément [Fill](msdn-online-vml-fill-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-241">See the [Fill](msdn-online-vml-fill-element.md) element for more details.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="3ec7a-242">FillColor</span><span class="sxs-lookup"><span data-stu-id="3ec7a-242">FillColor</span></span>    | <span data-ttu-id="3ec7a-243">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-243">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="3ec7a-244">Couleur principale du pinceau à utiliser pour remplir le tracé de cette forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-244">The primary color of the brush to use to fill the path of this shape.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3ec7a-245">Spécifié</span><span class="sxs-lookup"><span data-stu-id="3ec7a-245">Filled</span></span>       | <span data-ttu-id="3ec7a-246">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-246">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="3ec7a-247">Si la valeur est true, le chemin d’accès qui définit la forme est rempli.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-247">If True, the path defining the shape will be filled.</span></span> <span data-ttu-id="3ec7a-248">Par défaut, il est rempli à l’aide d’une couleur unie, sauf s’il existe un sous-élément Fill qui spécifie des propriétés de remplissage plus complexes.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-248">By default, it will be filled using a solid color unless there is a Fill subelement that specifies more complex fill properties.</span></span> <span data-ttu-id="3ec7a-249">Si la valeur est false, le remplissage est transparent.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-249">If False, the fill is transparent.</span></span>                                                                                                           |
| <span data-ttu-id="3ec7a-250">Livre</span><span class="sxs-lookup"><span data-stu-id="3ec7a-250">Flip</span></span>         | <span data-ttu-id="3ec7a-251">VgFlipOrientation.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-251">VgFlipOrientation.</span></span> <span data-ttu-id="3ec7a-252">Les valeurs sont les suivantes : X XY YX</span><span class="sxs-lookup"><span data-stu-id="3ec7a-252">Values are: X Y XY YX</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3ec7a-253">ForceDash</span><span class="sxs-lookup"><span data-stu-id="3ec7a-253">ForceDash</span></span>    | <span data-ttu-id="3ec7a-254">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-254">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="3ec7a-255">Indique qu’un contour en pointillés doit être rendu lorsqu’il n’y a aucune ligne et aucun remplissage pour une forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-255">Indication that a dashed outline should be rendered when there is no line and no fill for a shape.</span></span> <span data-ttu-id="3ec7a-256">Ce comportement est généralement utile pour rendre les formes invisibles visibles dans la modification des applications afin qu’elles puissent être sélectionnées et exploitées, par exemple dans une image interactive.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-256">This behavior is generally useful for making invisible shapes visible in editing applications so they can be selected and operated on, such as in an image map.</span></span>                                                                 |
| <span data-ttu-id="3ec7a-257">Formules</span><span class="sxs-lookup"><span data-stu-id="3ec7a-257">Formulas</span></span>     | <span data-ttu-id="3ec7a-258">IVgFormulas.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-258">IVgFormulas.</span></span> <span data-ttu-id="3ec7a-259">Tableau de formules qui définit une forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-259">An array of formulas that defines a shape.</span></span>                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3ec7a-260">Du</span><span class="sxs-lookup"><span data-stu-id="3ec7a-260">From</span></span>         | <span data-ttu-id="3ec7a-261">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-261">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="3ec7a-262">Point de départ de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-262">Starting point of line.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="3ec7a-263">HRef</span><span class="sxs-lookup"><span data-stu-id="3ec7a-263">HRef</span></span>         | <span data-ttu-id="3ec7a-264">[Chaîne](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-264">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-265">URL à laquelle accéder si l’utilisateur clique sur cette forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-265">The URL to jump to if this shape is clicked.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3ec7a-266">ImageData</span><span class="sxs-lookup"><span data-stu-id="3ec7a-266">ImageData</span></span>    | <span data-ttu-id="3ec7a-267">IVgImageData.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-267">IVgImageData.</span></span> <span data-ttu-id="3ec7a-268">Informations d’image si la forme est une image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-268">Image information if the shape is a picture.</span></span> <span data-ttu-id="3ec7a-269">Pour plus d’informations, consultez l’élément ImageData.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-269">See the ImageData element for more information.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="3ec7a-270">OnEd</span><span class="sxs-lookup"><span data-stu-id="3ec7a-270">OnEd</span></span>         | <span data-ttu-id="3ec7a-271">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-271">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="3ec7a-272">Masque tous les descripteurs à l’exception des poignées en haut à gauche et en bas à droite, comme dans les poignées pour un segment de ligne droite.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-272">Hides all handles except the top left and bottom right, as in the handles for a straight line segment.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="3ec7a-273">Opacity</span><span class="sxs-lookup"><span data-stu-id="3ec7a-273">Opacity</span></span>      | <span data-ttu-id="3ec7a-274">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-274">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="3ec7a-275">Opacité de la forme entière.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-275">The opacity of the entire shape.</span></span> <span data-ttu-id="3ec7a-276">Nombre compris entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-276">A number between 0.0 and 1.0.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="3ec7a-277">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3ec7a-277">Path</span></span>         | <span data-ttu-id="3ec7a-278">IVgPath.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-278">IVgPath.</span></span> <span data-ttu-id="3ec7a-279">Chaîne contenant les commandes qui définissent le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-279">A string containing the commands that define the path.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3ec7a-280">Points</span><span class="sxs-lookup"><span data-stu-id="3ec7a-280">Points</span></span>       | <span data-ttu-id="3ec7a-281">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-281">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span></span> <span data-ttu-id="3ec7a-282">Collection de points définissant une forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-282">A collection of points defining a shape.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="3ec7a-283">Imprimer</span><span class="sxs-lookup"><span data-stu-id="3ec7a-283">Print</span></span>        | <span data-ttu-id="3ec7a-284">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-284">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="3ec7a-285">Si la valeur est true, cette forme est destinée à être imprimée.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-285">If True, this shape is meant to be printed.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="3ec7a-286">Rotation</span><span class="sxs-lookup"><span data-stu-id="3ec7a-286">Rotation</span></span>     | <span data-ttu-id="3ec7a-287">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-287">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="3ec7a-288">Définit la rotation de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-288">Sets rotation of shape.</span></span> <span data-ttu-id="3ec7a-289">La valeur est propagée au style de forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-289">Value is propagated to the shape style.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="3ec7a-290">Scale</span><span class="sxs-lookup"><span data-stu-id="3ec7a-290">Scale</span></span>        | <span data-ttu-id="3ec7a-291">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-291">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="3ec7a-292">Échelle de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-292">Scale of shape.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="3ec7a-293">Shadow</span><span class="sxs-lookup"><span data-stu-id="3ec7a-293">Shadow</span></span>       | <span data-ttu-id="3ec7a-294">IVgShadow.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-294">IVgShadow.</span></span> <span data-ttu-id="3ec7a-295">Spécifie l’ombre de cette forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-295">Specifies the shadow for this shape.</span></span> <span data-ttu-id="3ec7a-296">Pour plus d’informations, consultez l’élément [Shadow](msdn-online-vml-shadow-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-296">See the [Shadow](msdn-online-vml-shadow-element.md) element for details.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="3ec7a-297">Arborescence</span><span class="sxs-lookup"><span data-stu-id="3ec7a-297">Spt</span></span>          | <span data-ttu-id="3ec7a-298">Réservé.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-298">Reserved.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="3ec7a-299">StartAngle</span><span class="sxs-lookup"><span data-stu-id="3ec7a-299">StartAngle</span></span>   | <span data-ttu-id="3ec7a-300">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-300">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="3ec7a-301">Angle de début de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-301">Start angle of shape.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="3ec7a-302">Trait</span><span class="sxs-lookup"><span data-stu-id="3ec7a-302">Stroke</span></span>       | <span data-ttu-id="3ec7a-303">VgStrokeFormat.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-303">VgStrokeFormat.</span></span> <span data-ttu-id="3ec7a-304">Pour plus d’informations, consultez élément Stroke.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-304">See Stroke element for details.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3ec7a-305">StrokeColor</span><span class="sxs-lookup"><span data-stu-id="3ec7a-305">StrokeColor</span></span>  | <span data-ttu-id="3ec7a-306">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-306">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="3ec7a-307">Couleur principale du pinceau à utiliser pour rayer le tracé de cette forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-307">The primary color of the brush to use to stroke the path of this shape.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="3ec7a-308">Rayé</span><span class="sxs-lookup"><span data-stu-id="3ec7a-308">Stroked</span></span>      | <span data-ttu-id="3ec7a-309">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-309">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="3ec7a-310">Si la valeur est true, le chemin d’accès qui définit la forme est rayé.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-310">If True, the path defining the shape will be stroked.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="3ec7a-311">StrokeWeight</span><span class="sxs-lookup"><span data-stu-id="3ec7a-311">StrokeWeight</span></span> | <span data-ttu-id="3ec7a-312">[VGLength](msdn-online-vml-vglength.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-312">[VGLength](msdn-online-vml-vglength.md).</span></span> <span data-ttu-id="3ec7a-313">Largeur du pinceau à utiliser pour rayer le tracé.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-313">The width of the brush to use to stroke the path.</span></span> <span data-ttu-id="3ec7a-314">Les plages sont comprises entre 0 et 1584.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-314">Ranges between 0 and 1584.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="3ec7a-315">TextPath</span><span class="sxs-lookup"><span data-stu-id="3ec7a-315">TextPath</span></span>     | <span data-ttu-id="3ec7a-316">IVgTextPath.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-316">IVgTextPath.</span></span> <span data-ttu-id="3ec7a-317">Spécifie l’objet TextPath de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-317">Specifies the TextPath object of the shape.</span></span> <span data-ttu-id="3ec7a-318">Pour plus d’informations, consultez l’élément [TextPath](msdn-online-vml-textpath-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-318">See the [TextPath](msdn-online-vml-textpath-element.md) element for more information.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="3ec7a-319">Pour</span><span class="sxs-lookup"><span data-stu-id="3ec7a-319">To</span></span>           | <span data-ttu-id="3ec7a-320">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-320">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="3ec7a-321">Point de terminaison de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-321">End point of line.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="3ec7a-322">Type</span><span class="sxs-lookup"><span data-stu-id="3ec7a-322">Type</span></span>         | <span data-ttu-id="3ec7a-323">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-323">String.</span></span> <span data-ttu-id="3ec7a-324">Type de forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-324">Type of shape.</span></span>                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a><span data-ttu-id="3ec7a-325">Sous-éléments de l’élément Shape</span><span class="sxs-lookup"><span data-stu-id="3ec7a-325">Subelements of the Shape Element</span></span>

<span data-ttu-id="3ec7a-326">Les sous-éléments suivants font partie du modèle d’objet VML.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-326">The following subelements are part of the VML object model.</span></span>

-   [<span data-ttu-id="3ec7a-327">Contexte</span><span class="sxs-lookup"><span data-stu-id="3ec7a-327">Background</span></span>](#background-element)
-   [<span data-ttu-id="3ec7a-328">Extrusion</span><span class="sxs-lookup"><span data-stu-id="3ec7a-328">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="3ec7a-329">Complète</span><span class="sxs-lookup"><span data-stu-id="3ec7a-329">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="3ec7a-330">Groupe</span><span class="sxs-lookup"><span data-stu-id="3ec7a-330">Group</span></span>](#group-element)
-   [<span data-ttu-id="3ec7a-331">Imagedata</span><span class="sxs-lookup"><span data-stu-id="3ec7a-331">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="3ec7a-332">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3ec7a-332">Path</span></span>](#path-element)
-   [<span data-ttu-id="3ec7a-333">Shadow</span><span class="sxs-lookup"><span data-stu-id="3ec7a-333">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="3ec7a-334">Appliquez</span><span class="sxs-lookup"><span data-stu-id="3ec7a-334">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="3ec7a-335">Stroke</span><span class="sxs-lookup"><span data-stu-id="3ec7a-335">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="3ec7a-336">TextPath</span><span class="sxs-lookup"><span data-stu-id="3ec7a-336">TextPath</span></span>](#textpath-element)

### <a name="background-element"></a><span data-ttu-id="3ec7a-337">Élément d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="3ec7a-337">Background element</span></span>

<span data-ttu-id="3ec7a-338">Décrit le remplissage de l’arrière-plan d’une page à l’aide des remplissages VML.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-338">Describes the fill of the background of a page using VML fills.</span></span>

<span data-ttu-id="3ec7a-339">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-339">**Attributes**</span></span>



|           |                                                                                                                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec7a-340">BWMode</span><span class="sxs-lookup"><span data-stu-id="3ec7a-340">BWMode</span></span>    | <span data-ttu-id="3ec7a-341">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-341">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="3ec7a-342">Détermine la façon dont la forme s’affiche dans une vue en noir et blanc dans des applications ou à l’impression.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-342">Determines how shape will render in black-and-white view in applications or when printed.</span></span>                                     |
| <span data-ttu-id="3ec7a-343">BWNormal</span><span class="sxs-lookup"><span data-stu-id="3ec7a-343">BWNormal</span></span>  | <span data-ttu-id="3ec7a-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="3ec7a-345">Quand BWMode est auto, cette propriété est consultée pour savoir comment afficher la forme en noir et blanc normal.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-345">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span>                        |
| <span data-ttu-id="3ec7a-346">BWPure</span><span class="sxs-lookup"><span data-stu-id="3ec7a-346">BWPure</span></span>    | <span data-ttu-id="3ec7a-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="3ec7a-348">Quand BWMode est auto, cette propriété est consultée pour savoir comment afficher la forme en noir et blanc pur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-348">When BWMode is Auto, this property is consulted for how to render the shape in pure black and white.</span></span>                          |
| <span data-ttu-id="3ec7a-349">Fill</span><span class="sxs-lookup"><span data-stu-id="3ec7a-349">Fill</span></span>      | <span data-ttu-id="3ec7a-350">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-350">VgFillFormat.</span></span> <span data-ttu-id="3ec7a-351">Spécifie le remplissage de cette forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-351">Specifies the fill for this shape.</span></span> <span data-ttu-id="3ec7a-352">Pour plus d’informations, consultez l’élément [Fill](msdn-online-vml-fill-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-352">See [Fill](msdn-online-vml-fill-element.md) element for more information.</span></span>                                                             |
| <span data-ttu-id="3ec7a-353">FillColor</span><span class="sxs-lookup"><span data-stu-id="3ec7a-353">FillColor</span></span> | <span data-ttu-id="3ec7a-354">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-354">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="3ec7a-355">Couleur principale du pinceau à utiliser pour remplir le tracé de cette forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-355">The primary color of the brush to use to fill the path of this shape.</span></span> <span data-ttu-id="3ec7a-356">Doublon de la valeur de couleur dans l’élément Fill.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-356">Duplicate of the Color value in the Fill element.</span></span> <span data-ttu-id="3ec7a-357">La valeur par défaut est blanc.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-357">The default is white.</span></span> |



 

### <a name="extrusion-element"></a><span data-ttu-id="3ec7a-358">Élément extrusion</span><span class="sxs-lookup"><span data-stu-id="3ec7a-358">Extrusion element</span></span>

<span data-ttu-id="3ec7a-359">Décrit une extrusion 3D de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-359">Describes a 3-D extrusion of the shape.</span></span>

<span data-ttu-id="3ec7a-360">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-360">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-361">AutoRotationCenter</span><span class="sxs-lookup"><span data-stu-id="3ec7a-361">AutoRotationCenter</span></span></td>
<td><span data-ttu-id="3ec7a-362"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-362"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="3ec7a-363">Si la valeur est true, le centre de rotation du groupe d’objets 3D (en fait, il n’y a qu’un seul objet dans le groupe) est déterminé automatiquement comme étant le centre du groupe ; dans le cas contraire, il est déterminé par les paramètres RotationCenter, qui sont une fraction de la forme avec 0, 0, le centre.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-363">If True, the center of rotation of the group of 3-D objects (in fact there is only ever one object in the group) is determined automatically to be the center of the group; otherwise it is determined by the RotationCenter parameters, which are a fraction of the shape with 0,0,0 being the center.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-364">Profondeur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-364">BackDepth</span></span></td>
<td><span data-ttu-id="3ec7a-365"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-365"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span></span> <span data-ttu-id="3ec7a-366">Quantité d’extrusion vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-366">Amount of backward extrusion.</span></span> <span data-ttu-id="3ec7a-367">Est compris entre 0 et 32767.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-367">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-368">Luminosité</span><span class="sxs-lookup"><span data-stu-id="3ec7a-368">Brightness</span></span></td>
<td><span data-ttu-id="3ec7a-369"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-369"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="3ec7a-370">Luminosité globale de la scène.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-370">Overall brightness of the scene.</span></span> <span data-ttu-id="3ec7a-371">La valeur par défaut est &quot; 20 000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-371">Default is &quot;20,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-372">Couleur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-372">Color</span></span></td>
<td><span data-ttu-id="3ec7a-373"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-373"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="3ec7a-374">Couleur de l’extrusion.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-374">The color of the extrusion.</span></span> <span data-ttu-id="3ec7a-375">Utilisé uniquement si ColorMode est personnalisé.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-375">Only used if ColorMode is Custom.</span></span> <span data-ttu-id="3ec7a-376">Dans le cas contraire, définit automatiquement la couleur de l’effet d’extrusion sur la même valeur que FillColor.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-376">Otherwise, Auto sets the extrusion effect color to the same as FillColor.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-377">ColorMode</span><span class="sxs-lookup"><span data-stu-id="3ec7a-377">ColorMode</span></span></td>
<td><span data-ttu-id="3ec7a-378">Vg3DColorMode.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-378">Vg3DColorMode.</span></span> <span data-ttu-id="3ec7a-379">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-379">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-380">Auto (par défaut)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-380">Auto (default)</span></span></li>
<li><span data-ttu-id="3ec7a-381">Custom</span><span class="sxs-lookup"><span data-stu-id="3ec7a-381">Custom</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-382">Diffusion</span><span class="sxs-lookup"><span data-stu-id="3ec7a-382">Diffusity</span></span></td>
<td><span data-ttu-id="3ec7a-383"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-383"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="3ec7a-384">Rapport entre l’incident et la lumière diffuse.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-384">The ratio of incident to diffusely reflected light.</span></span> <span data-ttu-id="3ec7a-385">Les valeurs inférieures à 1,0 sont normales, mais les valeurs supérieures à un peuvent générer des effets intéressants.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-385">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-386">Edge</span><span class="sxs-lookup"><span data-stu-id="3ec7a-386">Edge</span></span></td>
<td><span data-ttu-id="3ec7a-387"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-387"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="3ec7a-388">Définit la taille d’un bord biseauté arrondi simulé.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-388">Sets the size of a simulated rounded beveled edge.</span></span> <span data-ttu-id="3ec7a-389">Est compris entre 0 et 32767 dans la valeur de type virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-389">Ranges from 0 to 32767 in floating point pts.</span></span> <span data-ttu-id="3ec7a-390">La valeur par défaut est &quot; 1PT &quot; .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-390">Default is &quot;1pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-391">Facette</span><span class="sxs-lookup"><span data-stu-id="3ec7a-391">Facet</span></span></td>
<td><span data-ttu-id="3ec7a-392"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-392"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="3ec7a-393">Définit la facette de la scène.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-393">Sets the facet of the scene.</span></span> <span data-ttu-id="3ec7a-394">La valeur par défaut est &quot; 30 000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-394">Default is &quot;30,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-395">ForeDepth</span><span class="sxs-lookup"><span data-stu-id="3ec7a-395">ForeDepth</span></span></td>
<td><span data-ttu-id="3ec7a-396"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-396"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="3ec7a-397">Quantité d’extrusion vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-397">Amount of forward extrusion.</span></span> <span data-ttu-id="3ec7a-398">Est compris entre 0 et 32767.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-398">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-399">LightFace</span><span class="sxs-lookup"><span data-stu-id="3ec7a-399">LightFace</span></span></td>
<td><span data-ttu-id="3ec7a-400"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-400"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="3ec7a-401">Determimes si la face avant de l’objet répond aux modifications de l’éclairage 3D, par exemple quand un objet pivote.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-401">Determimes whether the front face of the object will respond to changes in the 3-D lighting, e.g., when an object rotates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-402">LightHarsh</span><span class="sxs-lookup"><span data-stu-id="3ec7a-402">LightHarsh</span></span></td>
<td><span data-ttu-id="3ec7a-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="3ec7a-404">Éclairage sévère de la source de lumière principale.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-404">Harsh lighting for the primary light source.</span></span> <span data-ttu-id="3ec7a-405">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-405">Default is False.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-406">LightHarsh2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-406">LightHarsh2</span></span></td>
<td><span data-ttu-id="3ec7a-407"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-407"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="3ec7a-408">Éclairage sévère de la source de lumière secondaire.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-408">Harsh lighting for the secondary light source.</span></span> <span data-ttu-id="3ec7a-409">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-409">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-410">LightLevel</span><span class="sxs-lookup"><span data-stu-id="3ec7a-410">LightLevel</span></span></td>
<td><span data-ttu-id="3ec7a-411"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-411"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="3ec7a-412">Intensité de la source de lumière principale.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-412">Intensity of the primary light source.</span></span> <span data-ttu-id="3ec7a-413">La valeur par défaut est &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-413">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-414">LightLevel2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-414">LightLevel2</span></span></td>
<td><span data-ttu-id="3ec7a-415"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-415"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="3ec7a-416">Intensité de la source de lumière secondaire.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-416">Intensity of the secondary light source.</span></span> <span data-ttu-id="3ec7a-417">La valeur par défaut est &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-417">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-418">LightPosition</span><span class="sxs-lookup"><span data-stu-id="3ec7a-418">LightPosition</span></span></td>
<td><span data-ttu-id="3ec7a-419">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-419">Vector3D.</span></span> <span data-ttu-id="3ec7a-420">Position de la source de lumière principale.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-420">Position of the primary light source.</span></span> <span data-ttu-id="3ec7a-421">La valeur par défaut est &quot; 50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-421">Default is &quot;50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-422">LightPosition2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-422">LightPosition2</span></span></td>
<td><span data-ttu-id="3ec7a-423">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-423">Vector3D.</span></span> <span data-ttu-id="3ec7a-424">Position de la source de lumière secondaire.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-424">Position of the secondary light source.</span></span> <span data-ttu-id="3ec7a-425">La valeur par défaut est &quot; -50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-425">Default is &quot;-50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-426">LockRotationCenter</span><span class="sxs-lookup"><span data-stu-id="3ec7a-426">LockRotationCenter</span></span></td>
<td><span data-ttu-id="3ec7a-427"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-427"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="3ec7a-428">&quot;Lockrotationcenter &quot; signifie que la rotation du groupe est définie par l’angle de rotation [1] degrés autour de l’axe y sur la page suivie de l’angle de rotation [0] degrés sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-428">&quot;Lockrotationcenter&quot; means that the rotation of the group is defined to be by rotation-angle[1] degrees about the y-axis on the page followed by rotation-angle[0] degrees about the x-axis.</span></span> <span data-ttu-id="3ec7a-429">Quand LockRotationCenter a la valeur false, la rotation est définie en tant que degrés d’orientation-angle sur le vecteur défini par l’orientation.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-429">When LockRotationCenter is False, the rotation is defined to be by orientation-angle degrees about the vector defined by orientation.</span></span> <span data-ttu-id="3ec7a-430">Par exemple, lockrotationcenter = false OrientationAngle = 45 orientation = (0, 1, 0) équivaut à lockrotationcenter = true RotationAngle = (0, 45).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-430">So, for example, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) is equivalent to lockrotationcenter=true rotationangle=(0,45).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-431">Métallique</span><span class="sxs-lookup"><span data-stu-id="3ec7a-431">Metal</span></span></td>
<td><span data-ttu-id="3ec7a-432"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-432"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="3ec7a-433">Fait en sorte que la lumière réfléchie modèle éclairé soit la couleur matérielle au lieu de la couleur de la source de lumière, ce qui rend l’objet plus métallique.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-433">Causes specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-434">Il en va</span><span class="sxs-lookup"><span data-stu-id="3ec7a-434">On</span></span></td>
<td><span data-ttu-id="3ec7a-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="3ec7a-436">Active et désactive l’affichage de l’effet de l’extrusion.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-436">Turns the display of the extrusion effect on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-437">Orientation</span><span class="sxs-lookup"><span data-stu-id="3ec7a-437">Orientation</span></span></td>
<td><span data-ttu-id="3ec7a-438">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-438">Vector3D.</span></span> <span data-ttu-id="3ec7a-439">Orientation de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-439">Orientation of the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-440">OrientationAngle</span><span class="sxs-lookup"><span data-stu-id="3ec7a-440">OrientationAngle</span></span></td>
<td><span data-ttu-id="3ec7a-441"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-441"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="3ec7a-442">Angle entre l’orientation de l’appareil photo et le plan XY.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-442">Angle between the orientation of the camera and the xy plane.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-443">Verticale</span><span class="sxs-lookup"><span data-stu-id="3ec7a-443">Plane</span></span></td>
<td><span data-ttu-id="3ec7a-444">Vg3DExtrudePlane.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-444">Vg3DExtrudePlane.</span></span> <span data-ttu-id="3ec7a-445">Autorise l’extrusion des plans orthogonals au plan de l’écran.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-445">Allows extrusion from planes orthogonal to the screen plane.</span></span> <span data-ttu-id="3ec7a-446">Requiert la spécification de ForeDepth et de l’effet de profondeur pour les unités de dessin au lieu de EMU.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-446">Requires ForeDepth and BackDepth to be specified in drawing units instead of emus.</span></span> <span data-ttu-id="3ec7a-447">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-447">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-448">XY</span><span class="sxs-lookup"><span data-stu-id="3ec7a-448">XY</span></span></li>
<li><span data-ttu-id="3ec7a-449">ZX</span><span class="sxs-lookup"><span data-stu-id="3ec7a-449">ZX</span></span></li>
<li><span data-ttu-id="3ec7a-450">YZ</span><span class="sxs-lookup"><span data-stu-id="3ec7a-450">YZ</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-451">Rendu</span><span class="sxs-lookup"><span data-stu-id="3ec7a-451">Render</span></span></td>
<td><span data-ttu-id="3ec7a-452">Vg3DRenderMode.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-452">Vg3DRenderMode.</span></span> <span data-ttu-id="3ec7a-453">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-453">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-454">Unie (par défaut)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-454">Solid (default)</span></span></li>
<li><span data-ttu-id="3ec7a-455">WireFrame</span><span class="sxs-lookup"><span data-stu-id="3ec7a-455">WireFrame</span></span></li>
<li><span data-ttu-id="3ec7a-456">BoundingCube</span><span class="sxs-lookup"><span data-stu-id="3ec7a-456">BoundingCube</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-457">RotationAngle</span><span class="sxs-lookup"><span data-stu-id="3ec7a-457">RotationAngle</span></span></td>
<td><span data-ttu-id="3ec7a-458"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-458"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="3ec7a-459">AngleX, AngleY ou AngleZ est contrôlé par l’attribut ShapeRotation.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-459">AngleX, AngleY, or AngleZ is controlled by the ShapeRotation attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-460">RotationCenter</span><span class="sxs-lookup"><span data-stu-id="3ec7a-460">RotationCenter</span></span></td>
<td><span data-ttu-id="3ec7a-461">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-461">Vector3D.</span></span> <span data-ttu-id="3ec7a-462">Centre de rotation.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-462">Center of rotation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-463">Éclat</span><span class="sxs-lookup"><span data-stu-id="3ec7a-463">Shininess</span></span></td>
<td><span data-ttu-id="3ec7a-464"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-464"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="3ec7a-465">Détermine la façon dont la réflexion spéculaire concentrée ou répartie est.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-465">Determines how concentrated or spread out specular reflection is.</span></span> <span data-ttu-id="3ec7a-466">Une valeur élevée est comprendra de 8 à 10 et se traduirait par un miroir, et une valeur basse serait de 2 à 3 et sequinedrait des vêtements de ré.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-466">A high value would be 8 to 10 and would approximate a mirror, and a low value would be 2 to 3 and would approximate sequined clothing.</span></span> <span data-ttu-id="3ec7a-467">Les valeurs 3 à 7 sont recommandées.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-467">Values of 3 to 7 are recommended.</span></span> <span data-ttu-id="3ec7a-468">Des valeurs élevées reflètent les sources de lumière de repérage.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-468">High values will reflect pinpoint light sources.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-469">SkewAmt</span><span class="sxs-lookup"><span data-stu-id="3ec7a-469">SkewAmt</span></span></td>
<td><span data-ttu-id="3ec7a-470"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-470"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span></span> <span data-ttu-id="3ec7a-471">Si le type est Parallel, l’attribut détermine la quantité d’inclinaison.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-471">If Type is Parallel, attribute determines the amount of skew.</span></span> <span data-ttu-id="3ec7a-472">Est compris entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-472">Ranges from 0 to 100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-473">SkewAngle</span><span class="sxs-lookup"><span data-stu-id="3ec7a-473">SkewAngle</span></span></td>
<td><span data-ttu-id="3ec7a-474"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-474"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="3ec7a-475">Si le type est Parallel, l’attribut détermine le degré d’inclinaison.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-475">If Type is Parallel, attribute determines the degree of skew.</span></span> <span data-ttu-id="3ec7a-476">La valeur par défaut est &quot; -45 &quot; .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-476">Default is &quot;-45&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-477">Specularity</span><span class="sxs-lookup"><span data-stu-id="3ec7a-477">Specularity</span></span></td>
<td><span data-ttu-id="3ec7a-478"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-478"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="3ec7a-479">Rapport entre l’incident et le modèle éclairé de lumière réfléchie.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-479">The ratio of incident to specularly reflected light.</span></span> <span data-ttu-id="3ec7a-480">Les valeurs inférieures à 1,0 sont normales, mais les valeurs supérieures à un peuvent générer des effets intéressants.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-480">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-481">Type</span><span class="sxs-lookup"><span data-stu-id="3ec7a-481">Type</span></span></td>
<td><span data-ttu-id="3ec7a-482">VgExtrusionType.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-482">VgExtrusionType.</span></span> <span data-ttu-id="3ec7a-483">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-483">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-484">Parallèle (par défaut)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-484">Parallel (default)</span></span></li>
<li><span data-ttu-id="3ec7a-485">Perspective</span><span class="sxs-lookup"><span data-stu-id="3ec7a-485">Perspective</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-486">Point</span><span class="sxs-lookup"><span data-stu-id="3ec7a-486">Viewpoint</span></span></td>
<td><span data-ttu-id="3ec7a-487">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-487">Vector3D.</span></span> <span data-ttu-id="3ec7a-488">Point à partir duquel la scène est affichée.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-488">The point where the scene is being viewed from.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-489">ViewpointOrigin</span><span class="sxs-lookup"><span data-stu-id="3ec7a-489">ViewpointOrigin</span></span></td>
<td><span data-ttu-id="3ec7a-490"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-490"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="3ec7a-491">Peut avoir des valeurs comprises entre 0,5 et-0,5 pour positionner l’origine du point de vue dans le cadre englobant de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-491">Can have values from 0.5 to -0.5 to position the origin of the viewpoint within the shape bounding box.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a><span data-ttu-id="3ec7a-492">Fill, élément</span><span class="sxs-lookup"><span data-stu-id="3ec7a-492">Fill element</span></span>

<span data-ttu-id="3ec7a-493">Décrit comment remplir un tracé pour obtenir des remplissages plus complexes qu’une couleur unie.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-493">Describes how a path should be filled for fills more complex than a solid color.</span></span>

<span data-ttu-id="3ec7a-494">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-494">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-495">AlignShape</span><span class="sxs-lookup"><span data-stu-id="3ec7a-495">AlignShape</span></span></td>
<td><span data-ttu-id="3ec7a-496"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-496"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="3ec7a-497">Alignez l’image avec la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-497">Align the image with the shape.</span></span> <span data-ttu-id="3ec7a-498">Si la valeur est false, l’image est alignée avec la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-498">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-499">Angle</span><span class="sxs-lookup"><span data-stu-id="3ec7a-499">Angle</span></span></td>
<td><span data-ttu-id="3ec7a-500"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-500"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="3ec7a-501">Angle de rotation du dégradé.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-501">The angle along which the gradient goes.</span></span> <span data-ttu-id="3ec7a-502">0 degré est le long de l’axe horizontal de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-502">0 degrees is along the horizontal axis from left to right.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-503">Aspect</span><span class="sxs-lookup"><span data-stu-id="3ec7a-503">Aspect</span></span></td>
<td><span data-ttu-id="3ec7a-504"><strong>VgAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-504"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="3ec7a-505">L’attribut ImageSize est ajusté pour conserver l’aspect de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-505">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="3ec7a-506">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-506">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3ec7a-507">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-507">Value</span></span></th>
<th><span data-ttu-id="3ec7a-508">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-508">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-509">Ignorer</span><span class="sxs-lookup"><span data-stu-id="3ec7a-509">Ignore</span></span></td>
<td><span data-ttu-id="3ec7a-510">Ignorer les problèmes d’aspect.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-510">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-511">Au moins</span><span class="sxs-lookup"><span data-stu-id="3ec7a-511">AtLeast</span></span></td>
<td><span data-ttu-id="3ec7a-512">L’image est au moins aussi grande que la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-512">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-513">AtMost</span><span class="sxs-lookup"><span data-stu-id="3ec7a-513">AtMost</span></span></td>
<td><span data-ttu-id="3ec7a-514">L’image n’est pas plus grande que la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-514">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-515">Couleur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-515">Color</span></span></td>
<td><span data-ttu-id="3ec7a-516"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> Couleur de remplissage principale.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-516"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> The main fill color.</span></span> <span data-ttu-id="3ec7a-517">Identique à l’attribut FillColor dans Shape.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-517">Same as FillColor attribute in shape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-518">Couleur2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-518">Color2</span></span></td>
<td><span data-ttu-id="3ec7a-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="3ec7a-520">Couleur secondaire d’un remplissage lorsque le type d’image est Pattern ou un remplissage dégradé.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-520">The secondary color for a fill when image type is Pattern or a gradient fill.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-521">Couleurs</span><span class="sxs-lookup"><span data-stu-id="3ec7a-521">Colors</span></span></td>
<td><span data-ttu-id="3ec7a-522"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-522"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span></span> <span data-ttu-id="3ec7a-523">Les couleurs intermédiaires dans le dégradé et leurs positions relatives le long du dégradé, par exemple &quot; 30% de rouge, 70% bleu, 90% vert &quot; .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-523">Intermediate colors in the gradient and their relative positions along the gradient, e.g., &quot;30% red, 70% blue, 90% green&quot;.</span></span> <span data-ttu-id="3ec7a-524">La couleur primaire (attribut Color dans Shape) est 0% et la couleur secondaire (attribut Color2) est 100%.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-524">Primary color (Color attribute in shape) is 0% and secondary color (Color2 attribute) is 100%.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-525">Priorité</span><span class="sxs-lookup"><span data-stu-id="3ec7a-525">Focus</span></span></td>
<td><span data-ttu-id="3ec7a-526"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-526"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span></span> <span data-ttu-id="3ec7a-527">Point focal pour le remplissage dégradé linéaire.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-527">Focal point for linear gradient fill.</span></span> <span data-ttu-id="3ec7a-528">Les valeurs sont comprises entre-100 et + 100.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-528">Values go from -100 to +100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-529">FocusPosition</span><span class="sxs-lookup"><span data-stu-id="3ec7a-529">FocusPosition</span></span></td>
<td><span data-ttu-id="3ec7a-530"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-530"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="3ec7a-531">Position du rectangle le plus profond pour les dégradés radiaux.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-531">Position of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="3ec7a-532">Le vecteur est une fraction (0,0-1,0) de la largeur et de la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-532">The vector is a fraction (0.0 - 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-533">FocusSize</span><span class="sxs-lookup"><span data-stu-id="3ec7a-533">FocusSize</span></span></td>
<td><span data-ttu-id="3ec7a-534"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a> Taille du rectangle le plus profond pour les dégradés radiaux.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-534"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Size of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="3ec7a-535">Le vecteur est une fraction (0,0 à 1,0) de la largeur et de la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-535">The vector is a fraction (0.0 to 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-536">Méthode</span><span class="sxs-lookup"><span data-stu-id="3ec7a-536">Method</span></span></td>
<td><span data-ttu-id="3ec7a-537">VgSigmaType.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-537">VgSigmaType.</span></span> <span data-ttu-id="3ec7a-538">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-538">Values include:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-539">Aucun</span><span class="sxs-lookup"><span data-stu-id="3ec7a-539">None</span></span></li>
<li><span data-ttu-id="3ec7a-540">Linéaire</span><span class="sxs-lookup"><span data-stu-id="3ec7a-540">Linear</span></span></li>
<li><span data-ttu-id="3ec7a-541">Sigma</span><span class="sxs-lookup"><span data-stu-id="3ec7a-541">Sigma</span></span></li>
<li><span data-ttu-id="3ec7a-542">Quelconque</span><span class="sxs-lookup"><span data-stu-id="3ec7a-542">Any</span></span></li>
</ul>
<p><span data-ttu-id="3ec7a-543">La valeur par défaut est Sigma.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-543">Default is Sigma.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-544">Il en va</span><span class="sxs-lookup"><span data-stu-id="3ec7a-544">On</span></span></td>
<td><span data-ttu-id="3ec7a-545"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-545"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="3ec7a-546">Active l’affichage du remplissage.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-546">Turns fill display on.</span></span> <span data-ttu-id="3ec7a-547">Identique à l’attribut Fill dans Shape.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-547">Same as Fill attribute in shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-548">Opacity</span><span class="sxs-lookup"><span data-stu-id="3ec7a-548">Opacity</span></span></td>
<td><span data-ttu-id="3ec7a-549"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-549"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="3ec7a-550">Opacité du remplissage.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-550">Opacity of the fill.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-551">Opacity2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-551">Opacity2</span></span></td>
<td><span data-ttu-id="3ec7a-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="3ec7a-553">Opacité secondaire pour les dégradés.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-553">The secondary opacity for gradients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-554">Origine</span><span class="sxs-lookup"><span data-stu-id="3ec7a-554">Origin</span></span></td>
<td><span data-ttu-id="3ec7a-555"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-555"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="3ec7a-556">Point relatif au coin supérieur gauche de l’image qui est traité comme l’origine de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-556">Point relative to upper left corner of the image that is treated as the origin of the image.</span></span> <span data-ttu-id="3ec7a-557">La valeur par défaut est le centre de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-557">Default is the center of the image.</span></span> <span data-ttu-id="3ec7a-558">Le vecteur est une fraction (de 0,0 à 1,0) de la largeur et de la hauteur de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-558">The vector is a fraction (from 0.0 to 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-559">Position</span><span class="sxs-lookup"><span data-stu-id="3ec7a-559">Position</span></span></td>
<td><span data-ttu-id="3ec7a-560"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-560"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="3ec7a-561">Point dans le rectangle de référence de la forme pour positionner l’origine de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-561">Point in the reference rectangle of the shape to position the origin of the image.</span></span> <span data-ttu-id="3ec7a-562">La valeur par défaut est le centre du rectangle de conteneur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-562">Default is the center of the container rectangle.</span></span> <span data-ttu-id="3ec7a-563">Le vecteur est une fraction (0,0-1,0) de la largeur et de la hauteur de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-563">The vector is a fraction (0.0 - 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-564">Taille</span><span class="sxs-lookup"><span data-stu-id="3ec7a-564">Size</span></span></td>
<td><span data-ttu-id="3ec7a-565"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-565"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="3ec7a-566">Taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-566">The size of the image.</span></span> <span data-ttu-id="3ec7a-567">La valeur par défaut est la taille en pixels de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-567">Default is pixel size of the image.</span></span> <span data-ttu-id="3ec7a-568">Peut être spécifié en coordonnées absolues ou en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-568">May be specified in absolute coordinates or percentage.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-569">Source</span><span class="sxs-lookup"><span data-stu-id="3ec7a-569">Src</span></span></td>
<td><span data-ttu-id="3ec7a-570"><a href="#data-types-used-in-the-vml-object-model">Chaîne</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-570"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="3ec7a-571">URL vers une image à charger pour les remplissages d’image et de motif.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-571">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="3ec7a-572">Cet attribut doit toujours être présent et pointer vers des données d’image valides pour qu’une image s’affiche.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-572">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-573">Type</span><span class="sxs-lookup"><span data-stu-id="3ec7a-573">Type</span></span></td>
<td><span data-ttu-id="3ec7a-574">VgFillType.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-574">VgFillType.</span></span> <span data-ttu-id="3ec7a-575">qui peut être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-575">May be one of the following types:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-576">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="3ec7a-576">Background</span></span></li>
<li><span data-ttu-id="3ec7a-577">Frame</span><span class="sxs-lookup"><span data-stu-id="3ec7a-577">Frame</span></span></li>
<li><span data-ttu-id="3ec7a-578">Dégradé</span><span class="sxs-lookup"><span data-stu-id="3ec7a-578">Gradient</span></span></li>
<li><span data-ttu-id="3ec7a-579">GradientCenter</span><span class="sxs-lookup"><span data-stu-id="3ec7a-579">GradientCenter</span></span></li>
<li><span data-ttu-id="3ec7a-580">GradientRadial</span><span class="sxs-lookup"><span data-stu-id="3ec7a-580">GradientRadial</span></span></li>
<li><span data-ttu-id="3ec7a-581">GradientTitle</span><span class="sxs-lookup"><span data-stu-id="3ec7a-581">GradientTitle</span></span></li>
<li><span data-ttu-id="3ec7a-582">GradientUnscaled</span><span class="sxs-lookup"><span data-stu-id="3ec7a-582">GradientUnscaled</span></span></li>
<li><span data-ttu-id="3ec7a-583">Modèle</span><span class="sxs-lookup"><span data-stu-id="3ec7a-583">Pattern</span></span></li>
<li><span data-ttu-id="3ec7a-584">Unie</span><span class="sxs-lookup"><span data-stu-id="3ec7a-584">Solid</span></span></li>
<li><span data-ttu-id="3ec7a-585">Tile</span><span class="sxs-lookup"><span data-stu-id="3ec7a-585">Tile</span></span></li>
</ul>
<span data-ttu-id="3ec7a-586">Les mosaïques, les modèles et les frames requièrent que les attributs d’image soient fournis.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-586">Tile, Pattern, and Frame require the image attributes to be supplied.</span></span> <span data-ttu-id="3ec7a-587">Les attributs gradient et GradientRadial requièrent que les attributs de dégradé soient fournis.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-587">Gradient and GradientRadial require the gradient attributes to be supplied.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a><span data-ttu-id="3ec7a-588">élément Group</span><span class="sxs-lookup"><span data-stu-id="3ec7a-588">Group element</span></span>

<span data-ttu-id="3ec7a-589">Un groupe est une collection de formes individuelles qui peuvent être positionnées et transformées en une unité.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-589">A group is a collection of individual shapes that can be positioned and transformed as a unit.</span></span>



|        |                                                                                              |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec7a-590">Élément</span><span class="sxs-lookup"><span data-stu-id="3ec7a-590">Item</span></span>   | <span data-ttu-id="3ec7a-591">[IVgShape](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-591">[IVgShape](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-592">Élément spécifié dans le tableau de formes.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-592">Specified item in the array of shapes.</span></span> |
| <span data-ttu-id="3ec7a-593">Longueur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-593">Length</span></span> | <span data-ttu-id="3ec7a-594">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-594">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-595">Nombre de formes dans ce groupe.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-595">Number of shapes in this group.</span></span>         |



 

### <a name="imagedata-element"></a><span data-ttu-id="3ec7a-596">Élément ImageData</span><span class="sxs-lookup"><span data-stu-id="3ec7a-596">Imagedata element</span></span>

<span data-ttu-id="3ec7a-597">Décrit une image à afficher en haut d’une forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-597">Describes a picture to be rendered on top of a shape.</span></span>



|             |                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec7a-598">Anticrénelage</span><span class="sxs-lookup"><span data-stu-id="3ec7a-598">BiLevel</span></span>     | <span data-ttu-id="3ec7a-599">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-599">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="3ec7a-600">Affichez l’image dans deux couleurs uniquement (généralement en noir et blanc).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-600">Display picture in only two colors (usually black and white).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="3ec7a-601">BlackLevel</span><span class="sxs-lookup"><span data-stu-id="3ec7a-601">BlackLevel</span></span>  | <span data-ttu-id="3ec7a-602">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-602">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="3ec7a-603">Permet de définir le niveau de manière à ce que les noirs apparaissent comme des véritables noirs et que toutes les autres couleurs soient visibles en tant que nuances au-dessus du noir.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-603">Allows adjustment to set the level so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="3ec7a-604">Chromakey</span><span class="sxs-lookup"><span data-stu-id="3ec7a-604">Chromakey</span></span>   | <span data-ttu-id="3ec7a-605">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-605">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="3ec7a-606">Couleur transparente de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-606">Transparent color of picture.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3ec7a-607">CropBottom</span><span class="sxs-lookup"><span data-stu-id="3ec7a-607">CropBottom</span></span>  | <span data-ttu-id="3ec7a-608">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-608">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-609">Distance de rognage à partir du bas de l’image exprimée sous la forme d’un pourcentage de la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-609">Crop distance from bottom of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="3ec7a-610">CropLeft</span><span class="sxs-lookup"><span data-stu-id="3ec7a-610">CropLeft</span></span>    | <span data-ttu-id="3ec7a-611">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-611">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-612">Distance de rognage à partir du bord gauche de l’image exprimée sous la forme d’une fraction de la taille de l’image (de 0,0 à 1,0).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-612">Crop distance from left edge of picture expressed as a fraction of picture size (from 0.0 to 1.0).</span></span> <span data-ttu-id="3ec7a-613">Toutefois, « out-recadrage » est pris en charge et, par conséquent, les valeurs inférieures à 0 et supérieures à 1 sont prises en charge ; par exemple,-5, 20 découpent les limites 25X la taille de l’image avec 4/5 d’un côté de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-613">However, "out-cropping" is supported and thus values of less than 0 and greater than 1 are supported; e.g., -5, 20 would out-crop the bounds 25X the picture size with 4/5 on one side of the picture.</span></span> |
| <span data-ttu-id="3ec7a-614">CropRight</span><span class="sxs-lookup"><span data-stu-id="3ec7a-614">CropRight</span></span>   | <span data-ttu-id="3ec7a-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-616">Distance de rognage à partir de la droite de l’image exprimée sous la forme d’un pourcentage de la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-616">Crop distance from right of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="3ec7a-617">CropTop</span><span class="sxs-lookup"><span data-stu-id="3ec7a-617">CropTop</span></span>     | <span data-ttu-id="3ec7a-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-619">Distance de rognage à partir du haut de l’image exprimée sous la forme d’un pourcentage de la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-619">Crop distance from top of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="3ec7a-620">EmbossColor</span><span class="sxs-lookup"><span data-stu-id="3ec7a-620">EmbossColor</span></span> | <span data-ttu-id="3ec7a-621">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-621">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="3ec7a-622">Il s’agit d’un pourcentage de la couleur de l’ombre pour créer un effet d’image en relief.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-622">This is set to a percentage of the shadow color to create an embossed picture effect.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="3ec7a-623">Maîtrise</span><span class="sxs-lookup"><span data-stu-id="3ec7a-623">Gain</span></span>        | <span data-ttu-id="3ec7a-624">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-624">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-625">Ajuste l’intensité de toutes les couleurs.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-625">Adjusts the intensity of all colors.</span></span> <span data-ttu-id="3ec7a-626">Définit essentiellement le degré de luminosité du blanc.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-626">Essentially sets how bright white will be.</span></span> <span data-ttu-id="3ec7a-627">Est compris entre 0 et 32767.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-627">Ranges from 0 to 32767.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="3ec7a-628">Gamma</span><span class="sxs-lookup"><span data-stu-id="3ec7a-628">Gamma</span></span>       | <span data-ttu-id="3ec7a-629">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-629">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="3ec7a-630">Correction gamma.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-630">Gamma correction.</span></span> <span data-ttu-id="3ec7a-631">L’amélioration de l’image donne une image plus contrastée.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-631">Increasing it gives an image more contrast.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="3ec7a-632">Nuances de gris</span><span class="sxs-lookup"><span data-stu-id="3ec7a-632">GrayScale</span></span>   | <span data-ttu-id="3ec7a-633">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-633">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="3ec7a-634">Affichez l’image en nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-634">Display picture in grayscale colors.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="3ec7a-635">Source</span><span class="sxs-lookup"><span data-stu-id="3ec7a-635">Src</span></span>         | <span data-ttu-id="3ec7a-636">[Chaîne](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-636">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-637">URL vers une image à charger pour les remplissages d’image et de motif.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-637">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="3ec7a-638">Cet attribut doit toujours être présent et pointer vers des données d’image valides pour qu’une image s’affiche.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-638">This attribute must always be present and point to valid image data for a picture to appear.</span></span>                                                                                                                                                           |



 

### <a name="path-element"></a><span data-ttu-id="3ec7a-639">Élément Path</span><span class="sxs-lookup"><span data-stu-id="3ec7a-639">Path element</span></span>

<span data-ttu-id="3ec7a-640">Définit le chemin d’accès qui compose la forme, à l’aide d’une chaîne qui contient un ensemble complet de commandes de « mouvement du stylet ».</span><span class="sxs-lookup"><span data-stu-id="3ec7a-640">Defines the path that makes up the shape, using a string that contains a rich set of "pen movement" commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-641">Limo</span><span class="sxs-lookup"><span data-stu-id="3ec7a-641">Limo</span></span></td>
<td><span data-ttu-id="3ec7a-642"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-642"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span></span> <span data-ttu-id="3ec7a-643">Définit le point d’étirement de la forme ; par exemple, pour une forme Giraffe, le point Limo serait sur le cou. par conséquent, lorsque la forme est redimensionnée, le cou est étiré et le reste de la forme conserve ses dimensions.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-643">Defines the point where the shape is stretched; e.g., for a giraffe shape, the limo point would be on the neck so when the shape is resized, the neck will stretch and the rest of the shape will maintain its dimensions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-644">TextBoxRect</span><span class="sxs-lookup"><span data-stu-id="3ec7a-644">TextBoxRect</span></span></td>
<td><span data-ttu-id="3ec7a-645"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-645"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span></span> <span data-ttu-id="3ec7a-646">Tableau contenant les rectangles qui définissent l’emplacement où le texte doit être placé.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-646">Array containing the rectangles that define where text should go.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-647">V</span><span class="sxs-lookup"><span data-stu-id="3ec7a-647">V</span></span></td>
<td><span data-ttu-id="3ec7a-648"><a href="#data-types-used-in-the-vml-object-model">Chaîne</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-648"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="3ec7a-649">Correspond à l’attribut v de la balise Path.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-649">Matches the v attribute on the Path tag.</span></span> <span data-ttu-id="3ec7a-650">Notez que le chemin d’accès peut correspondre à un attribut ou à un élément de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-650">Note that path may correspond to Path attribute or element.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-651">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-651">Value</span></span></td>
<td><span data-ttu-id="3ec7a-652"><a href="#data-types-used-in-the-vml-object-model">Chaîne</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-652"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="3ec7a-653">Représentation textuelle des commandes qui définissent le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-653">A text representation of the commands that define the path.</span></span> <span data-ttu-id="3ec7a-654">Les valeurs de coordonnée X ou y peuvent être une référence à une formule dans le formulaire &quot; @# &quot; où # est le nombre ordinal de la formule, par exemple, &quot; @2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-654">X or y-coordinate values can be a reference to a formula in the form &quot;@#&quot; where # is the formula's ordinal number, e.g., &quot;@2&quot;.</span></span> <span data-ttu-id="3ec7a-655">Cette chaîne d’attribut est constituée d’un ensemble complet de commandes, notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-655">This attribute string is made up of a rich set of commands including the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3ec7a-656">Commande</span><span class="sxs-lookup"><span data-stu-id="3ec7a-656">Command</span></span></th>
<th><span data-ttu-id="3ec7a-657">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-657">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-658">AE (angleellipseto)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-658">ae (angleellipseto)</span></span></td>
<td><span data-ttu-id="3ec7a-659"><strong>Centre</strong>(x, y) <strong>taille</strong>(w, h), angle de <strong>début</strong>, <strong>angle de fin</strong></span><span class="sxs-lookup"><span data-stu-id="3ec7a-659"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span></span><br/> <span data-ttu-id="3ec7a-660">Dessinez un segment d’une ellipse.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-660">Draw a segment of an ellipse.</span></span> <span data-ttu-id="3ec7a-661">Une ligne droite est dessinée à partir du point actuel jusqu’au point de départ du segment.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-661">A straight line is drawn from the current point to the start point of the segment.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-662">Al (angleelipse)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-662">al (angleelipse)</span></span></td>
<td><span data-ttu-id="3ec7a-663">Identique à AE, sauf qu’il existe un m implicite vers le point de départ du segment.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-663">Same as ae except that there is an implied m to the starting point of the segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-664">AR (ARC)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-664">ar (arc)</span></span></td>
<td><span data-ttu-id="3ec7a-665">Identique à.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-665">Same as at.</span></span> <span data-ttu-id="3ec7a-666">Toutefois, un nouveau sous-tracé est démarré par un m implicite jusqu’au point de départ de l’arc.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-666">However, a new subpath is started by an implied m to the start point of the arc.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-667">à (ArcTo)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-667">at (arcto)</span></span></td>
<td><span data-ttu-id="3ec7a-668"><strong>end</strong> <strong>gauche</strong>, <strong>haut</strong>, <strong>droite</strong>, <strong>bas</strong>, <strong>début</strong>(x, y) (x, y)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-668"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="3ec7a-669">Les quatre premières valeurs définissent le cadre englobant d’une ellipse.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-669">The first four values define the bounding box of an ellipse.</span></span> <span data-ttu-id="3ec7a-670">Les quatre derniers définissent deux vecteurs radials.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-670">The last four define two radial vectors.</span></span> <span data-ttu-id="3ec7a-671">Un segment de l’ellipse est dessiné qui commence à l’angle défini par le vecteur de démarrage RADIUS et se termine à l’angle défini par le vecteur de fin.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-671">A segment of the ellipse is drawn that starts at the angle defined by the start radius vector and ends at the angle defined by the end vector.</span></span> <span data-ttu-id="3ec7a-672">Une ligne droite est dessinée à partir du point actuel jusqu’au début de l’arc. L’arc est toujours dessiné dans le sens inverse des aiguilles d’une passe.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-672">A straight line is drawn from the current point to the start of the arc. The arc is always drawn in a counterclockwise direction.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-673">c (curveTo)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-673">c (curveto)</span></span></td>
<td><span data-ttu-id="3ec7a-674"><strong>Control1</strong>(x, y) <strong>Control2</strong>(x, y) <strong>à</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-674"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong>(x,y)</span></span> <br/> <span data-ttu-id="3ec7a-675">Dessinez une courbe de Bézier cubique à partir du point actuel jusqu’à la coordonnée donnée par les deux derniers paramètres, les points de contrôle donnés par les quatre premiers paramètres.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-675">Draw a cubic bezier curve from the current point to the coordinate given by the final two parameters, the control points given by the first four parameters.</span></span> <span data-ttu-id="3ec7a-676">Le point actuel devient le point de terminaison de la courbe de Bézier.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-676">The current point becomes the endpoint of the bezier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-677">e (fin)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-677">e (end)</span></span></td>
<td><span data-ttu-id="3ec7a-678">Terminer l’ensemble de sous-chemins en cours.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-678">End the current set of subpaths.</span></span> <span data-ttu-id="3ec7a-679">Un ensemble donné de sous-chemins (délimités par fin) est rempli à l’aide de eofill.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-679">A given set of subpaths (as delimited by end) are filled using eofill.</span></span> <span data-ttu-id="3ec7a-680">Les ensembles de sous-tracés suivants sont remplis indépendamment et superposés sur ceux qui existent déjà.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-680">Subsequent sets of subpaths are filled independently and superimposed on existing ones.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-681">l (LineTo)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-681">l (lineto)</span></span></td>
<td><span data-ttu-id="3ec7a-682">x, y</span><span class="sxs-lookup"><span data-stu-id="3ec7a-682">x,y</span></span><br/> <span data-ttu-id="3ec7a-683">Dessine une ligne du point actuel jusqu’à la coordonnée x, y donnée, qui devient le nouveau point actuel.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-683">Draw a line from the current point to the given x,y-coordinate, which becomes the new current point.</span></span> <span data-ttu-id="3ec7a-684">Des paires de coordonnées supplémentaires peuvent être spécifiées pour former une polyligne, par exemple &quot; l 10, 13, 45, 27, 89,-12 &quot; .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-684">Additional coordinate pairs may be specified to form a polyline, e.g., &quot;l 10,13,45,27,89,-12&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-685">m (MoveTo)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-685">m (moveto)</span></span></td>
<td><span data-ttu-id="3ec7a-686">x, y</span><span class="sxs-lookup"><span data-stu-id="3ec7a-686">x,y</span></span><br/> <span data-ttu-id="3ec7a-687">Démarre un nouveau sous-tracé à la coordonnée x, y donnée.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-687">Start a new subpath at the given x,y-coordinate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-688">NF (NoFill)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-688">nf (nofill)</span></span></td>
<td><span data-ttu-id="3ec7a-689">L’ensemble actuel de sous-chemins (délimité par fin) n’est pas rempli.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-689">The current set of subpaths (delimited by end) will not be filled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-690">NS (noStroke)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-690">ns (nostroke)</span></span></td>
<td><span data-ttu-id="3ec7a-691">L’ensemble actuel de sous-chemins (délimité par fin) n’est pas rayé.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-691">The current set of subpaths (delimited by end) will not be stroked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-692">QB (quadraticbezier)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-692">qb (quadraticbezier)</span></span></td>
<td><span data-ttu-id="3ec7a-693">(<strong>ControlPoint</strong>(x, y)) \*,<strong>end</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-693">(<strong>controlpoint</strong>(x, y))\*,<strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="3ec7a-694">Définit une ou plusieurs courbes de Bézier quadratiques au moyen de points de contrôle et d’un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-694">Defines one or more quadratic bezier curves by means of control points and an endpoint.</span></span> <span data-ttu-id="3ec7a-695">Les points intermédiaires (sur la courbe) sont obtenus par interpolation entre des points de contrôle successifs similaires aux polices TrueType.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-695">Intermediate (on-curve) points are obtained by interpolation between successive control points similar to TrueType fonts.</span></span> <span data-ttu-id="3ec7a-696">Le sous-tracé n’a pas besoin d’être un début, auquel cas le sous-tracé est fermé et le dernier point définit le point de départ.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-696">The subpath need not be a start, in which case the subpath is closed and the last point defines the start point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-697">qx (ellipticalquadrantx)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-697">qx (ellipticalquadrantx)</span></span></td>
<td><span data-ttu-id="3ec7a-698"><strong>fin</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-698"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="3ec7a-699">Un quart d’ellipse est dessiné du point actuel au point de terminaison donné.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-699">A quarter ellipse is drawn from the current point to the given endpoint.</span></span> <span data-ttu-id="3ec7a-700">Le segment elliptique est initialement tangent à une ligne parallèle à l’axe x ; autrement dit, le segment démarre horizontalement.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-700">The elliptical segment is initially tangential to a line parallel to the x-axis; i.e., the segment starts out horizontal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-701">qy (ellipticalquadranty)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-701">qy (ellipticalquadranty)</span></span></td>
<td><span data-ttu-id="3ec7a-702"><strong>fin</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-702"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="3ec7a-703">Identique à qx, à ceci près que le segment elliptique est initialement tangent à une ligne parallèle à l’axe y ; autrement dit, le segment démarre verticalement.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-703">Same as qx except that the elliptical segment is initially tangential to a line parallel to the y-axis; i.e., the segment starts out vertical.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-704">r (rlineto)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-704">r (rlineto)</span></span></td>
<td><span data-ttu-id="3ec7a-705">x, y</span><span class="sxs-lookup"><span data-stu-id="3ec7a-705">x,y</span></span> <br/> <span data-ttu-id="3ec7a-706">Dessinez une ligne du point actuel vers la coordonnée relative (CPX + x, cpy + y).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-706">Draw a line from the current point to the relative coordinate (cpx + x, cpy + y).</span></span> <span data-ttu-id="3ec7a-707">Si des paires de coordonnées supplémentaires sont fournies, chaque nouveau point est calculé par rapport au dernier.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-707">If additional coordinate pairs are given, each new point is computed relative to the last one.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-708">t (rmoveto)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-708">t (rmoveto)</span></span></td>
<td><span data-ttu-id="3ec7a-709">x, y</span><span class="sxs-lookup"><span data-stu-id="3ec7a-709">x,y</span></span><br/> <span data-ttu-id="3ec7a-710">Démarrez un nouveau sous-chemin d’accès aux coordonnées relatives (CPX + x, cpy + y) où CPX, cpy correspond à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-710">Start a new subpath at the relative coordinates ( cpx + x, cpy + y) where cpx, cpy is the current position.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-711">v (curveTo)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-711">v (curveto)</span></span></td>
<td><span data-ttu-id="3ec7a-712"><strong>Control1</strong>(x, y) <strong>Control2</strong>(x, y) <strong>à</strong> (x, y)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-712"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong> (x,y)</span></span> <br/> <span data-ttu-id="3ec7a-713">Courbe de Bézier cubique utilisant les coordonnées données relatives au point actuel.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-713">Cubic bezier curve using the given coordinates relative to the current point.</span></span> <span data-ttu-id="3ec7a-714">Tous les points sont calculés par rapport au même point de départ.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-714">All the points are computed relative to the same starting point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-715">WA (clockwisearcto)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-715">wa (clockwisearcto)</span></span></td>
<td><span data-ttu-id="3ec7a-716">Identique à, mais l’arc est dessiné dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-716">Same as at but the arc is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-717">WR (clockwisearc)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-717">wr (clockwisearc)</span></span></td>
<td><span data-ttu-id="3ec7a-718">Identique à AR mais est dessiné dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-718">Same as ar but is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-719">x (fermer)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-719">x (close)</span></span></td>
<td><span data-ttu-id="3ec7a-720">Fermer le sous-tracé en cours en dessinant une ligne droite à partir du point actuel sur le point MoveTo d’origine.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-720">Close the current subpath by drawing a straight line from the current point to the original moveto point.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a><span data-ttu-id="3ec7a-721">Élément Shadow</span><span class="sxs-lookup"><span data-stu-id="3ec7a-721">Shadow element</span></span>

<span data-ttu-id="3ec7a-722">Décrit un effet d’ombrage sur une forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-722">Describes a shadow effect on a shape.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-723">Couleur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-723">Color</span></span></td>
<td><span data-ttu-id="3ec7a-724"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-724"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="3ec7a-725">Couleur de l’ombre principale.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-725">Color of the primary shadow.</span></span> <span data-ttu-id="3ec7a-726">La valeur par défaut est RVB (128128128)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-726">Default is RGB(128,128,128)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-727">Couleur2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-727">Color2</span></span></td>
<td><span data-ttu-id="3ec7a-728"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-728"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="3ec7a-729">Couleur de la deuxième ombre, ou mise en surbrillance dans une ombre de relief ou d’empreinte.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-729">Color of the second shadow, or highlight in an embossed or engraved shadow.</span></span> <span data-ttu-id="3ec7a-730">La valeur par défaut est RVB (203203203).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-730">Default is RGB(203,203,203).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-731">Matrix</span><span class="sxs-lookup"><span data-stu-id="3ec7a-731">Matrix</span></span></td>
<td><span data-ttu-id="3ec7a-732"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-732"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span></span> <span data-ttu-id="3ec7a-733">Matrice de transformation de perspective au format &quot; Sxx, SXY, syx, SYY, PX, py &quot; [s = Scale, p = perspective].</span><span class="sxs-lookup"><span data-stu-id="3ec7a-733">A perspective transform matrix in the form, &quot;sxx,sxy,syx,syy,px,py&quot; [s=scale, p=perspective].</span></span> <span data-ttu-id="3ec7a-734">Les éléments s spécifient la façon dont l’ombre doit être mise à l’échelle par rapport à la forme, et les éléments p spécifient la façon dont l’ombre doit être faussée par rapport à la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-734">The s items specify how the shadow should scale with respect to the shape, and the p items specify how the shadow should skew with respect to the shape.</span></span> <span data-ttu-id="3ec7a-735">Par exemple, la matrice suivante redimensionne la forme d’un facteur de 2 et l’incline par un facteur de 4 dans toutes les directions :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-735">For example, the following matrix resizes the shape by a factor of 2 and skews it by a factor of 4 in all directions:</span></span> <br/> <span data-ttu-id="3ec7a-736">&quot;2, 2, 2, 2, 4, 4&quot;</span><span class="sxs-lookup"><span data-stu-id="3ec7a-736">&quot;2,2,2,2,4,4&quot;</span></span><br/> <span data-ttu-id="3ec7a-737">Cette matrice est utilisée uniquement si le type de l’ombre est défini sur perspective.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-737">This matrix is only used if the type of the shadow is set to perspective.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-738">Masquée</span><span class="sxs-lookup"><span data-stu-id="3ec7a-738">Obscured</span></span></td>
<td><span data-ttu-id="3ec7a-739"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-739"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="3ec7a-740">L’ombre peut être consultée si aucun remplissage n’est présent sur la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-740">The shadow can be seen through if there is no fill on the shape.</span></span> <span data-ttu-id="3ec7a-741">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-741">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-742">Offset</span><span class="sxs-lookup"><span data-stu-id="3ec7a-742">Offset</span></span></td>
<td><span data-ttu-id="3ec7a-743"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-743"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span></span> <span data-ttu-id="3ec7a-744">Quantité de décalage x, y à partir de l’emplacement de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-744">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="3ec7a-745">La valeur par défaut est &quot; 2pt, 2pt &quot; .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-745">Default is &quot;2pt,2pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-746">Offset2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-746">Offset2</span></span></td>
<td><span data-ttu-id="3ec7a-747"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-747"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="3ec7a-748">Nombre de décalages x, y à partir de l’emplacement de la forme ?.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-748">Amount of x,y second offset from the shape?s location.</span></span> <span data-ttu-id="3ec7a-749">Les valeurs sont soit une mesure absolue, soit une valeur fractionnaire de forme (-0,5 à + 0,5).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-749">Values are either an absolute measurement, or a fractional value of shape (-0.5 to +0.5).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-750">Il en va</span><span class="sxs-lookup"><span data-stu-id="3ec7a-750">On</span></span></td>
<td><span data-ttu-id="3ec7a-751"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-751"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="3ec7a-752">Active ou désactive l’affichage de l’ombre.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-752">Turns the display of the shadow on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-753">Opacity</span><span class="sxs-lookup"><span data-stu-id="3ec7a-753">Opacity</span></span></td>
<td><span data-ttu-id="3ec7a-754"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-754"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="3ec7a-755">Opacité de l’effet d’ombre.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-755">Opacity of the shadow effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-756">Origine</span><span class="sxs-lookup"><span data-stu-id="3ec7a-756">Origin</span></span></td>
<td><span data-ttu-id="3ec7a-757"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a> Paire de valeurs fractionnaires de forme comprise entre-0,5 et + 0,5.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-757"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> A pair of fractional values of shape from -0.5 to +0.5.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-758">Type</span><span class="sxs-lookup"><span data-stu-id="3ec7a-758">Type</span></span></td>
<td><span data-ttu-id="3ec7a-759"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-759"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span></span> <span data-ttu-id="3ec7a-760">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-760">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-761">Unique (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-761">Single (default)</span></span></li>
<li><span data-ttu-id="3ec7a-762">Double</span><span class="sxs-lookup"><span data-stu-id="3ec7a-762">Double</span></span></li>
<li><span data-ttu-id="3ec7a-763">Perspective</span><span class="sxs-lookup"><span data-stu-id="3ec7a-763">Perspective</span></span></li>
<li><span data-ttu-id="3ec7a-764">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="3ec7a-764">ShapeRelative</span></span></li>
<li><span data-ttu-id="3ec7a-765">DrawingRelative</span><span class="sxs-lookup"><span data-stu-id="3ec7a-765">DrawingRelative</span></span></li>
<li><span data-ttu-id="3ec7a-766">Relief</span><span class="sxs-lookup"><span data-stu-id="3ec7a-766">Emboss</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a><span data-ttu-id="3ec7a-767">Élément Skew</span><span class="sxs-lookup"><span data-stu-id="3ec7a-767">Skew element</span></span>

<span data-ttu-id="3ec7a-768">Décrit un effet d’inclinaison de perspective sur une forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-768">Describes a perspective skew effect on a shape.</span></span> <span data-ttu-id="3ec7a-769">L’inclinaison est appliquée aux données de graphique vectoriel, et non aux données d’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-769">The skew is applied to vector graphic data, not image data.</span></span>



|        |                                                                                                                                                                                                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec7a-770">Matrix</span><span class="sxs-lookup"><span data-stu-id="3ec7a-770">Matrix</span></span> | <span data-ttu-id="3ec7a-771">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-771">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-772">Matrice de transformation de perspective sous la forme «Sxx, SXY, syx, SYY, PX, py « \[ s = Scale, p = perspective \] .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-772">A perspective transform matrix in the form, "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective\].</span></span> <span data-ttu-id="3ec7a-773">Si le décalage est en unités absolues alors que PX, py sont en unités UME ^-1 ; Sinon, il s’agit d’une fraction inverse de la taille de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-773">If offset is in absolute units then px,py are in emu ^ -1 units; otherwise they are an inverse fraction of shape size.</span></span> |
| <span data-ttu-id="3ec7a-774">Offset</span><span class="sxs-lookup"><span data-stu-id="3ec7a-774">Offset</span></span> | <span data-ttu-id="3ec7a-775">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-775">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-776">Quantité de décalage x, y à partir de l’emplacement de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-776">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="3ec7a-777">La valeur par défaut est « 2pt, 2pt ».</span><span class="sxs-lookup"><span data-stu-id="3ec7a-777">Default is "2pt,2pt".</span></span>                                                                                                                                                   |
| <span data-ttu-id="3ec7a-778">Il en va</span><span class="sxs-lookup"><span data-stu-id="3ec7a-778">On</span></span>     | <span data-ttu-id="3ec7a-779">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-779">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="3ec7a-780">Active ou désactive l’affichage de l’inclinaison.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-780">Turns the display of the skew on or off.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="3ec7a-781">Origine</span><span class="sxs-lookup"><span data-stu-id="3ec7a-781">Origin</span></span> | <span data-ttu-id="3ec7a-782">[Vector2d](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-782">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="3ec7a-783">Paire de valeurs fractionnaires de forme comprise entre-0,5 et + 0,5.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-783">A pair of fractional values of shape from -0.5 to +0.5.</span></span>                                                                                                                                                                     |



 

### <a name="stroke-element"></a><span data-ttu-id="3ec7a-784">Stroke, élément</span><span class="sxs-lookup"><span data-stu-id="3ec7a-784">Stroke element</span></span>

<span data-ttu-id="3ec7a-785">Décrit comment dessiner le tracé si un point au-delà d’une ligne pleine avec une couleur unie est souhaité.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-785">Describes how to draw the path if something beyond a solid line with a solid color is desired.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-786">Couleur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-786">Color</span></span></td>
<td><span data-ttu-id="3ec7a-787"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-787"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="3ec7a-788">Couleur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-788">The color of the line.</span></span> <span data-ttu-id="3ec7a-789">Identique à l’attribut StrokeColor dans Shape mais le remplace.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-789">Same as StrokeColor attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-790">Couleur2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-790">Color2</span></span></td>
<td><span data-ttu-id="3ec7a-791"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-791"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="3ec7a-792">Couleur secondaire.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-792">Secondary color.</span></span> <span data-ttu-id="3ec7a-793">Utilisé quand FillType est un modèle.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-793">Used when FillType is Pattern.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-794">DashStyle</span><span class="sxs-lookup"><span data-stu-id="3ec7a-794">DashStyle</span></span></td>
<td><span data-ttu-id="3ec7a-795"><strong>VgLineDashStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-795"><strong>VgLineDashStyle</strong>.</span></span> <span data-ttu-id="3ec7a-796">Format du style des tirets.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-796">Dash style format.</span></span> <span data-ttu-id="3ec7a-797">Peut être une valeur spécifique ou une séquence de nombres avec un modèle de tiret défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-797">May be a specific value or a sequence of numbers with a user-defined dash pattern.</span></span> <span data-ttu-id="3ec7a-798">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-798">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-799">Unie (par défaut)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-799">Solid (default)</span></span></li>
<li><span data-ttu-id="3ec7a-800">ShortDash</span><span class="sxs-lookup"><span data-stu-id="3ec7a-800">ShortDash</span></span></li>
<li><span data-ttu-id="3ec7a-801">ShortDot</span><span class="sxs-lookup"><span data-stu-id="3ec7a-801">ShortDot</span></span></li>
<li><span data-ttu-id="3ec7a-802">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="3ec7a-802">ShortDashDot</span></span></li>
<li><span data-ttu-id="3ec7a-803">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="3ec7a-803">ShortDashDotDot</span></span></li>
<li><span data-ttu-id="3ec7a-804">Points</span><span class="sxs-lookup"><span data-stu-id="3ec7a-804">Dot</span></span></li>
<li><span data-ttu-id="3ec7a-805">Tiret</span><span class="sxs-lookup"><span data-stu-id="3ec7a-805">Dash</span></span></li>
<li><span data-ttu-id="3ec7a-806">Tiret-point</span><span class="sxs-lookup"><span data-stu-id="3ec7a-806">DashDot</span></span></li>
<li><span data-ttu-id="3ec7a-807">LongDash</span><span class="sxs-lookup"><span data-stu-id="3ec7a-807">LongDash</span></span></li>
<li><span data-ttu-id="3ec7a-808">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="3ec7a-808">LongDashDot</span></span></li>
<li><span data-ttu-id="3ec7a-809">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="3ec7a-809">LongDashDotDot</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-810">EndArrow</span><span class="sxs-lookup"><span data-stu-id="3ec7a-810">EndArrow</span></span></td>
<td><span data-ttu-id="3ec7a-811"><strong>VgArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-811"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="3ec7a-812">Pointe de flèche pour la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-812">Arrowhead for the end of the line.</span></span> <span data-ttu-id="3ec7a-813">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-813">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-814">Aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-814">None (default)</span></span></li>
<li><span data-ttu-id="3ec7a-815">Bloquer</span><span class="sxs-lookup"><span data-stu-id="3ec7a-815">Block</span></span></li>
<li><span data-ttu-id="3ec7a-816">Classique</span><span class="sxs-lookup"><span data-stu-id="3ec7a-816">Classic</span></span></li>
<li><span data-ttu-id="3ec7a-817">Losange</span><span class="sxs-lookup"><span data-stu-id="3ec7a-817">Diamond</span></span></li>
<li><span data-ttu-id="3ec7a-818">Ovale</span><span class="sxs-lookup"><span data-stu-id="3ec7a-818">Oval</span></span></li>
<li><span data-ttu-id="3ec7a-819">Ouvrir</span><span class="sxs-lookup"><span data-stu-id="3ec7a-819">Open</span></span></li>
<li><span data-ttu-id="3ec7a-820">Chevron</span><span class="sxs-lookup"><span data-stu-id="3ec7a-820">Chevron</span></span></li>
<li><span data-ttu-id="3ec7a-821">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="3ec7a-821">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-822">EndArrowLength</span><span class="sxs-lookup"><span data-stu-id="3ec7a-822">EndArrowLength</span></span></td>
<td><span data-ttu-id="3ec7a-823"><strong>VgArrowHeadLength</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-823"><strong>VgArrowHeadLength</strong>.</span></span> <span data-ttu-id="3ec7a-824">Longueur de la flèche pour la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-824">Arrowhead length for the end of the line.</span></span> <span data-ttu-id="3ec7a-825">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-825">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-826">Court</span><span class="sxs-lookup"><span data-stu-id="3ec7a-826">Short</span></span></li>
<li><span data-ttu-id="3ec7a-827">Moyenne (par défaut)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-827">Medium (default)</span></span></li>
<li><span data-ttu-id="3ec7a-828">Long</span><span class="sxs-lookup"><span data-stu-id="3ec7a-828">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-829">EndArrowWidth</span><span class="sxs-lookup"><span data-stu-id="3ec7a-829">EndArrowWidth</span></span></td>
<td><span data-ttu-id="3ec7a-830"><strong>VgArrowheadWidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-830"><strong>VgArrowheadWidth</strong>.</span></span> <span data-ttu-id="3ec7a-831">Largeur de la flèche pour la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-831">Arrowhead width for the end of the line.</span></span> <span data-ttu-id="3ec7a-832">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-832">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-833">Restreindre</span><span class="sxs-lookup"><span data-stu-id="3ec7a-833">Narrow</span></span></li>
<li><span data-ttu-id="3ec7a-834">Moyenne (par défaut)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-834">Medium (default)</span></span></li>
<li><span data-ttu-id="3ec7a-835">Large</span><span class="sxs-lookup"><span data-stu-id="3ec7a-835">Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-836">Extrem</span><span class="sxs-lookup"><span data-stu-id="3ec7a-836">EndCap</span></span></td>
<td><span data-ttu-id="3ec7a-837"><strong>VgLineEndCapStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-837"><strong>VgLineEndCapStyle</strong>.</span></span> <span data-ttu-id="3ec7a-838">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-838">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-839">À deux dimensions</span><span class="sxs-lookup"><span data-stu-id="3ec7a-839">Flat</span></span></li>
<li><span data-ttu-id="3ec7a-840">Carré</span><span class="sxs-lookup"><span data-stu-id="3ec7a-840">Square</span></span></li>
<li><span data-ttu-id="3ec7a-841">Round</span><span class="sxs-lookup"><span data-stu-id="3ec7a-841">Round</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-842">FillType</span><span class="sxs-lookup"><span data-stu-id="3ec7a-842">FillType</span></span></td>
<td><span data-ttu-id="3ec7a-843"><strong>VgLineFillType</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-843"><strong>VgLineFillType</strong>.</span></span> <span data-ttu-id="3ec7a-844">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-844">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-845">Unie (par défaut)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-845">Solid (default)</span></span></li>
<li><span data-ttu-id="3ec7a-846">Tile</span><span class="sxs-lookup"><span data-stu-id="3ec7a-846">Tile</span></span></li>
<li><span data-ttu-id="3ec7a-847">Modèle</span><span class="sxs-lookup"><span data-stu-id="3ec7a-847">Pattern</span></span></li>
<li><span data-ttu-id="3ec7a-848">Frame</span><span class="sxs-lookup"><span data-stu-id="3ec7a-848">Frame</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-849">ImageAlignShape</span><span class="sxs-lookup"><span data-stu-id="3ec7a-849">ImageAlignShape</span></span></td>
<td><span data-ttu-id="3ec7a-850"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-850"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="3ec7a-851">Alignez l’image avec la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-851">Align the image with the shape.</span></span> <span data-ttu-id="3ec7a-852">Si la valeur est false, l’image est alignée avec la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-852">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-853">ImageAspect</span><span class="sxs-lookup"><span data-stu-id="3ec7a-853">ImageAspect</span></span></td>
<td><span data-ttu-id="3ec7a-854"><strong>VgAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-854"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="3ec7a-855">L’attribut ImageSize est ajusté pour conserver l’aspect de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-855">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="3ec7a-856">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-856">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3ec7a-857">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-857">Value</span></span></th>
<th><span data-ttu-id="3ec7a-858">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-858">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-859">Ignorer</span><span class="sxs-lookup"><span data-stu-id="3ec7a-859">Ignore</span></span></td>
<td><span data-ttu-id="3ec7a-860">Ignorer les problèmes d’aspect.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-860">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-861">Au moins</span><span class="sxs-lookup"><span data-stu-id="3ec7a-861">AtLeast</span></span></td>
<td><span data-ttu-id="3ec7a-862">L’image est au moins aussi grande que la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-862">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-863">AtMost</span><span class="sxs-lookup"><span data-stu-id="3ec7a-863">AtMost</span></span></td>
<td><span data-ttu-id="3ec7a-864">L’image n’est pas plus grande que la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-864">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-865">ImageSize</span><span class="sxs-lookup"><span data-stu-id="3ec7a-865">ImageSize</span></span></td>
<td><span data-ttu-id="3ec7a-866"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2d</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-866"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="3ec7a-867">Taille de l’image avec laquelle former le pinceau.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-867">Size of the image to form the brush with.</span></span> <span data-ttu-id="3ec7a-868">La valeur par défaut est la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-868">Default is the size of the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-869">JoinStyle</span><span class="sxs-lookup"><span data-stu-id="3ec7a-869">JoinStyle</span></span></td>
<td><span data-ttu-id="3ec7a-870"><strong>VgLineJoinStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-870"><strong>VgLineJoinStyle</strong>.</span></span> <span data-ttu-id="3ec7a-871">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-871">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-872">Round (joint arrondi)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-872">Round (rounded joint)</span></span></li>
<li><span data-ttu-id="3ec7a-873">Biseau (joint biseauté)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-873">Bevel (beveled joint)</span></span></li>
<li><span data-ttu-id="3ec7a-874">Mitre (articulation à onglet)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-874">Miter (miter joint)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-875">LineStyle</span><span class="sxs-lookup"><span data-stu-id="3ec7a-875">LineStyle</span></span></td>
<td><span data-ttu-id="3ec7a-876"><strong>VgLineStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-876"><strong>VgLineStyle</strong>.</span></span> <span data-ttu-id="3ec7a-877">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-877">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-878">Unique</span><span class="sxs-lookup"><span data-stu-id="3ec7a-878">Single</span></span></li>
<li><span data-ttu-id="3ec7a-879">ThinThin (1:1:1)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-879">ThinThin (1:1:1)</span></span></li>
<li><span data-ttu-id="3ec7a-880">ThinThick (1:1:2)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-880">ThinThick (1:1:2)</span></span></li>
<li><span data-ttu-id="3ec7a-881">ThickThin (2:1:1)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-881">ThickThin (2:1:1)</span></span></li>
<li><span data-ttu-id="3ec7a-882">ThickBetweenThin (1:1:2:1:1)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-882">ThickBetweenThin (1:1:2:1:1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-883">MiterLimit</span><span class="sxs-lookup"><span data-stu-id="3ec7a-883">MiterLimit</span></span></td>
<td><span data-ttu-id="3ec7a-884"><a href="msdn-online-vml-vglength.md">Longueur</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-884"><a href="msdn-online-vml-vglength.md">Length</a>.</span></span> <span data-ttu-id="3ec7a-885">Distance maximale entre le point interne et le point externe d’une jointure.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-885">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="3ec7a-886">Ce nombre est un multiple de l’épaisseur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-886">This number is a multiple of the thickness of the line.</span></span> <span data-ttu-id="3ec7a-887">Est compris entre 0 et 32 767.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-887">Ranges from 0 to 32,767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-888">Il en va</span><span class="sxs-lookup"><span data-stu-id="3ec7a-888">On</span></span></td>
<td><span data-ttu-id="3ec7a-889"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-889"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="3ec7a-890">Active ou désactive l’affichage de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-890">Turns the display of the line on and off.</span></span> <span data-ttu-id="3ec7a-891">Identique à l’attribut Stroke dans Shape, mais le remplace.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-891">Same as Stroke attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-892">Opacity</span><span class="sxs-lookup"><span data-stu-id="3ec7a-892">Opacity</span></span></td>
<td><span data-ttu-id="3ec7a-893"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-893"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="3ec7a-894">Opacité du trait.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-894">Opacity of the stroke.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-895">Source</span><span class="sxs-lookup"><span data-stu-id="3ec7a-895">Src</span></span></td>
<td><span data-ttu-id="3ec7a-896">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-896">String.</span></span> <span data-ttu-id="3ec7a-897">URL vers une image à charger pour les remplissages d’image et de motif.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-897">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="3ec7a-898">Cet attribut doit toujours être présent et pointer vers des données d’image valides pour qu’une image s’affiche.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-898">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-899">StartArrow</span><span class="sxs-lookup"><span data-stu-id="3ec7a-899">StartArrow</span></span></td>
<td><span data-ttu-id="3ec7a-900"><strong>VgArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-900"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="3ec7a-901">Pointe de flèche pour le début de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-901">Arrowhead for the start of the line.</span></span> <span data-ttu-id="3ec7a-902">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-902">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-903">Aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-903">None (default)</span></span></li>
<li><span data-ttu-id="3ec7a-904">Bloquer</span><span class="sxs-lookup"><span data-stu-id="3ec7a-904">Block</span></span></li>
<li><span data-ttu-id="3ec7a-905">Classique</span><span class="sxs-lookup"><span data-stu-id="3ec7a-905">Classic</span></span></li>
<li><span data-ttu-id="3ec7a-906">Losange</span><span class="sxs-lookup"><span data-stu-id="3ec7a-906">Diamond</span></span></li>
<li><span data-ttu-id="3ec7a-907">Ovale</span><span class="sxs-lookup"><span data-stu-id="3ec7a-907">Oval</span></span></li>
<li><span data-ttu-id="3ec7a-908">Ouvrir</span><span class="sxs-lookup"><span data-stu-id="3ec7a-908">Open</span></span></li>
<li><span data-ttu-id="3ec7a-909">Chevron</span><span class="sxs-lookup"><span data-stu-id="3ec7a-909">Chevron</span></span></li>
<li><span data-ttu-id="3ec7a-910">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="3ec7a-910">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-911">StartArrowLength</span><span class="sxs-lookup"><span data-stu-id="3ec7a-911">StartArrowLength</span></span></td>
<td><span data-ttu-id="3ec7a-912">VgArrowHeadLength.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-912">VgArrowHeadLength.</span></span> <span data-ttu-id="3ec7a-913">Longueur de la flèche pour le début de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-913">Arrowhead length for the start of the line.</span></span> <span data-ttu-id="3ec7a-914">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-914">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-915">Court</span><span class="sxs-lookup"><span data-stu-id="3ec7a-915">Short</span></span></li>
<li><span data-ttu-id="3ec7a-916">Moyenne (par défaut)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-916">Medium (default)</span></span></li>
<li><span data-ttu-id="3ec7a-917">Long</span><span class="sxs-lookup"><span data-stu-id="3ec7a-917">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-918">StartArrowWidth</span><span class="sxs-lookup"><span data-stu-id="3ec7a-918">StartArrowWidth</span></span></td>
<td><span data-ttu-id="3ec7a-919">VgArrowheadWidth.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-919">VgArrowheadWidth.</span></span> <span data-ttu-id="3ec7a-920">Largeur de la flèche pour le début de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-920">Arrowhead width for the start of the line.</span></span> <span data-ttu-id="3ec7a-921">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-921">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-922">Étroit moyen (par défaut) large</span><span class="sxs-lookup"><span data-stu-id="3ec7a-922">Narrow Medium (default) Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-923">Poids</span><span class="sxs-lookup"><span data-stu-id="3ec7a-923">Weight</span></span></td>
<td><span data-ttu-id="3ec7a-924"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-924"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="3ec7a-925">Largeur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-925">Width of line.</span></span> <span data-ttu-id="3ec7a-926">Est compris entre 0 et 1584.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-926">Ranges from 0 to 1584.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="3ec7a-927">L’attribut DashStyle permet à l’utilisateur de spécifier un modèle de tirets personnalisé.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-927">The DashStyle attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="3ec7a-928">Cette opération s’effectue à l’aide d’une série de nombres.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-928">This is done using a series of numbers.</span></span> <span data-ttu-id="3ec7a-929">Les styles de tirets sont définis en termes de longueur du tiret (partie dessinée du trait) et de la longueur de l’espace entre les tirets.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-929">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="3ec7a-930">Les longueurs sont relatives à la largeur de la ligne ; une longueur de &quot; 1 &quot; est égale à la largeur de ligne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-930">The lengths are relative to the line width; a length of &quot;1&quot; is equal to the line width.</span></span> <span data-ttu-id="3ec7a-931">Le style d’extrémité est appliqué à chaque tiret. les styles de flèche ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-931">The EndCap style is applied to each dash, arrow styles are not.</span></span> <span data-ttu-id="3ec7a-932">La chaîne définit d’abord la longueur du tiret, puis la longueur de l’espace.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-932">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="3ec7a-933">Cela peut être répété pour former des styles de tiret complexes.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-933">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="3ec7a-934">La chaîne doit toujours contenir une paire de nombres ; Si elle contient un nombre impair de nombres, la dernière peut être ignorée.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-934">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span> <span data-ttu-id="3ec7a-935">Le tableau suivant répertorie des valeurs typiques et une description de l’effet prévu.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-935">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="3ec7a-936">&quot;0 &quot; signifie un point qui doit être quatre symétrique (avec des extrémités arrondies, il doit s’agir d’un cercle).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-936">&quot;0&quot; implies a dot that should be fourfold symmetrical (with round endcaps it should be a circle).</span></span> <span data-ttu-id="3ec7a-937">Si l’extrémité de la ligne est plate, une visionneuse doit choisir un tiret de système d’exploitation intégré si possible (c’est-à-dire un point rapide à dessiner).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-937">If the line endcap is Flat, a viewer should choose a built-in operating system dash where possible (i.e., something that is fast to draw).</span></span> <span data-ttu-id="3ec7a-938">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-938">The following shows some examples.</span></span>
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-939">&quot;2 2&quot;</span><span class="sxs-lookup"><span data-stu-id="3ec7a-939">&quot;2 2&quot;</span></span></td>
<td><span data-ttu-id="3ec7a-940">des tirets courts (chaque tiret et l’espace entre deux fois la largeur de la ligne)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-940">short-dashes (each dash and the space in between is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-941">&quot;1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="3ec7a-941">&quot;1 2&quot;</span></span></td>
<td><span data-ttu-id="3ec7a-942">point (chaque tiret correspond à la largeur de la ligne, tandis que chaque espace est deux fois plus large que la largeur de la ligne)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-942">dot (each dash is the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-943">&quot;4 2&quot;</span><span class="sxs-lookup"><span data-stu-id="3ec7a-943">&quot;4 2&quot;</span></span></td>
<td><span data-ttu-id="3ec7a-944">Dash (chaque tiret correspond à quatre fois la largeur de la ligne, tandis que chaque espace est deux fois plus large que la largeur de la ligne)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-944">dash (each dash is four times the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-945">&quot;8 2&quot;</span><span class="sxs-lookup"><span data-stu-id="3ec7a-945">&quot;8 2&quot;</span></span></td>
<td><span data-ttu-id="3ec7a-946">long tiret</span><span class="sxs-lookup"><span data-stu-id="3ec7a-946">long-dash</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-947">&quot;4 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="3ec7a-947">&quot;4 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="3ec7a-948">tiret-point</span><span class="sxs-lookup"><span data-stu-id="3ec7a-948">dash dot</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-949">&quot;8 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="3ec7a-949">&quot;8 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="3ec7a-950">long-tiret-point</span><span class="sxs-lookup"><span data-stu-id="3ec7a-950">long-dash dot</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-951">&quot;8 2 1 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="3ec7a-951">&quot;8 2 1 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="3ec7a-952">point-tiret long</span><span class="sxs-lookup"><span data-stu-id="3ec7a-952">long-dash dot dot</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a><span data-ttu-id="3ec7a-953">Élément TextPath</span><span class="sxs-lookup"><span data-stu-id="3ec7a-953">TextPath element</span></span>

<span data-ttu-id="3ec7a-954">Décrit un tracé vectoriel basé sur les données de texte, la police et les styles fournis.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-954">Describes a vector path based on the text data, font, and styles supplied.</span></span> <span data-ttu-id="3ec7a-955">Le chemin d’accès du texte est déformé pour se conformer à un élément de **chemin d’accès** , s’il est fourni.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-955">The text path is warped to conform to a **Path** element if supplied.</span></span>



|          |                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec7a-956">FitPath</span><span class="sxs-lookup"><span data-stu-id="3ec7a-956">FitPath</span></span>  | <span data-ttu-id="3ec7a-957">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-957">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="3ec7a-958">Dimensionne le texte pour remplir le tracé sur lequel il se trouve.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-958">Sizes the text to fill the path it lies out on.</span></span>                                 |
| <span data-ttu-id="3ec7a-959">FitShape</span><span class="sxs-lookup"><span data-stu-id="3ec7a-959">FitShape</span></span> | <span data-ttu-id="3ec7a-960">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-960">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="3ec7a-961">Étire le tracé du texte vers les bords de la zone de forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-961">Stretches the text path out to the edges of the shape box.</span></span>                      |
| <span data-ttu-id="3ec7a-962">Il en va</span><span class="sxs-lookup"><span data-stu-id="3ec7a-962">On</span></span>       | <span data-ttu-id="3ec7a-963">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-963">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="3ec7a-964">Détermine si les chemins d’accès aux caractères sont affichés ou non.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-964">Determines whether the character paths are displayed or not.</span></span>                    |
| <span data-ttu-id="3ec7a-965">String</span><span class="sxs-lookup"><span data-stu-id="3ec7a-965">String</span></span>   | <span data-ttu-id="3ec7a-966">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-966">String.</span></span> <span data-ttu-id="3ec7a-967">Texte à afficher sous la forme d’un tracé de texte.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-967">The text to render as a text path.</span></span>                                                                                    |
| <span data-ttu-id="3ec7a-968">SupprEspace</span><span class="sxs-lookup"><span data-stu-id="3ec7a-968">Trim</span></span>     | <span data-ttu-id="3ec7a-969">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-969">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="3ec7a-970">Supprime tout espace supplémentaire réservé pour les jambages ascendants et descendants s’il n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-970">Removes any additional space reserved for ascenders and descenders if not used.</span></span> |
| <span data-ttu-id="3ec7a-971">Cadencé</span><span class="sxs-lookup"><span data-stu-id="3ec7a-971">XScale</span></span>   | <span data-ttu-id="3ec7a-972">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-972">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="3ec7a-973">Utilisez une mesure x droite au lieu de mesurer le long du tracé.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-973">Use straight x measurement instead of measuring along the path.</span></span>                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a><span data-ttu-id="3ec7a-974">Types de données utilisés dans le modèle d’objet VML</span><span class="sxs-lookup"><span data-stu-id="3ec7a-974">Data Types Used in the VML Object Model</span></span>

<span data-ttu-id="3ec7a-975">Les types de données suivants sont utilisés par le modèle objet VML.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-975">The following data types are used by the VML Object Model.</span></span>

-   [<span data-ttu-id="3ec7a-976">Double</span><span class="sxs-lookup"><span data-stu-id="3ec7a-976">Double</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-977">Fixe</span><span class="sxs-lookup"><span data-stu-id="3ec7a-977">Fixed</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-978">Integer</span><span class="sxs-lookup"><span data-stu-id="3ec7a-978">Integer</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-979">IVgAdjustments</span><span class="sxs-lookup"><span data-stu-id="3ec7a-979">IVgAdjustments</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-980">IVgColor</span><span class="sxs-lookup"><span data-stu-id="3ec7a-980">IVgColor</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-981">IVgEquation</span><span class="sxs-lookup"><span data-stu-id="3ec7a-981">IVgEquation</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-982">IVgFixedRectangle</span><span class="sxs-lookup"><span data-stu-id="3ec7a-982">IVgFixedRectangle</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-983">IVgFixedRectangleArray</span><span class="sxs-lookup"><span data-stu-id="3ec7a-983">IVgFixedRectangleArray</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-984">IVgFormula</span><span class="sxs-lookup"><span data-stu-id="3ec7a-984">IVgFormula</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-985">IVgFormulas</span><span class="sxs-lookup"><span data-stu-id="3ec7a-985">IVgFormulas</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-986">IVgGradientColorArray</span><span class="sxs-lookup"><span data-stu-id="3ec7a-986">IVgGradientColorArray</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-987">IVgPoints</span><span class="sxs-lookup"><span data-stu-id="3ec7a-987">IVgPoints</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-988">IVgSkewMatrix</span><span class="sxs-lookup"><span data-stu-id="3ec7a-988">IVgSkewMatrix</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-989">IVgSkewOffset</span><span class="sxs-lookup"><span data-stu-id="3ec7a-989">IVgSkewOffset</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-990">IVgVector2D</span><span class="sxs-lookup"><span data-stu-id="3ec7a-990">IVgVector2D</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-991">IVgVector3D</span><span class="sxs-lookup"><span data-stu-id="3ec7a-991">IVgVector3D</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-992">Durée</span><span class="sxs-lookup"><span data-stu-id="3ec7a-992">Length</span></span>](/windows)
-   <span data-ttu-id="3ec7a-993">[Unité](/windows) :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-993">[Measure](/windows)</span></span>
-   [<span data-ttu-id="3ec7a-994">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3ec7a-994">String</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-995">VgBlackWhiteMode</span><span class="sxs-lookup"><span data-stu-id="3ec7a-995">VgBlackWhiteMode</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-996">VgFraction</span><span class="sxs-lookup"><span data-stu-id="3ec7a-996">VgFraction</span></span>](/windows)
-   [<span data-ttu-id="3ec7a-997">VgTriState</span><span class="sxs-lookup"><span data-stu-id="3ec7a-997">VgTriState</span></span>](/windows)

<span data-ttu-id="3ec7a-998">**Double (type de données)**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-998">**Double data type**</span></span>

<span data-ttu-id="3ec7a-999">Entier double précision avec une plage comprise entre-Infinity et Infinity.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-999">A double precision integer with range from -infinity to infinity.</span></span>

<span data-ttu-id="3ec7a-1000">**Type de données fixe**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1000">**Fixed data type**</span></span>

<span data-ttu-id="3ec7a-1001">Nombre à virgule flottante avec une plage comprise entre-32 766,0 et 32 766,0.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1001">Floating point number with range from -32,766.0 to 32,766.0.</span></span>

<span data-ttu-id="3ec7a-1002">**Integer (type de données)**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1002">**Integer data type**</span></span>

<span data-ttu-id="3ec7a-1003">Entier compris entre-Infinity et Infinity.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1003">An integer with a range from -infinity to infinity.</span></span>

<span data-ttu-id="3ec7a-1004">**Type de données IVgAdjustments**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1004">**IVgAdjustments data type**</span></span>

<span data-ttu-id="3ec7a-1005">Collection d’ajustements d’une forme qui peut être utilisée pour modifier les dimensions d’une forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1005">Collection of adjustments to a shape that can be used to change the dimensions of a shape.</span></span> <span data-ttu-id="3ec7a-1006">Les ajustements peuvent être utilisés en tant qu’espaces réservés temporaires ou pour une raison quelconque, vous pouvez utiliser des variables.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1006">Adjustments can be used as temporary placeholders or for any reason you would use variables.</span></span> <span data-ttu-id="3ec7a-1007">La collection ne contient que 8 ajustements.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1007">There are only 8 adjustments in the collection.</span></span>



| <span data-ttu-id="3ec7a-1008">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1008">Attributes</span></span> | <span data-ttu-id="3ec7a-1009">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1009">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec7a-1010">Exists</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1010">Exists</span></span>     | <span data-ttu-id="3ec7a-1011">[IVgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1011">[IVgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="3ec7a-1012">Détermine si un ajustement spécifié existe.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1012">Determines whether a specified adjustment exists.</span></span> <span data-ttu-id="3ec7a-1013">Notez qu’un index doit être utilisé ; en d’autres cas, Exists (Item) doit être utilisé pour récupérer l’existence d’un élément.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1013">Note that an index must be used; that is, exists( item ) must be used to retrieve the existence of an item.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="3ec7a-1014">Élément</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1014">Item</span></span>       | <span data-ttu-id="3ec7a-1015">[Long](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1015">[Long](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1016">Tableau d’ajustements indexés de 0 à 7.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1016">Array of adjustments indexed from 0 to 7.</span></span> <span data-ttu-id="3ec7a-1017">Notez que les ajustements peuvent être spécifiés pour SPARC. autrement dit, les valeurs de tableau intermédiaire ne peuvent pas toujours être remplies.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1017">Note that adjustments may be sparcely specified; that is, intermediate array values may not always be filled.</span></span> <span data-ttu-id="3ec7a-1018">Par exemple, les éléments 1, 3 et 5 peuvent avoir des valeurs pour une longueur de 3, avec l’élément (0), l’élément (2) et l’élément (4) spécifiés.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1018">For example, item 1, 3, and 5 could have values for a length of 3, with item(0), item(2), and item(4) specified.</span></span> <span data-ttu-id="3ec7a-1019">Pour voir si un élément existe, utilisez l’attribut exists.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1019">To see if an item exists, use the Exists attribute.</span></span> |
| <span data-ttu-id="3ec7a-1020">Longueur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1020">Length</span></span>     | <span data-ttu-id="3ec7a-1021">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1021">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1022">Nombre d’ajustements.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1022">Number of adjustments.</span></span> <span data-ttu-id="3ec7a-1023">Ne peut pas être supérieur à 8.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1023">Can be no greater than 8.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3ec7a-1024">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1024">Value</span></span>      | <span data-ttu-id="3ec7a-1025">[Chaîne](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1025">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1026">Représentation textuelle des valeurs numériques, avec des virgules entre chaque nombre.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1026">Text representation of numeric values, with commas between each number.</span></span>                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="3ec7a-1027">**IVgColor**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1027">**IVgColor**</span></span>

<span data-ttu-id="3ec7a-1028">Spécifie une couleur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1028">Specifies a color.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ec7a-1029">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1029">Attributes</span></span></th>
<th><span data-ttu-id="3ec7a-1030">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1030">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1031">RGB</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1031">RGB</span></span></td>
<td><span data-ttu-id="3ec7a-1032"><strong>VgRGBType</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1032"><strong>VgRGBType</strong>.</span></span> <span data-ttu-id="3ec7a-1033">Valeur RVB (longue) de la couleur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1033">RGB value (Long) of the color.</span></span> <span data-ttu-id="3ec7a-1034">Valide uniquement si le type est RVB.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1034">Only valid if Type is RGB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1035">R</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1035">R</span></span></td>
<td><span data-ttu-id="3ec7a-1036"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1036"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="3ec7a-1037">Composant rouge de la couleur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1037">Red component of the color.</span></span> <span data-ttu-id="3ec7a-1038">Peut être compris entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1038">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1039">G</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1039">G</span></span></td>
<td><span data-ttu-id="3ec7a-1040"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1040"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="3ec7a-1041">Composant vert de la couleur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1041">Green component of the color.</span></span> <span data-ttu-id="3ec7a-1042">Peut être compris entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1042">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1043">B</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1043">B</span></span></td>
<td><span data-ttu-id="3ec7a-1044"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1044"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="3ec7a-1045">Composant bleu de la couleur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1045">Blue component of the color.</span></span> <span data-ttu-id="3ec7a-1046">Peut être compris entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1046">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1047">String</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1047">String</span></span></td>
<td><span data-ttu-id="3ec7a-1048"><a href="#data-types-used-in-the-vml-object-model">Chaîne</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1048"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="3ec7a-1049">Représentation textuelle de la couleur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1049">Text representation of the color.</span></span> <span data-ttu-id="3ec7a-1050">Les types de couleur nommés suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1050">The following named color types are supported:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-1051">Noir (#000000)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1051">Black (#000000)</span></span></li>
<li><span data-ttu-id="3ec7a-1052">Silver (#C0C0C0)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1052">Silver (#C0C0C0)</span></span></li>
<li><span data-ttu-id="3ec7a-1053">Gris (#808080)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1053">Gray (#808080)</span></span></li>
<li><span data-ttu-id="3ec7a-1054">Blanc (#FFFFFF)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1054">White (#FFFFFF)</span></span></li>
<li><span data-ttu-id="3ec7a-1055">Marron (#800000)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1055">Maroon (#800000)</span></span></li>
<li><span data-ttu-id="3ec7a-1056">Rouge (#FF0000)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1056">Red (#FF0000)</span></span></li>
<li><span data-ttu-id="3ec7a-1057">Violet (#800080)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1057">Purple (#800080)</span></span></li>
<li><span data-ttu-id="3ec7a-1058">Fuchsia (#FF00FF)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1058">Fuchsia (#FF00FF)</span></span></li>
<li><span data-ttu-id="3ec7a-1059">Vert (#008000)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1059">Green (#008000)</span></span></li>
<li><span data-ttu-id="3ec7a-1060">Chaux (#00FF00)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1060">Lime (#00FF00)</span></span></li>
<li><span data-ttu-id="3ec7a-1061">Vert olive (#808000)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1061">Olive (#808000)</span></span></li>
<li><span data-ttu-id="3ec7a-1062">Jaune (#FFFF00)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1062">Yellow (#FFFF00)</span></span></li>
<li><span data-ttu-id="3ec7a-1063">Bleu marine (#000080)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1063">Navy (#000080)</span></span></li>
<li><span data-ttu-id="3ec7a-1064">Bleu (#0000FF)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1064">Blue (#0000FF)</span></span></li>
<li><span data-ttu-id="3ec7a-1065">Bleu-vert (#008080)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1065">Teal (#008080)</span></span></li>
<li><span data-ttu-id="3ec7a-1066">Aqua (#00FFFF)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1066">Aqua (#00FFFF)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1067">Type</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1067">Type</span></span></td>
<td><span data-ttu-id="3ec7a-1068"><strong>VgColorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1068"><strong>VgColorType</strong>.</span></span> <span data-ttu-id="3ec7a-1069">Type de couleur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1069">Type of color.</span></span> <span data-ttu-id="3ec7a-1070">L’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1070">One of the following types:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-1071">Mixte</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1071">Mixed</span></span></li>
<li><span data-ttu-id="3ec7a-1072">named</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1072">Named</span></span></li>
<li><span data-ttu-id="3ec7a-1073">RGB</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1073">RGB</span></span></li>
<li><span data-ttu-id="3ec7a-1074">Schéma</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1074">Scheme</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3ec7a-1075">**IVgEquation**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1075">**IVgEquation**</span></span>

<span data-ttu-id="3ec7a-1076">Équations utilisées pour les formules.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1076">Equations used for formulas.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1077">Opération</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1077">Operation</span></span></td>
<td><span data-ttu-id="3ec7a-1078"><strong>VgEquationOperationType</strong> Nom de l’opération à effectuer sur les paramètres.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1078"><strong>VgEquationOperationType</strong> Name of operation to perform on the parameters.</span></span> <span data-ttu-id="3ec7a-1079">Les opérations suivantes peuvent être utilisées dans une équation :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1079">The following operations can be used in an equation:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3ec7a-1080">Opération</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1080">Operation</span></span></th>
<th><span data-ttu-id="3ec7a-1081">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1081">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1082">Abs</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1082">Abs</span></span></td>
<td><span data-ttu-id="3ec7a-1083">Valeur absolue.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1083">Absolute value.</span></span> <br/> <span data-ttu-id="3ec7a-1084"><strong>ABS</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1084"><strong>abs</strong>(v)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1085">Atan2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1085">Atan2</span></span></td>
<td><span data-ttu-id="3ec7a-1086">Arithmétique polaire--résultats en unités FD (degrés multiplié par 65536).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1086">Polar arithmetic--results in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="3ec7a-1087"><strong>atan2</strong>(P1, v)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1087"><strong>atan2</strong>(p1,v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1088">Cos</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1088">Cos</span></span></td>
<td><span data-ttu-id="3ec7a-1089">Cosinus, argument en unités FD (degrés multiplié par 65536).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1089">Cosine, argument in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="3ec7a-1090">v \* <strong>COS</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1090">v \* <strong>cos</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1091">Cosatan2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1091">Cosatan2</span></span></td>
<td><span data-ttu-id="3ec7a-1092">Préserve la précision complète dans le calcul intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1092">Preserves full accuracy in intermediate calculation.</span></span><br/> <span data-ttu-id="3ec7a-1093">v \* <strong>cos (atan2 (</strong> P2, P1 <strong>))</strong></span><span class="sxs-lookup"><span data-stu-id="3ec7a-1093">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1094">Ellipse</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1094">Ellipse</span></span></td>
<td><span data-ttu-id="3ec7a-1095">Ellipse</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1095">Ellipse</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1096">Si</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1096">If</span></span></td>
<td><span data-ttu-id="3ec7a-1097">Test de condition if.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1097">If Condition test.</span></span> <span data-ttu-id="3ec7a-1098">v > 0 <strong>?</strong></span><span class="sxs-lookup"><span data-stu-id="3ec7a-1098">v > 0 <strong>?</strong></span></span> <span data-ttu-id="3ec7a-1099">P1 : P2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1099">p1 : p2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1100">Max</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1100">Max</span></span></td>
<td><span data-ttu-id="3ec7a-1101">Valeur la plus grande de deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1101">The greater of two values.</span></span> <br/> <span data-ttu-id="3ec7a-1102"><strong>Max</strong>(v, P1)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1102"><strong>max</strong>(v,p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1103">ExtracChaîne</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1103">Mid</span></span></td>
<td><span data-ttu-id="3ec7a-1104">Moyenne (v + P1)/2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1104">Average ( v + p1)/2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1105">Min</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1105">Min</span></span></td>
<td><span data-ttu-id="3ec7a-1106">La plus petite des deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1106">The lesser of two values.</span></span> <span data-ttu-id="3ec7a-1107"><strong>min</strong>(v, P1)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1107"><strong>min</strong>(v,p1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1108">Mod</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1108">Mod</span></span></td>
<td><span data-ttu-id="3ec7a-1109">Modulo.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1109">Modulus.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1110">Produit</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1110">Product</span></span></td>
<td><span data-ttu-id="3ec7a-1111">Utilisé pour la multiplication et la Division.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1111">Used for multiplication and division.</span></span> <span data-ttu-id="3ec7a-1112">v \* P1/P2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1112">v \* p1 / p2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1113">Sin</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1113">Sin</span></span></td>
<td><span data-ttu-id="3ec7a-1114">Sinus, argument en unités FD (degrés multiplié par 65536).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1114">Sine, argument in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="3ec7a-1115">v \* <strong>Sin</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1115">v \* <strong>sin</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1116">Sinatan2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1116">Sinatan2</span></span></td>
<td><span data-ttu-id="3ec7a-1117">Préserve la précision complète dans le calcul intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1117">Preserves full accuracy in intermediate calculation.</span></span> <span data-ttu-id="3ec7a-1118">v \* <strong>Sin</strong>(<strong>atan2</strong>(P2, P1))</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1118">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1119">Sqrt</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1119">Sqrt</span></span></td>
<td><span data-ttu-id="3ec7a-1120">Le résultat est positif et arrondit à la valeur inférieure.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1120">Result is positive and rounds down.</span></span> <br/> <span data-ttu-id="3ec7a-1121"><strong>sqrt</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1121"><strong>sqrt</strong>(v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1122">SUM</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1122">Sum</span></span></td>
<td><span data-ttu-id="3ec7a-1123">Utilisé pour l’addition et la soustraction.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1123">Used for addition and subtraction.</span></span><br/> <span data-ttu-id="3ec7a-1124">v + P1 P2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1124">v + p1 p2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1125">Sumangle</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1125">Sumangle</span></span></td>
<td><span data-ttu-id="3ec7a-1126">Angle existant (mis à l’échelle par 65536), où P1 et P2 sont exprimés en degrés.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1126">Existing angle (scaled by 65536), where p1 and p2 are in degrees.</span></span><br/> <span data-ttu-id="3ec7a-1127">v + P1 \* 65536 + P2 \* 65536</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1127">v + p1 \* 65536 + p2 \* 65536</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1128">Tan</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1128">Tan</span></span></td>
<td><span data-ttu-id="3ec7a-1129">Tangente, l’argument est en unités FD (degrés multiplié par 65536).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1129">Tangent, argument is in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="3ec7a-1130">v \* Tan (P1)</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1130">v \* tan( p1 )</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1131">Val</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1131">Val</span></span></td>
<td><span data-ttu-id="3ec7a-1132">Définit une valeur de repère à partir d’une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1132">Defines a guide value from some other value.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1133">Param1</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1133">Param1</span></span></td>
<td><span data-ttu-id="3ec7a-1134"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1134"><strong>Integer</strong>.</span></span> <span data-ttu-id="3ec7a-1135">Premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1135">The first parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1136">Paramtype1</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1136">Paramtype1</span></span></td>
<td><span data-ttu-id="3ec7a-1137"><strong>VgFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1137"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="3ec7a-1138">Type du premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1138">The type of the first parameter.</span></span> <span data-ttu-id="3ec7a-1139">Les valeurs suivantes sont admises :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1139">The following values are supported:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3ec7a-1140">Type</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1140">Type</span></span></th>
<th><span data-ttu-id="3ec7a-1141">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1142">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1142">Value</span></span></td>
<td><span data-ttu-id="3ec7a-1143">Le paramètre est une valeur simple.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1143">Parameter is simple value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1144">AdjustmentReference</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1144">AdjustmentReference</span></span></td>
<td><span data-ttu-id="3ec7a-1145">Le paramètre est une référence à un ajustement.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1145">Parameter is a reference to an adjustment.</span></span> <span data-ttu-id="3ec7a-1146">Par exemple, si le premier paramètre est 1, la valeur du premier ajustement sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1146">For example, if the first parameter is 1, then the value of the first adjustment will be used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1147">FormulaReference</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1147">FormulaReference</span></span></td>
<td><span data-ttu-id="3ec7a-1148">Le paramètre est le résultat d’une référence au résultat d’une formule précédente.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1148">Parameter is the result of a reference to the result of a previous formula.</span></span> <span data-ttu-id="3ec7a-1149">Par exemple, si le premier paramètre a la valeur 2, le résultat de la formule 2 sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1149">For example, if the first parameter is 2, then the result of formula 2 will be used.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1150">Param2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1150">Param2</span></span></td>
<td><span data-ttu-id="3ec7a-1151"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1151"><strong>Integer</strong>.</span></span> <span data-ttu-id="3ec7a-1152">Deuxième paramètre.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1152">The second parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1153">Paramtype2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1153">Paramtype2</span></span></td>
<td><span data-ttu-id="3ec7a-1154"><strong>VgFormulaParamType</strong> Type de paramètre 2.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1154"><strong>VgFormulaParamType</strong> The type of parameter 2.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1155">Val</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1155">Val</span></span></td>
<td><span data-ttu-id="3ec7a-1156"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1156"><strong>Integer</strong>.</span></span> <span data-ttu-id="3ec7a-1157">Résultat.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1157">The result.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1158">Valtype2</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1158">Valtype2</span></span></td>
<td><span data-ttu-id="3ec7a-1159"><strong>VgFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1159"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="3ec7a-1160">Type du résultat.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1160">The type of the result.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3ec7a-1161">**IVgFixedRectangle**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1161">**IVgFixedRectangle**</span></span>

<span data-ttu-id="3ec7a-1162">Spécifie un rectangle fixe.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1162">Specifies a fixed rectangle.</span></span>



| <span data-ttu-id="3ec7a-1163">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1163">Attributes</span></span> | <span data-ttu-id="3ec7a-1164">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1164">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec7a-1165">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1165">Value</span></span>      | <span data-ttu-id="3ec7a-1166">[Chaîne](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1166">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1167">Valeur de texte spécifiant le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1167">Text value specifying the path.</span></span>         |
| <span data-ttu-id="3ec7a-1168">Gauche</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1168">Left</span></span>       | <span data-ttu-id="3ec7a-1169">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1169">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1170">Coordonnée la plus à gauche du rectangle.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1170">Leftmost coordinate of the rectangle.</span></span>   |
| <span data-ttu-id="3ec7a-1171">Haut</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1171">Top</span></span>        | <span data-ttu-id="3ec7a-1172">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1172">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1173">Coordonnée la plus grande du rectangle.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1173">Topmost coordinate of the rectangle.</span></span>    |
| <span data-ttu-id="3ec7a-1174">Right</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1174">Right</span></span>      | <span data-ttu-id="3ec7a-1175">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1175">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1176">Coordonnée la plus à droite du rectangle.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1176">Rightmost coordinate of the rectangle.</span></span>  |
| <span data-ttu-id="3ec7a-1177">Bas</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1177">Bottom</span></span>     | <span data-ttu-id="3ec7a-1178">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1178">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1179">Coordonnée la plus basse du rectangle.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1179">Bottommost coordinate of the rectangle.</span></span> |



 

<span data-ttu-id="3ec7a-1180">**IVgFixedRectangleArray**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1180">**IVgFixedRectangleArray**</span></span>

<span data-ttu-id="3ec7a-1181">Tableau de rectangles fixes.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1181">Array of fixed rectangles.</span></span>



| <span data-ttu-id="3ec7a-1182">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1182">Attributes</span></span> | <span data-ttu-id="3ec7a-1183">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1183">Description</span></span>                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec7a-1184">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1184">Value</span></span>      | <span data-ttu-id="3ec7a-1185">[Chaîne](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1185">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1186">Représentation textuelle d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1186">Text representation of array.</span></span>                           |
| <span data-ttu-id="3ec7a-1187">Longueur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1187">Length</span></span>     | <span data-ttu-id="3ec7a-1188">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1188">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1189">Nombre de rectangles dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1189">Number of rectangles in this array.</span></span>                    |
| <span data-ttu-id="3ec7a-1190">Élément</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1190">Item</span></span>       | <span data-ttu-id="3ec7a-1191">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1191">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1192">Objet Rectangle à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1192">The rectangle object at the specified index.</span></span> |



 

<span data-ttu-id="3ec7a-1193">Type de données **IVgFormula**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1193">**IVgFormula** data type</span></span>

<span data-ttu-id="3ec7a-1194">Définitions des formules qui peuvent varier le tracé d’une forme ou être utilisées à d’autres fins de calcul.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1194">Definitions for formulas that can vary the path of a shape or be used for other calculation purposes.</span></span> <span data-ttu-id="3ec7a-1195">Les formules peuvent être basées sur l’attribut **Adj** d’une forme, ce qui peut changer.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1195">Formulas can be based on the **Adj** attribute of a shape, which can change.</span></span> <span data-ttu-id="3ec7a-1196">Les formules peuvent également faire référence à d’autres formules.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1196">Formulas can reference other formulas as well.</span></span>



| <span data-ttu-id="3ec7a-1197">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1197">Attributes</span></span> | <span data-ttu-id="3ec7a-1198">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1198">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec7a-1199">Eqn</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1199">Eqn</span></span>        | <span data-ttu-id="3ec7a-1200">[IVgEquation](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1200">[IVgEquation](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1201">Chaque formule définit une valeur unique comme résultat de l’évaluation de l’expression.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1201">Each formula defines a single value as the result of the evaluation of the expression.</span></span> <span data-ttu-id="3ec7a-1202">L’expression est définie par cet attribut et présente la forme générale d’une opération suivie de jusqu’à trois arguments, qui peuvent être des valeurs d’ajustement (par exemple, \# 2), des résultats de formules antérieures (par exemple, @2 ), des nombres fixes ou des valeurs prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1202">The expression is defined by this attribute and has the general form of an operation followed by up to three arguments, which may be adjustment values (e.g., \#2), the results of earlier formulas (e.g., @2), fixed numbers, or predefined values.</span></span> |



 

<span data-ttu-id="3ec7a-1203">**Type de données IVgFormulas**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1203">**IVgFormulas data type**</span></span>

<span data-ttu-id="3ec7a-1204">Collection d’objets de formule.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1204">A collection of formula objects.</span></span>



| <span data-ttu-id="3ec7a-1205">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1205">Attributes</span></span> | <span data-ttu-id="3ec7a-1206">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1206">Description</span></span>                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec7a-1207">Longueur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1207">Length</span></span>     | <span data-ttu-id="3ec7a-1208">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1208">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1209">Nombre d’objets de formule dans la collection.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1209">Number of formula objects in collection.</span></span>                                                |
| <span data-ttu-id="3ec7a-1210">Élément</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1210">Item</span></span>       | <span data-ttu-id="3ec7a-1211">[IVgFormula](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1211">[IVgFormula](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1212">Formule spécifique.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1212">A specific formula.</span></span> <span data-ttu-id="3ec7a-1213">Notez que le tableau de formules peut être hérité de le type de forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1213">Note that the formula array may be inherited fom the shape type.</span></span> |



 

<span data-ttu-id="3ec7a-1214">**IVgGradientColorArray**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1214">**IVgGradientColorArray**</span></span>

<span data-ttu-id="3ec7a-1215">Tableau de couleurs qui définissent un dégradé (plage de couleurs fusionnée).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1215">An array of colors that define a gradient (blended range of colors).</span></span>



| <span data-ttu-id="3ec7a-1216">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1216">Attributes</span></span> | <span data-ttu-id="3ec7a-1217">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1217">Description</span></span>                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec7a-1218">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1218">Value</span></span>      | <span data-ttu-id="3ec7a-1219">[Chaîne](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1219">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1220">Spécifie le tableau de couleurs ; par exemple, «Red. 2 ; vert. 4 ; noir. 7»</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1220">Specifies the array of colors; for example, "red .2; green .4; black .7"</span></span> |
| <span data-ttu-id="3ec7a-1221">Longueur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1221">Length</span></span>     | <span data-ttu-id="3ec7a-1222">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1222">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1223">Nombre de couleurs dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1223">Number of colors in the array.</span></span>                                          |



 



| <span data-ttu-id="3ec7a-1224">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1224">Methods</span></span>     | <span data-ttu-id="3ec7a-1225">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1225">Description</span></span>                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec7a-1226">AddColor</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1226">AddColor</span></span>    | <span data-ttu-id="3ec7a-1227">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1227">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="3ec7a-1228">Ajoute une nouvelle couleur au point de terminaison spécifié par fraction.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1228">Adds new color at endpoint specified by fraction.</span></span> <span data-ttu-id="3ec7a-1229">La nouvelle couleur est blanche par défaut et est la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1229">The new color is white by default and is the return value.</span></span> <span data-ttu-id="3ec7a-1230">La couleur peut ensuite être modifiée par référence.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1230">The color can then be changed by reference.</span></span> |
| <span data-ttu-id="3ec7a-1231">RemoveColor</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1231">RemoveColor</span></span> | <span data-ttu-id="3ec7a-1232">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1232">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="3ec7a-1233">Supprime une couleur au point de terminaison spécifié par fraction.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1233">Removes a color at endpoint specified by fraction.</span></span> <span data-ttu-id="3ec7a-1234">Remarque : si 0,0 ou 1,0 n’existe pas, il est implicite et le blanc de couleur est utilisé à ce stade.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1234">Note: if 0.0 or 1.0 does not exist, it is implied and the color white is used at that point.</span></span>          |



 

<span data-ttu-id="3ec7a-1235">**Type de données IVgPoints**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1235">**IVgPoints datatype**</span></span>

<span data-ttu-id="3ec7a-1236">Tableau de points qui définissent une forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1236">Array of points that define a shape.</span></span>



| <span data-ttu-id="3ec7a-1237">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1237">Attributes</span></span> | <span data-ttu-id="3ec7a-1238">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1238">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec7a-1239">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1239">Value</span></span>      | <span data-ttu-id="3ec7a-1240">[Chaîne](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1240">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1241">Représentation textuelle d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1241">Text representation of array.</span></span>           |
| <span data-ttu-id="3ec7a-1242">Longueur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1242">Length</span></span>     | <span data-ttu-id="3ec7a-1243">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1243">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="3ec7a-1244">Nombre de points dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1244">Number of points in this array.</span></span>        |
| <span data-ttu-id="3ec7a-1245">Élément</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1245">Item</span></span>       | <span data-ttu-id="3ec7a-1246">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1246">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="3ec7a-1247">Point au niveau de l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1247">The point at the specified index.</span></span> |



 

<span data-ttu-id="3ec7a-1248">**Type de données IVgSkewMatrix**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1248">**IVgSkewMatrix datatype**</span></span>

<span data-ttu-id="3ec7a-1249">Matrice utilisée pour incliner des formes, une matrice de transformation de perspective sous la forme "*Sxx, SXY, syx, SYY, PX, py* " \[ *s* = Scale, *p* = perspective \] .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1249">A matrix used for skewing shapes, a perspective transform matrix in the form, "*sxx,sxy,syx,syy,px,py* " \[*s* =scale, *p* =perspective\].</span></span> <span data-ttu-id="3ec7a-1250">Si le décalage est en unités absolues, alors *PX, py* sont en unités UME ^-1 ; Sinon, il s’agit d’une fraction inverse de la taille de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1250">If offset is in absolute units, then *px,py* are in emu ^-1 units; otherwise they are an inverse fraction of shape size.</span></span>



| <span data-ttu-id="3ec7a-1251">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1251">Attributes</span></span>   | <span data-ttu-id="3ec7a-1252">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1252">Description</span></span>                                         |
|--------------|-----------------------------------------------------|
| <span data-ttu-id="3ec7a-1253">XtoX</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1253">XtoX</span></span>         | <span data-ttu-id="3ec7a-1254">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1254">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="3ec7a-1255">YtoX</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1255">YtoX</span></span>         | <span data-ttu-id="3ec7a-1256">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1256">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="3ec7a-1257">XtoY</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1257">XtoY</span></span>         | <span data-ttu-id="3ec7a-1258">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1258">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="3ec7a-1259">YtoY</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1259">YtoY</span></span>         | <span data-ttu-id="3ec7a-1260">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1260">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="3ec7a-1261">PerspectiveX</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1261">PerspectiveX</span></span> | <span data-ttu-id="3ec7a-1262">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1262">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="3ec7a-1263">Perspective</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1263">PerspectiveY</span></span> | <span data-ttu-id="3ec7a-1264">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1264">[Double](#data-types-used-in-the-vml-object-model).</span></span> |



 

<span data-ttu-id="3ec7a-1265">**IVgSkewOffset**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1265">**IVgSkewOffset**</span></span>

<span data-ttu-id="3ec7a-1266">Spécifie le décalage de l’inclinaison.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1266">Specifies the offset of the skew.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ec7a-1267">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1267">Attributes</span></span></th>
<th><span data-ttu-id="3ec7a-1268">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1268">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1269">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1269">Value</span></span></td>
<td><span data-ttu-id="3ec7a-1270"><a href="#data-types-used-in-the-vml-object-model">Chaîne</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1270"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="3ec7a-1271">Représentation textuelle du décalage.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1271">Text representation of offset.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1272">X</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1272">X</span></span></td>
<td><span data-ttu-id="3ec7a-1273"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1273"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="3ec7a-1274">Composant X.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1274">X component.</span></span> <span data-ttu-id="3ec7a-1275">Pourcentage ou mesure.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1275">Percentage or measure.</span></span> <span data-ttu-id="3ec7a-1276">Si aucune unité n’est présente, le type ShapeRelative est implicite ; Sinon, le type absolu est implicite.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1276">If no units, then ShapeRelative type is implied; otherwise Absolute type is implied.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1277">O</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1277">Y</span></span></td>
<td><span data-ttu-id="3ec7a-1278"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1278"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="3ec7a-1279">Composant Y.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1279">Y component.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1280">Type</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1280">Type</span></span></td>
<td><span data-ttu-id="3ec7a-1281"><strong>VgSkewTransformType</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1281"><strong>VgSkewTransformType</strong>.</span></span> <span data-ttu-id="3ec7a-1282">Spécifie le type de transformation.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1282">Specifies the type of transformation.</span></span> <span data-ttu-id="3ec7a-1283">Les valeurs valides sont les points d’entier compris entre-Infinity et Infinity.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1283">Valid values are integer points ranging between -infinity and infinity.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3ec7a-1284">Type</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1284">Type</span></span></th>
<th><span data-ttu-id="3ec7a-1285">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1285">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1286">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1286">ShapeRelative</span></span></td>
<td><span data-ttu-id="3ec7a-1287">Les valeurs du décalage sont des pourcentages (proportions) de la taille de la forme d’origine ; par exemple, une valeur de 0,5 signifie un décalage de la moitié de la taille de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1287">The values of the offset are percentages (ratios) of the original shape's size; e.g., a value of 0.5 means an offset half the size of the shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1288">Absolu</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1288">Absolute</span></span></td>
<td><span data-ttu-id="3ec7a-1289">Les valeurs sont des unités absolues.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1289">The values are absolute units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3ec7a-1290">**Type de données IVgVector2D**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1290">**IVgVector2D data type**</span></span>

<span data-ttu-id="3ec7a-1291">Spécifie un vecteur à deux dimensions constitué de deux nombres **doubles** .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1291">Specifies a two-dimensional vector consisting of two **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ec7a-1292">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1292">Attributes</span></span></th>
<th><span data-ttu-id="3ec7a-1293">Description</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1293">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1294">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1294">Value</span></span></td>
<td><span data-ttu-id="3ec7a-1295"><strong>Chaîne</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1295"><strong>String</strong>.</span></span> <span data-ttu-id="3ec7a-1296">Représentation textuelle des deux nombres vectorisés séparés par un espace.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1296">Text representation of both vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1297">X</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1297">X</span></span></td>
<td><span data-ttu-id="3ec7a-1298"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1298"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="3ec7a-1299">Composant X de ce vecteur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1299">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1300">O</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1300">Y</span></span></td>
<td><span data-ttu-id="3ec7a-1301"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1301"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="3ec7a-1302">Composant Y de ce vecteur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1302">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1303">Type</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1303">Type</span></span></td>
<td><span data-ttu-id="3ec7a-1304"><strong>VgVectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1304"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="3ec7a-1305">Unités attendues pour ce vecteur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1305">Expected units for this vector.</span></span> <span data-ttu-id="3ec7a-1306">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1306">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-1307">Mesure</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1307">Measure</span></span></li>
<li><span data-ttu-id="3ec7a-1308">Longueur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1308">Length</span></span></li>
<li><span data-ttu-id="3ec7a-1309">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1309">AngleInDegrees</span></span></li>
<li><span data-ttu-id="3ec7a-1310">Fraction</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1310">Fraction</span></span></li>
<li><span data-ttu-id="3ec7a-1311">Nombre entier de pourcentage</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1311">Number Percentage Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3ec7a-1312">**Type de données IVgVector3D**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1312">**IVgVector3D data type**</span></span>

<span data-ttu-id="3ec7a-1313">Spécifie un vecteur à trois dimensions composé de trois nombres **doubles** .</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1313">Specifies a three-dimensional vector consisting of three **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1314">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1314">Value</span></span></td>
<td><span data-ttu-id="3ec7a-1315"><strong>Chaîne</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1315"><strong>String</strong>.</span></span> <span data-ttu-id="3ec7a-1316">Représentation textuelle de trois nombres vectorisés séparés par un espace.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1316">Text representation of three vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1317">X</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1317">X</span></span></td>
<td><span data-ttu-id="3ec7a-1318"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1318"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="3ec7a-1319">Composant X de ce vecteur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1319">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1320">O</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1320">Y</span></span></td>
<td><span data-ttu-id="3ec7a-1321"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1321"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="3ec7a-1322">Composant Y de ce vecteur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1322">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec7a-1323">Z</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1323">Z</span></span></td>
<td><span data-ttu-id="3ec7a-1324"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1324"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="3ec7a-1325">Composant Z de ce vecteur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1325">Z component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec7a-1326">Type</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1326">Type</span></span></td>
<td><span data-ttu-id="3ec7a-1327"><strong>VgVectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1327"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="3ec7a-1328">Unités attendues pour ce vecteur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1328">Expected units for this vector.</span></span> <span data-ttu-id="3ec7a-1329">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1329">Values are:</span></span>
<ul>
<li><span data-ttu-id="3ec7a-1330">Mesure</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1330">Measure</span></span></li>
<li><span data-ttu-id="3ec7a-1331">Longueur</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1331">Length</span></span></li>
<li><span data-ttu-id="3ec7a-1332">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1332">AngleInDegrees</span></span></li>
<li><span data-ttu-id="3ec7a-1333">Fraction</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1333">Fraction</span></span></li>
<li><span data-ttu-id="3ec7a-1334">Nombre</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1334">Number</span></span></li>
<li><span data-ttu-id="3ec7a-1335">Pourcentage</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1335">Percentage</span></span></li>
<li><span data-ttu-id="3ec7a-1336">Integer</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1336">Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3ec7a-1337">**Type de données de longueur**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1337">**Length data type**</span></span>

<span data-ttu-id="3ec7a-1338">Nombre à virgule flottante avec une plage comprise entre 0 et l’infini.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1338">A floating point number with a range from 0 to infinity.</span></span>

<span data-ttu-id="3ec7a-1339">**Type de données Measure**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1339">**Measure data type**</span></span>

<span data-ttu-id="3ec7a-1340">Nombre à virgule flottante de-Infinity à Infinity.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1340">A floating point number from -infinity to infinity.</span></span>

<span data-ttu-id="3ec7a-1341">**Type de données String**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1341">**String data type**</span></span>

<span data-ttu-id="3ec7a-1342">Données de caractères de n’importe quelle longueur.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1342">Character data of any length.</span></span>

<span data-ttu-id="3ec7a-1343">**VgBlackWhiteMode**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1343">**VgBlackWhiteMode**</span></span>

<span data-ttu-id="3ec7a-1344">Mode de rendu pour le noir et le blanc.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1344">Rendering mode for black and white.</span></span> <span data-ttu-id="3ec7a-1345">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1345">Possible values are:</span></span>

-   <span data-ttu-id="3ec7a-1346">**Color**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1346">**Color**</span></span>
-   <span data-ttu-id="3ec7a-1347">**Auto**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1347">**Auto**</span></span>
-   <span data-ttu-id="3ec7a-1348">**Semble**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1348">**GrayScale**</span></span>
-   <span data-ttu-id="3ec7a-1349">**LightGrayScale**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1349">**LightGrayScale**</span></span>
-   <span data-ttu-id="3ec7a-1350">**InverseGray**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1350">**InverseGray**</span></span>
-   <span data-ttu-id="3ec7a-1351">**GrayOutline**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1351">**GrayOutline**</span></span>
-   <span data-ttu-id="3ec7a-1352">**BlackTextAndLines**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1352">**BlackTextAndLines**</span></span>
-   <span data-ttu-id="3ec7a-1353">**HighContrast**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1353">**HighContrast**</span></span>
-   <span data-ttu-id="3ec7a-1354">**Noir**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1354">**Black**</span></span>
-   <span data-ttu-id="3ec7a-1355">**Blancs**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1355">**White**</span></span>
-   <span data-ttu-id="3ec7a-1356">**Dédessiné**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1356">**Undrawn**</span></span>

<span data-ttu-id="3ec7a-1357">**Type de données VgFraction**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1357">**VgFraction data type**</span></span>

<span data-ttu-id="3ec7a-1358">Nombre à virgule flottante avec une plage comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1358">Floating point number with range from 0.0 to 1.0.</span></span> <span data-ttu-id="3ec7a-1359">Les fractions peuvent également être spécifiées sous la forme d’un pourcentage. par exemple, « 50% ».</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1359">Fractions can also be specified as a percentage; e.g., "50%".</span></span>

<span data-ttu-id="3ec7a-1360">**Type de données VgTriState**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1360">**VgTriState datatype**</span></span>

<span data-ttu-id="3ec7a-1361">Énumération utilisée pour les valeurs qui peuvent être de l’un des trois États suivants :</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1361">Enumeration used for values that can be one of three states:</span></span>

-   <span data-ttu-id="3ec7a-1362">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1362">**TRUE**</span></span>
-   <span data-ttu-id="3ec7a-1363">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1363">**FALSE**</span></span>
-   <span data-ttu-id="3ec7a-1364">**CONDITIONS MIXTES**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-1364">**MIXED**</span></span>