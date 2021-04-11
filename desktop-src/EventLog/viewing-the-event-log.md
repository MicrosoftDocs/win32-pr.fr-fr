---
description: Lorsque l’utilisateur démarre observateur d’événements pour afficher les entrées du journal des événements, il appelle la fonction ReadEventLog pour obtenir les structures EVENTLOGRECORD.
ms.assetid: 1d5b62cb-cf5b-4f4c-8521-1c783ae3afc7
title: Affichage du journal des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c566fef29cfb110883741ddc0e6c298d6a1255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202407"
---
# <a name="viewing-the-event-log"></a><span data-ttu-id="c8154-103">Affichage du journal des événements</span><span class="sxs-lookup"><span data-stu-id="c8154-103">Viewing the Event Log</span></span>

<span data-ttu-id="c8154-104">Lorsque l’utilisateur démarre observateur d’événements pour afficher les entrées du journal des événements, il appelle la fonction [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) pour obtenir les structures [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) .</span><span class="sxs-lookup"><span data-stu-id="c8154-104">When the user starts Event Viewer to view the event log entries, it calls the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function to obtain the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structures.</span></span> <span data-ttu-id="c8154-105">L’observateur d’événements utilise la source d’événements et l’identificateur d’événement pour obtenir le texte du message pour chaque événement à partir du fichier de message inscrit (indiqué par la valeur de Registre **EventMessageFile** pour la source).</span><span class="sxs-lookup"><span data-stu-id="c8154-105">The Event Viewer uses the event source and event identifier to get message text for each event from the registered message file (indicated by the **EventMessageFile** registry value for the source).</span></span> <span data-ttu-id="c8154-106">Le observateur d’événements utilise la fonction [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) pour charger le fichier de message.</span><span class="sxs-lookup"><span data-stu-id="c8154-106">The Event Viewer uses the [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) function to load the message file.</span></span> <span data-ttu-id="c8154-107">Le observateur d’événements utilise ensuite la fonction [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) pour récupérer la chaîne de description de base du module chargé.</span><span class="sxs-lookup"><span data-stu-id="c8154-107">The Event Viewer then uses the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function to retrieve the base description string from the loaded module.</span></span> <span data-ttu-id="c8154-108">Enfin, le observateur d’événements remplace les paramètres d’insertion dans la chaîne de description de base pour produire la chaîne de message finale.</span><span class="sxs-lookup"><span data-stu-id="c8154-108">Finally, the Event Viewer replaces the insertion parameters in the base description string to yield the final message string.</span></span>

 

 
