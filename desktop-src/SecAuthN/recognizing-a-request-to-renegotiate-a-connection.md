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
# <a name="recognizing-a-request-to-renegotiate-a-connection"></a><span data-ttu-id="4954b-104">Reconnaissance d’une demande de renégociation d’une connexion</span><span class="sxs-lookup"><span data-stu-id="4954b-104">Recognizing a Request to Renegotiate a Connection</span></span>

<span data-ttu-id="4954b-105">La fonction [**DecryptMessage (général)**](decryptmessage--general.md) intercepte les demandes de renégociation provenant de l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="4954b-105">The [**DecryptMessage (General)**](decryptmessage--general.md) function traps requests for renegotiation coming from the message sender.</span></span> <span data-ttu-id="4954b-106">Il informe votre application en déchiffrant les données de message et en renvoyant la \_ valeur sec I \_ renégociée.</span><span class="sxs-lookup"><span data-stu-id="4954b-106">It notifies your application by decrypting the message data and returning the SEC\_I\_RENEGOTIATE value.</span></span>

<span data-ttu-id="4954b-107">Votre application doit gérer ces requêtes en appelant [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) (Servers) ou [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) (clients) et en transmettant le contenu de SECBUFFER_EXTRA retourné à partir de DecryptMessage dans le SECBUFFER_TOKEN.</span><span class="sxs-lookup"><span data-stu-id="4954b-107">Your application must handle such requests by calling [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) (servers) or [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) (clients) and passing the contents of SECBUFFER_EXTRA returned from DecryptMessage in the SECBUFFER_TOKEN.</span></span> <span data-ttu-id="4954b-108">Après que cet appel initial a retourné une valeur, procédez comme si votre application était en train de créer une nouvelle connexion.</span><span class="sxs-lookup"><span data-stu-id="4954b-108">After this initial call returns a value, proceed as though your application were creating a new connection.</span></span>

 

 



