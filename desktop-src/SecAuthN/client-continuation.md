---
description: Certains protocoles nécessitent plusieurs messages d’authentification.
ms.assetid: b4c4c38c-0286-49b1-b93d-4c6b885fe0f6
title: Continuation du client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca363489cf87a8fdf2743a8c26a7848c257212e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863870"
---
# <a name="client-continuation"></a><span data-ttu-id="078e6-103">Continuation du client</span><span class="sxs-lookup"><span data-stu-id="078e6-103">Client Continuation</span></span>

<span data-ttu-id="078e6-104">Certains protocoles nécessitent plusieurs messages d’authentification.</span><span class="sxs-lookup"><span data-stu-id="078e6-104">Some protocols require multiple authentication messages.</span></span> <span data-ttu-id="078e6-105">Dans ce cas, le client analyse la réponse du serveur et appelle [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) à nouveau à l’aide de l’état continue de l’appel précédent.</span><span class="sxs-lookup"><span data-stu-id="078e6-105">In this case, the client parses the response from the server and calls [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) again using the continue status from the previous call.</span></span> <span data-ttu-id="078e6-106">Le client vérifie l’état renvoyé à partir de cet appel et peut être amené à continuer pour les jambes supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="078e6-106">The client checks the return status from this call and might be required to continue for additional legs.</span></span> <span data-ttu-id="078e6-107">Elle utilise les informations de *pOutput* pour construire un message et l’envoyer au serveur.</span><span class="sxs-lookup"><span data-stu-id="078e6-107">It uses the information in *pOutput* to construct a message and sends it to the server.</span></span>

 

 
