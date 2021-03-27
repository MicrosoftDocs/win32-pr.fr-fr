---
description: Une application peut convertir un chemin d’accès en région en appelant la fonction PathToRegion.
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: Conversion de chemins d’accès en régions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3a576f04035f6e29bb37a23de956322639daf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754476"
---
# <a name="conversion-of-paths-to-regions"></a>Conversion de chemins d’accès en régions

Une application peut convertir un chemin d’accès en région en appelant la fonction [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) . Comme [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath), **PathToRegion** est utile lors de la création d’effets graphiques spéciaux. Par exemple, il n’existe aucune fonction permettant à une application de compenser un chemin d’accès ; Toutefois, il existe une fonction qui permet à une application de décaler une région ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)). À l’aide de **PathToRegion** , une application peut créer l’effet de l’animation d’une forme complexe en créant un tracé qui définit la forme, en convertissant le tracé en une région (en appelant **PathToRegion**), puis en dessinant, en déplaçant et en effaçant à plusieurs reprises la région (en appelant des fonctions dans une séquence, telles que [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **OffsetRgn** et **FillRgn**).

 

 



