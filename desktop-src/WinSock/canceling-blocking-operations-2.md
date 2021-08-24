---
description: Un thread peut, à tout moment, appeler WSAIsBlocking pour déterminer si un appel bloquant est actuellement en cours.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Annulation des opérations bloquantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5064948fe7c1c1262acb9f4f8ef25a3ad3e721e77a188f313541595ef75f9ce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030689"
---
# <a name="canceling-blocking-operations"></a>Annulation des opérations bloquantes

Un thread peut, à tout moment, appeler [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) pour déterminer si un appel bloquant est actuellement en cours. (cette fonction est implémentée dans Windows les shims de compatibilité 1,1 sockets et n’a donc aucun équivalent SPI.) Cela est clairement possible uniquement lorsque le Pseudo-blocage, par opposition au blocage réel, est utilisé par le fournisseur de services. Si nécessaire, [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) peut être appelé à tout moment pour annuler une opération de Pseudo-blocage en cours.

 

 
