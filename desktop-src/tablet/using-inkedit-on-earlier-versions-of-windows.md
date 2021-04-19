---
description: En raison du manque de reconnaissance sur les éditions non Tablet PC de Microsoft Windows XP, vous ne pouvez pas utiliser InkEdit pour restituer l’encre sur les éditions Windows 2000, Windows Server 2003 et autres que Tablet PC de Windows XP, et vous ne pouvez pas utiliser le contrôle pour entrer de l’encre sur ces systèmes d’exploitation.
ms.assetid: eb80ff91-5c09-43d1-afd4-6391097000c1
title: Utilisation d’InkEdit sur les versions antérieures de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08343b3d379a3f45985b1f586254e7a370998f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514007"
---
# <a name="using-inkedit-on-earlier-versions-of-windows"></a><span data-ttu-id="eb56c-103">Utilisation d’InkEdit sur les versions antérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="eb56c-103">Using InkEdit on Earlier Versions of Windows</span></span>

<span data-ttu-id="eb56c-104">En raison du manque de reconnaissance sur les éditions non Tablet PC de Microsoft Windows XP, vous ne pouvez pas utiliser [InkEdit](inkedit-control.md) pour restituer l’encre sur les éditions Windows 2000, windows Server 2003 et autres que Tablet PC de Windows XP, et vous ne pouvez pas utiliser le contrôle pour entrer de l’encre sur ces systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="eb56c-104">Because of the lack of recognizers on non-Tablet PC editions of Microsoft Windows XP, you cannot use [InkEdit](inkedit-control.md) to render ink on Windows 2000, Windows Server 2003, and non-Tablet PC editions of Windows XP, and you cannot use the control to input ink on these operating systems.</span></span>

<span data-ttu-id="eb56c-105">La propriété [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) du contrôle est définie sur **Disabled** (**IEM \_ désactivé** pour C++) et la tentative de modification de la propriété n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="eb56c-105">The control's [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property is set to **Disabled** (**IEM\_Disabled** for C++), and attempting to change the property has no effect.</span></span> <span data-ttu-id="eb56c-106">Vous pouvez assigner des valeurs à d’autres propriétés et copier et coller de l’encre dans d’autres applications, mais vous ne pouvez pas utiliser le contrôle pour accepter des mouvements ou collecter de l’encre.</span><span class="sxs-lookup"><span data-stu-id="eb56c-106">You can assign values to other properties and copy and paste ink to other applications, but you cannot use the control to accept gestures or collect ink.</span></span>

 

 



