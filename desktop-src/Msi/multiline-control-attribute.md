---
description: Si ce bit est défini sur un contrôle d’édition, le programme d’installation crée un contrôle d’édition de plusieurs lignes avec une barre de défilement verticale.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: Attribut de contrôle multiligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936bc4b3901293e950690e878a0f86229bb03b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202315"
---
# <a name="multiline-control-attribute"></a><span data-ttu-id="0eac7-103">Attribut de contrôle multiligne</span><span class="sxs-lookup"><span data-stu-id="0eac7-103">MultiLine Control Attribute</span></span>

<span data-ttu-id="0eac7-104">Si ce bit est défini sur un [contrôle d’édition](edit-control.md), le programme d’installation crée un contrôle d’édition de plusieurs lignes avec une barre de défilement verticale.</span><span class="sxs-lookup"><span data-stu-id="0eac7-104">If this bit is set on an [Edit control](edit-control.md), the installer creates a multiple line edit control with a vertical scroll bar.</span></span>

<span data-ttu-id="0eac7-105">Si ce bit n’est pas défini, il spécifie l’affichage d’un contrôle d’édition normal.</span><span class="sxs-lookup"><span data-stu-id="0eac7-105">If this bit is not set, it specifies displaying a normal edit control.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="0eac7-106">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="0eac7-106">Valid Controls</span></span>

<span data-ttu-id="0eac7-107">[Contrôle d’édition](edit-control.md).</span><span class="sxs-lookup"><span data-stu-id="0eac7-107">[Edit control](edit-control.md).</span></span>



| <span data-ttu-id="0eac7-108">Decimal</span><span class="sxs-lookup"><span data-stu-id="0eac7-108">Decimal</span></span> | <span data-ttu-id="0eac7-109">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="0eac7-109">Hexadecimal</span></span> | <span data-ttu-id="0eac7-110">Constante</span><span class="sxs-lookup"><span data-stu-id="0eac7-110">Constant</span></span>                            |
|---------|-------------|-------------------------------------|
| <span data-ttu-id="0eac7-111">65536</span><span class="sxs-lookup"><span data-stu-id="0eac7-111">65536</span></span>   | <span data-ttu-id="0eac7-112">0x00010000</span><span class="sxs-lookup"><span data-stu-id="0eac7-112">0x00010000</span></span>  | <span data-ttu-id="0eac7-113">**msidbControlAttributesMultiline**</span><span class="sxs-lookup"><span data-stu-id="0eac7-113">**msidbControlAttributesMultiline**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0eac7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0eac7-114">Remarks</span></span>

<span data-ttu-id="0eac7-115">Pour définir cet attribut sur un contrôle, incluez le bit multiligne dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="0eac7-115">To set this attribute on a control, include the MultiLine bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="0eac7-116">Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="0eac7-116">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



