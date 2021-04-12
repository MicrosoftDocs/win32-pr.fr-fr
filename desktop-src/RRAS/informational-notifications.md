---
title: Notifications d’information
description: Pour les États de connexion connus sous le nom d’état d’exécution, aucune action n’est requise du gestionnaire de notification à moins qu’une erreur ne se produise.
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6223c808309fcac3afc563f02c160412c80c88
ms.sourcegitcommit: dc13cc13522097188392392d85f99de48a213984
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2020
ms.locfileid: "104462786"
---
# <a name="informational-notifications"></a><span data-ttu-id="38964-103">Notifications d’information</span><span class="sxs-lookup"><span data-stu-id="38964-103">Informational Notifications</span></span>

<span data-ttu-id="38964-104">Pour les [États de connexion](connection-states.md) connus sous le nom d’état d’exécution, aucune action n’est requise du gestionnaire de notification à moins qu’une erreur ne se produise.</span><span class="sxs-lookup"><span data-stu-id="38964-104">For the [connection states](connection-states.md) known as running states, no action is required of the notification handler unless an error occurs.</span></span> <span data-ttu-id="38964-105">Les États en cours d’exécution se produisent pendant les parties de l’opération de connexion que RAS gère automatiquement, comme la connexion aux appareils nécessaires, l’authentification de l’utilisateur et l’attente d’un rappel du serveur distant.</span><span class="sxs-lookup"><span data-stu-id="38964-105">Running states occur during the parts of the connection operation that RAS handles automatically, such as connecting to the necessary devices, authenticating the user, and waiting for a callback from the remote server.</span></span> <span data-ttu-id="38964-106">La notification est simplement un rapport de progression vers le client.</span><span class="sxs-lookup"><span data-stu-id="38964-106">The notification is simply a progress report to the client.</span></span>

<span data-ttu-id="38964-107">Le client peut choisir de transmettre ces notifications d’information à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38964-107">The client can choose to pass these informational notifications on to the user.</span></span> <span data-ttu-id="38964-108">Dans certains États en cours d’exécution, le client peut souhaiter afficher des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="38964-108">In some running states, the client may want to display additional information.</span></span> <span data-ttu-id="38964-109">Par exemple, un gestionnaire de notification qui reçoit une \_ notification CONNECTDEVICE RASCS peut appeler la fonction [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) pour obtenir le nom et le type de l’appareil auquel la connexion est établie.</span><span class="sxs-lookup"><span data-stu-id="38964-109">For example, a notification handler that receives a RASCS\_ConnectDevice notification can call the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to get the name and type of the device being connected to.</span></span> <span data-ttu-id="38964-110">Un autre exemple est lorsque le client reçoit une \_ notification RASCS Projected.</span><span class="sxs-lookup"><span data-stu-id="38964-110">Another example is when the client receives a RASCS\_Projected notification.</span></span> <span data-ttu-id="38964-111">Cela se produit lorsque la phase de projection RAS de l’opération de connexion est terminée.</span><span class="sxs-lookup"><span data-stu-id="38964-111">This occurs when the RAS projection phase of the connection operation has been completed.</span></span> <span data-ttu-id="38964-112">Le client peut appeler la fonction [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) pour obtenir des informations supplémentaires sur la projection.</span><span class="sxs-lookup"><span data-stu-id="38964-112">The client can call the [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) function to get additional information about the projection.</span></span> <span data-ttu-id="38964-113">Le client peut utiliser ces informations pour indiquer à l’utilisateur les protocoles réseau qui peuvent être utilisés par cette connexion.</span><span class="sxs-lookup"><span data-stu-id="38964-113">The client can use this information to notify the user as to which network protocols can be used by this connection.</span></span>

<span data-ttu-id="38964-114">Vous devez éviter d’écrire du code qui dépend de l’ordre ou de l’occurrence d’États d’information particuliers, car cela peut varier d’une plateforme à l’autre.</span><span class="sxs-lookup"><span data-stu-id="38964-114">You should avoid writing code that depends on the order or occurrence of particular informational states, because this may vary between platforms.</span></span>

 

 




