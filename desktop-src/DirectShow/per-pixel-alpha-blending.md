---
description: Per-Pixel la fusion alpha
ms.assetid: 68661dc5-1423-47b2-a0df-858e5eb7f02b
title: Per-Pixel la fusion alpha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7e67084ae19df4a1aab81474dc8a9b1a313b9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515901"
---
# <a name="per-pixel-alpha-blending"></a>Per-Pixel la fusion alpha

Quatre sous-types de média ont été définis pour la fusion alpha par pixel. Ces sous-types sont pris en charge uniquement lorsque VMR est en mode de mixage. VMR rejette la connexion si elle n’est pas en mode de mixage lorsqu’un filtre en amont tente de se connecter à l’aide de l’un de ces sous-types. Ces sous-types sont définis dans UUID. h :

-   MEDIASUBTYPE \_ ARGB1555
-   MEDIASUBTYPE \_ ARGB4444
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ AYUV

Pour plus d’informations, consultez [sous-types de vidéo RVB non compressés](uncompressed-rgb-video-subtypes.md) et [**sous-types de vidéo YUV**](yuv-video-subtypes.md).

 

 



