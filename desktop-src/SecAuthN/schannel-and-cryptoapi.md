---
description: Schannel utilise CryptoAPI pour les opérations de chiffrement telles que le stockage des clés publiques/privées.
ms.assetid: 5ad9a171-5f69-4035-aac5-ae8d27d0abfb
title: Schannel et CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0684cd690911444b77ba27d2876e578fd71c73a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393356"
---
# <a name="schannel-and-cryptoapi"></a><span data-ttu-id="0cee4-103">Schannel et CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="0cee4-103">Schannel and CryptoAPI</span></span>

<span data-ttu-id="0cee4-104">Schannel utilise [CryptoAPI](../seccrypto/cryptography-essentials.md) pour les opérations de chiffrement telles que le stockage des [*clés publiques/privées*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0cee4-104">Schannel uses [CryptoAPI](../seccrypto/cryptography-essentials.md) for cryptographic operations such as storing [*public/private keys*](../secgloss/p-gly.md).</span></span>

<span data-ttu-id="0cee4-105">Les rubriques suivantes fournissent des informations détaillées sur la façon dont Schannel utilise CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="0cee4-105">The following topics provide detailed information about how Schannel makes use of CryptoAPI.</span></span>



| <span data-ttu-id="0cee4-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="0cee4-106">Topic</span></span>                                                                   | <span data-ttu-id="0cee4-107">Description</span><span class="sxs-lookup"><span data-stu-id="0cee4-107">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0cee4-108">Magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="0cee4-108">Certificate Stores</span></span>](certificate-stores.md)<br/>                 | <span data-ttu-id="0cee4-109">Les certificats client et serveur doivent être stockés dans un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="0cee4-109">Both client and server certificates must be stored in a certificate store.</span></span><br/>                                |
| [<span data-ttu-id="0cee4-110">CryptoAPI 2.0 les clés privées</span><span class="sxs-lookup"><span data-stu-id="0cee4-110">CryptoAPI 2.0 Private Keys</span></span>](cryptoapi-2-0-private-keys.md)<br/> | <span data-ttu-id="0cee4-111">Les informations d’identification Schannel sont représentées en interne en tant que structures de [**\_ contexte de certificat**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="0cee4-111">Schannel credentials are represented internally as [**CERT\_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structures.</span></span><br/> |



 

 

 
