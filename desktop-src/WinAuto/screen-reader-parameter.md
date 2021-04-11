---
title: Paramètre de lecteur d’écran
description: Le paramètre de lecteur d’écran indique si une application doit fournir des informations textuelles dans les situations où elle présenterait autrement les informations sous forme graphique.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c237f3d945b9782884ffc655cf87a203159a16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031512"
---
# <a name="screen-reader-parameter"></a>Paramètre de lecteur d’écran

Le paramètre de lecteur d’écran indique si une application doit fournir des informations textuelles dans les situations où elle présenterait autrement les informations sous forme graphique.

Ce paramètre est généralement défini par des aides à l’accessibilité, telles que les lecteurs d’écran. Les applications utilisent les indicateurs **SPI \_ GETSCREENREADER** et **SPI \_ SETSCREENREADER** avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour récupérer et définir le paramètre de lecteur d’écran.

> [!Note]  
> Le narrateur, le lecteur d’écran inclus avec Windows, ne définit pas les indicateurs **SPI \_ SETSCREENREADER** ou **SPI \_ GETSCREENREADER** .

 

 

 