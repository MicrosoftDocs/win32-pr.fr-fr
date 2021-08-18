---
description: Le \_32.dll Ws2 (et les protocoles en couches) appellera WSPCleanup une fois pour chaque appel de WSPStartup.
ms.assetid: c3b7b648-5727-47d6-9ddc-9d9f6511949d
title: Nettoyage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aefac8f58b7d6eed0380b7aa0e7759ff07e5af2a2762cde7d8e9bab445ca1fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741432"
---
# <a name="cleanup"></a>Nettoyage

Le \_32.dll Ws2 (et les protocoles en couches) appellera [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) une fois pour chaque appel de [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). À chaque appel, **WSPCleanup** doit décrémenter un compteur de référence par processus et, lorsque le compteur atteint zéro, le fournisseur de services doit se préparer à être déchargé de la mémoire. Le premier ordre d’activité consiste à terminer la transmission de toutes les données non envoyées sur les sockets configurés pour une fermeture normale. Ensuite, toutes les ressources détenues par le fournisseur doivent être libérées. Le fournisseur de services doit être laissé dans un État où il peut être immédiatement réinitialisé par un appel à **WSPStartup**.

 

 
