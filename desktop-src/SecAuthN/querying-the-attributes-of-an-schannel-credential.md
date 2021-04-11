---
description: Fournit des informations spécifiques à Schannel sur les informations d’identification.
ms.assetid: 0c357996-b85a-4231-b258-40b35ab83ae2
title: Interrogation des attributs d’une information d’identification Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc63ccc358561dea95cb1273e1367e7fbb39d390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202719"
---
# <a name="querying-the-attributes-of-an-schannel-credential"></a><span data-ttu-id="4c25d-103">Interrogation des attributs d’une information d’identification Schannel</span><span class="sxs-lookup"><span data-stu-id="4c25d-103">Querying the Attributes of an Schannel Credential</span></span>

<span data-ttu-id="4c25d-104">La fonction [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) fournit des informations spécifiques à Schannel sur les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="4c25d-104">The [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) function provides Schannel-specific information about a credential.</span></span> <span data-ttu-id="4c25d-105">Ces informations sont spécifiées à l’origine lors de la création des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="4c25d-105">This information is originally specified when the credential is created.</span></span> <span data-ttu-id="4c25d-106">Pour plus d’informations, consultez [obtention d’informations d’identification Schannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="4c25d-106">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span> <span data-ttu-id="4c25d-107">Les informations signalées par cette fonction sont valides pour toutes les connexions ([*contextes de sécurité*](../secgloss/s-gly.md)) créées à l’aide des informations d’identification spécifiées.</span><span class="sxs-lookup"><span data-stu-id="4c25d-107">The information reported by this function is valid for any connections ([*security contexts*](../secgloss/s-gly.md)) created by using the specified credential.</span></span>

 

 
