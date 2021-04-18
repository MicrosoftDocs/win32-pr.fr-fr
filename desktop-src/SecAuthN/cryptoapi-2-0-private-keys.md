---
description: Les informations d’identification Schannel sont représentées en interne en tant que structures de contexte de certificat \_ .
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: CryptoAPI 2.0 les clés privées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5180515b529e33ae385fa94688a7e8fb436bd32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542950"
---
# <a name="cryptoapi-20-private-keys"></a><span data-ttu-id="3dee9-103">CryptoAPI 2.0 les clés privées</span><span class="sxs-lookup"><span data-stu-id="3dee9-103">CryptoAPI 2.0 Private Keys</span></span>

<span data-ttu-id="3dee9-104">Les informations d’identification Schannel sont représentées en interne en tant que structures de [**\_ contexte de certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="3dee9-104">Schannel credentials are represented internally as [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structures.</span></span> <span data-ttu-id="3dee9-105">Schannel localise la [*clé privée*](/windows/desktop/SecGloss/p-gly) associée à un contexte de certificat particulier à l’aide de la propriété de certification de la clé de certificat \_ \_ Prov \_ info \_ prop \_ ID du certificat.</span><span class="sxs-lookup"><span data-stu-id="3dee9-105">Schannel locates the [*private key*](/windows/desktop/SecGloss/p-gly) associated with a particular certificate context using the certificate's CERT\_KEY\_PROV\_INFO\_PROP\_ID property.</span></span> <span data-ttu-id="3dee9-106">À l’aide de cette propriété, Schannel accède à la *clé privée* en appelant la fonction [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) .</span><span class="sxs-lookup"><span data-stu-id="3dee9-106">Using this property, Schannel accesses the *private key* by calling the [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) function.</span></span> <span data-ttu-id="3dee9-107">Pour plus d’informations, consultez [paires de clés publique/privée](/windows/desktop/SecCrypto/public-private-key-pairs).</span><span class="sxs-lookup"><span data-stu-id="3dee9-107">For additional details, see [Public/Private Key Pairs](/windows/desktop/SecCrypto/public-private-key-pairs).</span></span>

<span data-ttu-id="3dee9-108">Chaque information d’identification Schannel contient une référence à une ou plusieurs clés privées, chacune associée à un certificat particulier.</span><span class="sxs-lookup"><span data-stu-id="3dee9-108">Every Schannel credential contains a reference to one or more private keys, each associated with a particular certificate.</span></span> <span data-ttu-id="3dee9-109">Les [*clés privées*](/windows/desktop/SecGloss/p-gly) sont gérées de façon très différente selon que les informations d’identification concernent un client ou un serveur.</span><span class="sxs-lookup"><span data-stu-id="3dee9-109">The [*private keys*](/windows/desktop/SecGloss/p-gly) are handled quite differently depending on whether the credential is for a client or a server.</span></span>

## <a name="client-private-keys"></a><span data-ttu-id="3dee9-110">Clés privées du client</span><span class="sxs-lookup"><span data-stu-id="3dee9-110">Client Private Keys</span></span>

<span data-ttu-id="3dee9-111">Les [*clés privées*](/windows/desktop/SecGloss/p-gly) du client sont gérées par le [*fournisseur de services de chiffrement*](/windows/desktop/SecGloss/c-gly) (CSP) utilisé.</span><span class="sxs-lookup"><span data-stu-id="3dee9-111">Client [*private keys*](/windows/desktop/SecGloss/p-gly) are managed by the [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP) in use.</span></span> <span data-ttu-id="3dee9-112">Les clés privées du client sont généralement stockées par les fournisseurs de services de type [Prov \_ RSA \_ Full](/windows/desktop/SecCrypto/prov-rsa-full) ou Prov \_ RSA \_ signature.</span><span class="sxs-lookup"><span data-stu-id="3dee9-112">Client private keys are typically stored by CSPs of type [PROV\_RSA\_FULL](/windows/desktop/SecCrypto/prov-rsa-full) or PROV\_RSA\_SIGNATURE.</span></span>

<span data-ttu-id="3dee9-113">Si l’application cliente effectue l’appel [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) manuellement avant d’appeler [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), le client doit lier le descripteur du CSP au contexte de certificat à l’aide de la \_ propriété CERT Key \_ \_ \_ prop handle prop \_ ID.</span><span class="sxs-lookup"><span data-stu-id="3dee9-113">If the client application makes the [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) call manually then before calling [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), the client must bind the CSP's handle to the certificate context using the CERT\_KEY\_PROV\_HANDLE\_PROP\_ID property.</span></span> <span data-ttu-id="3dee9-114">Si Schannel trouve ce jeu de propriétés, il n’utilise pas la propriété CERTIFICATe de la \_ clé \_ Prov \_ info \_ prop \_ ID.</span><span class="sxs-lookup"><span data-stu-id="3dee9-114">If Schannel finds this property set, it does not use the CERT\_KEY\_PROV\_INFO\_PROP\_ID property.</span></span>

## <a name="server-private-keys"></a><span data-ttu-id="3dee9-115">Clés privées du serveur</span><span class="sxs-lookup"><span data-stu-id="3dee9-115">Server Private Keys</span></span>

<span data-ttu-id="3dee9-116">Les clés privées du serveur sont stockées par l’un des fournisseurs de services de chiffrement suivants :</span><span class="sxs-lookup"><span data-stu-id="3dee9-116">Server private keys are stored by one of the following CSPs:</span></span>

-   <span data-ttu-id="3dee9-117">PROUVER \_ RSA \_ Schannel</span><span class="sxs-lookup"><span data-stu-id="3dee9-117">PROV\_RSA\_SCHANNEL</span></span>
-   <span data-ttu-id="3dee9-118">PROUVER \_ DH \_ Schannel</span><span class="sxs-lookup"><span data-stu-id="3dee9-118">PROV\_DH\_SCHANNEL</span></span>
-   <span data-ttu-id="3dee9-119">PROUVER le \_ CSP Fortezza</span><span class="sxs-lookup"><span data-stu-id="3dee9-119">PROV\_FORTEZZA CSP</span></span>

<span data-ttu-id="3dee9-120">Le choix du fournisseur de services de chiffrement dépend de l' [*algorithme d’échange de clés*](/windows/desktop/SecGloss/k-gly)sélectionné.</span><span class="sxs-lookup"><span data-stu-id="3dee9-120">The choice of CSP depends on the selected [*key exchange algorithm*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="3dee9-121">Les clés privées du serveur doivent être de type au niveau de \_ KeyExchange.</span><span class="sxs-lookup"><span data-stu-id="3dee9-121">Server private keys must be of type AT\_KEYEXCHANGE.</span></span>

 

 
