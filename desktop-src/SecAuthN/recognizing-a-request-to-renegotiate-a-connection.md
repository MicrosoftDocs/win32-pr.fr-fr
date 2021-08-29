---
description: La fonction DecryptMessage (général) intercepte les demandes de renégociation provenant de l’expéditeur du message. Il informe votre application en déchiffrant les données de message et en renvoyant la \_ valeur sec I \_ renégociée.
ms.assetid: 036a93dc-7f52-42f8-945d-7f654289ef63
title: Reconnaissance d’une demande de renégociation d’une connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 799ed36292b9542795036a697869a00176d7f068eebb6981edd28adbec2e0d5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919678"
---
# <a name="recognizing-a-request-to-renegotiate-a-connection"></a>Reconnaissance d’une demande de renégociation d’une connexion

La fonction [**DecryptMessage (général)**](decryptmessage--general.md) intercepte les demandes de renégociation provenant de l’expéditeur du message. Il informe votre application en déchiffrant les données de message et en renvoyant la \_ valeur sec I \_ renégociée.

Votre application doit gérer ces requêtes en appelant [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) (Servers) ou [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) (clients) et en transmettant le contenu de SECBUFFER_EXTRA retourné à partir de DecryptMessage dans le SECBUFFER_TOKEN. Après que cet appel initial a retourné une valeur, procédez comme si votre application était en train de créer une nouvelle connexion.

 

 



