---
title: Élément String
description: Représente une ressource de type chaîne.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- Ruban des fenêtres d’élément de chaîne
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 577d318292081dddf4e2839967642c6115a474d6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030296"
---
# <a name="string-element"></a><span data-ttu-id="3f00b-104">Élément String</span><span class="sxs-lookup"><span data-stu-id="3f00b-104">String element</span></span>

<span data-ttu-id="3f00b-105">Représente une ressource de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="3f00b-105">Represents a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="3f00b-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="3f00b-106">Usage</span></span>

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a><span data-ttu-id="3f00b-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="3f00b-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f00b-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="3f00b-108">Attribute</span></span></th>
<th><span data-ttu-id="3f00b-109">Type</span><span class="sxs-lookup"><span data-stu-id="3f00b-109">Type</span></span></th>
<th><span data-ttu-id="3f00b-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3f00b-110">Required</span></span></th>
<th><span data-ttu-id="3f00b-111">Description</span><span class="sxs-lookup"><span data-stu-id="3f00b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3f00b-112"><strong>Contenu</strong></span><span class="sxs-lookup"><span data-stu-id="3f00b-112"><strong>Content</strong></span></span><br/></td>
<td><span data-ttu-id="3f00b-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="3f00b-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="3f00b-114">Non</span><span class="sxs-lookup"><span data-stu-id="3f00b-114">No</span></span><br/></td>
<td><span data-ttu-id="3f00b-115"><dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="3f00b-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3f00b-116">Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="3f00b-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f00b-117"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="3f00b-117"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="3f00b-118">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="3f00b-118">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="3f00b-119">Non</span><span class="sxs-lookup"><span data-stu-id="3f00b-119">No</span></span><br/></td>
<td><span data-ttu-id="3f00b-120">ID de ressource unique.</span><span class="sxs-lookup"><span data-stu-id="3f00b-120">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="3f00b-121">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="3f00b-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3f00b-122">Valeur entière comprise entre 2 et 59999, inclusive, ou 0X2 et 0xea5f en hexadécimal, inclus.</span><span class="sxs-lookup"><span data-stu-id="3f00b-122">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="3f00b-123">La longueur maximale est de 10 caractères, y compris des zéros non significatifs facultatifs.</span><span class="sxs-lookup"><span data-stu-id="3f00b-123">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3f00b-124"><strong>Symbole</strong></span><span class="sxs-lookup"><span data-stu-id="3f00b-124"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="3f00b-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="3f00b-125">xs:string</span></span><br/></td>
<td><span data-ttu-id="3f00b-126">Non</span><span class="sxs-lookup"><span data-stu-id="3f00b-126">No</span></span><br/></td>
<td><span data-ttu-id="3f00b-127">Symbole de ressource pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="3f00b-127">The resource symbol for the string.</span></span><br/> <br/><span data-ttu-id="3f00b-128">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="3f00b-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3f00b-129">Une lettre ou un trait de soulignement suivi d’une séquence de lettres, de chiffres ou de traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="3f00b-129">A letter or underscore followed by any sequence of letters, digits, or underscores.</span></span><br/> <span data-ttu-id="3f00b-130">La longueur maximale est de 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="3f00b-130">The maximum length is 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="3f00b-131">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3f00b-131">Child elements</span></span>



| <span data-ttu-id="3f00b-132">Élément</span><span class="sxs-lookup"><span data-stu-id="3f00b-132">Element</span></span>                                                                   | <span data-ttu-id="3f00b-133">Description</span><span class="sxs-lookup"><span data-stu-id="3f00b-133">Description</span></span>                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="3f00b-134">**String. Content**</span><span class="sxs-lookup"><span data-stu-id="3f00b-134">**String.Content**</span></span>](windowsribbon-element-string-content.md)<br/> | <span data-ttu-id="3f00b-135">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="3f00b-135">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="3f00b-136">**String.Id**</span><span class="sxs-lookup"><span data-stu-id="3f00b-136">**String.Id**</span></span>](windowsribbon-element-string-id.md)<br/>           | <span data-ttu-id="3f00b-137">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="3f00b-137">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="3f00b-138">**String. Symbol**</span><span class="sxs-lookup"><span data-stu-id="3f00b-138">**String.Symbol**</span></span>](windowsribbon-element-string-symbol.md)<br/>   | <span data-ttu-id="3f00b-139">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="3f00b-139">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3f00b-140">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3f00b-140">Parent elements</span></span>



| <span data-ttu-id="3f00b-141">Élément</span><span class="sxs-lookup"><span data-stu-id="3f00b-141">Element</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f00b-142">**Commande. KeyTip**</span><span class="sxs-lookup"><span data-stu-id="3f00b-142">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                         |
| [<span data-ttu-id="3f00b-143">**Commande. LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="3f00b-143">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>     |
| [<span data-ttu-id="3f00b-144">**Commande. LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="3f00b-144">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [<span data-ttu-id="3f00b-145">**Commande. TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="3f00b-145">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [<span data-ttu-id="3f00b-146">**Commande. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="3f00b-146">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a><span data-ttu-id="3f00b-147">Notes</span><span class="sxs-lookup"><span data-stu-id="3f00b-147">Remarks</span></span>

<span data-ttu-id="3f00b-148">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="3f00b-148">Optional.</span></span>

<span data-ttu-id="3f00b-149">Peut se produire au plus une fois pour chaque élément [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command. KeyTip**](windowsribbon-element-command-keytip.md), [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)ou [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) .</span><span class="sxs-lookup"><span data-stu-id="3f00b-149">May occur at most once for each [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip**](windowsribbon-element-command-keytip.md), [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), or [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) element.</span></span>

<span data-ttu-id="3f00b-150">La définition de chaîne est ajoutée au fichier d’en-tête du ruban, par exemple `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="3f00b-150">The string definition is added to the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="3f00b-151">La chaîne est ajoutée à une table de chaînes dans le fichier de ressources du ruban où un nom et un ID sont générés par l’infrastructure du ruban si aucun n’est déclaré.</span><span class="sxs-lookup"><span data-stu-id="3f00b-151">The string is added to a string table in the Ribbon resource file where a name and ID are generated by the Ribbon framework if none are declared.</span></span>

## <a name="examples"></a><span data-ttu-id="3f00b-152">Exemples</span><span class="sxs-lookup"><span data-stu-id="3f00b-152">Examples</span></span>

<span data-ttu-id="3f00b-153">L’exemple suivant illustre le balisage pour un élément [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) avec une déclaration de **chaîne** .</span><span class="sxs-lookup"><span data-stu-id="3f00b-153">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a><span data-ttu-id="3f00b-154">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3f00b-154">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="3f00b-155">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f00b-155">Minimum supported system</span></span><br/> | <span data-ttu-id="3f00b-156">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3f00b-156">Windows 7</span></span> |
| <span data-ttu-id="3f00b-157">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="3f00b-157">Can be empty</span></span>                        | <span data-ttu-id="3f00b-158">Non</span><span class="sxs-lookup"><span data-stu-id="3f00b-158">No</span></span>        |



 

 





