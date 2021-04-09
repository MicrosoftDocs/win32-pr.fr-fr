---
description: La table ProgId contient des informations sur les ID de programme et les ID de programme indépendants de version qui doivent être générés dans le cadre de la publication du produit.
ms.assetid: 66a7e170-6f70-4db7-98f4-8a074471b9f2
title: Table ProgId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293ce3748f691b664d55b0a1158a574472388202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953006"
---
# <a name="progid-table"></a><span data-ttu-id="df456-103">Table ProgId</span><span class="sxs-lookup"><span data-stu-id="df456-103">ProgId Table</span></span>

<span data-ttu-id="df456-104">La table ProgId contient des informations sur les ID de programme et les ID de programme indépendants de version qui doivent être générés dans le cadre de la publication du produit.</span><span class="sxs-lookup"><span data-stu-id="df456-104">The ProgId table contains information for program IDs and version independent program IDs that must be generated as a part of the product advertisement.</span></span>

<span data-ttu-id="df456-105">La table ProgId contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="df456-105">The ProgId table has the following columns.</span></span>



| <span data-ttu-id="df456-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="df456-106">Column</span></span>         | <span data-ttu-id="df456-107">Type</span><span class="sxs-lookup"><span data-stu-id="df456-107">Type</span></span>                         | <span data-ttu-id="df456-108">Clé</span><span class="sxs-lookup"><span data-stu-id="df456-108">Key</span></span> | <span data-ttu-id="df456-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="df456-109">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="df456-110">ProgId</span><span class="sxs-lookup"><span data-stu-id="df456-110">ProgId</span></span>         | [<span data-ttu-id="df456-111">Text</span><span class="sxs-lookup"><span data-stu-id="df456-111">Text</span></span>](text.md)             | <span data-ttu-id="df456-112">O</span><span class="sxs-lookup"><span data-stu-id="df456-112">Y</span></span>   | <span data-ttu-id="df456-113">N</span><span class="sxs-lookup"><span data-stu-id="df456-113">N</span></span>        |
| <span data-ttu-id="df456-114">ProgId \_ parent</span><span class="sxs-lookup"><span data-stu-id="df456-114">ProgId\_Parent</span></span> | [<span data-ttu-id="df456-115">Text</span><span class="sxs-lookup"><span data-stu-id="df456-115">Text</span></span>](text.md)             | <span data-ttu-id="df456-116">N</span><span class="sxs-lookup"><span data-stu-id="df456-116">N</span></span>   | <span data-ttu-id="df456-117">O</span><span class="sxs-lookup"><span data-stu-id="df456-117">Y</span></span>        |
| <span data-ttu-id="df456-118">Classe\_</span><span class="sxs-lookup"><span data-stu-id="df456-118">Class\_</span></span>        | [<span data-ttu-id="df456-119">GUID</span><span class="sxs-lookup"><span data-stu-id="df456-119">GUID</span></span>](guid.md)             | <span data-ttu-id="df456-120">N</span><span class="sxs-lookup"><span data-stu-id="df456-120">N</span></span>   | <span data-ttu-id="df456-121">O</span><span class="sxs-lookup"><span data-stu-id="df456-121">Y</span></span>        |
| <span data-ttu-id="df456-122">Description</span><span class="sxs-lookup"><span data-stu-id="df456-122">Description</span></span>    | [<span data-ttu-id="df456-123">Text</span><span class="sxs-lookup"><span data-stu-id="df456-123">Text</span></span>](text.md)             | <span data-ttu-id="df456-124">N</span><span class="sxs-lookup"><span data-stu-id="df456-124">N</span></span>   | <span data-ttu-id="df456-125">O</span><span class="sxs-lookup"><span data-stu-id="df456-125">Y</span></span>        |
| <span data-ttu-id="df456-126">Icône\_</span><span class="sxs-lookup"><span data-stu-id="df456-126">Icon\_</span></span>         | [<span data-ttu-id="df456-127">Identificateur</span><span class="sxs-lookup"><span data-stu-id="df456-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="df456-128">N</span><span class="sxs-lookup"><span data-stu-id="df456-128">N</span></span>   | <span data-ttu-id="df456-129">O</span><span class="sxs-lookup"><span data-stu-id="df456-129">Y</span></span>        |
| <span data-ttu-id="df456-130">IndexIcône</span><span class="sxs-lookup"><span data-stu-id="df456-130">IconIndex</span></span>      | [<span data-ttu-id="df456-131">Integer</span><span class="sxs-lookup"><span data-stu-id="df456-131">Integer</span></span>](integer.md)       | <span data-ttu-id="df456-132">N</span><span class="sxs-lookup"><span data-stu-id="df456-132">N</span></span>   | <span data-ttu-id="df456-133">O</span><span class="sxs-lookup"><span data-stu-id="df456-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="df456-134">Colonnes</span><span class="sxs-lookup"><span data-stu-id="df456-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="df456-135"><span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgId</span><span class="sxs-lookup"><span data-stu-id="df456-135"><span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgId</span></span>
</dt> <dd>

<span data-ttu-id="df456-136">ID de programme ou ID de programme indépendant de la version.</span><span class="sxs-lookup"><span data-stu-id="df456-136">The program ID or version independent program ID.</span></span> <span data-ttu-id="df456-137">Les ProgID répertoriés dans la table ProgId sont enregistrés si le CLSID répertorié dans la \_ colonne de classe de ce tableau est planifié pour être publié ou installé.</span><span class="sxs-lookup"><span data-stu-id="df456-137">ProgIds listed in the ProgId table are registered if the CLSID listed in the Class\_column of this table is scheduled to be advertised or installed.</span></span> <span data-ttu-id="df456-138">Lorsque le ProgId est sélectionné pour l’inscription, tous les ProgID qui font référence à cette ligne par le biais de la \_ colonne parente ProgID sont également sélectionnés pour l’inscription.</span><span class="sxs-lookup"><span data-stu-id="df456-138">When the ProgId is selected for registration, all ProgIds that refer to this row through the ProgId\_Parent column are also selected for registration.</span></span>

</dd> <dt>

<span data-ttu-id="df456-139"><span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId \_ parent</span><span class="sxs-lookup"><span data-stu-id="df456-139"><span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId\_Parent</span></span>
</dt> <dd>

<span data-ttu-id="df456-140">Défini uniquement pour les ID de programme indépendants de la version.</span><span class="sxs-lookup"><span data-stu-id="df456-140">Defined only for version independent program IDs.</span></span> <span data-ttu-id="df456-141">Ce champ est une clé étrangère dans la colonne ProgId.</span><span class="sxs-lookup"><span data-stu-id="df456-141">This field is a foreign key into the ProgId column.</span></span> <span data-ttu-id="df456-142">Pour définir un ID de programme indépendant de la version, entrez le ProgId correspondant dans la \_ colonne parente ProgID.</span><span class="sxs-lookup"><span data-stu-id="df456-142">To define a version independent program ID, enter the corresponding ProgId into the ProgId\_Parent column.</span></span> <span data-ttu-id="df456-143">Lorsque le ProgId est sélectionné pour l’installation, les ProgID indépendants de la version associés à la \_ colonne parente ProgID sont également sélectionnés pour l’inscription.</span><span class="sxs-lookup"><span data-stu-id="df456-143">When the ProgId is selected for installation, the corresponding version-independent ProgIds associated through the ProgId\_Parent column are also selected for registration.</span></span>

</dd> <dt>

<span data-ttu-id="df456-144"><span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Type\_</span><span class="sxs-lookup"><span data-stu-id="df456-144"><span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Class\_</span></span>
</dt> <dd>

<span data-ttu-id="df456-145">Clé étrangère facultative dans la [table de classe](class-table.md).</span><span class="sxs-lookup"><span data-stu-id="df456-145">An optional foreign key into the [Class table](class-table.md).</span></span> <span data-ttu-id="df456-146">Cette colonne doit avoir la valeur null pour un ProgId indépendant de la version.</span><span class="sxs-lookup"><span data-stu-id="df456-146">This column must be Null for a version independent ProgId.</span></span> <span data-ttu-id="df456-147">Si la \_ valeur de classe d’un ProgID est null, le ProgID est inscrit lorsqu’il apparaît dans la colonne ProgID d’une ligne dans la [table d’extension](extension-table.md) et qu’au moins un verbe est associé à l’extension dans la table de [verbes](verb-table.md).</span><span class="sxs-lookup"><span data-stu-id="df456-147">If the Class\_value for a ProgId is null, the ProgId is registered when it appears in the ProgId column of a row in the [Extension table](extension-table.md) and the extension has at least one Verb associated with it in the [Verb table](verb-table.md).</span></span> <span data-ttu-id="df456-148">Les ProgID sélectionnés pour l’inscription de cette manière n’installent pas les autres ProgID qui référencent le ProgId actuel via la \_ valeur ProgID par défaut.</span><span class="sxs-lookup"><span data-stu-id="df456-148">ProgIds selected for registration in this manner do not install other ProgIds that reference the current ProgId through the ProgId\_Default value.</span></span>

</dd> <dt>

<span data-ttu-id="df456-149"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="df456-149"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="df456-150">Description localisée facultative de l’ID de programme associé.</span><span class="sxs-lookup"><span data-stu-id="df456-150">An optional localized description of the associated program ID.</span></span>

</dd> <dt>

<span data-ttu-id="df456-151"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Située\_</span><span class="sxs-lookup"><span data-stu-id="df456-151"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="df456-152">Une clé étrangère facultative dans la [table d’icônes](icon-table.md) qui spécifie le fichier d’icône associé à ce ProgID.</span><span class="sxs-lookup"><span data-stu-id="df456-152">An optional foreign key into the [Icon table](icon-table.md) that specifies the icon file associated with this ProgId.</span></span> <span data-ttu-id="df456-153">Il est écrit sous la clé DefaultIcon associée à ce ProgId.</span><span class="sxs-lookup"><span data-stu-id="df456-153">This is written under the DefaultIcon key associated with this ProgId.</span></span> <span data-ttu-id="df456-154">Cette colonne doit avoir la valeur null pour un ProgId indépendant de la version.</span><span class="sxs-lookup"><span data-stu-id="df456-154">This column must be Null for a version independent ProgId.</span></span>

</dd> <dt>

<span data-ttu-id="df456-155"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IndexIcône</span><span class="sxs-lookup"><span data-stu-id="df456-155"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="df456-156">Index d’icône dans le fichier d’icône.</span><span class="sxs-lookup"><span data-stu-id="df456-156">The Icon index into the icon file.</span></span> <span data-ttu-id="df456-157">Cette colonne doit avoir la valeur null pour un ProgId indépendant de la version.</span><span class="sxs-lookup"><span data-stu-id="df456-157">This column must be Null for a version independent ProgId.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df456-158">Notes</span><span class="sxs-lookup"><span data-stu-id="df456-158">Remarks</span></span>

<span data-ttu-id="df456-159">Les actions [RegisterProgIdInfo](registerprogidinfo-action.md) et [UnregisterProgIdInfo](unregisterprogidinfo-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations contenues dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="df456-159">The [RegisterProgIdInfo](registerprogidinfo-action.md) and [UnregisterProgIdInfo](unregisterprogidinfo-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="df456-160">Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="df456-160">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="df456-161">Validation</span><span class="sxs-lookup"><span data-stu-id="df456-161">Validation</span></span>

<dl>

[<span data-ttu-id="df456-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="df456-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="df456-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="df456-163">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="df456-164">ICE32</span><span class="sxs-lookup"><span data-stu-id="df456-164">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="df456-165">ICE36</span><span class="sxs-lookup"><span data-stu-id="df456-165">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="df456-166">ICE89</span><span class="sxs-lookup"><span data-stu-id="df456-166">ICE89</span></span>](ice89.md)  
</dl>

 

 



