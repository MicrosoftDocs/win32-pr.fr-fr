---
description: La table des propriétés contient les noms et les valeurs des propriétés de toutes les propriétés définies dans l’installation. Les propriétés avec des valeurs NULL ne sont pas présentes dans la table.
ms.assetid: 1f4215b2-dc71-4e6e-bc2e-3b43316806b9
title: Table de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612ab63aa36de6cf91ec8176eefec84cef591c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756483"
---
# <a name="property-table"></a><span data-ttu-id="e175a-104">Table de propriétés</span><span class="sxs-lookup"><span data-stu-id="e175a-104">Property Table</span></span>

<span data-ttu-id="e175a-105">La table des propriétés contient les noms et les valeurs des propriétés de toutes les propriétés définies dans l’installation.</span><span class="sxs-lookup"><span data-stu-id="e175a-105">The Property table contains the property names and values for all defined properties in the installation.</span></span> <span data-ttu-id="e175a-106">Les propriétés avec des valeurs NULL ne sont pas présentes dans la table.</span><span class="sxs-lookup"><span data-stu-id="e175a-106">Properties with Null values are not present in the table.</span></span>

<span data-ttu-id="e175a-107">La table de propriétés contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="e175a-107">The Property table has the following columns.</span></span>



| <span data-ttu-id="e175a-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="e175a-108">Column</span></span>   | <span data-ttu-id="e175a-109">Type</span><span class="sxs-lookup"><span data-stu-id="e175a-109">Type</span></span>                         | <span data-ttu-id="e175a-110">Clé</span><span class="sxs-lookup"><span data-stu-id="e175a-110">Key</span></span> | <span data-ttu-id="e175a-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="e175a-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="e175a-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="e175a-112">Property</span></span> | [<span data-ttu-id="e175a-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="e175a-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="e175a-114">O</span><span class="sxs-lookup"><span data-stu-id="e175a-114">Y</span></span>   | <span data-ttu-id="e175a-115">N</span><span class="sxs-lookup"><span data-stu-id="e175a-115">N</span></span>        |
| <span data-ttu-id="e175a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e175a-116">Value</span></span>    | [<span data-ttu-id="e175a-117">Text</span><span class="sxs-lookup"><span data-stu-id="e175a-117">Text</span></span>](text.md)             | <span data-ttu-id="e175a-118">N</span><span class="sxs-lookup"><span data-stu-id="e175a-118">N</span></span>   | <span data-ttu-id="e175a-119">N</span><span class="sxs-lookup"><span data-stu-id="e175a-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e175a-120">Colonnes</span><span class="sxs-lookup"><span data-stu-id="e175a-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e175a-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété</span><span class="sxs-lookup"><span data-stu-id="e175a-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="e175a-122">Nom d'une propriété.</span><span class="sxs-lookup"><span data-stu-id="e175a-122">The name of a property.</span></span> <span data-ttu-id="e175a-123">Consultez [Propriétés](properties.md).</span><span class="sxs-lookup"><span data-stu-id="e175a-123">See [Properties](properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="e175a-124"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée</span><span class="sxs-lookup"><span data-stu-id="e175a-124"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="e175a-125">Valeur de chaîne localisable pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="e175a-125">A localizable string value for the property.</span></span> <span data-ttu-id="e175a-126">Cela peut ne jamais avoir la valeur null ou être une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="e175a-126">This may never be Null or an empty string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e175a-127">Notes</span><span class="sxs-lookup"><span data-stu-id="e175a-127">Remarks</span></span>

<span data-ttu-id="e175a-128">Notez que vous ne pouvez pas utiliser la table de propriétés pour affecter à une propriété la valeur d’une autre propriété.</span><span class="sxs-lookup"><span data-stu-id="e175a-128">Note that you cannot use the Property table to set a property to the value of another property.</span></span> <span data-ttu-id="e175a-129">Le programme d’installation ne fait rien de la chaîne de texte entrée dans la colonne valeur avant de définir la propriété dans la colonne propriété.</span><span class="sxs-lookup"><span data-stu-id="e175a-129">The installer does nothing to the text string entered in the Value column before setting the property in the Property column.</span></span> <span data-ttu-id="e175a-130">Si FirstProperty est entré dans la colonne de propriété et \[ SecondProperty \] dans la colonne valeur, la valeur de FirstProperty est définie sur la chaîne de texte « \[ SecondProperty \] » et non sur la valeur de la propriété SecondProperty.</span><span class="sxs-lookup"><span data-stu-id="e175a-130">If FirstProperty is entered into the Property column and \[SecondProperty\] in the Value column, the value of FirstProperty is set to the text string "\[SecondProperty\]" and not to the value of the SecondProperty property.</span></span> <span data-ttu-id="e175a-131">Cela est nécessaire pour empêcher la création de références circulaires dans la table de propriétés.</span><span class="sxs-lookup"><span data-stu-id="e175a-131">This is necessary to prevent creating circular references in the Property table.</span></span> <span data-ttu-id="e175a-132">Au lieu de cela, vous pouvez définir une propriété sur une autre à l’aide d’un [type d’action personnalisé 51](custom-action-type-51.md).</span><span class="sxs-lookup"><span data-stu-id="e175a-132">Instead, you can set one property to another by using a [Custom Action Type 51](custom-action-type-51.md).</span></span>

<span data-ttu-id="e175a-133">Notez que la propriété [**AdminProperties**](adminproperties.md) peut être utilisée pour remplacer les valeurs de la table de propriétés lors d’une [installation administrative](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="e175a-133">Note that the [**AdminProperties**](adminproperties.md) property can be used to override the values in the Property table during an [Administrative Installation](administrative-installation.md).</span></span>

<span data-ttu-id="e175a-134">N’utilisez pas de propriétés pour les mots de passe ou d’autres informations qui doivent rester sécurisées.</span><span class="sxs-lookup"><span data-stu-id="e175a-134">Do not use properties for passwords or other information that must remain secure.</span></span> <span data-ttu-id="e175a-135">Le programme d’installation peut écrire la valeur d’une propriété créée dans la table de propriétés, ou créée au moment de l’exécution, dans un journal ou dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="e175a-135">The installer may write the value of a property authored into the Property table, or created at runtime, into a log or the system registry.</span></span>

## <a name="validation"></a><span data-ttu-id="e175a-136">Validation</span><span class="sxs-lookup"><span data-stu-id="e175a-136">Validation</span></span>

<dl>

[<span data-ttu-id="e175a-137">ICE03</span><span class="sxs-lookup"><span data-stu-id="e175a-137">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e175a-138">ICE05</span><span class="sxs-lookup"><span data-stu-id="e175a-138">ICE05</span></span>](ice05.md)  
[<span data-ttu-id="e175a-139">ICE06</span><span class="sxs-lookup"><span data-stu-id="e175a-139">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e175a-140">ICE16</span><span class="sxs-lookup"><span data-stu-id="e175a-140">ICE16</span></span>](ice16.md)  
[<span data-ttu-id="e175a-141">ICE24</span><span class="sxs-lookup"><span data-stu-id="e175a-141">ICE24</span></span>](ice24.md)  
[<span data-ttu-id="e175a-142">ICE31</span><span class="sxs-lookup"><span data-stu-id="e175a-142">ICE31</span></span>](ice31.md)  
[<span data-ttu-id="e175a-143">ICE34</span><span class="sxs-lookup"><span data-stu-id="e175a-143">ICE34</span></span>](ice34.md)  
[<span data-ttu-id="e175a-144">ICE36</span><span class="sxs-lookup"><span data-stu-id="e175a-144">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="e175a-145">ICE40</span><span class="sxs-lookup"><span data-stu-id="e175a-145">ICE40</span></span>](ice40.md)  
[<span data-ttu-id="e175a-146">ICE46</span><span class="sxs-lookup"><span data-stu-id="e175a-146">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="e175a-147">ICE48</span><span class="sxs-lookup"><span data-stu-id="e175a-147">ICE48</span></span>](ice48.md)  
[<span data-ttu-id="e175a-148">ICE52</span><span class="sxs-lookup"><span data-stu-id="e175a-148">ICE52</span></span>](ice52.md)  
[<span data-ttu-id="e175a-149">ICE61</span><span class="sxs-lookup"><span data-stu-id="e175a-149">ICE61</span></span>](ice61.md)  
[<span data-ttu-id="e175a-150">ICE73</span><span class="sxs-lookup"><span data-stu-id="e175a-150">ICE73</span></span>](ice73.md)  
[<span data-ttu-id="e175a-151">ICE74</span><span class="sxs-lookup"><span data-stu-id="e175a-151">ICE74</span></span>](ice74.md)  
[<span data-ttu-id="e175a-152">ICE80</span><span class="sxs-lookup"><span data-stu-id="e175a-152">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="e175a-153">ICE87</span><span class="sxs-lookup"><span data-stu-id="e175a-153">ICE87</span></span>](ice87.md)  
[<span data-ttu-id="e175a-154">ICE88</span><span class="sxs-lookup"><span data-stu-id="e175a-154">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="e175a-155">ICE91</span><span class="sxs-lookup"><span data-stu-id="e175a-155">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="e175a-156">ICE99</span><span class="sxs-lookup"><span data-stu-id="e175a-156">ICE99</span></span>](ice99.md)  
</dl>

 

 



