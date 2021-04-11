---
description: Si ce bit est défini, la boîte de dialogue appelle régulièrement le programme d’installation.
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: TrackDiskSpace bit de style de boîte de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab0cf234071ace41432e20a598b38fb1fc431e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111994"
---
# <a name="trackdiskspace-dialog-style-bit"></a><span data-ttu-id="fe70c-103">TrackDiskSpace bit de style de boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="fe70c-103">TrackDiskSpace Dialog Style Bit</span></span>

<span data-ttu-id="fe70c-104">Si ce bit est défini, la boîte de dialogue appelle régulièrement le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="fe70c-104">If this bit is set, the dialog box periodically calls the installer.</span></span> <span data-ttu-id="fe70c-105">Si la propriété change, elle avertit les contrôles sur la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="fe70c-105">If the property changes, it notifies the controls on the dialog.</span></span> <span data-ttu-id="fe70c-106">Ce style peut être utilisé s’il existe un contrôle sur la boîte de dialogue indiquant l’espace disque.</span><span class="sxs-lookup"><span data-stu-id="fe70c-106">This style can be used if there is a control on the dialog indicating disk space.</span></span> <span data-ttu-id="fe70c-107">Si l’utilisateur bascule vers une autre application, ajoute ou supprime des fichiers, ou modifie l’espace disque disponible, vous pouvez implémenter rapidement la modification à l’aide de ce style.</span><span class="sxs-lookup"><span data-stu-id="fe70c-107">If the user switches to another application, adds or removes files, or otherwise modifies available disk space, you can quickly implement the change using this style.</span></span>

<span data-ttu-id="fe70c-108">Toute boîte de dialogue reposant sur la propriété [**OutOfDiskSpace**](outofdiskspace.md) pour déterminer s’il faut afficher une boîte de dialogue doit définir le bit de style de la boîte de dialogue TrackDiskSpace pour la boîte de dialogue afin de mettre à jour dynamiquement l’espace sur les volumes cibles.</span><span class="sxs-lookup"><span data-stu-id="fe70c-108">Any dialog box relying on the [**OutOfDiskSpace**](outofdiskspace.md) property to determine whether to bring up a dialog must set the TrackDiskSpace Dialog Style Bit for the dialog to dynamically update space on the target volumes.</span></span>

## <a name="value"></a><span data-ttu-id="fe70c-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe70c-109">Value</span></span>



| <span data-ttu-id="fe70c-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="fe70c-110">Decimal</span></span> | <span data-ttu-id="fe70c-111">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="fe70c-111">Hexadecimal</span></span> | <span data-ttu-id="fe70c-112">Constante</span><span class="sxs-lookup"><span data-stu-id="fe70c-112">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="fe70c-113">32</span><span class="sxs-lookup"><span data-stu-id="fe70c-113">32</span></span>      | <span data-ttu-id="fe70c-114">0x00000020</span><span class="sxs-lookup"><span data-stu-id="fe70c-114">0x00000020</span></span>  | <span data-ttu-id="fe70c-115">**msidbDialogAttributesTrackDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="fe70c-115">**msidbDialogAttributesTrackDiskSpace**</span></span> |



 

 

 



