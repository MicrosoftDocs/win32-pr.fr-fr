---
title: UUID
description: Fournit une désignation unique d’un objet tel qu’une interface, un vecteur de point d’entrée de gestionnaire ou un objet client.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 95d2d420502a5d92af64c902ffa82c709639d872
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101061"
---
# <a name="uuid-structure"></a><span data-ttu-id="f78ea-103">UUID, structure</span><span class="sxs-lookup"><span data-stu-id="f78ea-103">UUID structure</span></span>

<span data-ttu-id="f78ea-104">La structure **UUID** définit un identificateur unique universel (UUID).</span><span class="sxs-lookup"><span data-stu-id="f78ea-104">The **UUID** structure defines a Universally Unique Identifier (UUID).</span></span> <span data-ttu-id="f78ea-105">Un **UUID** fournit une désignation unique d’un objet tel qu’une interface, un vecteur de point d’entrée de gestionnaire ou un objet client.</span><span class="sxs-lookup"><span data-stu-id="f78ea-105">A **UUID** provides a unique designation of an object such as an interface, a manager entry-point vector, or a client object.</span></span>

<span data-ttu-id="f78ea-106">La structure **UUID** est un `typedef` synonyme de la structure [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) .</span><span class="sxs-lookup"><span data-stu-id="f78ea-106">The **UUID** structure is a `typedef`'d synonym for the [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f78ea-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f78ea-107">Syntax</span></span>

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a><span data-ttu-id="f78ea-108">Notes</span><span class="sxs-lookup"><span data-stu-id="f78ea-108">Remarks</span></span>

<span data-ttu-id="f78ea-109">Les bibliothèques Runtime RPC utilisent des **UUID** pour vérifier la compatibilité entre les clients et les serveurs, et pour effectuer une sélection parmi plusieurs implémentations d’une interface.</span><span class="sxs-lookup"><span data-stu-id="f78ea-109">The RPC run-time libraries use **UUID** s to check for compatibility between clients and servers, and to select among multiple implementations of an interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f78ea-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f78ea-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f78ea-111">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="f78ea-111">**Header**</span></span> | <span data-ttu-id="f78ea-112">Défini dans rpcdce. h ; inclure RPC. h</span><span class="sxs-lookup"><span data-stu-id="f78ea-112">Defined in rpcdce.h; include rpc.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="f78ea-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f78ea-113">See also</span></span>

<span data-ttu-id="f78ea-114">[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 [UUID \_ VECTEUR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)</span><span class="sxs-lookup"><span data-stu-id="f78ea-114">[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)
[UUID\_VECTOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)</span></span>