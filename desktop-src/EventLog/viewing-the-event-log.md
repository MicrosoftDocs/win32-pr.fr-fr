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
# <a name="viewing-the-event-log"></a>Affichage du journal des événements

Lorsque l’utilisateur démarre observateur d’événements pour afficher les entrées du journal des événements, il appelle la fonction [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) pour obtenir les structures [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) . L’observateur d’événements utilise la source d’événements et l’identificateur d’événement pour obtenir le texte du message pour chaque événement à partir du fichier de message inscrit (indiqué par la valeur de Registre **EventMessageFile** pour la source). Le observateur d’événements utilise la fonction [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) pour charger le fichier de message. Le observateur d’événements utilise ensuite la fonction [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) pour récupérer la chaîne de description de base du module chargé. Enfin, le observateur d’événements remplace les paramètres d’insertion dans la chaîne de description de base pour produire la chaîne de message finale.

 

 
