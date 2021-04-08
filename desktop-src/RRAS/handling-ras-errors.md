---
title: Gestion des erreurs RAS
description: Lorsqu’une erreur se produit, le gestionnaire de connexions d’accès à distance appelle le gestionnaire de notification du client.
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- RAS du service d’accès à distance, Erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f37c18a795f5675fc6df80da6027526f81a87010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674778"
---
# <a name="handling-ras-errors"></a><span data-ttu-id="8eaa2-104">Gestion des erreurs RAS</span><span class="sxs-lookup"><span data-stu-id="8eaa2-104">Handling RAS Errors</span></span>

<span data-ttu-id="8eaa2-105">Lorsqu’une erreur se produit, le gestionnaire de connexions d’accès à distance appelle le gestionnaire de notification du client.</span><span class="sxs-lookup"><span data-stu-id="8eaa2-105">When an error occurs, the Remote Access Connection Manager invokes the client's notification handler.</span></span> <span data-ttu-id="8eaa2-106">La notification indique l’état de la connexion lorsque l’erreur s’est produite, ainsi qu’un code qui identifie l’erreur.</span><span class="sxs-lookup"><span data-stu-id="8eaa2-106">The notification indicates the connection state when the error occurred, and a code that identifies the error.</span></span> <span data-ttu-id="8eaa2-107">Dans ce cas, le gestionnaire de notifications doit appeler [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) pour mettre fin à la connexion RAS.</span><span class="sxs-lookup"><span data-stu-id="8eaa2-107">In these cases, the notification handler should call [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) to end the RAS connection.</span></span>

<span data-ttu-id="8eaa2-108">Les codes d’erreur qui identifient les erreurs RAS sont définis dans le fichier raserror. h.</span><span class="sxs-lookup"><span data-stu-id="8eaa2-108">The error codes that identify RAS errors are defined in the file raserror.h.</span></span> <span data-ttu-id="8eaa2-109">Le client RAS peut utiliser la fonction [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) pour obtenir une chaîne d’affichage décrivant l’erreur.</span><span class="sxs-lookup"><span data-stu-id="8eaa2-109">The RAS client can use the [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) function to get a display string describing the error.</span></span> <span data-ttu-id="8eaa2-110">Pour obtenir une description de ces erreurs, consultez [codes d’erreur du routage et de l’accès à distance](routing-and-remote-access-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="8eaa2-110">See [Routing and Remote Access Error Codes](routing-and-remote-access-error-codes.md) for a description of these errors.</span></span>

 

 




