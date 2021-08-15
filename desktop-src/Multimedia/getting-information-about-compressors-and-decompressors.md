---
title: Obtention d’informations sur les compresseurs et les décompresseurs
description: Obtention d’informations sur les compresseurs et les décompresseurs
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- Video Compression Manager (VCM), obtention d’informations sur les compresseurs
- VCM (Video Compression Manager), obtention d’informations sur les compresseurs
- ICGetInfo fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404b6acacd97b514edcf0328a8127f97152554015694eba3f8e5bf3b76214de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678610"
---
# <a name="getting-information-about-compressors-and-decompressors"></a>Obtention d’informations sur les compresseurs et les décompresseurs

Pour obtenir des informations générales sur un compresseur ou un décompresseur, votre application peut utiliser la fonction [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) . Cette fonction remplit une structure [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) avec des informations sur le compresseur ou le décompresseur. Votre application doit allouer la mémoire pour la structure **ICINFO** et lui passer un pointeur dans **ICGetInfo**. À moins que votre application ne recherche un compresseur ou décompresseur particulier, les indicateurs de la structure **ICINFO** fournissent les informations les plus utiles sur les fonctionnalités d’un compresseur ou d’un décompresseur.

pour obtenir la fréquence d’images clé par défaut et la valeur de qualité par défaut d’un compresseur ou d’un décompresseur, votre application peut envoyer les messages [**ICM \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) et [**ICM \_ GETDEFAULTQUALITY**](icm-getdefaultquality.md) (ou utiliser les macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) et [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) ).

Pour déterminer le meilleur format d’affichage d’un compresseur ou d’un décompresseur, votre application peut utiliser la fonction [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) .

pour déterminer si un compresseur ou un décompresseur peut afficher une boîte de dialogue à propos de, envoyez le [**ICM \_ à propos**](icm-about.md) du message (ou utilisez la macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) ). vous pouvez également afficher la boîte de dialogue à propos d’un compresseur ou d’un décompresseur en envoyant le ICM \_ à propos du message et en modifiant la valeur du paramètre *wParam* (ou à l’aide de la macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) ).

 

 




