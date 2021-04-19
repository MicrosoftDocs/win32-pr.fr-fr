---
title: OP_PACKAGE
description: Définition du OP_PACKAGE IDL
ms.assetid: 065266a6-6db5-4113-bd2b-22ac6063236d
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 6220b3815ad6ff360af7255a91fc34d71125f38c
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "106513749"
---
# <a name="op_package-structure"></a><span data-ttu-id="01825-103">Structure OP_PACKAGE</span><span class="sxs-lookup"><span data-stu-id="01825-103">OP_PACKAGE structure</span></span>

<span data-ttu-id="01825-104">Contient une structure qui contient un OP_PACKAGE_COLLECTION sérialisé.</span><span class="sxs-lookup"><span data-stu-id="01825-104">Contains a structure that contains a serialized OP_PACKAGE_COLLECTION.</span></span>

## <a name="syntax"></a><span data-ttu-id="01825-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01825-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE
{
    GUID    EncryptionType;
    OP_BLOB EncryptionContext;
    OP_BLOB WrappedPartCollection;
    ULONG   cbDecryptedPartCollection;
    OP_BLOB Extension;
} OP_PACKAGE, *POP_PACKAGE;
```

## <a name="members"></a><span data-ttu-id="01825-106">Membres</span><span class="sxs-lookup"><span data-stu-id="01825-106">Members</span></span>

### <a name="encryptiontype"></a><span data-ttu-id="01825-107">EncryptionType</span><span class="sxs-lookup"><span data-stu-id="01825-107">EncryptionType</span></span>

<span data-ttu-id="01825-108">Réservé pour une utilisation ultérieure et doit être défini sur GUID_NULL.</span><span class="sxs-lookup"><span data-stu-id="01825-108">Reserved for future use and MUST be set to GUID_NULL.</span></span>

### <a name="encryptioncontext"></a><span data-ttu-id="01825-109">EncryptionContext</span><span class="sxs-lookup"><span data-stu-id="01825-109">EncryptionContext</span></span>

<span data-ttu-id="01825-110">Réservé pour une utilisation ultérieure et doit être défini sur tous les zéros.</span><span class="sxs-lookup"><span data-stu-id="01825-110">Reserved for future use and MUST be set to all zeros.</span></span>

### <a name="wrappedpartcollection"></a><span data-ttu-id="01825-111">WrappedPartCollection</span><span class="sxs-lookup"><span data-stu-id="01825-111">WrappedPartCollection</span></span>

<span data-ttu-id="01825-112">Structure OP_BLOB qui contient une structure OP_PACKAGE_COLLECTION sérialisée.</span><span class="sxs-lookup"><span data-stu-id="01825-112">An OP_BLOB structure that contains a serialized OP_PACKAGE_COLLECTION structure.</span></span>

### <a name="cbdecryptedpartcollection"></a><span data-ttu-id="01825-113">cbDecryptedPartCollection</span><span class="sxs-lookup"><span data-stu-id="01825-113">cbDecryptedPartCollection</span></span>

<span data-ttu-id="01825-114">Réservé pour une utilisation ultérieure et doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="01825-114">Reserved for future use and MUST be set to zero.</span></span>

### <a name="extension"></a><span data-ttu-id="01825-115">Extension</span><span class="sxs-lookup"><span data-stu-id="01825-115">Extension</span></span>

<span data-ttu-id="01825-116">Réservé pour une utilisation ultérieure et doit être défini sur tous les zéros.</span><span class="sxs-lookup"><span data-stu-id="01825-116">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="01825-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01825-117">See also</span></span>

[<span data-ttu-id="01825-118">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="01825-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="01825-119">**\_objet BLOB op**</span><span class="sxs-lookup"><span data-stu-id="01825-119">**OP\_BLOB**</span></span>](odj-op_blob.md)

[<span data-ttu-id="01825-120">**\_collection de packages op \_**</span><span class="sxs-lookup"><span data-stu-id="01825-120">**OP\_PACKAGE\_COLLECTION**</span></span>](odj-op_package_collection.md)
