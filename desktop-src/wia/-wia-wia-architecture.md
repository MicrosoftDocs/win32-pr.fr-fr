---
description: WIA est implémenté en tant que serveur hors processus COM (Component Object Model) pour garantir le bon fonctionnement des applications clientes.
ms.assetid: 9f3d1848-36ab-4e0f-a7f4-312bc85ecc00
title: Architecture WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09652258ee249fb3c68e65472e863ccd35154ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553841"
---
# <a name="wia-architecture"></a><span data-ttu-id="8aa03-103">Architecture WIA</span><span class="sxs-lookup"><span data-stu-id="8aa03-103">WIA Architecture</span></span>

<span data-ttu-id="8aa03-104">WIA est implémenté en tant que serveur hors processus COM (Component Object Model) pour garantir le bon fonctionnement des applications clientes.</span><span class="sxs-lookup"><span data-stu-id="8aa03-104">WIA is implemented as a Component Object Model (COM) out-of-process server to ensure the robust operation of client applications.</span></span> <span data-ttu-id="8aa03-105">Contrairement à la plupart des applications serveur de processus, l’acquisition d’images Windows (WIA) évite les pénalités de performances lors du transfert de données d’image en fournissant son propre mécanisme de transfert de données, [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="8aa03-105">Unlike most out of process server applications, Windows Image Acquisition (WIA) avoids performance penalties during image data transfer by providing its own data transfer mechanism, [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span> <span data-ttu-id="8aa03-106">Cette interface haute performance utilise une fenêtre de mémoire partagée pour transférer des données vers le client.</span><span class="sxs-lookup"><span data-stu-id="8aa03-106">This high performance interface uses a shared memory window to transfer data to the client.</span></span>

<span data-ttu-id="8aa03-107">WIA comporte trois composants principaux : un Gestionnaire de périphériques, une bibliothèque du service de minipilote et un minipilote d’appareil.</span><span class="sxs-lookup"><span data-stu-id="8aa03-107">WIA has three main components: a Device Manager, a Minidriver Service Library, and a Device Minidriver.</span></span>

-   <span data-ttu-id="8aa03-108">Le Gestionnaire de périphériques énumère les périphériques d’acquisition d’images, récupère les propriétés de l’appareil, configure les événements pour les appareils et crée des objets d’appareil.</span><span class="sxs-lookup"><span data-stu-id="8aa03-108">The Device Manager enumerates imaging devices, retrieves device properties, sets up events for devices, and creates device objects.</span></span>
-   <span data-ttu-id="8aa03-109">La bibliothèque du service de minipilote implémente tous les services indépendants de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8aa03-109">The Minidriver Service Library implements all services that are device independent.</span></span>
-   <span data-ttu-id="8aa03-110">Le minipilote d’appareil mappe les propriétés et les commandes WIA à l’appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="8aa03-110">The Device Minidriver maps WIA properties and commands to the specific device.</span></span>

<span data-ttu-id="8aa03-111">Le diagramme suivant illustre l’architecture WIA :</span><span class="sxs-lookup"><span data-stu-id="8aa03-111">The following diagram illustrates the WIA architecture:</span></span>

![architecture WIA](images/wiarch.gif)

 

 



