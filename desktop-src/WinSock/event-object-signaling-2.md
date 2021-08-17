---
description: WSPEventSelect se comporte exactement comme WSPAsyncSelect, sauf que, au lieu de provoquer l’envoi d’un message Windows à l’occurrence d’un \_ événement réseau fd XXX nommé (par exemple, fd \_ READ, fd \_ WRITE, etc.), un objet d’événement désigné est défini.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Signalement d’objet d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eed237db696298a2f8053fb61cb0009d9d25d7f37497e0a19d58044d27d8dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132621"
---
# <a name="event-object-signaling"></a>Signalement d’objet d’événement

[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) se comporte exactement comme [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , sauf que, au lieu de provoquer l’envoi d’un message Windows à l’occurrence d’un \_ événement réseau fd XXX nommé (par exemple, fd \_ READ, fd \_ WRITE, etc.), un objet d’événement désigné est défini.

En outre, le fait qu’un événement réseau FD xxx particulier s’est \_ produit est mémorisé par le fournisseur de services. Cette opération est nécessaire, car l’occurrence de tout événement réseau désigné entraîne la signalisation d’un objet d’événement unique. Un appel à [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) entraîne la copie du contenu actuel de la mémoire d’événements réseau vers une mémoire tampon fournie par le client et la mémoire d’événements réseau à effacer. Le client peut également désigner un objet d’événement particulier à effacer de manière atomique en même temps que la mémoire de l’événement réseau.

 

 
