---
description: Le fournisseur de services de chiffrement de base Microsoft est le fournisseur du fournisseur de services de chiffrement (CSP) initial et est distribué avec les versions 1,0 et 2,0 de CryptoAPI. Il s’agit d’un fournisseur à usage général qui prend en charge les signatures numériques et le chiffrement des données.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Fournisseur de services de chiffrement de base Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53bd4b2f7faf140e57d25b54d3161b47dcaf740
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581887"
---
# <a name="microsoft-base-cryptographic-provider"></a><span data-ttu-id="9ce08-104">Fournisseur de services de chiffrement de base Microsoft</span><span class="sxs-lookup"><span data-stu-id="9ce08-104">Microsoft Base Cryptographic Provider</span></span>

<span data-ttu-id="9ce08-105">Le fournisseur de services de chiffrement de base Microsoft est le fournisseur du [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) initial et est distribué avec les versions 1,0 et 2,0 de [*CryptoAPI*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9ce08-105">The Microsoft Base Cryptographic Provider is the initial [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) provider, and is distributed with [*CryptoAPI*](../secgloss/c-gly.md) versions 1.0 and 2.0.</span></span> <span data-ttu-id="9ce08-106">Il s’agit d’un fournisseur à usage général qui prend en charge les [*signatures numériques*](../secgloss/d-gly.md) et le chiffrement des données.</span><span class="sxs-lookup"><span data-stu-id="9ce08-106">It is a general-purpose provider that supports [*digital signatures*](../secgloss/d-gly.md) and data encryption.</span></span>

<span data-ttu-id="9ce08-107">L’algorithme de clé publique RSA est utilisé pour toutes les opérations de clé publique.</span><span class="sxs-lookup"><span data-stu-id="9ce08-107">The RSA public key algorithm is used for all public key operations.</span></span>

<span data-ttu-id="9ce08-108">Pour assurer la compatibilité descendante avec les versions antérieures, la nouvelle version du fournisseur conserve la désignation de version 1,0 du nom dans wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="9ce08-108">To maintain backward compatibility with earlier versions the new version of the provider retains the version 1.0 designation of the name in Wincrypt.h.</span></span> <span data-ttu-id="9ce08-109">Toutefois, la version 2,0 de ce fournisseur est actuellement commercialisée.</span><span class="sxs-lookup"><span data-stu-id="9ce08-109">However, version 2.0 of this provider is currently shipping.</span></span> <span data-ttu-id="9ce08-110">Pour déterminer la version réelle du fournisseur en cours d’utilisation, appelez [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) avec l’argument *DwParam* défini sur **pp \_ version**.</span><span class="sxs-lookup"><span data-stu-id="9ce08-110">To determine the actual version of the provider in use, call [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with the *dwParam* argument set to **PP\_VERSION**.</span></span> <span data-ttu-id="9ce08-111">Si 0x0200 est retourné dans *pbData*, vous avez la version 2,0.</span><span class="sxs-lookup"><span data-stu-id="9ce08-111">If 0x0200 is returned in *pbData*, then you have version 2.0.</span></span>

|                   | <span data-ttu-id="9ce08-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ce08-112">Value</span></span>            |
|-------------------|------------------|
| <span data-ttu-id="9ce08-113">**Type de fournisseur**</span><span class="sxs-lookup"><span data-stu-id="9ce08-113">**Provider type**</span></span> | <span data-ttu-id="9ce08-114">PROUVER \_ RSA \_ Full</span><span class="sxs-lookup"><span data-stu-id="9ce08-114">PROV\_RSA\_FULL</span></span>  |
| <span data-ttu-id="9ce08-115">**Nom du fournisseur**</span><span class="sxs-lookup"><span data-stu-id="9ce08-115">**Provider name**</span></span> | <span data-ttu-id="9ce08-116">MS \_ Def \_ Prov</span><span class="sxs-lookup"><span data-stu-id="9ce08-116">MS\_DEF\_PROV</span></span>    |



 

 

 
