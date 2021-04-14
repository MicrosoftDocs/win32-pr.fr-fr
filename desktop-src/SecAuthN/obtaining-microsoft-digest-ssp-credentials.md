---
description: Les informations d’identification de l’utilisateur sont requises par Microsoft Digest ; le client et le serveur doivent présenter des informations d’identification valides pour pouvoir établir un contexte de sécurité pour l’échange de messages. Les handles d’informations d’identification sont utilisés pour obtenir et présenter les informations d’identification.
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: Obtention d’informations d’identification SSP Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61895ecc8e49713665af4542689729bc491d9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484712"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a><span data-ttu-id="9b12a-104">Obtention d’informations d’identification SSP Microsoft Digest</span><span class="sxs-lookup"><span data-stu-id="9b12a-104">Obtaining Microsoft Digest SSP Credentials</span></span>

<span data-ttu-id="9b12a-105">Les [*informations d’identification*](../secgloss/c-gly.md) de l’utilisateur sont requises par Microsoft Digest ; le client et le serveur doivent présenter des informations d’identification valides pour pouvoir établir un [*contexte de sécurité*](../secgloss/s-gly.md) pour l’échange de messages.</span><span class="sxs-lookup"><span data-stu-id="9b12a-105">User [*credentials*](../secgloss/c-gly.md) are required by Microsoft Digest; both client and server must present valid credentials before they can establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="9b12a-106">Les handles d’informations d’identification sont utilisés pour obtenir et présenter les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="9b12a-106">Credentials handles are used to obtain and present credentials.</span></span>

<span data-ttu-id="9b12a-107">Étant donné que le handle d’informations d’identification est utilisé pour stocker les informations de configuration, le même handle ne peut pas être utilisé pour les opérations côté client et côté serveur.</span><span class="sxs-lookup"><span data-stu-id="9b12a-107">Because the credential handle is used to store configuration information, the same handle cannot be used for both client-side and server-side operations.</span></span> <span data-ttu-id="9b12a-108">Cela signifie que les applications qui prennent en charge les connexions client et serveur doivent obtenir au moins deux handles d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="9b12a-108">This means that applications that support both client and server connections must obtain a minimum of two credentials handles.</span></span>

<span data-ttu-id="9b12a-109">Pour obtenir un descripteur des informations d’identification requises par Microsoft Digest, appelez la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .</span><span class="sxs-lookup"><span data-stu-id="9b12a-109">To get a handle to the credentials required by Microsoft Digest, call the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span>

<span data-ttu-id="9b12a-110">Les exemples de langage C suivants montrent comment obtenir des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="9b12a-110">The following C language examples demonstrate obtaining credentials.</span></span>

-   [<span data-ttu-id="9b12a-111">Obtention des informations d’identification Digest par défaut</span><span class="sxs-lookup"><span data-stu-id="9b12a-111">Obtaining Default Digest Credentials</span></span>](obtaining-default-digest-credentials.md)
-   [<span data-ttu-id="9b12a-112">Obtention d’autres informations d’identification de Digest</span><span class="sxs-lookup"><span data-stu-id="9b12a-112">Obtaining Alternate Digest Credentials</span></span>](obtaining-alternate-digest-credentials.md)

 

 
