---
description: 'L’API graphique utilise les rappels suivants :'
ms.assetid: a8e083ab-b5e3-4186-99fb-cbb536e9d529
title: Rappels d’API de graphique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11f4f559307e457822cd0e7ce18ef4b44119697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034518"
---
# <a name="graphing-api-callbacks"></a><span data-ttu-id="4b93a-103">Rappels d’API de graphique</span><span class="sxs-lookup"><span data-stu-id="4b93a-103">Graphing API Callbacks</span></span>

<span data-ttu-id="4b93a-104">L’API graphique utilise les rappels suivants :</span><span class="sxs-lookup"><span data-stu-id="4b93a-104">The Graphing API uses the following callbacks:</span></span>



| <span data-ttu-id="4b93a-105">Rappel</span><span class="sxs-lookup"><span data-stu-id="4b93a-105">Callback</span></span>                                                          | <span data-ttu-id="4b93a-106">Description</span><span class="sxs-lookup"><span data-stu-id="4b93a-106">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b93a-107">*PFNPEER \_ les \_ données de sécurité gratuites \_*</span><span class="sxs-lookup"><span data-stu-id="4b93a-107">*PFNPEER\_FREE\_SECURITY\_DATA*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_free_security_data) | <span data-ttu-id="4b93a-108">Spécifie la fonction que l’infrastructure graphique des homologues appelle pour libérer les données retournées par [*PFNPEER \_ Secure \_ Record*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) et [*PFNPEER \_ valident \_*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) les rappels d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="4b93a-108">Specifies the function that the Peer Graphing Infrastructure calls to free data returned by [*PFNPEER\_SECURE\_RECORD*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) and [*PFNPEER\_VALIDATE\_RECORD*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) callbacks.</span></span> |
| [<span data-ttu-id="4b93a-109">*\_enregistrement sécurisé \_ PFNPEER*</span><span class="sxs-lookup"><span data-stu-id="4b93a-109">*PFNPEER\_SECURE\_RECORD*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record)            | <span data-ttu-id="4b93a-110">Spécifie la fonction que l’infrastructure graphique des homologues appelle pour sécuriser les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="4b93a-110">Specifies the function that the Peer Graphing Infrastructure calls to secure records.</span></span>                                                                                                                                        |
| [<span data-ttu-id="4b93a-111">*PFNPEER \_ valider l' \_ enregistrement*</span><span class="sxs-lookup"><span data-stu-id="4b93a-111">*PFNPEER\_VALIDATE\_RECORD*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record)        | <span data-ttu-id="4b93a-112">Spécifie la fonction que l’infrastructure graphique des homologues appelle pour valider les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="4b93a-112">Specifies the function that the Peer Graphing Infrastructure calls to validate records.</span></span>                                                                                                                                      |



 

 

 



