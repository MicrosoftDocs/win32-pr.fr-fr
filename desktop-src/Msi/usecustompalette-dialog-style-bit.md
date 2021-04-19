---
description: Si ce bit est défini, les images de la boîte de dialogue sont créées avec la palette personnalisée (une par boîte de dialogue reçue à partir du premier contrôle créé). Si le bit n’est pas défini, les images sont rendues à l’aide d’une palette par défaut.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: UseCustomPalette bit de style de boîte de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507ed1c900c564e3e791f4d0bbc5f8658798fdb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535615"
---
# <a name="usecustompalette-dialog-style-bit"></a><span data-ttu-id="4a919-104">UseCustomPalette bit de style de boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="4a919-104">UseCustomPalette Dialog Style Bit</span></span>

<span data-ttu-id="4a919-105">Si ce bit est défini, les images de la boîte de dialogue sont créées avec la palette personnalisée (une par boîte de dialogue reçue à partir du premier contrôle créé).</span><span class="sxs-lookup"><span data-stu-id="4a919-105">If this bit is set, the pictures on the dialog box are created with the custom palette (one per dialog received from the first control created).</span></span> <span data-ttu-id="4a919-106">Si le bit n’est pas défini, les images sont rendues à l’aide d’une palette par défaut.</span><span class="sxs-lookup"><span data-stu-id="4a919-106">If the bit is not set, the pictures are rendered using a default palette.</span></span>

<span data-ttu-id="4a919-107">En général, vous définissez ce bit si la boîte de dialogue contient une image avec une palette spéciale, ou plusieurs images partageant une palette personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4a919-107">Typically one would set this bit if the dialog contains a picture with a special palette, or several pictures sharing a custom palette.</span></span> <span data-ttu-id="4a919-108">Le bit ne doit pas être défini si la boîte de dialogue contient plusieurs images avec différentes palettes.</span><span class="sxs-lookup"><span data-stu-id="4a919-108">The bit should not be set if the dialog contains several pictures with different palettes.</span></span> <span data-ttu-id="4a919-109">Dans ce cas, la palette par défaut est susceptible d’obtenir un résultat satisfaisant pour toutes les images.</span><span class="sxs-lookup"><span data-stu-id="4a919-109">In this case, the default palette is most likely to give a satisfactory result for all pictures.</span></span>

## <a name="value"></a><span data-ttu-id="4a919-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a919-110">Value</span></span>



| <span data-ttu-id="4a919-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="4a919-111">Decimal</span></span> | <span data-ttu-id="4a919-112">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="4a919-112">Hexadecimal</span></span> | <span data-ttu-id="4a919-113">Constante</span><span class="sxs-lookup"><span data-stu-id="4a919-113">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="4a919-114">64</span><span class="sxs-lookup"><span data-stu-id="4a919-114">64</span></span>      | <span data-ttu-id="4a919-115">0x00000040</span><span class="sxs-lookup"><span data-stu-id="4a919-115">0x00000040</span></span>  | <span data-ttu-id="4a919-116">**msidbDialogAttributesUseCustomPalette**</span><span class="sxs-lookup"><span data-stu-id="4a919-116">**msidbDialogAttributesUseCustomPalette**</span></span> |



 

 

 



