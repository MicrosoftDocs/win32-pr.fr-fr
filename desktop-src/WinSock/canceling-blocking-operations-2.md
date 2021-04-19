---
description: Un thread peut, à tout moment, appeler WSAIsBlocking pour déterminer si un appel bloquant est actuellement en cours.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Annulation des opérations bloquantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502870b8935dc97c1d6c3714808d1c6532780f7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536968"
---
# <a name="canceling-blocking-operations"></a>Annulation des opérations bloquantes

Un thread peut, à tout moment, appeler [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) pour déterminer si un appel bloquant est actuellement en cours. (Cette fonction est implémentée dans les shims de compatibilité Windows Sockets 1,1 et n’a donc aucun équivalent SPI.) Cela est clairement possible uniquement lorsque le Pseudo-blocage, par opposition au blocage réel, est utilisé par le fournisseur de services. Si nécessaire, [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) peut être appelé à tout moment pour annuler une opération de Pseudo-blocage en cours.

 

 
