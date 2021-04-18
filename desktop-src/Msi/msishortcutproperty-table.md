---
description: La table MsiShortcutProperty permet au programme d’installation de Windows de définir des propriétés pour les raccourcis qui sont également des objets de shell Windows.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Table MsiShortcutProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f295feabd6ff9b1677fdcf47791959b0fbb8a920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529799"
---
# <a name="msishortcutproperty-table"></a><span data-ttu-id="07f5f-103">Table MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="07f5f-103">MsiShortcutProperty Table</span></span>

<span data-ttu-id="07f5f-104">La table MsiShortcutProperty permet au programme d’installation de Windows de définir des propriétés pour les raccourcis qui sont également des objets de [shell Windows](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="07f5f-104">The MsiShortcutProperty table enables Window Installer to set properties for shortcuts that are also [Windows Shell](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) objects.</span></span> <span data-ttu-id="07f5f-105">À compter de Windows Vista et de Windows Server 2008, le shell Windows fournit une interface IPropertyStore pour les objets Shell tels que les raccourcis.</span><span class="sxs-lookup"><span data-stu-id="07f5f-105">Beginning with Windows Vista and Windows Server 2008 the Windows Shell provides an IPropertyStore Interface for shell objects such as shortcuts.</span></span> <span data-ttu-id="07f5f-106">Un package Windows Installer 5,0 s’exécutant sur Windows Server 2008 R2 ou Windows 7 peut définir ces propriétés lors de l’installation du raccourci.</span><span class="sxs-lookup"><span data-stu-id="07f5f-106">A Windows Installer 5.0 package running on Windows Server 2008 R2 or Windows 7 can set these properties when the shortcut is installed.</span></span>

<span data-ttu-id="07f5f-107">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="07f5f-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="07f5f-108">Cette table est disponible à partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="07f5f-108">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="07f5f-109">La table MsiShortcutProperty contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="07f5f-109">The MsiShortcutProperty table has the following columns.</span></span>



| <span data-ttu-id="07f5f-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="07f5f-110">Column</span></span>              | <span data-ttu-id="07f5f-111">Type</span><span class="sxs-lookup"><span data-stu-id="07f5f-111">Type</span></span>                         | <span data-ttu-id="07f5f-112">Clé</span><span class="sxs-lookup"><span data-stu-id="07f5f-112">Key</span></span> | <span data-ttu-id="07f5f-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="07f5f-113">Nullable</span></span> |
|---------------------|------------------------------|-----|----------|
| <span data-ttu-id="07f5f-114">MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="07f5f-114">MsiShortcutProperty</span></span> | [<span data-ttu-id="07f5f-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="07f5f-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="07f5f-116">O</span><span class="sxs-lookup"><span data-stu-id="07f5f-116">Y</span></span>   | <span data-ttu-id="07f5f-117">N</span><span class="sxs-lookup"><span data-stu-id="07f5f-117">N</span></span>        |
| <span data-ttu-id="07f5f-118">Raccourci\_</span><span class="sxs-lookup"><span data-stu-id="07f5f-118">Shortcut\_</span></span>          | [<span data-ttu-id="07f5f-119">Identificateur</span><span class="sxs-lookup"><span data-stu-id="07f5f-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="07f5f-120">N</span><span class="sxs-lookup"><span data-stu-id="07f5f-120">N</span></span>   | <span data-ttu-id="07f5f-121">N</span><span class="sxs-lookup"><span data-stu-id="07f5f-121">N</span></span>        |
| <span data-ttu-id="07f5f-122">PropertyKey</span><span class="sxs-lookup"><span data-stu-id="07f5f-122">PropertyKey</span></span>         | [<span data-ttu-id="07f5f-123">Correct</span><span class="sxs-lookup"><span data-stu-id="07f5f-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="07f5f-124">N</span><span class="sxs-lookup"><span data-stu-id="07f5f-124">N</span></span>   | <span data-ttu-id="07f5f-125">N</span><span class="sxs-lookup"><span data-stu-id="07f5f-125">N</span></span>        |
| <span data-ttu-id="07f5f-126">PropVariantValue</span><span class="sxs-lookup"><span data-stu-id="07f5f-126">PropVariantValue</span></span>    | [<span data-ttu-id="07f5f-127">Correct</span><span class="sxs-lookup"><span data-stu-id="07f5f-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="07f5f-128">N</span><span class="sxs-lookup"><span data-stu-id="07f5f-128">N</span></span>   | <span data-ttu-id="07f5f-129">N</span><span class="sxs-lookup"><span data-stu-id="07f5f-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="07f5f-130">Colonnes</span><span class="sxs-lookup"><span data-stu-id="07f5f-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="07f5f-131"><span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="07f5f-131"><span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty</span></span>
</dt> <dd>

<span data-ttu-id="07f5f-132">Identificateur unique de cette ligne de la table MsiShortcutProperty.</span><span class="sxs-lookup"><span data-stu-id="07f5f-132">Unique identifier for this row of the MsiShortcutProperty table.</span></span>

</dd> <dt>

<span data-ttu-id="07f5f-133"><span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Gestionnaires\_</span><span class="sxs-lookup"><span data-stu-id="07f5f-133"><span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Shortcut\_</span></span>
</dt> <dd>

<span data-ttu-id="07f5f-134">Clé dans le tableau de [raccourcis](shortcut-table.md) qui identifie le raccourci ayant un jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="07f5f-134">A key into the [Shortcut](shortcut-table.md) table that identifies the shortcut having a property set.</span></span>

</dd> <dt>

<span data-ttu-id="07f5f-135"><span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey</span><span class="sxs-lookup"><span data-stu-id="07f5f-135"><span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey</span></span>
</dt> <dd>

<span data-ttu-id="07f5f-136">Valeur de chaîne qui fournit des informations pour la structure [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) .</span><span class="sxs-lookup"><span data-stu-id="07f5f-136">A string value that provides information for the [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure.</span></span> <span data-ttu-id="07f5f-137">Les informations contenues dans ce champ doivent faire référence au nom canonique d’une propriété inscrite auprès du système de propriétés Windows.</span><span class="sxs-lookup"><span data-stu-id="07f5f-137">The information in this field must refer to the canonical name of a property registered with the Windows property system.</span></span> <span data-ttu-id="07f5f-138">Pour plus d’informations sur le système de propriétés Windows, consultez [vue d’ensemble du système de propriétés](/previous-versions//bb776909(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="07f5f-138">For more information about the Windows property system, see the [Property System Overview](/previous-versions//bb776909(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="07f5f-139"><span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue</span><span class="sxs-lookup"><span data-stu-id="07f5f-139"><span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue</span></span>
</dt> <dd>

<span data-ttu-id="07f5f-140">Valeur de chaîne qui fournit des informations pour la structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="07f5f-140">A string value that provides information for the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

</dd> </dl>

<span data-ttu-id="07f5f-141">Plusieurs propriétés peuvent être définies sur un raccourci.</span><span class="sxs-lookup"><span data-stu-id="07f5f-141">Multiple properties can be set on a shortcut.</span></span> <span data-ttu-id="07f5f-142">Si la même propriété est définie plusieurs fois sur le même raccourci, la valeur est définie dans un ordre non spécifié.</span><span class="sxs-lookup"><span data-stu-id="07f5f-142">If the same property is set multiple times on the same shortcut the value is set in an unspecified order.</span></span>

<span data-ttu-id="07f5f-143">Windows Installer pouvez définir des propriétés de raccourci uniquement lors de l’installation ou de la réinstallation du raccourci.</span><span class="sxs-lookup"><span data-stu-id="07f5f-143">Windows Installer can set shortcut properties only when the shortcut is installed or reinstalled.</span></span> <span data-ttu-id="07f5f-144">Un correctif qui ne réinstalle pas un raccourci qui a déjà été installé ne met pas à jour les propriétés du raccourci.</span><span class="sxs-lookup"><span data-stu-id="07f5f-144">A patch that does not reinstall a shortcut that has already been installed does not update the shortcut's properties.</span></span> <span data-ttu-id="07f5f-145">Un correctif peut mettre à jour les propriétés en incluant un tableau de [raccourcis](shortcut-table.md) dans le package correctif et en réinstallant le raccourci.</span><span class="sxs-lookup"><span data-stu-id="07f5f-145">A patch can update the properties by including a [Shortcut](shortcut-table.md) table in the patch package and reinstalling the shortcut.</span></span>

## <a name="remarks"></a><span data-ttu-id="07f5f-146">Notes</span><span class="sxs-lookup"><span data-stu-id="07f5f-146">Remarks</span></span>

<span data-ttu-id="07f5f-147">[Windows Installer message d’erreur](windows-installer-error-messages.md) 1946 est retourné en tant qu’avertissement et l’installation se poursuit, si Windows Installer ne parvient pas à définir une propriété de raccourci spécifiée dans la table MsiShortcutProperty.</span><span class="sxs-lookup"><span data-stu-id="07f5f-147">[Windows Installer Error Message](windows-installer-error-messages.md) 1946 is returned as a warning, and the installation continues, if Windows Installer is unable to set a shortcut property specified in the MsiShortcutProperty table.</span></span>

## <a name="validation"></a><span data-ttu-id="07f5f-148">Validation</span><span class="sxs-lookup"><span data-stu-id="07f5f-148">Validation</span></span>

<dl>

[<span data-ttu-id="07f5f-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="07f5f-149">ICE03</span></span>](ice03.md)  
</dl>

 

 
