---
title: Résolution des problèmes de connexion Internet
description: Dans ce scénario, un utilisateur tente d’accéder à www.msn.com à l’aide du protocole HTTPS, mais il ne peut pas se connecter. Vous pouvez utiliser les commandes netsh et Moniteur réseau pour collecter et afficher les traces afin de déterminer la raison de l’échec de la connexion.
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753636c1186243a96e3cef5a4ab73244556daec4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839797"
---
# <a name="troubleshooting-internet-connections"></a><span data-ttu-id="11d8d-104">Résolution des problèmes de connexion Internet</span><span class="sxs-lookup"><span data-stu-id="11d8d-104">Troubleshooting Internet Connections</span></span>

<span data-ttu-id="11d8d-105">Dans ce scénario, un utilisateur tente d’accéder à www.msn.com à l’aide du protocole HTTPS, mais il ne peut pas se connecter.</span><span class="sxs-lookup"><span data-stu-id="11d8d-105">In this scenario, a user is attempting to browse to www.msn.com using the https protocol, but is unable to connect.</span></span> <span data-ttu-id="11d8d-106">Vous pouvez utiliser les commandes netsh et Moniteur réseau pour collecter et afficher les traces afin de déterminer la raison de l’échec de la connexion.</span><span class="sxs-lookup"><span data-stu-id="11d8d-106">You can use Netsh and Network Monitor to collect and view traces in order to help determine why the connection failed.</span></span>

<span data-ttu-id="11d8d-107">Tout d’abord, vous pouvez utiliser Netsh pour démarrer une trace.</span><span class="sxs-lookup"><span data-stu-id="11d8d-107">First, you can use netsh to start a trace.</span></span> <span data-ttu-id="11d8d-108">Tapez **netsh trace Start Scenario = internetclient tracefile = MSN. etl** démarre le suivi de tous les fournisseurs activés dans le cadre du scénario internetclient, en enregistrant les résultats dans un fichier nommé MSN. etl.</span><span class="sxs-lookup"><span data-stu-id="11d8d-108">Typing **netsh trace start scenario = InternetClient tracefile=msn.etl** starts tracing for all of the providers enabled under the InternetClient scenario, saving the results to a file named msn.etl.</span></span> <span data-ttu-id="11d8d-109">Après avoir utilisé un navigateur Web pour tenter d’atteindre www.msn.com, la saisie de **netsh trace stop** se termine et met en corrélation le fichier de trace.</span><span class="sxs-lookup"><span data-stu-id="11d8d-109">After using a web browser to attempt to reach www.msn.com, typing **netsh trace stop** terminates and correlates the trace file.</span></span>

<span data-ttu-id="11d8d-110">Vous pouvez ensuite ouvrir le fichier MSN. etl dans Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="11d8d-110">You can then open the msn.etl file in Network Monitor.</span></span> <span data-ttu-id="11d8d-111">Les événements sont regroupés par ID d’activité dans le volet gauche.</span><span class="sxs-lookup"><span data-stu-id="11d8d-111">The events are grouped by activity ID in the left pane.</span></span> <span data-ttu-id="11d8d-112">L’utilisation de la description de filtre **. Contains (« MSN »)** affiche uniquement les événements qui incluent la chaîne « MSN » dans leur description de protocole.</span><span class="sxs-lookup"><span data-stu-id="11d8d-112">Using the filter **description.contains("msn")** will show only those events which include the string "msn" in their protocol description.</span></span>

![résolution des problèmes de connexion Internet à l’aide du moniteur réseau (1)](images/internetclient1.png)

<span data-ttu-id="11d8d-114">Ensuite, vous pouvez examiner les événements dans le résumé des frames pour identifier un événement qui semble pertinent.</span><span class="sxs-lookup"><span data-stu-id="11d8d-114">Next, you can review the events in the frame summary to identify an event which looks relevant.</span></span> <span data-ttu-id="11d8d-115">Après avoir sélectionné l’événement, cliquez avec le bouton droit et pointez sur Rechercher des conversations, puis cliquez sur UTEvent pour sélectionner la conversation au niveau du UTEvent.</span><span class="sxs-lookup"><span data-stu-id="11d8d-115">After you select the event, right-click and point to Find Conversations, then click UTEvent to select the conversation at the UTEvent level.</span></span>

![résolution des problèmes de connexion Internet à l’aide du moniteur réseau (2)](images/internetclient2.png)

<span data-ttu-id="11d8d-117">L’activité normalisée associée dans le volet gauche est ensuite mise en surbrillance, dans ce cas UTEvent ActivityID 397.</span><span class="sxs-lookup"><span data-stu-id="11d8d-117">The associated normalized activity in the left pane is then highlighted, in this case UTEvent ActivityID 397.</span></span>

![résolution des problèmes de connexion Internet à l’aide du moniteur réseau (3)](images/internetclient3.png)

<span data-ttu-id="11d8d-119">En utilisant Moniteur réseau pour afficher et filtrer les informations de trace, le nombre d’événements à examiner a été réduit de 1989 à 96.</span><span class="sxs-lookup"><span data-stu-id="11d8d-119">By using Network Monitor to view and filter the trace information, the number of events to examine has been reduced from 1989 to 96.</span></span>

 

 




