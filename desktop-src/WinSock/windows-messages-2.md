---
description: Windows Sockets 1,1 a introduit le mécanisme Async-SELECT pour fournir des indications d’événements réseau qui n’impliquaient pas l’interrogation ou le blocage.
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Messages Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0f60bb597a7dd92c0039dd805a971bb8587ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524938"
---
# <a name="windows-messages"></a>Messages Windows

Windows Sockets 1,1 a introduit le mécanisme Async-SELECT pour fournir des indications d’événements réseau qui n’impliquaient pas l’interrogation ou le blocage. La fonction [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) est utilisée pour enregistrer un intérêt dans un ou plusieurs événements réseau, comme indiqué dans le précédent, et fournir un handle de fenêtre à utiliser pour la notification. Lorsqu’un événement réseau désigné se produit, un message Windows spécifié par le client est envoyé à la fenêtre indiquée. Pour ce faire, le fournisseur de services doit utiliser la fonction [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) .

Dans Windows, cela peut ne pas être le mécanisme de notification le plus efficace et il est peu commode pour les démons et les services qui ne souhaitent pas ouvrir de fenêtres. Le mécanisme de signalisation de l’objet d’événement décrit dans les éléments suivants est introduit pour résoudre ce problème.

 

 
