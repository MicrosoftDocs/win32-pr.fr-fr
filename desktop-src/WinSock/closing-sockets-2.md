---
description: WSPCloseSocket libère le descripteur de socket afin que toutes les opérations en attente dans les threads du même processus soient abandonnées, et toute autre référence à ce dernier échoue.
ms.assetid: 658d0c35-05d4-4b51-a4d3-a3b441a2c735
title: Fermeture de Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc35b7ba401e43494d49815e17eca19bd25b0080a385c40813209037c858a456
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051687"
---
# <a name="closing-sockets"></a>Fermeture de Sockets

[**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) libère le descripteur de socket afin que toutes les opérations en attente dans les threads du même processus soient abandonnées, et toute autre référence à ce dernier échoue. Notez qu’un décompte de références doit être utilisé pour les sockets partagés et seulement s’il s’agit de la dernière référence à un Socket sous-jacent, si les informations associées à ce Socket doivent être ignorées, à condition que la fermeture normale ne soit pas demandée (autrement dit, \_ DONTLINGER n’est pas défini). Dans le cas où \_ DONTLINGER est défini, toutes les données mises en file d’attente pour la transmission sont envoyées, si possible, avant la publication des informations associées au socket. Pour plus d’informations, consultez **WSPCloseSocket** .

pour les fournisseurs de services nonIFS, [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) doit être appelé pour libérer le handle de socket à la DLL Windows sockets 2.

 

 
