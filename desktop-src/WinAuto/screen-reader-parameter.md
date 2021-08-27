---
title: Paramètre de lecteur d’écran
description: Le paramètre de lecteur d’écran indique si une application doit fournir des informations textuelles dans les situations où elle présenterait autrement les informations sous forme graphique.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818ad36cfe833c1c9a3f39047cd88e6b4e8be55972d521ce524bb1e0618a48ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098419"
---
# <a name="screen-reader-parameter"></a>Paramètre de lecteur d’écran

Le paramètre de lecteur d’écran indique si une application doit fournir des informations textuelles dans les situations où elle présenterait autrement les informations sous forme graphique.

Ce paramètre est généralement défini par des aides à l’accessibilité, telles que les lecteurs d’écran. Les applications utilisent les indicateurs **SPI \_ GETSCREENREADER** et **SPI \_ SETSCREENREADER** avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour récupérer et définir le paramètre de lecteur d’écran.

> [!Note]  
> narrator, le lecteur d’écran inclus avec Windows, ne définit pas les indicateurs **spi \_ SETSCREENREADER** ou **spi \_ GETSCREENREADER** .

 

 

 