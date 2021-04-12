---
title: ODJ_SID
description: Définition du ODJ_SID IDL
ms.assetid: 1d06f725-6cd4-42cf-b171-c78a095690cb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dd51f2e8a54eaf5be566e5a25f013ca1d87b9341
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104032047"
---
# <a name="odj_sid-structure"></a><span data-ttu-id="4a49c-103">Structure ODJ_SID</span><span class="sxs-lookup"><span data-stu-id="4a49c-103">ODJ_SID structure</span></span>

<span data-ttu-id="4a49c-104">Contient un identificateur de sécurité (SID).</span><span class="sxs-lookup"><span data-stu-id="4a49c-104">Contains a Security Identifier (SID).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a49c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a49c-105">Syntax</span></span>

```C++
typedef struct _ODJ_SID
{
    UCHAR Revision;
    UCHAR SubAuthorityCount;
    SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
    [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
}   ODJ_SID, *PODJ_SID;
```

## <a name="members"></a><span data-ttu-id="4a49c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4a49c-106">Members</span></span>

### <a name="revision"></a><span data-ttu-id="4a49c-107">Révision</span><span class="sxs-lookup"><span data-stu-id="4a49c-107">Revision</span></span>

<span data-ttu-id="4a49c-108">Doit être défini sur la révision SID.</span><span class="sxs-lookup"><span data-stu-id="4a49c-108">Must be set to the SID revision.</span></span>

### <a name="subauthoritycount"></a><span data-ttu-id="4a49c-109">SubAuthorityCount</span><span class="sxs-lookup"><span data-stu-id="4a49c-109">SubAuthorityCount</span></span>

<span data-ttu-id="4a49c-110">Doit être défini sur le nombre d’éléments dans la sous-autorité.</span><span class="sxs-lookup"><span data-stu-id="4a49c-110">Must be set to the number of elements in SubAuthority.</span></span>

### <a name="identifierauthority"></a><span data-ttu-id="4a49c-111">IdentifierAuthority</span><span class="sxs-lookup"><span data-stu-id="4a49c-111">IdentifierAuthority</span></span>

<span data-ttu-id="4a49c-112">Doit être défini sur l’identificateur de l’autorité de SID.</span><span class="sxs-lookup"><span data-stu-id="4a49c-112">Must be set to the SID authority identifier.</span></span>

### <a name="subauthority"></a><span data-ttu-id="4a49c-113">Sous-autorité</span><span class="sxs-lookup"><span data-stu-id="4a49c-113">SubAuthority</span></span>

<span data-ttu-id="4a49c-114">Doit contenir un tableau de sous-autorités SID.</span><span class="sxs-lookup"><span data-stu-id="4a49c-114">Must contain an array of SID sub authorities.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a49c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a49c-115">See also</span></span>

[<span data-ttu-id="4a49c-116">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="4a49c-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="4a49c-117">**\_autorité d' \_ identificateur SID \_ ODJ**</span><span class="sxs-lookup"><span data-stu-id="4a49c-117">**ODJ\_SID\_IDENTIFIER\_AUTHORITY**</span></span>](odj-sid_identifier_authority.md)
