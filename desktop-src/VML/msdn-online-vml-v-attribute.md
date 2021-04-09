---
title: Attribut VML V
description: Attribut VML V
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690518e998163f7e47fb326b3037e6a4ec397e8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101832"
---
# <a name="vml-v-attribute"></a><span data-ttu-id="bda84-103">Attribut VML V</span><span class="sxs-lookup"><span data-stu-id="bda84-103">VML V Attribute</span></span>

<span data-ttu-id="bda84-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bda84-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bda84-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="bda84-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bda84-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="bda84-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bda84-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="bda84-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bda84-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bda84-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bda84-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bda84-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bda84-110">Définit les commandes qui composent un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="bda84-110">Defines the commands that make up a path.</span></span> <span data-ttu-id="bda84-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bda84-111">Read/write.</span></span> <span data-ttu-id="bda84-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="bda84-112">**String**.</span></span>

<span data-ttu-id="bda84-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="bda84-113">**Applies To**</span></span>

[<span data-ttu-id="bda84-114">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="bda84-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="bda84-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="bda84-115">**Tag Syntax**</span></span>

<span data-ttu-id="bda84-116"><v : *élément* v = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="bda84-116"><v: *element* v=" *expression* "></span></span>

<span data-ttu-id="bda84-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="bda84-117">**Script Syntax**</span></span>

<span data-ttu-id="bda84-118">*Element* . v = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="bda84-118">*element* .v="*expression*"</span></span>

<span data-ttu-id="bda84-119">*expression* = *élément*. v</span><span class="sxs-lookup"><span data-stu-id="bda84-119">*expression*=*element*.v</span></span>

<span data-ttu-id="bda84-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="bda84-120">**Remarks**</span></span>

<span data-ttu-id="bda84-121">Remplace l’attribut de **chemin d’accès** d’une forme.</span><span class="sxs-lookup"><span data-stu-id="bda84-121">Overrides the **Path** attribute of a shape.</span></span> <span data-ttu-id="bda84-122">Les coordonnées peuvent être des nombres fixes, des nombres relatifs ou des références à des formules (en utilisant le format « @n », où n est un numéro de formule ; par exemple, « @2 » fait référence à la deuxième formule dans le tableau de formules).</span><span class="sxs-lookup"><span data-stu-id="bda84-122">Coordinates can be fixed numbers, relative numbers, or references to formulas (by using the format of "@n" where n is a formula number; for example, "@2" refers to the second formula in the formula array).</span></span>

<span data-ttu-id="bda84-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="bda84-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="bda84-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bda84-124">**Example**</span></span>

<span data-ttu-id="bda84-125">Un rectangle est créé à l’aide de l’attribut **V** .</span><span class="sxs-lookup"><span data-stu-id="bda84-125">A rectangle is created using the **V** attribute.</span></span> <span data-ttu-id="bda84-126">Notez qu’une lettre minuscule L (commande **LineTo** ) est utilisée après le premier jeu de coordonnées délimitées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="bda84-126">Note that a lowercase letter L (**lineto** command) is used after the first set of comma-delimited coordinates.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 