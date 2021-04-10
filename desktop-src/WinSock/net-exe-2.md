---
description: Net.exe peut être utilisé pour arrêter et démarrer le protocole IPv6.
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074696b71ce000ef330f2c88fceef0f60b0222e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862553"
---
# <a name="netexe"></a><span data-ttu-id="69e9a-103">Net.exe</span><span class="sxs-lookup"><span data-stu-id="69e9a-103">Net.exe</span></span>

<span data-ttu-id="69e9a-104">Net.exe peut être utilisé pour arrêter et démarrer le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="69e9a-104">Net.exe can be used to stop and start the IPv6 protocol.</span></span> <span data-ttu-id="69e9a-105">Le redémarrage D’ipv6 réinitialise le protocole comme si l’ordinateur redémarrait, ce qui peut modifier les numéros d’interface.</span><span class="sxs-lookup"><span data-stu-id="69e9a-105">Restarting IPv6 reinitializes the protocol as if the computer were restarting, which may change interface numbers.</span></span> <span data-ttu-id="69e9a-106">Net.exe possède de nombreuses sous-commandes.</span><span class="sxs-lookup"><span data-stu-id="69e9a-106">Net.exe has many subcommands.</span></span> <span data-ttu-id="69e9a-107">Les commandes suivantes s’appliquent à IPv6 :</span><span class="sxs-lookup"><span data-stu-id="69e9a-107">The following commands are relevant to IPv6:</span></span>

<dl> <dt>

<span data-ttu-id="69e9a-108"><span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop tcpip6**</span><span class="sxs-lookup"><span data-stu-id="69e9a-108"><span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop tcpip6**</span></span>
</dt> <dd>

<span data-ttu-id="69e9a-109">Arrête le protocole IPv6 et le décharge de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="69e9a-109">Stops the IPv6 protocol and unloads it from memory.</span></span> <span data-ttu-id="69e9a-110">Cette commande échoue si des sockets IPv6 sont ouverts.</span><span class="sxs-lookup"><span data-stu-id="69e9a-110">This command fails if any IPv6 sockets are open.</span></span>

</dd> <dt>

<span data-ttu-id="69e9a-111"><span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**NET START tcpip6**</span><span class="sxs-lookup"><span data-stu-id="69e9a-111"><span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start tcpip6**</span></span>
</dt> <dd>

<span data-ttu-id="69e9a-112">Démarre le protocole IPv6 s’il a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="69e9a-112">Starts the IPv6 protocol if it was stopped.</span></span> <span data-ttu-id="69e9a-113">Si un nouveau fichier de pilote de Tcpip6.sys est présent dans le répertoire% SystemRoot% \\ system32 \\ drivers, ce fichier de pilote est chargé.</span><span class="sxs-lookup"><span data-stu-id="69e9a-113">If a new Tcpip6.sys driver file is present in the %systemroot%\\System32\\Drivers directory, that driver file is loaded.</span></span>

</dd> </dl>

 

 



