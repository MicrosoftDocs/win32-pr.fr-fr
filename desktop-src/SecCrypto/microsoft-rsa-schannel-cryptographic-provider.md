---
description: Le fournisseur de services de chiffrement Microsoft RSA/SChannel prend en charge le hachage, la signature des données et la vérification de signature.
ms.assetid: 34ede85a-579f-400f-a53e-e40711fcaaf3
title: Fournisseur de services de chiffrement Microsoft RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782e1971f59911b36c3812a4508530a5e1801194
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581967"
---
# <a name="microsoft-rsaschannel-cryptographic-provider"></a><span data-ttu-id="ff745-103">Fournisseur de services de chiffrement Microsoft RSA/Schannel</span><span class="sxs-lookup"><span data-stu-id="ff745-103">Microsoft RSA/Schannel Cryptographic Provider</span></span>

<span data-ttu-id="ff745-104">Le fournisseur de services de chiffrement Microsoft [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) prend en charge le hachage, la signature des données et la vérification de signature.</span><span class="sxs-lookup"><span data-stu-id="ff745-104">The Microsoft [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) Cryptographic Provider supports hashing, data signing, and signature verification.</span></span> <span data-ttu-id="ff745-105">L’identificateur d’algorithme CALG \_ SSL3 \_ SHAMD5 est utilisé pour l’authentification du client SSL 3,0 et TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="ff745-105">The algorithm identifier CALG\_SSL3\_SHAMD5 is used for SSL 3.0 and TLS 1.0 client authentication.</span></span> <span data-ttu-id="ff745-106">Ce CSP prend en charge la dérivation de clés pour les protocoles SSL2, PCT1, SSL3 et TLS1.</span><span class="sxs-lookup"><span data-stu-id="ff745-106">This CSP supports key derivation for the SSL2, PCT1, SSL3, and TLS1 protocols.</span></span> <span data-ttu-id="ff745-107">Le [*hachage*](../secgloss/h-gly.md) se compose d’une concaténation d’un hachage MD5 avec un hachage SHA et signé avec une [*clé privée*](../secgloss/p-gly.md)RSA.</span><span class="sxs-lookup"><span data-stu-id="ff745-107">The [*hash*](../secgloss/h-gly.md) consists of a concatenation of a MD5 hash with a SHA hash and signed with a RSA [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="ff745-108">Elle peut être exportée vers d’autres pays/régions.</span><span class="sxs-lookup"><span data-stu-id="ff745-108">It can be exported to other countries/regions.</span></span>



|                   | <span data-ttu-id="ff745-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff745-109">Value</span></span>                         |
|-------------------|-------------------------------|
| <span data-ttu-id="ff745-110">**Type de fournisseur**</span><span class="sxs-lookup"><span data-stu-id="ff745-110">**Provider type**</span></span> | <span data-ttu-id="ff745-111">PROUVER \_ RSA \_ Schannel</span><span class="sxs-lookup"><span data-stu-id="ff745-111">PROV\_RSA\_SCHANNEL</span></span>           |
| <span data-ttu-id="ff745-112">**Nom du fournisseur**</span><span class="sxs-lookup"><span data-stu-id="ff745-112">**Provider name**</span></span> | <span data-ttu-id="ff745-113">MS \_ Def \_ RSA \_ Schannel \_ Prov</span><span class="sxs-lookup"><span data-stu-id="ff745-113">MS\_DEF\_RSA\_SCHANNEL\_PROV</span></span>  |



 

<span data-ttu-id="ff745-114">Pour plus d’informations sur les fournisseurs RSA/Schannel, voir [CSP Functions](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ff745-114">For more information about RSA/Schannel providers, see [CSP Functions](cryptography-functions.md).</span></span>

 

 
