---
description: utilisation d’NSPStartup et de NSPCleanup pour l’initialisation et le nettoyage des fournisseurs d’espaces de noms dans le SPI Winsock (Windows sockets).
ms.assetid: c9f55845-190d-440f-8b27-1be9585137e2
title: Initialisation et nettoyage du fournisseur d’espace de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4007533bb1456268ee3a1110da4681a7041a56ed80c0d9a522790c8a0c9a94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612979"
---
# <a name="namespace-provider-initialization-and-cleanup"></a>Initialisation et nettoyage du fournisseur d’espace de noms

-   [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)
-   [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)

Comme c’est le cas pour le SPI de transport, un fournisseur d’espaces de noms est initialisé avec un appel à [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) et se termine par un appel final à [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup). Les appels à la fonction Startup peuvent être imbriqués, mais seront mis en correspondance par les appels correspondants à la fonction Cleanup. Un fournisseur doit utiliser le décompte de références pour déterminer à quel moment l’appel final à **NSPCleanup** s’est produit.

 

 



