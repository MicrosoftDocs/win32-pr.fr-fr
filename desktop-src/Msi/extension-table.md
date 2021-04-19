---
description: La table d’extension contient des informations sur les serveurs d’extension de nom de fichier qui doivent être générés dans le cadre de la publication du produit. Chaque ligne génère un ensemble de clés et de valeurs de registre.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Table d’extension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef52f7248f44dcb63255244bbd8abd4ac8181d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524547"
---
# <a name="extension-table"></a><span data-ttu-id="d6794-104">Table d’extension</span><span class="sxs-lookup"><span data-stu-id="d6794-104">Extension Table</span></span>

<span data-ttu-id="d6794-105">La table d’extension contient des informations sur les serveurs d’extension de nom de fichier qui doivent être générés dans le cadre de la publication du produit.</span><span class="sxs-lookup"><span data-stu-id="d6794-105">The Extension table contains information about file name extension servers that must be generated as a part of product advertisement.</span></span> <span data-ttu-id="d6794-106">Chaque ligne génère un ensemble de clés et de valeurs de registre.</span><span class="sxs-lookup"><span data-stu-id="d6794-106">Each row generates a set of registry keys and values.</span></span>

<span data-ttu-id="d6794-107">La table d’extension contient les colonnes indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d6794-107">The Extension table contains the columns shown in the following table.</span></span>



| <span data-ttu-id="d6794-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="d6794-108">Column</span></span>      | <span data-ttu-id="d6794-109">Type</span><span class="sxs-lookup"><span data-stu-id="d6794-109">Type</span></span>                         | <span data-ttu-id="d6794-110">Clé</span><span class="sxs-lookup"><span data-stu-id="d6794-110">Key</span></span> | <span data-ttu-id="d6794-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="d6794-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="d6794-112">Extension</span><span class="sxs-lookup"><span data-stu-id="d6794-112">Extension</span></span>   | [<span data-ttu-id="d6794-113">Text</span><span class="sxs-lookup"><span data-stu-id="d6794-113">Text</span></span>](text.md)             | <span data-ttu-id="d6794-114">O</span><span class="sxs-lookup"><span data-stu-id="d6794-114">Y</span></span>   | <span data-ttu-id="d6794-115">N</span><span class="sxs-lookup"><span data-stu-id="d6794-115">N</span></span>        |
| <span data-ttu-id="d6794-116">-\_</span><span class="sxs-lookup"><span data-stu-id="d6794-116">Component\_</span></span> | [<span data-ttu-id="d6794-117">Identificateur</span><span class="sxs-lookup"><span data-stu-id="d6794-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="d6794-118">O</span><span class="sxs-lookup"><span data-stu-id="d6794-118">Y</span></span>   | <span data-ttu-id="d6794-119">N</span><span class="sxs-lookup"><span data-stu-id="d6794-119">N</span></span>        |
| <span data-ttu-id="d6794-120">ProgId\_</span><span class="sxs-lookup"><span data-stu-id="d6794-120">ProgId\_</span></span>    | [<span data-ttu-id="d6794-121">Text</span><span class="sxs-lookup"><span data-stu-id="d6794-121">Text</span></span>](text.md)             | <span data-ttu-id="d6794-122">N</span><span class="sxs-lookup"><span data-stu-id="d6794-122">N</span></span>   | <span data-ttu-id="d6794-123">O</span><span class="sxs-lookup"><span data-stu-id="d6794-123">Y</span></span>        |
| <span data-ttu-id="d6794-124">MIME\_</span><span class="sxs-lookup"><span data-stu-id="d6794-124">MIME\_</span></span>      | [<span data-ttu-id="d6794-125">Text</span><span class="sxs-lookup"><span data-stu-id="d6794-125">Text</span></span>](text.md)             | <span data-ttu-id="d6794-126">N</span><span class="sxs-lookup"><span data-stu-id="d6794-126">N</span></span>   | <span data-ttu-id="d6794-127">O</span><span class="sxs-lookup"><span data-stu-id="d6794-127">Y</span></span>        |
| <span data-ttu-id="d6794-128">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="d6794-128">Feature\_</span></span>   | [<span data-ttu-id="d6794-129">Identificateur</span><span class="sxs-lookup"><span data-stu-id="d6794-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="d6794-130">N</span><span class="sxs-lookup"><span data-stu-id="d6794-130">N</span></span>   | <span data-ttu-id="d6794-131">N</span><span class="sxs-lookup"><span data-stu-id="d6794-131">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d6794-132">Colonnes</span><span class="sxs-lookup"><span data-stu-id="d6794-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d6794-133"><span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Poste</span><span class="sxs-lookup"><span data-stu-id="d6794-133"><span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Extension</span></span>
</dt> <dd>

<span data-ttu-id="d6794-134">Extension associée à la ligne de table.</span><span class="sxs-lookup"><span data-stu-id="d6794-134">The extension associated with the table row.</span></span> <span data-ttu-id="d6794-135">L’extension peut comporter jusqu’à 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="d6794-135">The extension can be up to 255 characters long.</span></span> <span data-ttu-id="d6794-136">Entrez l’extension dans ce champ sans la période précédente.</span><span class="sxs-lookup"><span data-stu-id="d6794-136">Enter the extension in this field without the preceding period.</span></span>

</dd> <dt>

<span data-ttu-id="d6794-137"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="d6794-137"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="d6794-138">Clé externe de la première colonne de la table de [composants](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d6794-138">An external key to the first column of the [Component](component-table.md) table.</span></span> <span data-ttu-id="d6794-139">Cette colonne fait référence au composant qui contrôle l’installation de l’extension.</span><span class="sxs-lookup"><span data-stu-id="d6794-139">This column references the component that controls the installation of the extension.</span></span>

</dd> <dt>

<span data-ttu-id="d6794-140"><span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgId\_</span><span class="sxs-lookup"><span data-stu-id="d6794-140"><span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgId\_</span></span>
</dt> <dd>

<span data-ttu-id="d6794-141">ID de programme associé à cette extension.</span><span class="sxs-lookup"><span data-stu-id="d6794-141">The Program ID associated with this extension.</span></span> <span data-ttu-id="d6794-142">Il s’agit d’une clé étrangère dans la table [ProgID](progid-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d6794-142">This is a foreign key into the [ProgId](progid-table.md) table.</span></span>

</dd> <dt>

<span data-ttu-id="d6794-143"><span id="MIME_"></span><span id="mime_"></span>MIME\_</span><span class="sxs-lookup"><span data-stu-id="d6794-143"><span id="MIME_"></span><span id="mime_"></span>MIME\_</span></span>
</dt> <dd>

<span data-ttu-id="d6794-144">Type de contenu qui doit être écrit pour la colonne d’extension.</span><span class="sxs-lookup"><span data-stu-id="d6794-144">The Content Type that is to be written for the Extension column.</span></span>

<span data-ttu-id="d6794-145">Clé externe de la première colonne de la table [MIME](mime-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d6794-145">An external key to the first column of the [MIME](mime-table.md) table.</span></span>

</dd> <dt>

<span data-ttu-id="d6794-146"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="d6794-146"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="d6794-147">Une clé externe dans la première colonne de la table de [fonctionnalités](feature-table.md) spécifiant la fonctionnalité qui fournit le serveur d’extension.</span><span class="sxs-lookup"><span data-stu-id="d6794-147">An external key into the first column of the [Feature](feature-table.md) table specifying the feature that provides the extension server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6794-148">Notes</span><span class="sxs-lookup"><span data-stu-id="d6794-148">Remarks</span></span>

<span data-ttu-id="d6794-149">La table d’extension est référencée lorsque l’action [RegisterExtensionInfo](registerextensioninfo-action.md) ou l’action [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="d6794-149">The Extension table is referred to when the [RegisterExtensionInfo](registerextensioninfo-action.md) action or the [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) action is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="d6794-150">Validation</span><span class="sxs-lookup"><span data-stu-id="d6794-150">Validation</span></span>

<dl>

[<span data-ttu-id="d6794-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="d6794-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d6794-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="d6794-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d6794-153">ICE15</span><span class="sxs-lookup"><span data-stu-id="d6794-153">ICE15</span></span>](ice15.md)  
[<span data-ttu-id="d6794-154">ICE19</span><span class="sxs-lookup"><span data-stu-id="d6794-154">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="d6794-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="d6794-155">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d6794-156">ICE41</span><span class="sxs-lookup"><span data-stu-id="d6794-156">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="d6794-157">ICE69</span><span class="sxs-lookup"><span data-stu-id="d6794-157">ICE69</span></span>](ice69.md)  
</dl>

 

 



