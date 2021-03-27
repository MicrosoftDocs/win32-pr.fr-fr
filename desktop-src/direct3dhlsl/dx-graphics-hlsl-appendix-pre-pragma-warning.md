---
title: Warning (directive pragma)
description: Directive pragma qui modifie le comportement des messages d’avertissement du compilateur.
ms.assetid: 69488014-36e3-4c87-8b65-6123b5e87bcb
keywords:
- Warning (directive de pragma) HLSL
topic_type:
- apiref
api_name:
- warning pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7599886b47830b33c69f11c0c341c7775c644dd3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940446"
---
# <a name="warning-pragma-directive"></a><span data-ttu-id="0abca-104">Warning (directive pragma)</span><span class="sxs-lookup"><span data-stu-id="0abca-104">warning pragma Directive</span></span>

<span data-ttu-id="0abca-105">Directive pragma qui modifie le comportement des messages d’avertissement du compilateur.</span><span class="sxs-lookup"><span data-stu-id="0abca-105">Pragma directive that modifies the behavior of compiler warning messages.</span></span>



| <span data-ttu-id="0abca-106">\#pragma warning ( *Warning-specifier* : *Warning-Number-List* \[ ; *Warning-specifier* : *Warning-Number-List*... \] )</span><span class="sxs-lookup"><span data-stu-id="0abca-106">\#pragma warning( *warning-specifier* : *warning-number-list* \[; *warning-specifier* : *warning-number-list*...\] )</span></span> |
|----------------------------------------------------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="0abca-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0abca-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0abca-108">Élément</span><span class="sxs-lookup"><span data-stu-id="0abca-108">Item</span></span></th>
<th><span data-ttu-id="0abca-109">Description</span><span class="sxs-lookup"><span data-stu-id="0abca-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0abca-110"><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>Warning-specifier</em></span><span class="sxs-lookup"><span data-stu-id="0abca-110"><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>warning-specifier</em></span></span><br/></td>
<td><span data-ttu-id="0abca-111">Comportement à définir pour les avertissements spécifiés.</span><span class="sxs-lookup"><span data-stu-id="0abca-111">Behavior to set for the specified warnings.</span></span> <span data-ttu-id="0abca-112">Ce paramètre peut prendre l’une des valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0abca-112">This parameter can take one of the values listed in the following table.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0abca-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="0abca-113">Value</span></span></th>
<th><span data-ttu-id="0abca-114">Description</span><span class="sxs-lookup"><span data-stu-id="0abca-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0abca-115">once</span><span class="sxs-lookup"><span data-stu-id="0abca-115">once</span></span></td>
<td><span data-ttu-id="0abca-116">Affiche le message des avertissements avec les nombres spécifiés une seule fois.</span><span class="sxs-lookup"><span data-stu-id="0abca-116">Display the message of the warnings with the specified numbers only once.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0abca-117">default</span><span class="sxs-lookup"><span data-stu-id="0abca-117">default</span></span></td>
<td><span data-ttu-id="0abca-118">Rétablit la valeur par défaut du comportement des avertissements avec les nombres spécifiés.</span><span class="sxs-lookup"><span data-stu-id="0abca-118">Reset the behavior of the warnings with the specified numbers to their default value.</span></span> <span data-ttu-id="0abca-119">Cela a également pour effet d’activer un avertissement sur qui est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="0abca-119">This also has the effect of turning a warning on that is off by default.</span></span> <span data-ttu-id="0abca-120">L’avertissement est généré à son niveau par défaut.</span><span class="sxs-lookup"><span data-stu-id="0abca-120">The warning will be generated at its default level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0abca-121">1, 2, 3, 4</span><span class="sxs-lookup"><span data-stu-id="0abca-121">1, 2, 3, 4</span></span></td>
<td><span data-ttu-id="0abca-122">Applique le niveau spécifié aux avertissements avec les nombres spécifiés.</span><span class="sxs-lookup"><span data-stu-id="0abca-122">Apply the specified level to the warnings with the specified numbers.</span></span> <span data-ttu-id="0abca-123">Cela a également pour effet d’activer un avertissement sur qui est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="0abca-123">This also has the effect of turning a warning on that is off by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0abca-124">disable</span><span class="sxs-lookup"><span data-stu-id="0abca-124">disable</span></span></td>
<td><span data-ttu-id="0abca-125">N’émettez pas les avertissements avec les nombres spécifiés.</span><span class="sxs-lookup"><span data-stu-id="0abca-125">Do not issue the warnings with the specified numbers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0abca-126">erreur</span><span class="sxs-lookup"><span data-stu-id="0abca-126">error</span></span></td>
<td><span data-ttu-id="0abca-127">Signalez les avertissements avec les nombres spécifiés en tant qu’erreurs.</span><span class="sxs-lookup"><span data-stu-id="0abca-127">Report the warnings with the specified numbers as errors.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0abca-128"><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>AVERTISSEMENT : nombre-liste</em></span><span class="sxs-lookup"><span data-stu-id="0abca-128"><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>warning-number-list</em></span></span></p></td>
<td><p><span data-ttu-id="0abca-129">Liste délimitée par des espaces blancs des numéros des avertissements pour modifier le comportement de.</span><span class="sxs-lookup"><span data-stu-id="0abca-129">White space-delimited list of the numbers of the warnings to modify the behavior of.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="0abca-130">Notes</span><span class="sxs-lookup"><span data-stu-id="0abca-130">Remarks</span></span>

<span data-ttu-id="0abca-131">Vous pouvez spécifier n’importe quel nombre de changements de comportement d’avertissement distincts dans le même pragma d’avertissement en séparant les modifications par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="0abca-131">You can specify any number of distinct warning behavior changes within the same warning pragma by separating the changes with semicolons.</span></span>

<span data-ttu-id="0abca-132">Le compilateur ajoute 4000 à tout numéro d’avertissement compris entre 0 et 999.</span><span class="sxs-lookup"><span data-stu-id="0abca-132">The compiler will add 4000 to any warning number that is between 0 and 999.</span></span> <span data-ttu-id="0abca-133">Pour les numéros d’avertissement supérieurs à 4699, (ceux associés à la génération de code), le pragma d’avertissement n’a d’effet que lorsqu’il est placé en dehors des définitions de fonction.</span><span class="sxs-lookup"><span data-stu-id="0abca-133">For warning numbers greater than 4699, (those associated with code generation) the warning pragma has effect only when placed outside function definitions.</span></span> <span data-ttu-id="0abca-134">Le pragma est ignoré s’il spécifie un nombre supérieur à 4699 et est utilisé à l’intérieur d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="0abca-134">The pragma is ignored if it specifies a number greater than 4699 and is used inside a function.</span></span>

<span data-ttu-id="0abca-135">Le pragma warning Warning ne prend pas en charge les fonctionnalités **Push** et **pop** du pragma warning inclus dans le compilateur C++.</span><span class="sxs-lookup"><span data-stu-id="0abca-135">The HLSL warning pragma does not support the **push** and **pop** functionality of the warning pragma included in the C++ compiler.</span></span>

## <a name="examples"></a><span data-ttu-id="0abca-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="0abca-136">Examples</span></span>

<span data-ttu-id="0abca-137">L’exemple suivant désactive les avertissements 4507 et 4034, affiche l’avertissement 4385 une fois, et signale l’avertissement 4164 comme une erreur.</span><span class="sxs-lookup"><span data-stu-id="0abca-137">The following example disables warnings 4507 and 4034, displays warning 4385 once once, and reports warning 4164 as an error.</span></span>


```
#pragma warning( disable : 4507 34; once : 4385; error : 164 )
```



<span data-ttu-id="0abca-138">L’exemple précédent est fonctionnellement équivalent à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="0abca-138">The preceding example is functionally equivalent to the following:</span></span>


```
#pragma warning( disable : 4507 34 )
#pragma warning( once : 4385 )
#pragma warning( error : 164 )
```



## <a name="see-also"></a><span data-ttu-id="0abca-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0abca-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0abca-140">Directives de préprocesseur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0abca-140">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="0abca-141">\#Directive pragma (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0abca-141">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





