---
description: Si le bit de contrôle bitmap est défini, le texte du contrôle est remplacé par une image bitmap. La colonne de texte dans la table de contrôle est une clé étrangère dans la table binaire.
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Attribut de contrôle bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bda78231c1689c4c5faebeab98fbf6566c7e667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864437"
---
# <a name="bitmap-control-attribute"></a><span data-ttu-id="9125c-104">Attribut de contrôle bitmap</span><span class="sxs-lookup"><span data-stu-id="9125c-104">Bitmap Control Attribute</span></span>

<span data-ttu-id="9125c-105">Si le bit de contrôle bitmap est défini, le texte du contrôle est remplacé par une image bitmap.</span><span class="sxs-lookup"><span data-stu-id="9125c-105">If the Bitmap Control bit is set, the text in the control is replaced by a bitmap image.</span></span> <span data-ttu-id="9125c-106">La colonne de texte dans la [table de contrôle](control-table.md) est une clé étrangère dans la [table binaire](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="9125c-106">The Text column in the [Control table](control-table.md) is a foreign key into the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="9125c-107">Si ce bit n’est pas défini, le texte du contrôle est spécifié dans la colonne text de la [table Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="9125c-107">If this bit is not set, the text in the control is specified in the Text column of the [Control table](control-table.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="9125c-108">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="9125c-108">Valid Controls</span></span>

[<span data-ttu-id="9125c-109">CheckBox</span><span class="sxs-lookup"><span data-stu-id="9125c-109">CheckBox</span></span>](checkbox-control.md)

 

[<span data-ttu-id="9125c-110">Boutons</span><span class="sxs-lookup"><span data-stu-id="9125c-110">PushButton</span></span>](pushbutton-control.md)

 

[<span data-ttu-id="9125c-111">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="9125c-111">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="9125c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="9125c-112">Value</span></span>



| <span data-ttu-id="9125c-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="9125c-113">Decimal</span></span> | <span data-ttu-id="9125c-114">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="9125c-114">Hexadecimal</span></span> | <span data-ttu-id="9125c-115">Constante</span><span class="sxs-lookup"><span data-stu-id="9125c-115">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="9125c-116">262 144</span><span class="sxs-lookup"><span data-stu-id="9125c-116">262144</span></span>  | <span data-ttu-id="9125c-117">0x00040000</span><span class="sxs-lookup"><span data-stu-id="9125c-117">0x00040000</span></span>  | <span data-ttu-id="9125c-118">**msidbControlAttributesBitmap**</span><span class="sxs-lookup"><span data-stu-id="9125c-118">**msidbControlAttributesBitmap**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9125c-119">Notes</span><span class="sxs-lookup"><span data-stu-id="9125c-119">Remarks</span></span>

<span data-ttu-id="9125c-120">Pour définir cet attribut sur un contrôle, incluez le bit de bitmap dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="9125c-120">To set this attribute on a control, include the Bitmap bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="9125c-121">La colonne de texte de la table de contrôle est utilisée comme clé étrangère de la [table binaire](binary-table.md). par conséquent, le contrôle ne peut pas contenir à la fois une image d’icône et du texte.</span><span class="sxs-lookup"><span data-stu-id="9125c-121">The Text column in the Control table is used as a foreign key to the [Binary table](binary-table.md), therefore the control cannot contain both an icon image and text.</span></span>

<span data-ttu-id="9125c-122">Ne définissez pas à la fois l' [icône](icon-control-attribute.md) et les bits de bitmap.</span><span class="sxs-lookup"><span data-stu-id="9125c-122">Do not set both the [Icon](icon-control-attribute.md) and Bitmap bits.</span></span>

<span data-ttu-id="9125c-123">Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="9125c-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



