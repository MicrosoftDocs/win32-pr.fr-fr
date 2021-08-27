---
description: La destination par défaut peut être modifiée en rappelant simplement WSPConnect, même si le socket est déjà connecté. Les datagrammes mis en file d’attente pour la réception sont ignorés si la nouvelle adresse est différente de l’adresse spécifiée dans un WSPConnect précédent.
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: Reconnexion et déconnexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4c50872b6690c42d97c3696bcfcb2586b9b5b510c17aafc5dcc159b17ed56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121359"
---
# <a name="reconnecting-and-disconnecting"></a>Reconnexion et déconnexion

La destination par défaut peut être modifiée en rappelant simplement [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) , même si le socket est déjà connecté. Les datagrammes mis en file d’attente pour la réception sont ignorés si la nouvelle adresse est différente de l’adresse spécifiée dans un **WSPConnect** précédent.

Si l’adresse fournie pour le socket n’est que des zéros, le socket est déconnecté. l’adresse distante par défaut est indéterminée, de sorte que les appels [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) et [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) retournent le code d’erreur WSAENOTCONN, bien que [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) et [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) puissent toujours être utilisés.

 

 
