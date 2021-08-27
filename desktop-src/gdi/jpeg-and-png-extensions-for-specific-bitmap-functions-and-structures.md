---
description: sur certaines versions de Microsoft Windows, les fonctions StretchDIBits et SetDIBitsToDevice permettent de transmettre des images JPEG et PNG en tant qu’image source aux périphériques d’impression.
ms.assetid: a38a807d-44df-40a2-8af7-0ce5e532cba2
title: Extensions JPEG et PNG pour des structures et des fonctions bitmap spécifiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd7dcd2713b737d86f90ab0d49fdf4eed1216f807a4debdffa1963e43a42a9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115289"
---
# <a name="jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures"></a>Extensions JPEG et PNG pour des structures et des fonctions bitmap spécifiques

sur certaines versions de Microsoft Windows, les fonctions [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) et [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) permettent de transmettre des images JPEG et PNG en tant qu’image source aux périphériques d’impression. Cette extension n’est pas conçue pour fournir une décompression JPEG et PNG générale aux applications, mais plutôt pour permettre aux applications d’envoyer des images JPEG et PNG compressées directement aux imprimantes ayant une prise en charge matérielle pour les images JPEG et PNG.

Les structures [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) et [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) sont étendues pour permettre la spécification de valeurs de **bicompression** indiquant que les données bitmap sont une image JPEG ou png. Ces valeurs de compression sont valides uniquement pour [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) et [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) lorsque le paramètre *HDC* spécifie un périphérique d’impression. Pour prendre en charge la mise en file d’attente de métafichiers de l’imprimante, l’application ne doit pas s’appuyer sur la valeur de retour pour déterminer si l’appareil prend en charge le fichier JPEG ou PNG. L’application doit émettre QUERYESCSUPPORT avec la séquence d’échappement correspondante avant d’appeler **SetDIBitsToDevice** et **StretchDIBits**. Si l’échappement de validation échoue, l’application doit ensuite revenir à sa propre prise en charge JPEG ou PNG pour décompresser l’image dans une image bitmap.

 

 
