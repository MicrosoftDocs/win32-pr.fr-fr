---
description: Les informations d’identification sont requises par le processus d’authentification Schannel. le client et le serveur doivent obtenir des informations d’identification valides pour établir un contexte de sécurité pour l’échange de messages. Pour obtenir un exemple qui illustre cette procédure, consultez obtention d’informations d’identification.
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: Obtention des informations d’identification Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e5a5b82b3ed76e905c967009da52d17bff0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756436"
---
# <a name="obtaining-schannel-credentials"></a><span data-ttu-id="c47ff-104">Obtention des informations d’identification Schannel</span><span class="sxs-lookup"><span data-stu-id="c47ff-104">Obtaining Schannel Credentials</span></span>

<span data-ttu-id="c47ff-105">Les informations d’identification sont requises par le processus d’authentification Schannel. le client et le serveur doivent obtenir des informations d’identification valides pour établir un [*contexte de sécurité*](../secgloss/s-gly.md) pour l’échange de messages.</span><span class="sxs-lookup"><span data-stu-id="c47ff-105">Credentials are required by the Schannel authentication process; both client and server must obtain valid credentials to establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="c47ff-106">Pour obtenir un exemple qui illustre cette procédure, consultez [obtention d’informations d’identification](getting-a-certificate-for-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="c47ff-106">For an example that demonstrates this procedure, see [Getting credentials](getting-a-certificate-for-schannel.md).</span></span>

<span data-ttu-id="c47ff-107">Votre application obtient les informations d’identification en appelant la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , qui retourne un handle aux informations d’identification demandées.</span><span class="sxs-lookup"><span data-stu-id="c47ff-107">Your application obtains credentials by calling the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function, which returns a handle to the requested credentials.</span></span> <span data-ttu-id="c47ff-108">Étant donné que les handles d’informations d’identification sont utilisés pour stocker les informations de configuration, le même handle ne peut pas être utilisé pour les opérations côté client et côté serveur.</span><span class="sxs-lookup"><span data-stu-id="c47ff-108">Because credentials handles are used to store configuration information, the same handle cannot be used for both client-side and server-side operations.</span></span> <span data-ttu-id="c47ff-109">Cela signifie que les applications qui prennent en charge les connexions client et serveur doivent obtenir au moins deux handles d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c47ff-109">This means that applications that support both client and server connections must obtain a minimum of two credentials handles.</span></span>

<span data-ttu-id="c47ff-110">Dans Windows XP, une structure [**Schannel \_ cred**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) spécifie les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c47ff-110">In Windows XP, an [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure specifies the following:</span></span>

-   <span data-ttu-id="c47ff-111">Un protocole de sécurité</span><span class="sxs-lookup"><span data-stu-id="c47ff-111">A security protocol</span></span>
-   <span data-ttu-id="c47ff-112">Chiffrements autorisés</span><span class="sxs-lookup"><span data-stu-id="c47ff-112">The allowable ciphers</span></span>
-   <span data-ttu-id="c47ff-113">Puissance de chiffrement minimale et maximale</span><span class="sxs-lookup"><span data-stu-id="c47ff-113">Minimum and maximum cipher strengths</span></span>
-   <span data-ttu-id="c47ff-114">Un certificat [*X. 509*](../secgloss/x-gly.md) utilisé pour l’authentification, requis pour le serveur, facultatif pour le client, sauf si le serveur demande l’authentification du client.</span><span class="sxs-lookup"><span data-stu-id="c47ff-114">An [*X.509*](../secgloss/x-gly.md) certificate used for authentication — Required for server, optional for client unless server requests client authentication.</span></span>

<span data-ttu-id="c47ff-115">Transmettez la structure [**Schannel \_ cred**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (via le paramètre *pAuthData* ) à la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .</span><span class="sxs-lookup"><span data-stu-id="c47ff-115">Pass the [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure (via the *pAuthData* parameter) to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span> <span data-ttu-id="c47ff-116">Cette fonction retourne le handle d’informations d’identification requis pour établir un [*contexte de sécurité*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c47ff-116">This function returns the credentials handle required to establish a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="c47ff-117">Pour plus d’informations sur la définition des chiffrements utilisés avec Schannel, consultez [spécification des chiffrements Schannel et des niveaux de chiffrement](specifying-schannel-ciphers-and-cipher-strengths.md).</span><span class="sxs-lookup"><span data-stu-id="c47ff-117">For detailed information on setting the ciphers used with Schannel, see [Specifying Schannel Ciphers and Cipher Strengths](specifying-schannel-ciphers-and-cipher-strengths.md).</span></span>

<span data-ttu-id="c47ff-118">Pour plus d’informations sur les certificats, consultez [fonctions de certificat et de magasin de certificats](../seccrypto/cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c47ff-118">For information about certificates, see [Certificate and Certificate Store Functions](../seccrypto/cryptography-functions.md).</span></span>

<span data-ttu-id="c47ff-119">Pour obtenir un exemple illustrant l’ouverture d’un [*magasin de certificats*](../secgloss/c-gly.md) et la localisation d’un certificat à utiliser pour l’authentification Schannel, consultez [obtention d’un certificat](getting-a-certificate-for-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="c47ff-119">For an example that demonstrates opening a [*certificate store*](../secgloss/c-gly.md) and locating a certificate to use for Schannel authentication, see [Getting a Certificate](getting-a-certificate-for-schannel.md).</span></span>

 

 
