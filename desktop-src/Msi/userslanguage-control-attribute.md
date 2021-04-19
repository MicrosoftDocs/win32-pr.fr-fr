---
description: Si cet indicateur de bit est défini, les polices sont créées à l’aide de la page de codes de l’interface utilisateur par défaut de l’utilisateur. Si l’indicateur binaire n’est pas défini, les polices sont créées à l’aide de la page de codes de la base de données.
ms.assetid: 6a3dbabe-6a14-4401-b46c-e8a0bd0cbe63
title: Attribut de contrôle UsersLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff4109c5c0819b199343bb8ee38bfecc069ad4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517797"
---
# <a name="userslanguage-control-attribute"></a><span data-ttu-id="8f72e-104">Attribut de contrôle UsersLanguage</span><span class="sxs-lookup"><span data-stu-id="8f72e-104">UsersLanguage Control Attribute</span></span>

<span data-ttu-id="8f72e-105">Si cet indicateur de bit est défini, les polices sont créées à l’aide de la page de codes de l’interface utilisateur par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f72e-105">If this bit flag is set, fonts are created using the user's default UI code page.</span></span> <span data-ttu-id="8f72e-106">Si l’indicateur binaire n’est pas défini, les polices sont créées à l’aide de la page de codes de la base de données.</span><span class="sxs-lookup"><span data-stu-id="8f72e-106">If the bit flag is not set, fonts are created using the database code page.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="8f72e-107">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="8f72e-107">Valid Controls</span></span>

[<span data-ttu-id="8f72e-108">Text</span><span class="sxs-lookup"><span data-stu-id="8f72e-108">Text</span></span>](text-control.md)

 

[<span data-ttu-id="8f72e-109">ListBox</span><span class="sxs-lookup"><span data-stu-id="8f72e-109">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="8f72e-110">ComboBox</span><span class="sxs-lookup"><span data-stu-id="8f72e-110">ComboBox</span></span>](combobox-control.md)

## <a name="value"></a><span data-ttu-id="8f72e-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f72e-111">Value</span></span>



| <span data-ttu-id="8f72e-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="8f72e-112">Decimal</span></span> | <span data-ttu-id="8f72e-113">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="8f72e-113">Hexadecimal</span></span> | <span data-ttu-id="8f72e-114">Constante</span><span class="sxs-lookup"><span data-stu-id="8f72e-114">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="8f72e-115">1 048 576</span><span class="sxs-lookup"><span data-stu-id="8f72e-115">1048576</span></span> | <span data-ttu-id="8f72e-116">0x00100000</span><span class="sxs-lookup"><span data-stu-id="8f72e-116">0x00100000</span></span>  | <span data-ttu-id="8f72e-117">**msidbControlAttributesUsersLanguage**</span><span class="sxs-lookup"><span data-stu-id="8f72e-117">**msidbControlAttributesUsersLanguage**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8f72e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="8f72e-118">Remarks</span></span>

<span data-ttu-id="8f72e-119">Cet attribut de contrôle peut être utilisé pour afficher le texte que l’utilisateur a entré dans un contrôle [Edit](edit-control.md) ou [PathEdit](pathedit-control.md) .</span><span class="sxs-lookup"><span data-stu-id="8f72e-119">This control attribute can be used to display text that the user has entered into an [Edit](edit-control.md) or [PathEdit](pathedit-control.md) control.</span></span>

<span data-ttu-id="8f72e-120">Le contrôle d’édition, le contrôle PathEdit, le contrôle [DirectoryList](directorylist-control.md) et le [contrôle DirectoryCombo](directorycombo-control.md) utilisent toujours les polices créées dans la page de codes de l’interface utilisateur par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f72e-120">The Edit control, PathEdit control, [DirectoryList control](directorylist-control.md) and [DirectoryCombo control](directorycombo-control.md) always use the fonts created in the user's default UI code page.</span></span> <span data-ttu-id="8f72e-121">Cela peut entraîner des problèmes si des langues supplémentaires ont été installées sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8f72e-121">This can cause problems if additional languages have been installed on the operating system.</span></span> <span data-ttu-id="8f72e-122">Dans ce cas, les polices sur l’ordinateur peuvent ne pas être en mesure de représenter tous les caractères dans les langues ajoutées.</span><span class="sxs-lookup"><span data-stu-id="8f72e-122">In this case, the fonts on the computer may not be able to represent all the characters in the added languages.</span></span> <span data-ttu-id="8f72e-123">Pour déterminer les polices qui peuvent être utilisées, recherchez les valeurs dans **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ FontLink \\ SystemLink**.</span><span class="sxs-lookup"><span data-stu-id="8f72e-123">To determine what fonts can be used, look up the values in **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\FontLink\\SystemLink**.</span></span>

<span data-ttu-id="8f72e-124">Pour plus d’informations, consultez [contrôles](controls.md)et [attributs](control-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="8f72e-124">For more information, see [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



