---
title: Choix d’une séquence de protocole
description: Les meilleures pratiques pour le choix d’une séquence de protocole impliquent l’utilisation de ncacn \_ IP \_ TCP et Ncalrpc, et non ncacn \_ NP, ncacn \_ SPX et ncadg \_ \.
ms.assetid: 4b81b534-f001-4522-bf63-044bf5f414f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732e00d46f1b471870447e228935a794db8d5dc5aa6486e3296b9936cd1be7cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932222"
---
# <a name="choosing-a-protocol-sequence"></a>Choix d’une séquence de protocole

**Bonne pratique :** Utilisez [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) pour effectuer un appel distant. Utilisez [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) pour les appels locaux. N’utilisez pas [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), [**ncacn \_ SPX**](/windows/desktop/Midl/ncacn-spx)ou l’une des séquences de protocole **ncadg \_ \*** ; elles sont moins efficaces et ont des capacités inférieures.

 

 