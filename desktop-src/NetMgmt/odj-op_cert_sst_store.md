---
title: OP_CERT_SST_STORE
description: Définition du OP_CERT_SST_STORE IDL
ms.assetid: 6c44756e-29f9-48fc-b678-d2b1f0fb90d4
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 294d21d730e1cce478088cddb43686706217ec5b
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104383435"
---
# <a name="op_cert_sst_store-structure"></a><span data-ttu-id="b8a9a-103">Structure OP_CERT_SST_STORE</span><span class="sxs-lookup"><span data-stu-id="b8a9a-103">OP_CERT_SST_STORE structure</span></span>

<span data-ttu-id="b8a9a-104">Contient un magasin de certificats sérialisés.</span><span class="sxs-lookup"><span data-stu-id="b8a9a-104">Contains a serialized certificate store.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a9a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8a9a-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_SST_STORE
{
    ULONG                       StoreLocation;
    [string] wchar_t            *pStoreName;
    ULONG                       cbSst;
    [size_is(cbSst)]    PBYTE   pSst;
} OP_CERT_SST_STORE, *POP_CERT_SST_STORE;
```

## <a name="members"></a><span data-ttu-id="b8a9a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b8a9a-106">Members</span></span>

### <a name="storelocation"></a><span data-ttu-id="b8a9a-107">StoreLocation</span><span class="sxs-lookup"><span data-stu-id="b8a9a-107">StoreLocation</span></span>

<span data-ttu-id="b8a9a-108">Contient un identificateur pour le magasin de certificats à partir d' [**emplacements du magasin système**](../seccrypto/system-store-locations.md).</span><span class="sxs-lookup"><span data-stu-id="b8a9a-108">Contains an identifier for the certificate store from [**System Store Locations**](../seccrypto/system-store-locations.md).</span></span>

### <a name="pstorename"></a><span data-ttu-id="b8a9a-109">pStoreName</span><span class="sxs-lookup"><span data-stu-id="b8a9a-109">pStoreName</span></span>

<span data-ttu-id="b8a9a-110">Contient le nom du magasin.</span><span class="sxs-lookup"><span data-stu-id="b8a9a-110">Contains the name of the store.</span></span>

### <a name="cbsst"></a><span data-ttu-id="b8a9a-111">cbSst</span><span class="sxs-lookup"><span data-stu-id="b8a9a-111">cbSst</span></span>

<span data-ttu-id="b8a9a-112">Contient la taille de pSst en octets.</span><span class="sxs-lookup"><span data-stu-id="b8a9a-112">Contains the size of pSst in bytes.</span></span>

### <a name="psst"></a><span data-ttu-id="b8a9a-113">pSst</span><span class="sxs-lookup"><span data-stu-id="b8a9a-113">pSst</span></span>

<span data-ttu-id="b8a9a-114">Contient un magasin de certificats sérialisés (voir [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span><span class="sxs-lookup"><span data-stu-id="b8a9a-114">Contains a serialized certificate store (see [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span></span>

## <a name="see-also"></a><span data-ttu-id="b8a9a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8a9a-115">See also</span></span>

[<span data-ttu-id="b8a9a-116">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="b8a9a-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)