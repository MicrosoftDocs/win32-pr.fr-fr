---
title: élément Command
description: Représente une définition de commande.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- Ruban des fenêtres d’élément de commande
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e1df5b62c7b2d7c55345ba8d6da366d04697054
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443480"
---
# <a name="command-element"></a><span data-ttu-id="e4f72-104">élément Command</span><span class="sxs-lookup"><span data-stu-id="e4f72-104">Command element</span></span>

<span data-ttu-id="e4f72-105">Représente une définition de commande.</span><span class="sxs-lookup"><span data-stu-id="e4f72-105">Represents a Command definition.</span></span>

## <a name="usage"></a><span data-ttu-id="e4f72-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="e4f72-106">Usage</span></span>

``` syntax
<Command
  Name = "xs:string"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string"
  Comment = "xs:string"
  LabelTitle = "xs:string"
  LabelDescription = "xs:string"
  TooltipTitle = "xs:string"
  TooltipDescription = "xs:string"
  Keytip = "xs:string">
  child elements
</Command>
```

## <a name="attributes"></a><span data-ttu-id="e4f72-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="e4f72-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e4f72-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="e4f72-108">Attribute</span></span></th>
<th><span data-ttu-id="e4f72-109">Type</span><span class="sxs-lookup"><span data-stu-id="e4f72-109">Type</span></span></th>
<th><span data-ttu-id="e4f72-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e4f72-110">Required</span></span></th>
<th><span data-ttu-id="e4f72-111">Description</span><span class="sxs-lookup"><span data-stu-id="e4f72-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4f72-112"><strong>Commentaire</strong></span><span class="sxs-lookup"><span data-stu-id="e4f72-112"><strong>Comment</strong></span></span><br/></td>
<td><span data-ttu-id="e4f72-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="e4f72-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="e4f72-114">Non</span><span class="sxs-lookup"><span data-stu-id="e4f72-114">No</span></span><br/></td>
<td><span data-ttu-id="e4f72-115">Utilisé pour annoter l’élément Command.</span><span class="sxs-lookup"><span data-stu-id="e4f72-115">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="e4f72-116">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="e4f72-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e4f72-117">Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="e4f72-117">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> <span data-ttu-id="e4f72-118">Longueur maximale : 250 caractères.</span><span class="sxs-lookup"><span data-stu-id="e4f72-118">Maximum length: 250 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4f72-119"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="e4f72-119"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="e4f72-120">XS : positiveInteger Union XS : String</span><span class="sxs-lookup"><span data-stu-id="e4f72-120">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="e4f72-121">Non</span><span class="sxs-lookup"><span data-stu-id="e4f72-121">No</span></span><br/></td>
<td><span data-ttu-id="e4f72-122">ID de ressource unique.</span><span class="sxs-lookup"><span data-stu-id="e4f72-122">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="e4f72-123">
<dt><span></span><span></span><strong></strong> (Union de XS : positiveInteger et XS : String)</span><span class="sxs-lookup"><span data-stu-id="e4f72-123">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e4f72-124">Valeur entière comprise entre 2 et 59999, inclusive, ou 0X2 et 0xea5f en hexadécimal, inclus.</span><span class="sxs-lookup"><span data-stu-id="e4f72-124">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="e4f72-125">La longueur maximale est de 10 caractères, y compris des zéros non significatifs facultatifs.</span><span class="sxs-lookup"><span data-stu-id="e4f72-125">Maximum length is 10 characters, including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4f72-126"><strong>KeyTip</strong></span><span class="sxs-lookup"><span data-stu-id="e4f72-126"><strong>Keytip</strong></span></span><br/></td>
<td><span data-ttu-id="e4f72-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="e4f72-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="e4f72-128">Non</span><span class="sxs-lookup"><span data-stu-id="e4f72-128">No</span></span><br/></td>
<td><span data-ttu-id="e4f72-129">Chaîne qui représente le raccourci clavier d’un élément de commande.</span><span class="sxs-lookup"><span data-stu-id="e4f72-129">A string that represents the keyboard shortcut of a command element.</span></span><br/> <br/><span data-ttu-id="e4f72-130">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="e4f72-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e4f72-131">Chaîne composée d’une séquence de caractères, y compris un espace blanc.</span><span class="sxs-lookup"><span data-stu-id="e4f72-131">A string composed of any sequence of characters, including white space.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4f72-132"><strong>LabelDescription</strong></span><span class="sxs-lookup"><span data-stu-id="e4f72-132"><strong>LabelDescription</strong></span></span><br/></td>
<td><span data-ttu-id="e4f72-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="e4f72-133">xs:string</span></span><br/></td>
<td><span data-ttu-id="e4f72-134">Non</span><span class="sxs-lookup"><span data-stu-id="e4f72-134">No</span></span><br/></td>
<td><span data-ttu-id="e4f72-135">Chaîne qui représente le texte affiché sur un élément Command.</span><span class="sxs-lookup"><span data-stu-id="e4f72-135">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="e4f72-136">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="e4f72-136">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e4f72-137">Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="e4f72-137">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4f72-138"><strong>LabelTitle</strong></span><span class="sxs-lookup"><span data-stu-id="e4f72-138"><strong>LabelTitle</strong></span></span><br/></td>
<td><span data-ttu-id="e4f72-139">xs:string</span><span class="sxs-lookup"><span data-stu-id="e4f72-139">xs:string</span></span><br/></td>
<td><span data-ttu-id="e4f72-140">Non</span><span class="sxs-lookup"><span data-stu-id="e4f72-140">No</span></span><br/></td>
<td><span data-ttu-id="e4f72-141">Chaîne qui représente le texte affiché sur un élément Command.</span><span class="sxs-lookup"><span data-stu-id="e4f72-141">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="e4f72-142">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="e4f72-142">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e4f72-143">Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="e4f72-143">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4f72-144"><strong>Nom</strong></span><span class="sxs-lookup"><span data-stu-id="e4f72-144"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="e4f72-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="e4f72-145">xs:string</span></span><br/></td>
<td><span data-ttu-id="e4f72-146">Non</span><span class="sxs-lookup"><span data-stu-id="e4f72-146">No</span></span><br/></td>
<td><span data-ttu-id="e4f72-147"><dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="e4f72-147"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e4f72-148">Chaîne qui se compose d’une lettre ou d’un trait de soulignement suivi d’une séquence de chiffres, de lettres ou de traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="e4f72-148">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="e4f72-149">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="e4f72-149">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4f72-150"><strong>Symbole</strong></span><span class="sxs-lookup"><span data-stu-id="e4f72-150"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="e4f72-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="e4f72-151">xs:string</span></span><br/></td>
<td><span data-ttu-id="e4f72-152">Non</span><span class="sxs-lookup"><span data-stu-id="e4f72-152">No</span></span><br/></td>
<td><span data-ttu-id="e4f72-153"><dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="e4f72-153"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e4f72-154">Chaîne qui se compose d’une lettre ou d’un trait de soulignement suivi d’une séquence de chiffres, de lettres ou de traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="e4f72-154">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="e4f72-155">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="e4f72-155">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4f72-156"><strong>TooltipDescription</strong></span><span class="sxs-lookup"><span data-stu-id="e4f72-156"><strong>TooltipDescription</strong></span></span><br/></td>
<td><span data-ttu-id="e4f72-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="e4f72-157">xs:string</span></span><br/></td>
<td><span data-ttu-id="e4f72-158">Non</span><span class="sxs-lookup"><span data-stu-id="e4f72-158">No</span></span><br/></td>
<td><span data-ttu-id="e4f72-159">Chaîne qui représente le texte affiché sur un élément Command.</span><span class="sxs-lookup"><span data-stu-id="e4f72-159">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="e4f72-160">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="e4f72-160">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e4f72-161">Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="e4f72-161">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4f72-162"><strong>TooltipTitle</strong></span><span class="sxs-lookup"><span data-stu-id="e4f72-162"><strong>TooltipTitle</strong></span></span><br/></td>
<td><span data-ttu-id="e4f72-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="e4f72-163">xs:string</span></span><br/></td>
<td><span data-ttu-id="e4f72-164">Non</span><span class="sxs-lookup"><span data-stu-id="e4f72-164">No</span></span><br/></td>
<td><span data-ttu-id="e4f72-165">Chaîne qui représente le texte affiché sur un élément Command.</span><span class="sxs-lookup"><span data-stu-id="e4f72-165">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="e4f72-166">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="e4f72-166">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e4f72-167">Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="e4f72-167">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="e4f72-168">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e4f72-168">Child elements</span></span>



| <span data-ttu-id="e4f72-169">Élément</span><span class="sxs-lookup"><span data-stu-id="e4f72-169">Element</span></span>                                                                                                     | <span data-ttu-id="e4f72-170">Description</span><span class="sxs-lookup"><span data-stu-id="e4f72-170">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="e4f72-171">**Commande. Comment.**</span><span class="sxs-lookup"><span data-stu-id="e4f72-171">**Command.Comment**</span></span>](windowsribbon-element-command-comment.md)<br/>                                 | <span data-ttu-id="e4f72-172">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="e4f72-172">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e4f72-173">**Command.Id**</span><span class="sxs-lookup"><span data-stu-id="e4f72-173">**Command.Id**</span></span>](windowsribbon-element-command-id.md)<br/>                                           | <span data-ttu-id="e4f72-174">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="e4f72-174">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e4f72-175">**Commande. KeyTip**</span><span class="sxs-lookup"><span data-stu-id="e4f72-175">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                                   | <span data-ttu-id="e4f72-176">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="e4f72-176">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e4f72-177">**Commande. LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="e4f72-177">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>               | <span data-ttu-id="e4f72-178">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="e4f72-178">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e4f72-179">**Commande. LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="e4f72-179">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                           | <span data-ttu-id="e4f72-180">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="e4f72-180">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e4f72-181">**Commande. LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="e4f72-181">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> | <span data-ttu-id="e4f72-182">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="e4f72-182">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e4f72-183">**Commande. LargeImages**</span><span class="sxs-lookup"><span data-stu-id="e4f72-183">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         | <span data-ttu-id="e4f72-184">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="e4f72-184">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e4f72-185">**Command.Name**</span><span class="sxs-lookup"><span data-stu-id="e4f72-185">**Command.Name**</span></span>](windowsribbon-element-command-name.md)<br/>                                       | <span data-ttu-id="e4f72-186">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="e4f72-186">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e4f72-187">**Commande. SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="e4f72-187">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | <span data-ttu-id="e4f72-188">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="e4f72-188">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e4f72-189">**Commande. SmallImages**</span><span class="sxs-lookup"><span data-stu-id="e4f72-189">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         | <span data-ttu-id="e4f72-190">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="e4f72-190">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e4f72-191">**Command. Symbol**</span><span class="sxs-lookup"><span data-stu-id="e4f72-191">**Command.Symbol**</span></span>](windowsribbon-element-command-symbol.md)<br/>                                   | <span data-ttu-id="e4f72-192">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="e4f72-192">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e4f72-193">**Commande. TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="e4f72-193">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/>           | <span data-ttu-id="e4f72-194">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="e4f72-194">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e4f72-195">**Commande. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="e4f72-195">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>                       | <span data-ttu-id="e4f72-196">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="e4f72-196">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="e4f72-197">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e4f72-197">Parent elements</span></span>



| <span data-ttu-id="e4f72-198">Élément</span><span class="sxs-lookup"><span data-stu-id="e4f72-198">Element</span></span>                                                                               |
|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4f72-199">**Application. commandes**</span><span class="sxs-lookup"><span data-stu-id="e4f72-199">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e4f72-200">Remarques</span><span class="sxs-lookup"><span data-stu-id="e4f72-200">Remarks</span></span>

<span data-ttu-id="e4f72-201">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e4f72-201">Required.</span></span>

<span data-ttu-id="e4f72-202">Peut se produire une ou plusieurs fois pour chaque élément [**application. Commands**](windowsribbon-element-application-commands.md) .</span><span class="sxs-lookup"><span data-stu-id="e4f72-202">May occur one or more times for each [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>

<span data-ttu-id="e4f72-203">Les éléments enfants de l’élément de **commande** peuvent se produire dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="e4f72-203">The child elements of the **Command** element may occur in any order.</span></span>

<span data-ttu-id="e4f72-204">En général, les ressources de commande sont déclarées dans le balisage du ruban, mais elles peuvent également être définies au moment de l’exécution avec un appel à [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="e4f72-204">Typically, Command resources are declared in Ribbon markup, but they can also be set at run time with a call to [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> <span data-ttu-id="e4f72-205">Par exemple, il est possible de définir la propriété de [ \_ \_ KeyTip KeyTip de l’interface utilisateur](windowsribbon-reference-properties-uipkey-keytip.md) pour une commande au lieu de déclarer une valeur dans le balisage avec l’élément [**Command. KeyTip**](windowsribbon-element-command-keytip.md) .</span><span class="sxs-lookup"><span data-stu-id="e4f72-205">For example, it is possible to set the [UI\_PKEY\_Keytip](windowsribbon-reference-properties-uipkey-keytip.md) property for a Command instead of declaring a value in markup with the [**Command.Keytip**](windowsribbon-element-command-keytip.md) element.</span></span>

<span data-ttu-id="e4f72-206">Dans les cas où les propriétés de commande, telles que les étiquettes et les images, ne peuvent pas être définies avec des [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) , elles peuvent être invalidées avec un appel à [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="e4f72-206">In cases where Command properties, such as labels and images, cannot be set with [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) they can be invalidated with a call to [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span> <span data-ttu-id="e4f72-207">Après l’invalidation, l’infrastructure interroge l’application hôte pour obtenir les détails des ressources.</span><span class="sxs-lookup"><span data-stu-id="e4f72-207">After invalidation, the framework queries the host application for the resource details.</span></span>

> [!Note]  
> <span data-ttu-id="e4f72-208">Une ressource ne peut pas être rétablie à partir de la table de ressources de balisage une fois qu’elle a été invalidée.</span><span class="sxs-lookup"><span data-stu-id="e4f72-208">A resource cannot be reinstated from the markup resource table after it has been invalidated.</span></span>

 

<span data-ttu-id="e4f72-209">Une définition de commande est ajoutée au fichier d’en-tête de balisage du ruban pour chaque **commande** déclarée dans le balisage.</span><span class="sxs-lookup"><span data-stu-id="e4f72-209">A Command definition is added to the Ribbon markup header file for each **Command** declared in markup.</span></span>

<span data-ttu-id="e4f72-210">La valeur de *KeyTip* agit comme touche d’accès rapide pour une commande, sauf si cette commande est exposée par le biais d’un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="e4f72-210">The value of *Keytip* acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="e4f72-211">Dans ce cas, le Framework ignore la valeur *KeyTip* et utilise à la place un caractère précédé d’un signe & comme spécifié par *LabelTitle* ou [l' \_ \_ étiquette de l’interface utilisateur](windowsribbon-reference-properties-uipkey-label.md).</span><span class="sxs-lookup"><span data-stu-id="e4f72-211">In this case, the framework ignores the *Keytip* value and instead uses a character preceded by an ampersand as specified by *LabelTitle* or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="e4f72-212">Si aucune esperluette n’est spécifiée par *LabelTitle* ou par l’étiquette de l’interface utilisateur, aucune touche d’accès ou touche d’accès \_ \_ rapide n’est exposée.</span><span class="sxs-lookup"><span data-stu-id="e4f72-212">If no ampersand is specified by *LabelTitle* or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

## <a name="examples"></a><span data-ttu-id="e4f72-213">Exemples</span><span class="sxs-lookup"><span data-stu-id="e4f72-213">Examples</span></span>

<span data-ttu-id="e4f72-214">L’exemple suivant montre un manifeste d’éléments de **commande** pour un onglet de **démarrage** .</span><span class="sxs-lookup"><span data-stu-id="e4f72-214">The following example shows a manifest of **Command** elements for a **Home** tab.</span></span>


```XML
<Application.Commands>
```




```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```




```XML
</Application.Commands>
```



## <a name="element-information"></a><span data-ttu-id="e4f72-215">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e4f72-215">Element information</span></span>

* <span data-ttu-id="e4f72-216">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4f72-216">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="e4f72-217">**Peut être vide**: non</span><span class="sxs-lookup"><span data-stu-id="e4f72-217">**Can be empty**: No</span></span>



 

