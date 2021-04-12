---
title: Éviter le polymorphisme
description: Les nouveaux types de données incluent deux types polymorphes, INT \_ PTR et long \_ ptr.
ms.assetid: 3d18016d-772c-45bc-8057-7281e71a8707
keywords:
- Programmation Windows de polymorphisme 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec0fd26944d58a9ba0d253da8b8dbcd68156436
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311104"
---
# <a name="avoiding-polymorphism"></a><span data-ttu-id="d5528-104">Éviter le polymorphisme</span><span class="sxs-lookup"><span data-stu-id="d5528-104">Avoiding Polymorphism</span></span>

<span data-ttu-id="d5528-105">Les nouveaux types de données incluent deux types polymorphes, **int \_ ptr** et **long \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="d5528-105">The new data types include two polymorphic types, **INT\_PTR** and **LONG\_PTR**.</span></span> <span data-ttu-id="d5528-106">Sur Windows 32 bits, le **\_ ptr int** est mappé à **int** et le **\_ ptr long** est mappé à **long**.</span><span class="sxs-lookup"><span data-stu-id="d5528-106">On 32-bit Windows, the **INT\_PTR** maps to **int** and the **LONG\_PTR** maps to **long**.</span></span> <span data-ttu-id="d5528-107">Sur Windows 64 bits, les deux types sont mappés au type intrinsèque **\_ \_ Int64** .</span><span class="sxs-lookup"><span data-stu-id="d5528-107">On 64-bit Windows, both types map to the **\_\_int64** intrinsic type.</span></span> <span data-ttu-id="d5528-108">Le compilateur MIDL prend en charge ces types pour les appels de procédure distante, mais il existe une limitation inhérente que vous devez garder à l’esprit lorsque vous les utilisez dans un environnement distribué.</span><span class="sxs-lookup"><span data-stu-id="d5528-108">The MIDL compiler supports these types for remote procedure calls, but there is an inherent limitation that you must keep in mind when using them in a distributed environment.</span></span> <span data-ttu-id="d5528-109">Veillez à commenter votre code en conséquence.</span><span class="sxs-lookup"><span data-stu-id="d5528-109">Be sure to comment your code accordingly.</span></span>

<span data-ttu-id="d5528-110">Quelle que soit la taille de la plateforme, la taille du câble de ces types polymorphes est toujours de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d5528-110">Regardless of the platform size, the wire size of these polymorphic types is always 32 bits.</span></span> <span data-ttu-id="d5528-111">Lors du démarshaling sur Windows 64 bits, la signature de la bibliothèque Runtime étend les valeurs signées et assigne zéro aux octets de poids fort pour une valeur non signée.</span><span class="sxs-lookup"><span data-stu-id="d5528-111">When unmarshaling on 64-bit Windows, the run-time library sign extends signed values and assigns zero to the high-order bytes for an unsigned value.</span></span> <span data-ttu-id="d5528-112">Lorsque vous mettez une valeur 64 bits sur le câble, le temps d’exécution tronque les octets de poids fort.</span><span class="sxs-lookup"><span data-stu-id="d5528-112">When putting a 64-bit value on the wire, the run time truncates the high-order bytes.</span></span> <span data-ttu-id="d5528-113">Ainsi, seules les valeurs 32 bits de poids faible sont utilisables.</span><span class="sxs-lookup"><span data-stu-id="d5528-113">Thus, only the low-order 32-bit values are usable.</span></span>

<span data-ttu-id="d5528-114">Utilisez les types polymorphes uniquement lorsque cela est nécessaire pour le portage.</span><span class="sxs-lookup"><span data-stu-id="d5528-114">Use the polymorphic types only when necessary for porting.</span></span> <span data-ttu-id="d5528-115">Pour les nouvelles interfaces, utilisez les types d’entiers intrinsèques MIDL **\_ \_ Int32** et **\_ \_ Int64**, ou utilisez un type pointeur ou un handle de contexte, selon la valeur la plus appropriée pour le type de données transférées.</span><span class="sxs-lookup"><span data-stu-id="d5528-115">For new interfaces, use the MIDL intrinsic integer types **\_\_int32** and **\_\_int64**, or use a pointer type or context handle, whichever is most appropriate for the kind of data being transferred.</span></span>

<span data-ttu-id="d5528-116">Le compilateur 64 bits prend en charge un nouveau **\_ \_ int3264** intrinsèque polymorphe.</span><span class="sxs-lookup"><span data-stu-id="d5528-116">The 64-bit compiler supports a new polymorphic intrinsic **\_\_int3264**.</span></span> <span data-ttu-id="d5528-117">Là encore, ce type a été développé pour prendre en charge les efforts de Portage, dans ce cas pour prendre en charge les types **\_ ptr PTR** en toute transparence.</span><span class="sxs-lookup"><span data-stu-id="d5528-117">Again, this type was developed to support porting efforts, in this case to support the **UINT\_PTR** types transparently.</span></span> <span data-ttu-id="d5528-118">(Un autre intrinsèque, **\_ \_ long3264**, prendra en charge le type **\_ ptr ulong** .) N’utilisez pas directement **\_ \_ int3264** ; utilisez le type de **\_ pointeur int** lorsque vous avez besoin d’un type polymorphe pour des raisons de Portage.</span><span class="sxs-lookup"><span data-stu-id="d5528-118">(Another intrinsic, **\_\_long3264**, will support the **ULONG\_PTR** type.) Do not use **\_\_int3264** directly; use the **INT\_PTR** type when you need a polymorphic type for porting reasons.</span></span>

 

 




