---
description: en raison du manque de reconnaissance sur les éditions non tablet PC de Microsoft Windows XP, vous ne pouvez pas utiliser InkEdit pour restituer l’encre sur Windows 2000, Windows Server 2003 et les éditions non-tablet PC de Windows XP, et vous ne pouvez pas utiliser le contrôle pour entrer de l’encre sur ces systèmes d’exploitation.
ms.assetid: eb80ff91-5c09-43d1-afd4-6391097000c1
title: Utilisation d’InkEdit sur les versions antérieures de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa98089a2ede778be09719767f96a1129a1be0d4004828172651e637cd81d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966608"
---
# <a name="using-inkedit-on-earlier-versions-of-windows"></a>Utilisation d’InkEdit sur les versions antérieures de Windows

en raison du manque de reconnaissance sur les éditions non tablet PC de Microsoft Windows XP, vous ne pouvez pas utiliser [InkEdit](inkedit-control.md) pour restituer l’encre sur Windows 2000, Windows Server 2003 et les éditions non-tablet PC de Windows XP, et vous ne pouvez pas utiliser le contrôle pour entrer de l’encre sur ces systèmes d’exploitation.

La propriété [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) du contrôle est définie sur **Disabled** (**IEM \_ désactivé** pour C++) et la tentative de modification de la propriété n’a aucun effet. Vous pouvez assigner des valeurs à d’autres propriétés et copier et coller de l’encre dans d’autres applications, mais vous ne pouvez pas utiliser le contrôle pour accepter des mouvements ou collecter de l’encre.

 

 



