---
description: Si un socket est en mode non bloquant, toute opération d’e/s doit être terminée immédiatement ou renvoyer le code d’erreur WSAEWOULDBLOCK indiquant que l’opération ne peut pas être terminée immédiatement.
ms.assetid: badd279b-ec71-4761-9066-d501aa2485c2
title: Entrée/sortie non bloquantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9f6fec896c8daf1998e71a20a23a296b7b5a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526128"
---
# <a name="nonblocking-inputoutput"></a>Entrée/sortie non bloquantes

Si un socket est en mode non bloquant, toute opération d’e/s doit être terminée immédiatement ou renvoyer le code d’erreur WSAEWOULDBLOCK indiquant que l’opération ne peut pas être terminée immédiatement. Dans ce dernier cas, un mécanisme est nécessaire pour déterminer s’il est approprié de retenter l’opération dans l’attente que l’opération aboutisse. Un ensemble d’événements réseau a été défini à cet effet. Ces événements peuvent être interrogés ou attendus à l’aide de [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)), ou ils peuvent être inscrits pour la remise asynchrone en appelant [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) ou [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). Pour plus d’informations, consultez [notification des événements réseau](notification-of-network-events-2.md) .

 

 
