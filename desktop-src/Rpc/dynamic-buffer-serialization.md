---
title: Sérialisation de mémoire tampon dynamique
description: Lors de l’utilisation du style de mémoire tampon dynamique de la sérialisation, la mémoire tampon de marshaling est allouée par le stub, et les données sont encodées dans cette mémoire tampon et retournées. Lors du démarshaling, vous fournissez la mémoire tampon qui contient les données.
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c1b97124c502e48c4d3ba18e424770bc936496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462215"
---
# <a name="dynamic-buffer-serialization"></a>Sérialisation de mémoire tampon dynamique

Lors de l’utilisation du style de mémoire tampon dynamique de la sérialisation, la mémoire tampon de marshaling est allouée par le stub, et les données sont encodées dans cette mémoire tampon et retournées. Lors du démarshaling, vous fournissez la mémoire tampon qui contient les données.

Le style de mémoire tampon dynamique de la sérialisation utilise les routines suivantes :

-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

La fonction [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) alloue la mémoire nécessaire pour le handle d’encodage, puis l’initialise. L’application peut appeler [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) pour réinitialiser le descripteur. Elle appelle [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) pour libérer la mémoire du handle. Pour créer un descripteur de décodage correspondant au handle d’encodage de mémoire tampon dynamique, utilisez [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).

 

 




