---
description: La gestion des couleurs ICM (Microsoft Image Color Management) garantit qu’une image de couleur, un graphique ou un objet texte est rendu le plus près possible de son intention d’origine sur n’importe quel appareil, en dépit des différences entre les technologies d’imagerie et les capacités de couleur entre les appareils.
ms.assetid: 55452048-aacd-4772-9345-3efcf0350ce6
title: ICM-Enabled les fonctions de stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ec35b11a46646a6f7588443ac7a66aee23aae10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528329"
---
# <a name="icm-enabled-pen-functions"></a>ICM-Enabled les fonctions de stylet

La gestion des couleurs ICM (Microsoft Image Color Management) garantit qu’une image de couleur, un graphique ou un objet texte est rendu le plus près possible de son intention d’origine sur n’importe quel appareil, en dépit des différences entre les technologies d’imagerie et les capacités de couleur entre les appareils. Que vous scanniez une image ou un autre graphique sur un scanneur de couleurs, que vous la téléchargeiez sur Internet, que vous la visualisiez ou la modifiiez à l’écran, que vous la déformiez sur du papier, sur un film ou sur un autre média, ICM version 2,0 vous aide à conserver les couleurs cohérentes et précises. Pour plus d’informations sur ICM, consultez [système de couleurs Windows](/previous-versions//dd372446(v=vs.85))

Il existe différentes fonctions dans l’interface GDI (Graphics Device Interface) qui utilisent ou opèrent sur les données de couleur. Les fonctions de stylet suivantes sont activées pour une utilisation avec ICM :

-   [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen)
-   [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen)

 

 
