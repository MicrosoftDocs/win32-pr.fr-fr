---
description: Une fois qu’un pilote de périphérique a converti un fichier journal entier en commandes d’appareils brutes, le fichier de commandes converties est renvoyé au spouleur.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Moniteurs de port
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4b00e4171b3fd6e366a66deae8f5e70578ca92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536494"
---
# <a name="port-monitors"></a><span data-ttu-id="12d75-103">Moniteurs de port</span><span class="sxs-lookup"><span data-stu-id="12d75-103">Port Monitors</span></span>

<span data-ttu-id="12d75-104">Une fois qu’un pilote de périphérique a converti un fichier journal entier en commandes d’appareils brutes, le fichier de commandes converties est renvoyé au spouleur.</span><span class="sxs-lookup"><span data-stu-id="12d75-104">Once a device driver has converted an entire journal file into raw device commands, the file of converted commands is passed back to the spooler.</span></span> <span data-ttu-id="12d75-105">Le spouleur envoie ces commandes de bas niveau à une analyse.</span><span class="sxs-lookup"><span data-stu-id="12d75-105">The spooler sends these low-level commands to a monitor.</span></span> <span data-ttu-id="12d75-106">Un moniteur de port est un fichier. dll qui transmet les commandes d’appareil brutes sur le réseau, via un port parallèle ou via un port série à l’appareil de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="12d75-106">A port monitor is a .dll that passes the raw device commands over the network, through a parallel port, or through a serial port to the printer device.</span></span> <span data-ttu-id="12d75-107">Des moniteurs de port personnalisés peuvent être installés pour prendre en charge le passage des données de l’appareil via d’autres ports de communication.</span><span class="sxs-lookup"><span data-stu-id="12d75-107">Custom port monitors can be installed to support passing device data through other communication ports.</span></span>

<span data-ttu-id="12d75-108">Utilisez les fonctions suivantes pour travailler avec les moniteurs de port.</span><span class="sxs-lookup"><span data-stu-id="12d75-108">Use the following functions to work with port monitors.</span></span>



| <span data-ttu-id="12d75-109">Fonction</span><span class="sxs-lookup"><span data-stu-id="12d75-109">Function</span></span>                               | <span data-ttu-id="12d75-110">Description</span><span class="sxs-lookup"><span data-stu-id="12d75-110">Description</span></span>                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="12d75-111">**AddMonitor**</span><span class="sxs-lookup"><span data-stu-id="12d75-111">**AddMonitor**</span></span>](addmonitor.md)       | <span data-ttu-id="12d75-112">Installe un moniteur de port local et relie les fichiers de configuration, de données et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="12d75-112">Installs a local port monitor and links the configuration, data, and monitor files.</span></span> |
| [<span data-ttu-id="12d75-113">**DeleteMonitor**</span><span class="sxs-lookup"><span data-stu-id="12d75-113">**DeleteMonitor**</span></span>](deletemonitor.md) | <span data-ttu-id="12d75-114">Supprime un moniteur de port ajouté par la fonction [**AddMonitor**](addmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="12d75-114">Removes a port monitor added by the [**AddMonitor**](addmonitor.md) function.</span></span>      |
| [<span data-ttu-id="12d75-115">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="12d75-115">**EnumMonitors**</span></span>](enummonitors.md)   | <span data-ttu-id="12d75-116">Énumère les moniteurs de port installés sur un serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="12d75-116">Enumerates the port monitors installed on a specified server.</span></span>                       |



 

 

 



