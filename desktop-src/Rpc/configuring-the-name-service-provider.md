---
title: Configuration du fournisseur de services de noms
description: Si votre application distribuée inscrit son interface auprès d’un service de noms, le client et le serveur doivent tous les deux utiliser le même service de noms.
ms.assetid: a3f201e1-1a01-4794-9026-05e51a96afc0
keywords:
- Appel de procédure distante RPC, tâches, configuration du fournisseur de services de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7a44ec9a1c83eb7c37f10caae6ca3870679bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029190"
---
# <a name="configuring-the-name-service-provider"></a><span data-ttu-id="68e43-104">Configuration du fournisseur de services de noms</span><span class="sxs-lookup"><span data-stu-id="68e43-104">Configuring the Name Service Provider</span></span>

<span data-ttu-id="68e43-105">Si votre application distribuée inscrit son interface auprès d’un service de noms, le client et le serveur doivent tous les deux utiliser le même service de noms.</span><span class="sxs-lookup"><span data-stu-id="68e43-105">If your distributed application registers its interface with a name service, both the client and server must be using the same name service.</span></span> <span data-ttu-id="68e43-106">Microsoft RPC interagit avec Microsoft Locator et tout fournisseur de services de noms (NSP) conforme à l’interface NSI (Microsoft RPC Name Service Interface), par exemple, le DCE service d’annuaire de cellules/service d’annuaires de cellules accessible via le démon de service de nom (NSID) Digital Equipment Corporation.</span><span class="sxs-lookup"><span data-stu-id="68e43-106">Microsoft RPC interoperates with Microsoft Locator and any name service provider (NSP) that adheres to the Microsoft RPC name service interface (NSI)—for example, the DCE Cell Directory Service accessed through Digital Equipment Corporation's name service daemon (NSID).</span></span> <span data-ttu-id="68e43-107">Le localisateur Microsoft, qui est conçu pour une utilisation dans les environnements Windows, est le fournisseur de services de noms par défaut.</span><span class="sxs-lookup"><span data-stu-id="68e43-107">Microsoft Locator, which is designed for use in Windows environments, is the default name service provider.</span></span>

<span data-ttu-id="68e43-108">Cette section présente l’installation et la configuration des fournisseurs de services de noms :</span><span class="sxs-lookup"><span data-stu-id="68e43-108">This section presents a discussion of installing and configuring name service providers:</span></span>

-   [<span data-ttu-id="68e43-109">Configuration du service de noms</span><span class="sxs-lookup"><span data-stu-id="68e43-109">Configuring the Name Service</span></span>](configuring-the-name-service-for-windows-xp-windows-2000-or-windows-nt.md)
-   [<span data-ttu-id="68e43-110">Configuration du service de noms pour Windows 95</span><span class="sxs-lookup"><span data-stu-id="68e43-110">Configuring the Name Service for Windows 95</span></span>](configuring-the-name-service-for-windows-95.md)
-   [<span data-ttu-id="68e43-111">Configuration du service de noms pour Windows 3. x ou MS-DOS</span><span class="sxs-lookup"><span data-stu-id="68e43-111">Configuring the Name Service for Windows 3.x or MS-DOS</span></span>](configuring-the-name-service-for-windows-3-x-or-ms-dos.md)
-   [<span data-ttu-id="68e43-112">Démarrage et arrêt de Microsoft Locator</span><span class="sxs-lookup"><span data-stu-id="68e43-112">Starting and Stopping Microsoft Locator</span></span>](starting-and-stopping-microsoft-locator.md)

 

 




