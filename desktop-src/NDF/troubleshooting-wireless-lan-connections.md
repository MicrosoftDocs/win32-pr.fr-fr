---
title: Résolution des problèmes de connexion LAN sans fil
description: Dans ce scénario, un utilisateur tente de se connecter à un réseau local sans fil, mais il n’est pas en mesure de se connecter. Vous pouvez utiliser les commandes netsh et Moniteur réseau pour collecter et afficher les traces afin de déterminer la raison de l’échec de la connexion.
ms.assetid: 558dae83-aa16-4751-a497-d7a0da01ce5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55878afcee0091634415d4dbc465d1b143f46057
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029683"
---
# <a name="troubleshooting-wireless-lan-connections"></a><span data-ttu-id="06e7a-104">Résolution des problèmes de connexion LAN sans fil</span><span class="sxs-lookup"><span data-stu-id="06e7a-104">Troubleshooting Wireless LAN Connections</span></span>

<span data-ttu-id="06e7a-105">Dans ce scénario, un utilisateur tente de se connecter à un réseau local sans fil, mais il n’est pas en mesure de se connecter.</span><span class="sxs-lookup"><span data-stu-id="06e7a-105">In this scenario, a user is attempting to connect to a wireless LAN, but is unable to connect.</span></span> <span data-ttu-id="06e7a-106">Vous pouvez utiliser les commandes netsh et Moniteur réseau pour collecter et afficher les traces afin de déterminer la raison de l’échec de la connexion.</span><span class="sxs-lookup"><span data-stu-id="06e7a-106">You can use Netsh and Network Monitor to collect and view traces in order to help determine why the connection failed.</span></span>

<span data-ttu-id="06e7a-107">Tout d’abord, vous pouvez utiliser Netsh pour démarrer une trace.</span><span class="sxs-lookup"><span data-stu-id="06e7a-107">First, you can use netsh to start a trace.</span></span> <span data-ttu-id="06e7a-108">Le fait de taper **netsh trace Start scénario = WLAN tracefile = wlanwpp. etl** démarre le suivi de tous les fournisseurs activés dans le cadre du scénario de réseau local sans fil, en enregistrant les résultats dans un fichier nommé wlanwpp. etl.</span><span class="sxs-lookup"><span data-stu-id="06e7a-108">Typing **netsh trace start scenario = wlan tracefile=wlanwpp.etl** starts tracing for all of the providers enabled under the WLAN scenario, saving the results to a file named wlanwpp.etl.</span></span> <span data-ttu-id="06e7a-109">Après une tentative de connexion au réseau local sans fil, la saisie de **netsh trace stop** se termine et met en corrélation le fichier de trace.</span><span class="sxs-lookup"><span data-stu-id="06e7a-109">After attempting to connect to the wireless LAN, typing **netsh trace stop** terminates and correlates the trace file.</span></span>

<span data-ttu-id="06e7a-110">Vous pouvez ensuite ouvrir le fichier wlanwpp. etl dans Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="06e7a-110">You can then open the wlanwpp.etl file in Network Monitor.</span></span> <span data-ttu-id="06e7a-111">Les événements sont regroupés par ID d’activité dans le volet gauche.</span><span class="sxs-lookup"><span data-stu-id="06e7a-111">The events are grouped by activity ID in the left pane.</span></span>

![résolution des problèmes de connexion de réseau local sans fil à l’aide du moniteur réseau (1)](images/1wlan.png)

<span data-ttu-id="06e7a-113">L’ETL contient de nombreux suivis provenant d’autres fournisseurs de réseau qui sont activés.</span><span class="sxs-lookup"><span data-stu-id="06e7a-113">The ETL contains lot of traces from other network providers that are enabled.</span></span> <span data-ttu-id="06e7a-114">Vous pouvez appliquer un filtre pour afficher uniquement les événements pertinents pour le fournisseur **\_ MicrosoftWindowsWlanAutoConfig WLAN** .</span><span class="sxs-lookup"><span data-stu-id="06e7a-114">You can apply a filter to display only those events which are relevant to the **WLAN\_MicrosoftWindowsWlanAutoConfig** provider.</span></span>

![résolution des problèmes de connexion de réseau local sans fil à l’aide du moniteur réseau (2)](images/2wlan.png)

<span data-ttu-id="06e7a-116">Une fois le filtre appliqué, vous pouvez examiner les événements dans le résumé des frames pour identifier un événement qui semble pertinent.</span><span class="sxs-lookup"><span data-stu-id="06e7a-116">After the filter has been applied, you can review the events in the frame summary to identify an event which looks relevant.</span></span> <span data-ttu-id="06e7a-117">Après avoir sélectionné l’événement, cliquez avec le bouton droit et pointez sur Rechercher des conversations, puis cliquez sur netpair.</span><span class="sxs-lookup"><span data-stu-id="06e7a-117">After you select the event, right-click and point to Find Conversations, then click NetEvent.</span></span>

![résolution des problèmes de connexion de réseau local sans fil à l’aide du moniteur réseau (3)](images/3wlan.png)

<span data-ttu-id="06e7a-119">Le développement des éléments sous un ID d’activité dans le volet gauche vous permet d’afficher tous les autres fournisseurs pertinents pour la tentative de connexion.</span><span class="sxs-lookup"><span data-stu-id="06e7a-119">Expanding the items under an activity ID in the left pane will allow you to view all of the other relevant providers for the connection attempt.</span></span> <span data-ttu-id="06e7a-120">Pour afficher les événements d’autres fournisseurs, tous les filtres sont supprimés en cliquant sur **supprimer** dans le volet **filtre d’affichage** .</span><span class="sxs-lookup"><span data-stu-id="06e7a-120">To view the events from other providers, all filters are removed by clicking **Remove** in the **Display Filter** pane.</span></span> <span data-ttu-id="06e7a-121">Les suivis peuvent être analysés en faisant défiler le résumé des frames, en sélectionnant des événements supplémentaires, le cas échéant, pour obtenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="06e7a-121">The traces can be analyzed by scrolling through the frame summary, selecting additional events as needed to gather more information.</span></span> <span data-ttu-id="06e7a-122">Dans ce cas, le volet Détails du cadre fournit des informations indiquant que l’échec est dû à une défaillance de l’échange de clés, ce qui est probablement dû au fait que l’utilisateur a entré une clé de passe incorrecte.</span><span class="sxs-lookup"><span data-stu-id="06e7a-122">In this case, the Frame Details pane provides information that the failure is due to key exchange failure, most likely due to the user entering the wrong pass key.</span></span>

 

 




