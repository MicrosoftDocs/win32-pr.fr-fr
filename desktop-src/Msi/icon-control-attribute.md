---
description: Si ce bit est défini, le texte est remplacé par une image d’icône et la colonne de texte dans la table de contrôle est une clé étrangère dans la table binaire.
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Icon, attribut de contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60c19674ac26f108109fad04e0836ed8dfeba6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527353"
---
# <a name="icon-control-attribute"></a><span data-ttu-id="4a83e-103">Icon, attribut de contrôle</span><span class="sxs-lookup"><span data-stu-id="4a83e-103">Icon Control Attribute</span></span>

<span data-ttu-id="4a83e-104">Si ce bit est défini, le texte est remplacé par une image d’icône et la colonne de texte dans la [table de contrôle](control-table.md) est une clé étrangère dans la [table binaire](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="4a83e-104">If this bit is set, text is replaced by an icon image and the Text column in the [Control table](control-table.md) is a foreign key into the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="4a83e-105">Si ce bit n’est pas défini, le texte du contrôle est spécifié dans la colonne text de la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="4a83e-105">If this bit is not set, text in the control is specified in the Text column of the [Control table](control-table.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="4a83e-106">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="4a83e-106">Valid Controls</span></span>

[<span data-ttu-id="4a83e-107">CheckBox</span><span class="sxs-lookup"><span data-stu-id="4a83e-107">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="4a83e-108">Boutons</span><span class="sxs-lookup"><span data-stu-id="4a83e-108">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="4a83e-109">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="4a83e-109">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="4a83e-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a83e-110">Value</span></span>



| <span data-ttu-id="4a83e-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="4a83e-111">Decimal</span></span> | <span data-ttu-id="4a83e-112">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="4a83e-112">Hexadecimal</span></span> | <span data-ttu-id="4a83e-113">Constante</span><span class="sxs-lookup"><span data-stu-id="4a83e-113">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="4a83e-114">5242288</span><span class="sxs-lookup"><span data-stu-id="4a83e-114">5242288</span></span> | <span data-ttu-id="4a83e-115">0x00080000</span><span class="sxs-lookup"><span data-stu-id="4a83e-115">0x00080000</span></span>  | <span data-ttu-id="4a83e-116">**msidbControlAttributesIcon**</span><span class="sxs-lookup"><span data-stu-id="4a83e-116">**msidbControlAttributesIcon**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4a83e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4a83e-117">Remarks</span></span>

<span data-ttu-id="4a83e-118">Pour définir cet attribut sur un contrôle, incluez les bits d’icône dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="4a83e-118">To set this attribute on a control, include the Icon bits in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="4a83e-119">La colonne de texte de la table de contrôle est utilisée comme clé étrangère de la [table binaire](binary-table.md). par conséquent, le contrôle ne peut pas contenir à la fois une image d’icône et du texte.</span><span class="sxs-lookup"><span data-stu-id="4a83e-119">The Text column in the Control table is used as a foreign key to the [Binary table](binary-table.md), therefore the control cannot contain both an icon image and text.</span></span>

<span data-ttu-id="4a83e-120">Ne définissez pas à la fois l’icône et les bits de [bitmap](bitmap-control-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="4a83e-120">Do not set both the Icon and [Bitmap](bitmap-control-attribute.md) bits.</span></span>

<span data-ttu-id="4a83e-121">Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="4a83e-121">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



