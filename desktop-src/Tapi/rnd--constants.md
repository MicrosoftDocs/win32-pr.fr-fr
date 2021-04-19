---
description: Les constantes suivantes peuvent être retournées en tant qu’erreurs.
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: Constantes RND_ (Rnderr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a89b6747fb9fef775bbf40fac472081567ff1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544087"
---
# <a name="rnd_-constants"></a><span data-ttu-id="017e1-103">RND, \_ constantes</span><span class="sxs-lookup"><span data-stu-id="017e1-103">RND\_ Constants</span></span>

<span data-ttu-id="017e1-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="017e1-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="017e1-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="017e1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="017e1-106">Les constantes suivantes peuvent être retournées en tant qu’erreurs.</span><span class="sxs-lookup"><span data-stu-id="017e1-106">The following constants may be returned as errors.</span></span>

<dl> <dt>

<span data-ttu-id="017e1-107"><span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**\_durée non valide de RND \_**</span><span class="sxs-lookup"><span data-stu-id="017e1-107"><span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**RND\_INVALID\_TIME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="017e1-108">0xe0000200</span><span class="sxs-lookup"><span data-stu-id="017e1-108">0xe0000200</span></span>
</dt> <dt>



<span data-ttu-id="017e1-109">La valeur d’heure entrée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="017e1-109">The time value entered is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="017e1-110"><span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**nom du serveur de RND \_ null \_ \_**</span><span class="sxs-lookup"><span data-stu-id="017e1-110"><span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**RND\_NULL\_SERVER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="017e1-111">0xe0000201</span><span class="sxs-lookup"><span data-stu-id="017e1-111">0xe0000201</span></span>
</dt> <dt>



<span data-ttu-id="017e1-112">Le nom du serveur est **null**, probablement parce que [**ITConferenceBlob :: init**](itconferenceblob-init.md) n’a pas été exécuté ou n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="017e1-112">The server name is **NULL**, probably because [**ITConferenceBlob::Init**](itconferenceblob-init.md) has not been run or did not succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="017e1-113"><span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND \_ déjà \_ connecté**</span><span class="sxs-lookup"><span data-stu-id="017e1-113"><span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="017e1-114">0xe0000202</span><span class="sxs-lookup"><span data-stu-id="017e1-114">0xe0000202</span></span>
</dt> <dt>



<span data-ttu-id="017e1-115">La méthode [**ITDirectory :: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) a été appelée, mais une connexion existe déjà.</span><span class="sxs-lookup"><span data-stu-id="017e1-115">The [**ITDirectory::Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) method was called, but a connection already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="017e1-116"><span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND \_ non \_ connecté**</span><span class="sxs-lookup"><span data-stu-id="017e1-116"><span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="017e1-117">0xe0000203</span><span class="sxs-lookup"><span data-stu-id="017e1-117">0xe0000203</span></span>
</dt> <dt>



<span data-ttu-id="017e1-118">La méthode [**ITDirectory :: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) n’a pas été appelée ou a échoué.</span><span class="sxs-lookup"><span data-stu-id="017e1-118">The [**ITDirectory::Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) method has not been called, or failed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="017e1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="017e1-119">Requirements</span></span>



| <span data-ttu-id="017e1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="017e1-120">Requirement</span></span> | <span data-ttu-id="017e1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="017e1-121">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="017e1-122">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="017e1-122">TAPI version</span></span><br/> | <span data-ttu-id="017e1-123">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="017e1-123">Requires TAPI 3.0 or later</span></span><br/>                                               |
| <span data-ttu-id="017e1-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="017e1-124">Header</span></span><br/>       | <dl> <span data-ttu-id="017e1-125"><dt>Rnderr. h</dt></span><span class="sxs-lookup"><span data-stu-id="017e1-125"><dt>Rnderr.h</dt></span></span> </dl> |



 

 




