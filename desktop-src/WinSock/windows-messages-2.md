---
description: Windows Les sockets 1,1 ont introduit le mécanisme Async-SELECT pour fournir des indications d’événements réseau qui n’impliquent pas l’interrogation ou le blocage.
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Windows Messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bab33ecb4d2898c8f1e363ab19ad425503e9d005bf24229a29f581aadf1788f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993209"
---
# <a name="windows-messages"></a>Windows Messages

Windows Les sockets 1,1 ont introduit le mécanisme Async-SELECT pour fournir des indications d’événements réseau qui n’impliquent pas l’interrogation ou le blocage. La fonction [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) est utilisée pour enregistrer un intérêt dans un ou plusieurs événements réseau, comme indiqué dans le précédent, et fournir un handle de fenêtre à utiliser pour la notification. lorsqu’un événement réseau désigné se produit, un message Windows spécifié par le client est envoyé à la fenêtre indiquée. Pour ce faire, le fournisseur de services doit utiliser la fonction [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) .

dans Windows, il est possible qu’il ne s’agit pas du mécanisme de notification le plus efficace et qu’il ne soit pas pratique pour les démons et les services qui ne souhaitent pas ouvrir de fenêtres. Le mécanisme de signalisation de l’objet d’événement décrit dans les éléments suivants est introduit pour résoudre ce problème.

 

 
