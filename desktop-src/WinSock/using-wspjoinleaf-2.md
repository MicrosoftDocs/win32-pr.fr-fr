---
description: Comme mentionné précédemment, WSPJoinLeaf est utilisé pour joindre un nœud terminal dans une session multipoint.
ms.assetid: 03325f5e-4d4a-405b-b644-3d8c03435e17
title: Utilisation de WSPJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 057be0e2c1f2c3ffec21d64f3e95f6ad0ee584698e66f57cf4489ff6be887dc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121009"
---
# <a name="using-wspjoinleaf"></a>Utilisation de WSPJoinLeaf

Comme mentionné précédemment, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) est utilisé pour joindre un nœud terminal dans une session multipoint. **WSPJoinLeaf** a les mêmes paramètres et la même sémantique que [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) , sauf qu’il retourne un descripteur de socket (comme dans [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)) et qu’il a un paramètre *dwFlags* supplémentaire. Le paramètre *dwFlags* est utilisé pour indiquer si le socket doit agir uniquement comme un expéditeur, uniquement comme récepteur, ou les deux. Seuls les sockets multipoint peuvent être utilisés pour les *paramètres d'* entrée dans cette fonction. Si le socket multipoint est en mode non bloquant, le descripteur de socket retourné n’est pas utilisable tant qu’une indication FD Connect correspondante n' \_ a pas été reçue. Une application racine dans une session multipoint peut appeler **WSPJoinLeaf** une ou plusieurs fois pour ajouter un certain nombre de nœuds terminaux, mais au plus une demande de connexion multipoint peut être en suspens à la fois.

Le descripteur de socket retourné par [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) est différent selon que le descripteur de socket d’entrée, *s*, est une \_ racine c ou une \_ feuille c. Lorsqu’il est utilisé avec un \_ Socket racine c, le paramètre *Name* désigne un nœud terminal particulier à ajouter et le descripteur de socket retourné est un \_ Socket feuille c correspondant au nœud terminal qui vient d’être ajouté. Il n’est pas destiné à être utilisé pour l’échange de données multipoint, mais est plutôt utilisé pour recevoir des indications d’événements réseau (par exemple \_ , FD Close) pour la connexion qui existe à la feuille c particulière \_ . Certaines implémentations multipoint peuvent également permettre l’utilisation de ce Socket pour les conversations latérales entre la racine et un nœud terminal individuel. Une \_ indication FD Close doit être fournie pour ce Socket si le nœud terminal correspondant appelle [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) à supprimer de la session multipoint. En effet, l’appel de **WSPCloseSocket** sur le \_ Socket feuille c retourné par [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) amène le socket dans le nœud terminal correspondant à recevoir la \_ notification FD Close.

Quand [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) est appelé avec un \_ Socket feuille c, le paramètre *Name* contient l’adresse de l’application racine (pour un schéma de contrôle enraciné) ou une session multipoint existante (schéma de contrôle non enraciné) et le descripteur de socket retourné est le même que le descripteur de socket d’entrée. Dans un schéma de contrôle enraciné, le client racine place son \_ Socket racine c en mode d’écoute en appelant [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)). La notification d’acceptation FD standard est \_ remise lorsque le nœud terminal demande de se joindre à la session multipoint. Le client racine utilise la fonction [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) habituelle pour admettre le nouveau nœud terminal. La valeur retournée par **WSPAccept** est également un \_ descripteur de socket feuille c comme ceux retournés par **WSPJoinLeaf**. Pour prendre en charge les schémas multipoint qui autorisent les jointures lancées à la racine et initiées par les feuilles, il est acceptable pour un \_ Socket racine c qui est déjà en mode d’écoute d’être utilisé comme entrée dans **WSPJoinLeaf**.

Un client racine multipoint est généralement responsable du démontage ordonné d’une session multipoint. Une telle application peut utiliser [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) ou [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) sur un \_ Socket racine c pour provoquer tous les \_ sockets de feuille c associés, y compris ceux retournés à partir de [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) et leurs Sockets de feuille c correspondants \_ dans les nœuds terminaux distants, pour obtenir une \_ notification FD Close.

 

 
