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
# <a name="using-inkedit-on-earlier-versions-of-windows"></a>Utilisation d’InkEdit sur les versions antérieures de Windows

En raison du manque de reconnaissance sur les éditions non Tablet PC de Microsoft Windows XP, vous ne pouvez pas utiliser [InkEdit](inkedit-control.md) pour restituer l’encre sur les éditions Windows 2000, windows Server 2003 et autres que Tablet PC de Windows XP, et vous ne pouvez pas utiliser le contrôle pour entrer de l’encre sur ces systèmes d’exploitation.

La propriété [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) du contrôle est définie sur **Disabled** (**IEM \_ désactivé** pour C++) et la tentative de modification de la propriété n’a aucun effet. Vous pouvez assigner des valeurs à d’autres propriétés et copier et coller de l’encre dans d’autres applications, mais vous ne pouvez pas utiliser le contrôle pour accepter des mouvements ou collecter de l’encre.

 

 



