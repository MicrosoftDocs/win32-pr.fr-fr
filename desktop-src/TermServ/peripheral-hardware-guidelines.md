---
title: Instructions relatives au matériel périphérique
description: Si leur périphérique matériel n’est pas conçu pour fonctionner sur une session à distance, les fournisseurs doivent s’assurer que le logiciel du pilote de périphérique force la désactivation de la redirection de l’appareil à l’aide d’une stratégie système ou d’une stratégie de groupe.
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8e8e6a81a75abdef76851fedcb979526e1653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380182"
---
# <a name="peripheral-hardware-guidelines"></a><span data-ttu-id="8e56b-103">Instructions relatives au matériel périphérique</span><span class="sxs-lookup"><span data-stu-id="8e56b-103">Peripheral hardware guidelines</span></span>

<span data-ttu-id="8e56b-104">Sur un client Connexion Bureau à distance (RDC), le serveur hôte de session Bureau à distance (hôte de session Bureau à distance) est l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8e56b-104">To a Remote Desktop Connection (RDC) client, the Remote Desktop Session Host (RD Session Host) server is the local computer.</span></span> <span data-ttu-id="8e56b-105">Par conséquent, les périphériques tels que les lecteurs de disque et les imprimantes attachées au serveur apparaissent en tant qu’appareils locaux sur un client.</span><span class="sxs-lookup"><span data-stu-id="8e56b-105">Consequently, devices such as disk drives and printers attached to the server appear as local devices to a client.</span></span> <span data-ttu-id="8e56b-106">En revanche, les lecteurs et imprimantes connectés à un terminal client peuvent apparaître comme des périphériques distants, selon les options sélectionnées pour la connexion, le serveur utilisé et la version du logiciel client utilisée.</span><span class="sxs-lookup"><span data-stu-id="8e56b-106">In contrast, drives and printers attached to a client terminal can appear to be remote devices, depending on the options selected for the connection, the server used, and the version of the client software used.</span></span>

<span data-ttu-id="8e56b-107">Tandis que la version initiale de Services Bureau à distance ne prenait pas en charge les applications qui envoient des sorties directement aux ports série, parallèle et audio attachés au terminal client, les versions actuelles autorisent ces appareils à apparaître en tant qu’appareils locaux pour les applications qui s’exécutent dans la session de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="8e56b-107">While the initial release of Remote Desktop Services did not support applications that send output directly to serial, parallel, and sound ports attached to the client terminal, the current versions do allow these devices to appear as local devices to applications running in the Remote Desktop Services session.</span></span>

<span data-ttu-id="8e56b-108">Si leur périphérique matériel n’est pas conçu pour fonctionner sur une session à distance, les fournisseurs doivent s’assurer que le logiciel du pilote de périphérique force la désactivation de la redirection de l’appareil à l’aide d’une stratégie système ou d’une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8e56b-108">If their hardware device is not designed to work over a remote session, vendors must ensure that the device driver software forces disabling the redirection of the device by using a system policy or group policy.</span></span>

 

 




