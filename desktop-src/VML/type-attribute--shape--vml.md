---
title: Attribut type (Shape) (VML)
description: Attribut type (Shape) (VML)
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e53b275d6b6327b3d3783704dbd06156e643f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031398"
---
# <a name="type-attribute-shapevml"></a><span data-ttu-id="d3ef0-103">Attribut type (Shape) (VML)</span><span class="sxs-lookup"><span data-stu-id="d3ef0-103">Type Attribute (Shape)(VML)</span></span>

<span data-ttu-id="d3ef0-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d3ef0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d3ef0-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d3ef0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d3ef0-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="d3ef0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d3ef0-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="d3ef0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d3ef0-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d3ef0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d3ef0-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d3ef0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d3ef0-110">Définit une référence à l’ID d’un élément [Typedeforme](msdn-online-vml-shapetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d3ef0-110">Defines a reference to the ID of a [ShapeType](msdn-online-vml-shapetype-element.md) element.</span></span> <span data-ttu-id="d3ef0-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d3ef0-111">Read/write.</span></span> <span data-ttu-id="d3ef0-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="d3ef0-112">**String**.</span></span>

<span data-ttu-id="d3ef0-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="d3ef0-113">**Applies To**</span></span>

[<span data-ttu-id="d3ef0-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="d3ef0-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d3ef0-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="d3ef0-115">**Tag Syntax**</span></span>

``` syntax
<v:
          element 
          type=" expression ">
```

<span data-ttu-id="d3ef0-116">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="d3ef0-116">**Script Syntax**</span></span>

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

<span data-ttu-id="d3ef0-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="d3ef0-117">**Remarks**</span></span>

<span data-ttu-id="d3ef0-118">Si l’attribut de **type** fait référence à l’ID d’un élément **Typedeforme** , les remplissages, les tracés et les traits de **Typedeforme** sont utilisés comme modèles pour créer la forme.</span><span class="sxs-lookup"><span data-stu-id="d3ef0-118">If the **Type** attribute references the ID of a **ShapeType** element, the fills, paths, and strokes of the **ShapeType** are used as templates to create the shape.</span></span> <span data-ttu-id="d3ef0-119">Les valeurs dérivées de **Typedeforme** peuvent être remplacées par des valeurs de forme individuelle.</span><span class="sxs-lookup"><span data-stu-id="d3ef0-119">Values derived from **ShapeType** can be overridden by individual shape values.</span></span>

<span data-ttu-id="d3ef0-120">S’il est utilisé dans les balises, la valeur de chaîne doit commencer par un symbole de signe dièse ( \# ).</span><span class="sxs-lookup"><span data-stu-id="d3ef0-120">If used in tags, the string value must begin with a number sign (\#) symbol.</span></span>

<span data-ttu-id="d3ef0-121">**Attribut standard VML**</span><span class="sxs-lookup"><span data-stu-id="d3ef0-121">**VML Standard Attribute**</span></span>

<span data-ttu-id="d3ef0-122">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="d3ef0-122">**Example**</span></span>

<span data-ttu-id="d3ef0-123">Une forme **Typedeforme** est créée avec « MyType » comme ID.</span><span class="sxs-lookup"><span data-stu-id="d3ef0-123">A **ShapeType** shape is created with the "mytype" as an ID.</span></span>


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



<span data-ttu-id="d3ef0-124">Ensuite, si vous créez une forme à l’aide des valeurs **Typedeforme** , la forme aura les attributs du « MyType » **Typedeforme**; autrement dit, « shape01 » aura un remplissage rouge avec un trait bleu.</span><span class="sxs-lookup"><span data-stu-id="d3ef0-124">Then if you create a shape using the **ShapeType** values, the shape will have the attributes of the "mytype" **ShapeType**; that is, "shape01" will have a red fill with a blue stroke.</span></span>


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



<span data-ttu-id="d3ef0-125">Vous pouvez remplacer les valeurs héritées, par exemple en remplaçant la couleur par le vert.</span><span class="sxs-lookup"><span data-stu-id="d3ef0-125">You can override the inherited values, for example, by changing the color to green.</span></span>


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



<span data-ttu-id="d3ef0-126">[Exemple d’attribut de type](/previous-versions/bb264099(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d3ef0-126">[Type Attribute Example](/previous-versions/bb264099(v=vs.85)).</span></span> <span data-ttu-id="d3ef0-127">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="d3ef0-127">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 