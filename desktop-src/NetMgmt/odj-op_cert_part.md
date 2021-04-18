---
title: OP_CERT_PART
description: Définition du OP_CERT_PART IDL
ms.assetid: 30492801-f26e-447f-bcbf-d1108e7ae524
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: feb4f05171204442085f7d69691aa010d13e6042
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "106509285"
---
# <a name="op_cert_part-structure"></a><span data-ttu-id="d278d-103">Structure OP_CERT_PART</span><span class="sxs-lookup"><span data-stu-id="d278d-103">OP_CERT_PART structure</span></span>

<span data-ttu-id="d278d-104">Contient des magasins de certificats et PFX sérialisés.</span><span class="sxs-lookup"><span data-stu-id="d278d-104">Contains serialized PFX and certificate stores.</span></span>

## <a name="syntax"></a><span data-ttu-id="d278d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d278d-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_PART
{
    ULONG                                       cPfxStores;
    [size_is(cPfxStores)]   POP_CERT_PFX_STORE  pPfxStores;
    ULONG                                       cSstStores;
    [size_is(cSstStores)]   POP_CERT_SST_STORE  pSstStores;
    OP_BLOB                                     Extension;
} OP_CERT_PART, *POP_CERT_PART;
```

## <a name="members"></a><span data-ttu-id="d278d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d278d-106">Members</span></span>

### <a name="cpfxstores"></a><span data-ttu-id="d278d-107">cPfxStores</span><span class="sxs-lookup"><span data-stu-id="d278d-107">cPfxStores</span></span>

<span data-ttu-id="d278d-108">Contient le nombre d’éléments dans pPfxStores.</span><span class="sxs-lookup"><span data-stu-id="d278d-108">Contains the number of elements in pPfxStores.</span></span>

### <a name="ppfxstores"></a><span data-ttu-id="d278d-109">pPfxStores</span><span class="sxs-lookup"><span data-stu-id="d278d-109">pPfxStores</span></span>

<span data-ttu-id="d278d-110">Contient un tableau de structures OP_CERT_PFX_STORE.</span><span class="sxs-lookup"><span data-stu-id="d278d-110">Contains an array of OP_CERT_PFX_STORE structures.</span></span>

### <a name="csststores"></a><span data-ttu-id="d278d-111">cSstStores</span><span class="sxs-lookup"><span data-stu-id="d278d-111">cSstStores</span></span>

<span data-ttu-id="d278d-112">Contient le nombre d’éléments dans pSstStores.</span><span class="sxs-lookup"><span data-stu-id="d278d-112">Contains the number of elements in pSstStores.</span></span>

### <a name="psststores"></a><span data-ttu-id="d278d-113">pSstStores</span><span class="sxs-lookup"><span data-stu-id="d278d-113">pSstStores</span></span>

<span data-ttu-id="d278d-114">Contient un tableau de structures OP_CERT_SST_STORE.</span><span class="sxs-lookup"><span data-stu-id="d278d-114">Contains an array of OP_CERT_SST_STORE structures.</span></span>

### <a name="extension"></a><span data-ttu-id="d278d-115">Extension</span><span class="sxs-lookup"><span data-stu-id="d278d-115">Extension</span></span>

<span data-ttu-id="d278d-116">Réservé pour une utilisation ultérieure et doit contenir uniquement des zéros.</span><span class="sxs-lookup"><span data-stu-id="d278d-116">Reserved for future use and must contain all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="d278d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d278d-117">See also</span></span>

[<span data-ttu-id="d278d-118">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="d278d-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="d278d-119">**\_ \_ magasin pfx du certificat op \_**</span><span class="sxs-lookup"><span data-stu-id="d278d-119">**OP\_CERT\_PFX\_STORE**</span></span>](odj-op_cert_pfx_store.md)

[<span data-ttu-id="d278d-120">**\_ \_ magasin SST du certificat op \_**</span><span class="sxs-lookup"><span data-stu-id="d278d-120">**OP\_CERT\_SST\_STORE**</span></span>](odj-op_cert_sst_store.md)

[<span data-ttu-id="d278d-121">**\_objet BLOB op**</span><span class="sxs-lookup"><span data-stu-id="d278d-121">**OP\_BLOB**</span></span>](odj-op_blob.md)

