---
description: WSPEventSelect se comporte exactement comme WSPAsyncSelect, sauf que, au lieu de provoquer l’envoi d’un message Windows à l’occurrence d’un \_ événement réseau FD xxx nommé (par exemple, FD \_ Read, FD \_ Write, etc.), un objet d’événement désigné est défini.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Signalement d’objet d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42854a1f4e116c8dba100025007362898d183f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544660"
---
# <a name="event-object-signaling"></a>Signalement d’objet d’événement

[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) se comporte exactement comme [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , sauf que, au lieu de provoquer l’envoi d’un message Windows à l’occurrence d’un \_ événement réseau FD xxx nommé (par exemple, FD \_ Read, FD \_ Write, etc.), un objet d’événement désigné est défini.

En outre, le fait qu’un événement réseau FD xxx particulier s’est \_ produit est mémorisé par le fournisseur de services. Cette opération est nécessaire, car l’occurrence de tout événement réseau désigné entraîne la signalisation d’un objet d’événement unique. Un appel à [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) entraîne la copie du contenu actuel de la mémoire d’événements réseau vers une mémoire tampon fournie par le client et la mémoire d’événements réseau à effacer. Le client peut également désigner un objet d’événement particulier à effacer de manière atomique en même temps que la mémoire de l’événement réseau.

 

 
