---
description: Utilisation d’NSPStartup et de NSPCleanup pour l’initialisation et le nettoyage des fournisseurs d’espaces de noms dans le SPI Windows Sockets (Winsock).
ms.assetid: c9f55845-190d-440f-8b27-1be9585137e2
title: Initialisation et nettoyage du fournisseur d’espace de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fedd7b40d79e755262df581c92e1fe3bdbfb06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526139"
---
# <a name="namespace-provider-initialization-and-cleanup"></a><span data-ttu-id="c8ad7-103">Initialisation et nettoyage du fournisseur d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="c8ad7-103">Namespace Provider Initialization and Cleanup</span></span>

-   [<span data-ttu-id="c8ad7-104">**NSPStartup**</span><span class="sxs-lookup"><span data-stu-id="c8ad7-104">**NSPStartup**</span></span>](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)
-   [<span data-ttu-id="c8ad7-105">**NSPCleanup**</span><span class="sxs-lookup"><span data-stu-id="c8ad7-105">**NSPCleanup**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)

<span data-ttu-id="c8ad7-106">Comme c’est le cas pour le SPI de transport, un fournisseur d’espaces de noms est initialisé avec un appel à [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) et se termine par un appel final à [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup).</span><span class="sxs-lookup"><span data-stu-id="c8ad7-106">As is the case for the transport SPI, a namespace provider is initialized with a call to [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) and is terminated with a final call to [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup).</span></span> <span data-ttu-id="c8ad7-107">Les appels à la fonction Startup peuvent être imbriqués, mais seront mis en correspondance par les appels correspondants à la fonction Cleanup.</span><span class="sxs-lookup"><span data-stu-id="c8ad7-107">Calls to the startup function may be nested, but will be matched by corresponding calls to the cleanup function.</span></span> <span data-ttu-id="c8ad7-108">Un fournisseur doit utiliser le décompte de références pour déterminer à quel moment l’appel final à **NSPCleanup** s’est produit.</span><span class="sxs-lookup"><span data-stu-id="c8ad7-108">A provider should employ reference counting to determine when the final call to **NSPCleanup** has occurred.</span></span>

 

 



