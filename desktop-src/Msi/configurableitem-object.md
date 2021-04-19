---
description: L’objet ConfigurableItem représente une ligne unique de la table ModuleConfiguration.
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: Objet ConfigurableItem (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem
- IMsmConfigurableItem
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4436be457adcca37ba40f15bbe0ecd6b0445fb2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542754"
---
# <a name="configurableitem-object"></a><span data-ttu-id="49cde-103">Objet ConfigurableItem</span><span class="sxs-lookup"><span data-stu-id="49cde-103">ConfigurableItem object</span></span>

<span data-ttu-id="49cde-104">L' **objet ConfigurableItem** représente une ligne unique de la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="49cde-104">The **ConfigurableItem object** represents a single row from the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="49cde-105">Il s’agit d’un « attribut » configurable unique du module.</span><span class="sxs-lookup"><span data-stu-id="49cde-105">This is a single configurable "attribute" from the module.</span></span> <span data-ttu-id="49cde-106">L’interface se compose de propriétés en lecture seule, une pour chaque colonne de la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="49cde-106">The interface consists read-only properties, one for each column in the ModuleConfiguration table.</span></span> <span data-ttu-id="49cde-107">La définition de l’interface est la suivante.</span><span class="sxs-lookup"><span data-stu-id="49cde-107">The Interface definition is as follows.</span></span>

## <a name="members"></a><span data-ttu-id="49cde-108">Membres</span><span class="sxs-lookup"><span data-stu-id="49cde-108">Members</span></span>

<span data-ttu-id="49cde-109">L’objet **ConfigurableItem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="49cde-109">The **ConfigurableItem** object has these types of members:</span></span>

-   [<span data-ttu-id="49cde-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="49cde-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49cde-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="49cde-111">Properties</span></span>

<span data-ttu-id="49cde-112">L’objet **ConfigurableItem** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="49cde-112">The **ConfigurableItem** object has these properties.</span></span>



| <span data-ttu-id="49cde-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="49cde-113">Property</span></span>                                                         | <span data-ttu-id="49cde-114">Description</span><span class="sxs-lookup"><span data-stu-id="49cde-114">Description</span></span>                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49cde-115">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="49cde-115">**Attributes**</span></span>](configurableitem-attributes.md)<br/>     | <span data-ttu-id="49cde-116">Retourne la valeur dans le champ attributs de l’enregistrement de cet objet dans la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="49cde-116">Returns the value in the Attributes field of this object's record in the ModuleConfiguration table.</span></span><br/>                            |
| [<span data-ttu-id="49cde-117">**Context**</span><span class="sxs-lookup"><span data-stu-id="49cde-117">**Context**</span></span>](configurableitem-context.md)<br/>           | <span data-ttu-id="49cde-118">Retourne la valeur dans le champ de contexte de l’enregistrement de cet objet dans la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="49cde-118">Returns the value in the Context field of this object's record in the ModuleConfiguration table.</span></span><br/>                               |
| [<span data-ttu-id="49cde-119">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="49cde-119">**DefaultValue**</span></span>](configurableitem-defaultvalue.md)<br/> | <span data-ttu-id="49cde-120">Retourne la valeur dans le champ DefaultValue de l’enregistrement de cet objet dans la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="49cde-120">Returns the value in the DefaultValue field of this object's record in the ModuleConfiguration table.</span></span><br/>                          |
| [<span data-ttu-id="49cde-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="49cde-121">**Description**</span></span>](configurableitem-description.md)<br/>   | <span data-ttu-id="49cde-122">Retourne la valeur dans le champ Description de l’enregistrement de cet objet dans la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="49cde-122">Returns the value in the Description field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="49cde-123">**NomComplet**</span><span class="sxs-lookup"><span data-stu-id="49cde-123">**DisplayName**</span></span>](configurableitem-displayname.md)<br/>   | <span data-ttu-id="49cde-124">Retourne la valeur dans le champ DisplayName de l’enregistrement de cet objet dans la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="49cde-124">Returns the value in the DisplayName field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="49cde-125">**Format**</span><span class="sxs-lookup"><span data-stu-id="49cde-125">**Format**</span></span>](configurableitem-format.md)<br/>             | <span data-ttu-id="49cde-126">Retourne la valeur dans le champ format de l’enregistrement de cet objet dans la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="49cde-126">Returns the value in the Format field of this object's record in the ModuleConfiguration table.</span></span><br/>                                |
| [<span data-ttu-id="49cde-127">**HelpKeyword**</span><span class="sxs-lookup"><span data-stu-id="49cde-127">**HelpKeyword**</span></span>](configurableitem-helpkeyword.md)<br/>   | <span data-ttu-id="49cde-128">Retourne la valeur dans le champ HelpKeyword de l’enregistrement de cet objet dans la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="49cde-128">Returns the value in the HelpKeyword field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="49cde-129">**HelpLocation**</span><span class="sxs-lookup"><span data-stu-id="49cde-129">**HelpLocation**</span></span>](configurableitem-helplocation.md)<br/> | <span data-ttu-id="49cde-130">Retourne la valeur dans le champ HelpLocation de l’enregistrement de cet objet dans la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="49cde-130">Returns the value in the HelpLocation field of this object's record in the ModuleConfiguration table.</span></span><br/>                          |
| [<span data-ttu-id="49cde-131">**Nom**</span><span class="sxs-lookup"><span data-stu-id="49cde-131">**Name**</span></span>](configurableitem-name.md)<br/>                 | <span data-ttu-id="49cde-132">Retourne la valeur dans le champ nom de l’enregistrement de cet objet dans la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="49cde-132">Returns the value in the Name field of this object's record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span><br/> |
| [<span data-ttu-id="49cde-133">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="49cde-133">**Type**</span></span>](configurableitem-type.md)<br/>                 | <span data-ttu-id="49cde-134">Retourne la valeur dans le champ type de l’enregistrement de cet objet dans la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="49cde-134">Returns the value in the Type field of this object's record in the ModuleConfiguration table.</span></span><br/>                                  |



 

## <a name="c"></a><span data-ttu-id="49cde-135">C++</span><span class="sxs-lookup"><span data-stu-id="49cde-135">C++</span></span>

<span data-ttu-id="49cde-136">interface **IMsmConfigurableItem : IDispatch**</span><span class="sxs-lookup"><span data-stu-id="49cde-136">interface **IMsmConfigurableItem : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="49cde-137">ID d’interface</span><span class="sxs-lookup"><span data-stu-id="49cde-137">Interface ID</span></span>



| <span data-ttu-id="49cde-138">Constante</span><span class="sxs-lookup"><span data-stu-id="49cde-138">Constant</span></span>                      | <span data-ttu-id="49cde-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="49cde-139">Value</span></span>                                  |
|-------------------------------|----------------------------------------|
| <span data-ttu-id="49cde-140">**IID \_ IMsmConfigurableItem**</span><span class="sxs-lookup"><span data-stu-id="49cde-140">**IID\_IMsmConfigurableItem**</span></span> | <span data-ttu-id="49cde-141">{4D6E6284-D21D-401E-84F6-909E00B50F71}</span><span class="sxs-lookup"><span data-stu-id="49cde-141">{4D6E6284-D21D-401E-84F6-909E00B50F71}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="49cde-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49cde-142">Requirements</span></span>



| <span data-ttu-id="49cde-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49cde-143">Requirement</span></span> | <span data-ttu-id="49cde-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="49cde-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49cde-145">Version</span><span class="sxs-lookup"><span data-stu-id="49cde-145">Version</span></span><br/> | <span data-ttu-id="49cde-146">Mergemod.dll 2,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="49cde-146">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="49cde-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="49cde-147">Header</span></span><br/>  | <dl> <span data-ttu-id="49cde-148"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="49cde-148"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="49cde-149">DLL</span><span class="sxs-lookup"><span data-stu-id="49cde-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="49cde-150"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49cde-150"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




