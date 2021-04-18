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
# <a name="using-inkpicture-on-earlier-versions-of-windows"></a>Utilisation d’InkPicture sur des versions antérieures de Windows

Vous pouvez utiliser le [contrôle InkPicture](inkpicture-control.md) pour restituer l’encre sur les éditions Microsoft Windows 2000, windows Server 2003 et non-Tablet PC de Windows XP. Toutefois, vous ne pouvez pas utiliser le contrôle pour entrer de l’encre sur ces systèmes d’exploitation.

La propriété [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) du contrôle est définie sur **false** et la tentative de modification de la propriété n’a aucun effet. Vous pouvez assigner des valeurs à d’autres propriétés et manipuler par programmation l’encre, mais vous ne pouvez pas utiliser le contrôle pour collecter l’encre.

 

 



