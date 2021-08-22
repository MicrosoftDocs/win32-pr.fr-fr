---
description: Avant de pouvoir utiliser un socket pour configurer une connexion ou recevoir une demande de connexion, il faut qu’il soit lié à une adresse locale.
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: Liaison à une adresse locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd4691e6581cbe1a3a2dee21d7dc4e0a0672812121028c515ad192b30279f61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132752"
---
# <a name="binding-to-a-local-address"></a>Liaison à une adresse locale

Avant de pouvoir utiliser un socket pour configurer une connexion ou recevoir une demande de connexion, il faut qu’il soit lié à une adresse locale. Cela peut être fait explicitement en appelant [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)), ou implicitement par [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) si le socket est indépendant lorsque cette fonction est appelée.

 

 
