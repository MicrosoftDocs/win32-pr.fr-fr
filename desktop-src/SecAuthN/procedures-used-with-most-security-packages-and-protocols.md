---
description: Le modèle SSPI (Security Support Provider Interface) fournit une interface unique pour une application de transport client/serveur utilisant les différents packages de sécurité disponibles sur un ordinateur ou un réseau.
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: Procédures utilisées avec la plupart des packages de sécurité et des protocoles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 611ecbf7f2a124ea9352a71c7197d298f30a43391e3692303fcd3f7bc533cc4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920748"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a>Procédures utilisées avec la plupart des packages de sécurité et des protocoles

Le modèle SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) fournit une interface unique pour une application de transport client/serveur utilisant les différents [*packages de sécurité*](../secgloss/s-gly.md) disponibles sur un ordinateur ou un réseau. SSPI permet à une application d’utiliser un package de sécurité sans avoir à gérer les [*protocoles de sécurité*](../secgloss/s-gly.md) sous-jacents du package. En même temps, SSPI permet également aux applications sophistiquées orientées sécurité de tirer parti des fonctionnalités avancées des packages de sécurité spécifiques.

Les applications initialisent SSPI à l’aide des étapes suivantes pour sécuriser une connexion réseau pour la plupart des packages de sécurité :

-   [Utilisation de SecBufferDesc et SecBuffer](using-secbufferdesc-and-secbuffer.md)
-   [Initialisation de SSPI](initializing-sspi.md)
-   [Établissement d’une connexion sécurisée avec authentification](establishing-a-secure-connection-with-authentication.md)
-   [Garantir l’intégrité des communications pendant la Exchange des messages](ensuring-communication-integrity-during-message-exchange.md)
-   [Fin d’une session SSPI](ending-an-sspi-session.md)

 

 
