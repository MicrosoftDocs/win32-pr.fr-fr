---
title: Configuration du service de noms pour Windows 3. x ou MS-DOS
description: Appel de procédure distante (RPC) et configuration du service de noms pour Windows 3. x ou MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533a0d8556f9cc51d0842768d0df1bdd0d553b5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029366"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a><span data-ttu-id="83ec3-103">Configuration du service de noms pour Windows 3. x ou MS-DOS</span><span class="sxs-lookup"><span data-stu-id="83ec3-103">Configuring the Name Service for Windows 3.x or MS-DOS</span></span>

<span data-ttu-id="83ec3-104">Lorsque vous exécutez Setup.exe pour installer la bibliothèque Runtime RPC 16 bits, vous êtes invité à sélectionner un fournisseur de services de noms :</span><span class="sxs-lookup"><span data-stu-id="83ec3-104">When you run Setup.exe to install the 16-bit RPC run-time library, it prompts you to select a name service provider:</span></span>

-   <span data-ttu-id="83ec3-105">Si vous choisissez **installer le fournisseur de services de noms par défaut**, le NSP par défaut, Microsoft Locator, est installé.</span><span class="sxs-lookup"><span data-stu-id="83ec3-105">If you choose **Install Default Name Service Provider**, the default NSP, Microsoft Locator, is installed.</span></span>
-   <span data-ttu-id="83ec3-106">Si vous choisissez **installer le fournisseur de services de noms personnalisés**, renseignez la boîte de dialogue **définir l’adresse réseau** pour installer le service d’annuaire de cellules/service d’annuaires de cellules DCE en tant que NSP.</span><span class="sxs-lookup"><span data-stu-id="83ec3-106">If you choose **Install Custom Name Service Provider**, complete the **Define Network Address** dialog box to install the DCE Cell Directory Service as your NSP.</span></span> <span data-ttu-id="83ec3-107">Le service d’annuaire de cellules/service d’annuaires de cellules DCE est le NSP utilisé avec les serveurs DCE.</span><span class="sxs-lookup"><span data-stu-id="83ec3-107">The DCE Cell Directory Service is the NSP used with DCE servers.</span></span>

<span data-ttu-id="83ec3-108">L’adresse réseau est le nom de l’ordinateur hôte qui exécute le démon NSI (NSID).</span><span class="sxs-lookup"><span data-stu-id="83ec3-108">The network address is the name of the host computer that runs the NSI daemon (nsid).</span></span> <span data-ttu-id="83ec3-109">Cet ordinateur joue le rôle de passerelle vers le service d’annuaire de cellules/service d’annuaires de cellules DCE, en passant les appels de fonction NSI entre les ordinateurs qui exécutent des systèmes d’exploitation Microsoft et des ordinateurs DCE.</span><span class="sxs-lookup"><span data-stu-id="83ec3-109">This computer acts as a gateway to the DCE Cell Directory Service, passing NSI function calls between computers that run Microsoft operating systems and DCE computers.</span></span> <span data-ttu-id="83ec3-110">L’adresse réseau peut comporter 80 caractères ou moins, par exemple, 11.1.9.169 est une adresse valide.</span><span class="sxs-lookup"><span data-stu-id="83ec3-110">The network address can be 80 characters or less—for example, 11.1.9.169 is a valid address.</span></span>

 

 




