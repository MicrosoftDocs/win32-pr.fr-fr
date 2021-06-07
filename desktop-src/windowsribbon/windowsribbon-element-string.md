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
ms.openlocfilehash: 0b0dab5d7ce1485aad5fe1e15442069c488933aa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443900"
---
# <a name="string-element"></a><span data-ttu-id="d75b4-104">Élément String</span><span class="sxs-lookup"><span data-stu-id="d75b4-104">String element</span></span>

<span data-ttu-id="d75b4-105">Représente une ressource de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="d75b4-105">Represents a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="d75b4-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="d75b4-106">Usage</span></span>

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a><span data-ttu-id="d75b4-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="d75b4-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d75b4-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="d75b4-108">Attribute</span></span></th>
<th><span data-ttu-id="d75b4-109">Type</span><span class="sxs-lookup"><span data-stu-id="d75b4-109">Type</span></span></th>
<th><span data-ttu-id="d75b4-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d75b4-110">Required</span></span></th>
<th><span data-ttu-id="d75b4-111">Description</span><span class="sxs-lookup"><span data-stu-id="d75b4-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d75b4-112"><strong>Contenu</strong></span><span class="sxs-lookup"><span data-stu-id="d75b4-112"><strong>Content</strong></span></span><br/></td>
<td><span data-ttu-id="d75b4-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="d75b4-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="d75b4-114">Non</span><span class="sxs-lookup"><span data-stu-id="d75b4-114">No</span></span><br/></td>
<td><span data-ttu-id="d75b4-115"><dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="d75b4-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d75b4-116">Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="d75b4-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d75b4-117"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="d75b4-117"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="d75b4-118">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="d75b4-118">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="d75b4-119">Non</span><span class="sxs-lookup"><span data-stu-id="d75b4-119">No</span></span><br/></td>
<td><span data-ttu-id="d75b4-120">ID de ressource unique.</span><span class="sxs-lookup"><span data-stu-id="d75b4-120">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="d75b4-121">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="d75b4-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d75b4-122">Valeur entière comprise entre 2 et 59999, inclusive, ou 0X2 et 0xea5f en hexadécimal, inclus.</span><span class="sxs-lookup"><span data-stu-id="d75b4-122">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="d75b4-123">La longueur maximale est de 10 caractères, y compris des zéros non significatifs facultatifs.</span><span class="sxs-lookup"><span data-stu-id="d75b4-123">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d75b4-124"><strong>Symbole</strong></span><span class="sxs-lookup"><span data-stu-id="d75b4-124"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="d75b4-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="d75b4-125">xs:string</span></span><br/></td>
<td><span data-ttu-id="d75b4-126">Non</span><span class="sxs-lookup"><span data-stu-id="d75b4-126">No</span></span><br/></td>
<td><span data-ttu-id="d75b4-127">Symbole de ressource pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="d75b4-127">The resource symbol for the string.</span></span><br/> <br/><span data-ttu-id="d75b4-128">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="d75b4-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d75b4-129">Une lettre ou un trait de soulignement suivi d’une séquence de lettres, de chiffres ou de traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="d75b4-129">A letter or underscore followed by any sequence of letters, digits, or underscores.</span></span><br/> <span data-ttu-id="d75b4-130">La longueur maximale est de 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="d75b4-130">The maximum length is 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d75b4-131">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d75b4-131">Child elements</span></span>



| <span data-ttu-id="d75b4-132">Élément</span><span class="sxs-lookup"><span data-stu-id="d75b4-132">Element</span></span>                                                                   | <span data-ttu-id="d75b4-133">Description</span><span class="sxs-lookup"><span data-stu-id="d75b4-133">Description</span></span>                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="d75b4-134">**String. Content**</span><span class="sxs-lookup"><span data-stu-id="d75b4-134">**String.Content**</span></span>](windowsribbon-element-string-content.md)<br/> | <span data-ttu-id="d75b4-135">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="d75b4-135">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="d75b4-136">**String.Id**</span><span class="sxs-lookup"><span data-stu-id="d75b4-136">**String.Id**</span></span>](windowsribbon-element-string-id.md)<br/>           | <span data-ttu-id="d75b4-137">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="d75b4-137">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="d75b4-138">**String. Symbol**</span><span class="sxs-lookup"><span data-stu-id="d75b4-138">**String.Symbol**</span></span>](windowsribbon-element-string-symbol.md)<br/>   | <span data-ttu-id="d75b4-139">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="d75b4-139">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="d75b4-140">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d75b4-140">Parent elements</span></span>



| <span data-ttu-id="d75b4-141">Élément</span><span class="sxs-lookup"><span data-stu-id="d75b4-141">Element</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d75b4-142">**Commande. KeyTip**</span><span class="sxs-lookup"><span data-stu-id="d75b4-142">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                         |
| [<span data-ttu-id="d75b4-143">**Commande. LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="d75b4-143">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>     |
| [<span data-ttu-id="d75b4-144">**Commande. LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="d75b4-144">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [<span data-ttu-id="d75b4-145">**Commande. TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="d75b4-145">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [<span data-ttu-id="d75b4-146">**Commande. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="d75b4-146">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a><span data-ttu-id="d75b4-147">Remarques</span><span class="sxs-lookup"><span data-stu-id="d75b4-147">Remarks</span></span>

<span data-ttu-id="d75b4-148">facultatif.</span><span class="sxs-lookup"><span data-stu-id="d75b4-148">Optional.</span></span>

<span data-ttu-id="d75b4-149">Peut se produire au plus une fois pour chaque élément [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command. KeyTip**](windowsribbon-element-command-keytip.md), [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)ou [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) .</span><span class="sxs-lookup"><span data-stu-id="d75b4-149">May occur at most once for each [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip**](windowsribbon-element-command-keytip.md), [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), or [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) element.</span></span>

<span data-ttu-id="d75b4-150">La définition de chaîne est ajoutée au fichier d’en-tête du ruban, par exemple `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="d75b4-150">The string definition is added to the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="d75b4-151">La chaîne est ajoutée à une table de chaînes dans le fichier de ressources du ruban où un nom et un ID sont générés par l’infrastructure du ruban si aucun n’est déclaré.</span><span class="sxs-lookup"><span data-stu-id="d75b4-151">The string is added to a string table in the Ribbon resource file where a name and ID are generated by the Ribbon framework if none are declared.</span></span>

## <a name="examples"></a><span data-ttu-id="d75b4-152">Exemples</span><span class="sxs-lookup"><span data-stu-id="d75b4-152">Examples</span></span>

<span data-ttu-id="d75b4-153">L’exemple suivant illustre le balisage pour un élément [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) avec une déclaration de **chaîne** .</span><span class="sxs-lookup"><span data-stu-id="d75b4-153">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a><span data-ttu-id="d75b4-154">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d75b4-154">Element information</span></span>

- <span data-ttu-id="d75b4-155">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="d75b4-155">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="d75b4-156">**Peut être vide**: non</span><span class="sxs-lookup"><span data-stu-id="d75b4-156">**Can be empty**: No</span></span>



 

 





