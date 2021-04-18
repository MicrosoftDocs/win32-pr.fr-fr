---
description: Vous pouvez utiliser le contrôle InkPicture pour restituer l’encre sur les éditions Microsoft Windows 2000, Windows Server 2003 et non-Tablet PC de Windows XP. Toutefois, vous ne pouvez pas utiliser le contrôle pour entrer de l’encre sur ces systèmes d’exploitation.
ms.assetid: e5d00b0f-0a4f-4ea2-ae63-dfb6bc8c2caf
title: Utilisation d’InkPicture sur des versions antérieures de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbd2bf8545524787c9e37f70c43d954ab440910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543081"
---
# <a name="using-inkpicture-on-earlier-versions-of-windows"></a><span data-ttu-id="767de-104">Utilisation d’InkPicture sur des versions antérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="767de-104">Using InkPicture on Earlier Versions of Windows</span></span>

<span data-ttu-id="767de-105">Vous pouvez utiliser le [contrôle InkPicture](inkpicture-control.md) pour restituer l’encre sur les éditions Microsoft Windows 2000, windows Server 2003 et non-Tablet PC de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="767de-105">You can use the [InkPicture Control](inkpicture-control.md) to render ink on Microsoft Windows 2000, Windows Server 2003, and non-Tablet PC editions of Windows XP.</span></span> <span data-ttu-id="767de-106">Toutefois, vous ne pouvez pas utiliser le contrôle pour entrer de l’encre sur ces systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="767de-106">However, you cannot use the control to input ink on these operating systems.</span></span>

<span data-ttu-id="767de-107">La propriété [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) du contrôle est définie sur **false** et la tentative de modification de la propriété n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="767de-107">The control's [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) property is set to **FALSE**, and attempting to change the property has no effect.</span></span> <span data-ttu-id="767de-108">Vous pouvez assigner des valeurs à d’autres propriétés et manipuler par programmation l’encre, mais vous ne pouvez pas utiliser le contrôle pour collecter l’encre.</span><span class="sxs-lookup"><span data-stu-id="767de-108">You can assign values to other properties and programmatically manipulate ink, but you cannot use the control to collect ink.</span></span>

 

 



