---
description: La table PublishComponent associe les composants listés dans la table de composants à une chaîne de texte de qualificateur et un GUID d’ID de catégorie.
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: Table PublishComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb0edfd811873242629c36257fdce5a80fe9d91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531930"
---
# <a name="publishcomponent-table"></a><span data-ttu-id="d2139-103">Table PublishComponent</span><span class="sxs-lookup"><span data-stu-id="d2139-103">PublishComponent Table</span></span>

<span data-ttu-id="d2139-104">La table PublishComponent associe les composants listés dans la [table de composants](component-table.md) à une chaîne de texte de qualificateur et un GUID d’ID de catégorie.</span><span class="sxs-lookup"><span data-stu-id="d2139-104">The PublishComponent table associates components listed in the [Component table](component-table.md) with a qualifier text-string and a category ID GUID.</span></span> <span data-ttu-id="d2139-105">Les composants avec des fonctionnalités parallèles qui ont été regroupées de cette façon sont appelés composants qualifiés.</span><span class="sxs-lookup"><span data-stu-id="d2139-105">Components with parallel functionality that have been grouped together in this way are referred to as qualified components.</span></span> <span data-ttu-id="d2139-106">Consultez [composants qualifiés](qualified-components.md).</span><span class="sxs-lookup"><span data-stu-id="d2139-106">See [Qualified Components](qualified-components.md).</span></span> <span data-ttu-id="d2139-107">Cela fournit au programme d’installation une méthode pour l’indirection d’un seul niveau lorsqu’il fait référence aux composants.</span><span class="sxs-lookup"><span data-stu-id="d2139-107">This provides the installer with a method for single-level indirection when referring to components.</span></span> <span data-ttu-id="d2139-108">Consultez [utilisation des composants qualifiés](using-qualified-components.md).</span><span class="sxs-lookup"><span data-stu-id="d2139-108">See [Using Qualified Components](using-qualified-components.md).</span></span>

<span data-ttu-id="d2139-109">La table PublishComponent contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2139-109">The PublishComponent table has the following columns.</span></span>



| <span data-ttu-id="d2139-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="d2139-110">Column</span></span>      | <span data-ttu-id="d2139-111">Type</span><span class="sxs-lookup"><span data-stu-id="d2139-111">Type</span></span>                         | <span data-ttu-id="d2139-112">Clé</span><span class="sxs-lookup"><span data-stu-id="d2139-112">Key</span></span> | <span data-ttu-id="d2139-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="d2139-113">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="d2139-114">ComponentId</span><span class="sxs-lookup"><span data-stu-id="d2139-114">ComponentId</span></span> | [<span data-ttu-id="d2139-115">GUID</span><span class="sxs-lookup"><span data-stu-id="d2139-115">GUID</span></span>](guid.md)             | <span data-ttu-id="d2139-116">O</span><span class="sxs-lookup"><span data-stu-id="d2139-116">Y</span></span>   | <span data-ttu-id="d2139-117">N</span><span class="sxs-lookup"><span data-stu-id="d2139-117">N</span></span>        |
| <span data-ttu-id="d2139-118">Qualificateur</span><span class="sxs-lookup"><span data-stu-id="d2139-118">Qualifier</span></span>   | [<span data-ttu-id="d2139-119">Text</span><span class="sxs-lookup"><span data-stu-id="d2139-119">Text</span></span>](text.md)             | <span data-ttu-id="d2139-120">O</span><span class="sxs-lookup"><span data-stu-id="d2139-120">Y</span></span>   | <span data-ttu-id="d2139-121">N</span><span class="sxs-lookup"><span data-stu-id="d2139-121">N</span></span>        |
| <span data-ttu-id="d2139-122">-\_</span><span class="sxs-lookup"><span data-stu-id="d2139-122">Component\_</span></span> | [<span data-ttu-id="d2139-123">Identificateur</span><span class="sxs-lookup"><span data-stu-id="d2139-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="d2139-124">O</span><span class="sxs-lookup"><span data-stu-id="d2139-124">Y</span></span>   | <span data-ttu-id="d2139-125">N</span><span class="sxs-lookup"><span data-stu-id="d2139-125">N</span></span>        |
| <span data-ttu-id="d2139-126">AppData</span><span class="sxs-lookup"><span data-stu-id="d2139-126">AppData</span></span>     | [<span data-ttu-id="d2139-127">Text</span><span class="sxs-lookup"><span data-stu-id="d2139-127">Text</span></span>](text.md)             | <span data-ttu-id="d2139-128">N</span><span class="sxs-lookup"><span data-stu-id="d2139-128">N</span></span>   | <span data-ttu-id="d2139-129">O</span><span class="sxs-lookup"><span data-stu-id="d2139-129">Y</span></span>        |
| <span data-ttu-id="d2139-130">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="d2139-130">Feature\_</span></span>   | [<span data-ttu-id="d2139-131">Identificateur</span><span class="sxs-lookup"><span data-stu-id="d2139-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="d2139-132">N</span><span class="sxs-lookup"><span data-stu-id="d2139-132">N</span></span>   | <span data-ttu-id="d2139-133">N</span><span class="sxs-lookup"><span data-stu-id="d2139-133">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d2139-134">Colonnes</span><span class="sxs-lookup"><span data-stu-id="d2139-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d2139-135"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span><span class="sxs-lookup"><span data-stu-id="d2139-135"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span></span>
</dt> <dd>

<span data-ttu-id="d2139-136">[GUID](guid.md) de chaîne qui représente la catégorie des composants regroupés.</span><span class="sxs-lookup"><span data-stu-id="d2139-136">A string [GUID](guid.md) that represents the category of components being grouped together.</span></span> <span data-ttu-id="d2139-137">Notez que le titre de cette colonne est trompeur.</span><span class="sxs-lookup"><span data-stu-id="d2139-137">Note that this column's title is misleading.</span></span> <span data-ttu-id="d2139-138">Il s’agit du GUID de la catégorie des composants qualifiés et qui n’est pas le même GUID que celui figurant dans la colonne ComponentId de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="d2139-138">This is the GUID for the category of qualified components and is not the same GUID appearing in the ComponentId column of the [Component table](component-table.md).</span></span> <span data-ttu-id="d2139-139">Ici, il fait référence à un serveur qui fournit les fonctionnalités d’un composant à des clients externes plutôt qu’au composant lui-même.</span><span class="sxs-lookup"><span data-stu-id="d2139-139">Here it refers to a server that provides the functionality of a component to external clients rather than the component itself.</span></span>

</dd> <dt>

<span data-ttu-id="d2139-140"><span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualificateur</span><span class="sxs-lookup"><span data-stu-id="d2139-140"><span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualifier</span></span>
</dt> <dd>

<span data-ttu-id="d2139-141">Chaîne de texte qui qualifie la valeur dans la colonne ComponentId.</span><span class="sxs-lookup"><span data-stu-id="d2139-141">A text string that qualifies the value in the ComponentId column.</span></span> <span data-ttu-id="d2139-142">Un qualificateur est utilisé pour distinguer plusieurs formes du même composant, par exemple un composant implémenté dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="d2139-142">A qualifier is used to distinguish multiple forms of the same component, such as a component that is implemented in multiple languages.</span></span> <span data-ttu-id="d2139-143">Il s’agit des chaînes de texte de qualificateur retournées par [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="d2139-143">These are the qualifier text-strings returned by [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

</dd> <dt>

<span data-ttu-id="d2139-144"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="d2139-144"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="d2139-145">Clé externe dans la colonne une de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="d2139-145">External key into column one of the [Component table](component-table.md).</span></span> <span data-ttu-id="d2139-146">Cet identificateur fait référence à l’enregistrement du composant qualifié dans la table des composants.</span><span class="sxs-lookup"><span data-stu-id="d2139-146">This identifier refers to the qualified component's record in the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="d2139-147"><span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData</span><span class="sxs-lookup"><span data-stu-id="d2139-147"><span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData</span></span>
</dt> <dd>

<span data-ttu-id="d2139-148">Texte localisable facultatif qui décrit le composant qualifié de cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d2139-148">An optional localizable text describing the qualified component of this record.</span></span> <span data-ttu-id="d2139-149">La chaîne est généralement analysée par l’application et peut être affichée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d2139-149">The string is commonly parsed by the application and can be displayed to the user.</span></span> <span data-ttu-id="d2139-150">Il doit décrire le composant qualifié.</span><span class="sxs-lookup"><span data-stu-id="d2139-150">It should describe the qualified component.</span></span> <span data-ttu-id="d2139-151">Ce peut être récupéré avec [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="d2139-151">This can be retrieved with [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

</dd> <dt>

<span data-ttu-id="d2139-152"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="d2139-152"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="d2139-153">Clé externe dans la colonne une du [tableau des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="d2139-153">External key into column one of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="d2139-154">Il s’agit de la fonctionnalité qui utilise ce composant qualifié.</span><span class="sxs-lookup"><span data-stu-id="d2139-154">This is the feature using this qualified component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2139-155">Notes</span><span class="sxs-lookup"><span data-stu-id="d2139-155">Remarks</span></span>

<span data-ttu-id="d2139-156">Cette table est référencée lorsque l' [action PublishComponents](publishcomponents-action.md) ou l' [action UnpublishComponents](unpublishcomponents-action.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="d2139-156">This table is referred to when the [PublishComponents action](publishcomponents-action.md) or the [UnpublishComponents action](unpublishcomponents-action.md) is executed.</span></span>

<span data-ttu-id="d2139-157">Notez que le nom de cette table est trompeur.</span><span class="sxs-lookup"><span data-stu-id="d2139-157">Note that the name of this table is misleading.</span></span> <span data-ttu-id="d2139-158">Cette table n’est pas nécessaire pour créer la publication.</span><span class="sxs-lookup"><span data-stu-id="d2139-158">This table is not required in order to author advertisement.</span></span> <span data-ttu-id="d2139-159">Pour plus d’informations sur la façon de définir l’état d’installation des composants à publier, consultez la colonne attributs de la table des [composants](component-table.md) et de la [table des fonctionnalités](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d2139-159">See the Attributes column of the [Component table](component-table.md) and [Feature table](feature-table.md) for information on how to set the installation state of components to advertise.</span></span>

## <a name="validation"></a><span data-ttu-id="d2139-160">Validation</span><span class="sxs-lookup"><span data-stu-id="d2139-160">Validation</span></span>

<dl>

[<span data-ttu-id="d2139-161">ICE03</span><span class="sxs-lookup"><span data-stu-id="d2139-161">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d2139-162">ICE06</span><span class="sxs-lookup"><span data-stu-id="d2139-162">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d2139-163">ICE19</span><span class="sxs-lookup"><span data-stu-id="d2139-163">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="d2139-164">ICE22</span><span class="sxs-lookup"><span data-stu-id="d2139-164">ICE22</span></span>](ice22.md)  
[<span data-ttu-id="d2139-165">ICE32</span><span class="sxs-lookup"><span data-stu-id="d2139-165">ICE32</span></span>](ice32.md)  
</dl>

 

 



