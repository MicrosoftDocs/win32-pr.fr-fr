---
description: La fonction DecryptMessage (général) intercepte les demandes de renégociation provenant de l’expéditeur du message. Il informe votre application en déchiffrant les données de message et en renvoyant la \_ valeur sec I \_ renégociée.
ms.assetid: 036a93dc-7f52-42f8-945d-7f654289ef63
title: Reconnaissance d’une demande de renégociation d’une connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8ae8083c59485b8b7c917fe03893fa363f5a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034474"
---
# <a name="recognizing-a-request-to-renegotiate-a-connection"></a>Reconnaissance d’une demande de renégociation d’une connexion

La fonction [**DecryptMessage (général)**](decryptmessage--general.md) intercepte les demandes de renégociation provenant de l’expéditeur du message. Il informe votre application en déchiffrant les données de message et en renvoyant la \_ valeur sec I \_ renégociée.

Votre application doit gérer ces requêtes en appelant [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) (Servers) ou [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) (clients) et en transmettant le contenu de SECBUFFER_EXTRA retourné à partir de DecryptMessage dans le SECBUFFER_TOKEN. Après que cet appel initial a retourné une valeur, procédez comme si votre application était en train de créer une nouvelle connexion.

 

 



