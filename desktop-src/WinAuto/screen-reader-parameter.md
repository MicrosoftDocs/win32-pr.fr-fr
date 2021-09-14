---
title: Paramètre de lecteur d’écran
description: Le paramètre de lecteur d’écran indique si une application doit fournir des informations textuelles dans les situations où elle présenterait autrement les informations sous forme graphique.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c237f3d945b9782884ffc655cf87a203159a16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010640"
---
# <a name="screen-reader-parameter"></a>Paramètre de lecteur d’écran

Le paramètre de lecteur d’écran indique si une application doit fournir des informations textuelles dans les situations où elle présenterait autrement les informations sous forme graphique.

Ce paramètre est généralement défini par des aides à l’accessibilité, telles que les lecteurs d’écran. Les applications utilisent les indicateurs **SPI \_ GETSCREENREADER** et **SPI \_ SETSCREENREADER** avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour récupérer et définir le paramètre de lecteur d’écran.

> [!Note]  
> narrator, le lecteur d’écran inclus avec Windows, ne définit pas les indicateurs **spi \_ SETSCREENREADER** ou **spi \_ GETSCREENREADER** .

 

 

 