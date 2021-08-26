---
description: la gestion des couleurs des images Microsoft (ICM) garantit qu’une image de couleur, un graphique ou un objet texte est rendu aussi fidèlement que possible à son intention d’origine sur n’importe quel appareil, en dépit des différences entre les technologies d’imagerie et les capacités de couleur entre les appareils.
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: ICM-Enabled les fonctions de contexte de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33337aeea32f1ca84b74e3fc45e9bd67dbfe1ce1a5300a502a5303f55cab357
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944199"
---
# <a name="icm-enabled-device-context-functions"></a>ICM-Enabled les fonctions de contexte de périphérique

la gestion des couleurs des images Microsoft (ICM) garantit qu’une image de couleur, un graphique ou un objet texte est rendu aussi fidèlement que possible à son intention d’origine sur n’importe quel appareil, en dépit des différences entre les technologies d’imagerie et les capacités de couleur entre les appareils. (pour plus d’informations, consultez [Windows système de couleurs](/previous-versions//dd372446(v=vs.85)).)

Il existe différentes fonctions dans l’interface GDI (Graphics Device Interface) qui utilisent ou opèrent sur les données de couleur. Les fonctions de contexte de périphérique suivantes sont activées pour une utilisation avec ICM :

-   [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [**SélectionnerObjet**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
