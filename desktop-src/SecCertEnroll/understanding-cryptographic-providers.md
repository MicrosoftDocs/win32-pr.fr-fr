---
description: Les fournisseurs implémentent des algorithmes de chiffrement, génèrent des clés, fournissent un stockage de clés et authentifient les utilisateurs. Les fournisseurs peuvent être implémentés dans le matériel, les logiciels ou les deux.
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: Comprendre les fournisseurs de services de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11861b99dc8a19fc4300be2c9707462235f4a792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952558"
---
# <a name="understanding-cryptographic-providers"></a><span data-ttu-id="af294-104">Comprendre les fournisseurs de services de chiffrement</span><span class="sxs-lookup"><span data-stu-id="af294-104">Understanding Cryptographic Providers</span></span>

<span data-ttu-id="af294-105">Le concept de fournisseur de services de chiffrement introduit dans l’API de chiffrement ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) et qui a évolué quelque peu dans l' [*API de chiffrement : Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) est essentiel à l’implémentation sécurisée des fonctionnalités de chiffrement sur les systèmes d’exploitation Microsoft.</span><span class="sxs-lookup"><span data-stu-id="af294-105">The cryptographic provider concept that was introduced in Cryptography API ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) and which evolved somewhat in [*Cryptography API: Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) is central to the secure implementation of cryptographic functionality on Microsoft operating systems.</span></span> <span data-ttu-id="af294-106">Ces deux SDK ont été utilisés pour créer de nombreuses applications et sont appelés en interne par d’autres kits de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="af294-106">These two SDKs have been used to create many applications and are called internally by other SDKs.</span></span> <span data-ttu-id="af294-107">Par exemple, Active Directory Services de certificats et l’API d’inscription de certificats s’appuient sur CryptoAPI et CNG.</span><span class="sxs-lookup"><span data-stu-id="af294-107">For example, Active Directory Certificate Services and the Certificate Enrollment API rely on CryptoAPI and CNG.</span></span>

<span data-ttu-id="af294-108">En général, les fournisseurs implémentent des algorithmes de chiffrement, génèrent des clés, fournissent un stockage de clés et authentifient les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="af294-108">In general, providers implement cryptographic algorithms, generate keys, provide key storage, and authenticate users.</span></span> <span data-ttu-id="af294-109">Les fournisseurs peuvent être implémentés dans le matériel, les logiciels ou les deux.</span><span class="sxs-lookup"><span data-stu-id="af294-109">Providers can be implemented in hardware, software, or both.</span></span> <span data-ttu-id="af294-110">Les applications générées à l’aide d’CryptoAPI ou CNG ne peuvent pas modifier les clés créées par les fournisseurs, et elles ne peuvent pas modifier l’implémentation de l’algorithme de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="af294-110">Applications built by using CryptoAPI or CNG cannot alter the keys created by providers, and they cannot alter cryptographic algorithm implementation.</span></span> <span data-ttu-id="af294-111">Les différents fournisseurs créés par Microsoft sont distribués avec les systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="af294-111">The multiple providers created by Microsoft are distributed with the operating systems.</span></span> <span data-ttu-id="af294-112">D’autres fournisseurs ont été créés et distribués par des tiers.</span><span class="sxs-lookup"><span data-stu-id="af294-112">Other providers have been created and distributed by third parties.</span></span>

<span data-ttu-id="af294-113">Les rubriques suivantes mettent en évidence les différences entre les fournisseurs associés à CryptoAPI et celles associées à CNG.</span><span class="sxs-lookup"><span data-stu-id="af294-113">The following topics highlight the differences between providers associated with CryptoAPI and those associated with CNG.</span></span> <span data-ttu-id="af294-114">En règle générale, cette documentation fait référence aux fournisseurs sans référence au kit de développement logiciel (SDK) auquel ils sont associés, en notant l’Association uniquement lorsqu’elle est pertinente.</span><span class="sxs-lookup"><span data-stu-id="af294-114">Typically, this documentation refers to providers without reference to the SDK with which they are associated, noting the association only when it is relevant.</span></span>

-   [<span data-ttu-id="af294-115">Fournisseurs de services de chiffrement CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="af294-115">CryptoAPI Cryptographic Service Providers</span></span>](cryptoapi-cryptographic-service-providers.md)
-   [<span data-ttu-id="af294-116">Fournisseurs d’algorithmes de chiffrement CNG</span><span class="sxs-lookup"><span data-stu-id="af294-116">CNG Cryptographic Algorithm Providers</span></span>](cng-cryptographic-algorithm-providers.md)
-   [<span data-ttu-id="af294-117">Fournisseurs de stockage de clés CNG</span><span class="sxs-lookup"><span data-stu-id="af294-117">CNG Key Storage Providers</span></span>](cng-key-storage-providers.md)
-   [<span data-ttu-id="af294-118">Énumération des fournisseurs installés</span><span class="sxs-lookup"><span data-stu-id="af294-118">Enumerating Installed Providers</span></span>](enumerating-installed-providers.md)

## <a name="related-topics"></a><span data-ttu-id="af294-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af294-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af294-120">Utilisation de l’API d’inscription de certificats</span><span class="sxs-lookup"><span data-stu-id="af294-120">Using the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
