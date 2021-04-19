---
description: Si le bit de contrôle ComboList est défini sur une zone de liste déroulante, le champ d’édition est remplacé par un champ de texte statique. Cela empêche un utilisateur d’entrer une nouvelle valeur et oblige l’utilisateur à choisir uniquement l’une des valeurs prédéfinies.
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: Attribut de contrôle ComboList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dcb1c51e8eccaba03c3b4d905b0501e8a3f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541894"
---
# <a name="combolist-control-attribute"></a><span data-ttu-id="abaed-104">Attribut de contrôle ComboList</span><span class="sxs-lookup"><span data-stu-id="abaed-104">ComboList Control Attribute</span></span>

<span data-ttu-id="abaed-105">Si le bit de contrôle ComboList est défini sur une zone de liste déroulante, le champ d’édition est remplacé par un champ de texte statique.</span><span class="sxs-lookup"><span data-stu-id="abaed-105">If the ComboList Control bit is set on a combo box, the edit field is replaced by a static text field.</span></span> <span data-ttu-id="abaed-106">Cela empêche un utilisateur d’entrer une nouvelle valeur et oblige l’utilisateur à choisir uniquement l’une des valeurs prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="abaed-106">This prevents a user from entering a new value and requires the user to choose only one of the predefined values.</span></span>

<span data-ttu-id="abaed-107">Si ce bit n’est pas défini, la zone de liste déroulante contient un champ d’édition.</span><span class="sxs-lookup"><span data-stu-id="abaed-107">If this bit is not set, the combo box has an edit field.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="abaed-108">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="abaed-108">Valid Controls</span></span>

[<span data-ttu-id="abaed-109">ComboBox</span><span class="sxs-lookup"><span data-stu-id="abaed-109">ComboBox</span></span>](combobox-control.md)

## <a name="value"></a><span data-ttu-id="abaed-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="abaed-110">Value</span></span>



| <span data-ttu-id="abaed-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="abaed-111">Decimal</span></span> | <span data-ttu-id="abaed-112">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="abaed-112">Hexadecimal</span></span> | <span data-ttu-id="abaed-113">Description</span><span class="sxs-lookup"><span data-stu-id="abaed-113">Description</span></span>                     |
|---------|-------------|---------------------------------|
| <span data-ttu-id="abaed-114">131 072</span><span class="sxs-lookup"><span data-stu-id="abaed-114">131072</span></span>  | <span data-ttu-id="abaed-115">0x00020000</span><span class="sxs-lookup"><span data-stu-id="abaed-115">0x00020000</span></span>  | <span data-ttu-id="abaed-116">msidbControlAttributesComboList</span><span class="sxs-lookup"><span data-stu-id="abaed-116">msidbControlAttributesComboList</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="abaed-117">Notes</span><span class="sxs-lookup"><span data-stu-id="abaed-117">Remarks</span></span>

<span data-ttu-id="abaed-118">Pour définir cet attribut sur un contrôle, incluez le bit ComboList dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="abaed-118">To set this attribute on a control, include the ComboList bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="abaed-119">Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="abaed-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



