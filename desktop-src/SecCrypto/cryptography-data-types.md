---
description: Les types de données suivants sont utilisés par les fonctions de chiffrement, les interfaces et les objets.
ms.assetid: 9d6a065d-c765-4d17-9f4c-38a984439278
title: Types de données de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84c6f21faa25e1ccc478c178a3f21458ff589ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513382"
---
# <a name="cryptography-data-types"></a><span data-ttu-id="cb091-103">Types de données de chiffrement</span><span class="sxs-lookup"><span data-stu-id="cb091-103">Cryptography Data Types</span></span>

<span data-ttu-id="cb091-104">Les types de données suivants sont utilisés par les fonctions de chiffrement, les interfaces et les objets.</span><span class="sxs-lookup"><span data-stu-id="cb091-104">The following data types are used by cryptography functions, interfaces, and objects.</span></span>



| <span data-ttu-id="cb091-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="cb091-105">Data type</span></span>                                                                      | <span data-ttu-id="cb091-106">Description</span><span class="sxs-lookup"><span data-stu-id="cb091-106">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb091-107">**\_ID ALG**</span><span class="sxs-lookup"><span data-stu-id="cb091-107">**ALG\_ID**</span></span>](alg-id.md)                                                      | <span data-ttu-id="cb091-108">Spécifie les identificateurs d’algorithme.</span><span class="sxs-lookup"><span data-stu-id="cb091-108">Specifies algorithm identifiers.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="cb091-109">**\_ \_ réponse OCSP du serveur HCERT \_**</span><span class="sxs-lookup"><span data-stu-id="cb091-109">**HCERT\_SERVER\_OCSP\_RESPONSE**</span></span>](hcert-server-ocsp-response.md)            | <span data-ttu-id="cb091-110">Représente un handle vers une réponse OCSP associée à une chaîne de certificat de serveur.</span><span class="sxs-lookup"><span data-stu-id="cb091-110">Represents a handle to an OCSP response associated with a server certificate chain.</span></span>                                                                                                              |
| [<span data-ttu-id="cb091-111">**HCRYPTHASH**</span><span class="sxs-lookup"><span data-stu-id="cb091-111">**HCRYPTHASH**</span></span>](hcrypthash.md)                                               | <span data-ttu-id="cb091-112">Spécifie des handles vers un [*objet de hachage*](../secgloss/h-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cb091-112">Specifies handles to a [*hash object*](../secgloss/h-gly.md).</span></span>                                                                                      |
| [<span data-ttu-id="cb091-113">**HCRYPTKEY**</span><span class="sxs-lookup"><span data-stu-id="cb091-113">**HCRYPTKEY**</span></span>](hcryptkey.md)                                                 | <span data-ttu-id="cb091-114">Spécifie des handles vers des clés de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="cb091-114">Specifies handles to cryptographic keys.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="cb091-115">**HCRYPTOIDFUNCADDR**</span><span class="sxs-lookup"><span data-stu-id="cb091-115">**HCRYPTOIDFUNCADDR**</span></span>](hcryptoidfuncaddr.md)                                 | <span data-ttu-id="cb091-116">Représente un handle vers une fonction qui peut être installée à l’aide d’un [*identificateur d’objet*](../secgloss/o-gly.md) (OID).</span><span class="sxs-lookup"><span data-stu-id="cb091-116">Represents a handle to a function that can be installed by using an [*object identifier*](../secgloss/o-gly.md) (OID).</span></span>                 |
| [<span data-ttu-id="cb091-117">**HCRYPTOIDFUNCSET**</span><span class="sxs-lookup"><span data-stu-id="cb091-117">**HCRYPTOIDFUNCSET**</span></span>](hcryptoidfuncset.md)                                   | <span data-ttu-id="cb091-118">Représente un handle vers un ensemble de fonctions qui peuvent être installées à l’aide d’un OID.</span><span class="sxs-lookup"><span data-stu-id="cb091-118">Represents a handle to a set of functions that can be installed by using an OID.</span></span>                                                                                                                 |
| [<span data-ttu-id="cb091-119">**HCRYPTPROV \_ hérité**</span><span class="sxs-lookup"><span data-stu-id="cb091-119">**HCRYPTPROV\_LEGACY**</span></span>](hcryptprov-legacy.md)                                | <span data-ttu-id="cb091-120">Utilisé pour remplacer le type de données [**HCRYPTPROV**](hcryptprov.md) dans lequel le type de données **HCRYPTPROV** n’est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="cb091-120">Used to replace the [**HCRYPTPROV**](hcryptprov.md) data type where the **HCRYPTPROV** data type is no longer used.</span></span>                                                                             |
| [<span data-ttu-id="cb091-121">**\_handle de clé HCRYPTPROV ou \_ NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cb091-121">**HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE**</span></span>](hcryptprov-or-ncrypt-key-handle.md) | <span data-ttu-id="cb091-122">Spécifie un descripteur pour un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) CryptoAPI ou un CSP CNG.</span><span class="sxs-lookup"><span data-stu-id="cb091-122">Specifies a handle to a CryptoAPI [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or CNG CSP.</span></span> |
| [<span data-ttu-id="cb091-123">**HCRYPTPROV**</span><span class="sxs-lookup"><span data-stu-id="cb091-123">**HCRYPTPROV**</span></span>](hcryptprov.md)                                               | <span data-ttu-id="cb091-124">Spécifie un descripteur pour un fournisseur de services de chiffrement CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="cb091-124">Specifies a handle to a CryptoAPI CSP.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="cb091-125">**\_handle KEYSVCC**</span><span class="sxs-lookup"><span data-stu-id="cb091-125">**KEYSVCC\_HANDLE**</span></span>](keysvcc-handle.md)                                      | <span data-ttu-id="cb091-126">Spécifie des handles pour le service de clé.</span><span class="sxs-lookup"><span data-stu-id="cb091-126">Specifies handles to the key service.</span></span>                                                                                                                                                            |



 

 

 
