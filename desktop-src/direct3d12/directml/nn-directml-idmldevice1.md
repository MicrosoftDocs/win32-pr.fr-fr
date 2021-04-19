---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: Représente un appareil DirectML, utilisé pour créer des opérateurs, des tables de liaison, des enregistreurs de commande et d’autres objets.
helpviewer_keywords:
- IDMLDevice1
- IDMLDevice1 interface
- IDMLDevice1 interface
- described
- direct3d12.idmldevice1
- directml/IDMLDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1
- directml/IDMLDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.h
api_name:
- IDMLDevice1
ms.openlocfilehash: a23d6ec4299a2aa3ca7e9f6873167412d094af8d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106538241"
---
# <a name="idmldevice1-interface-directmlh"></a><span data-ttu-id="2a9f8-103">Interface IDMLDevice1 (directml. h)</span><span class="sxs-lookup"><span data-stu-id="2a9f8-103">IDMLDevice1 interface (directml.h)</span></span>

<span data-ttu-id="2a9f8-104">Représente un appareil DirectML, utilisé pour créer des opérateurs, des tables de liaison, des enregistreurs de commande et d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="2a9f8-104">Represents a DirectML device, which is used to create operators, binding tables, command recorders, and other objects.</span></span> <span data-ttu-id="2a9f8-105">L’interface **IDMLDevice1** hérite de [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span><span class="sxs-lookup"><span data-stu-id="2a9f8-105">The **IDMLDevice1** interface inherits from [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

<span data-ttu-id="2a9f8-106">Un appareil DirectML est toujours associé à un seul appareil Direct3D 12 sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="2a9f8-106">A DirectML device is always associated with exactly one underlying Direct3D 12 device.</span></span> <span data-ttu-id="2a9f8-107">Tous les objets créés par l’appareil DirectML conservent une référence forte à leur périphérique parent.</span><span class="sxs-lookup"><span data-stu-id="2a9f8-107">All objects created by the DirectML device maintain a strong reference to their parent device.</span></span> <span data-ttu-id="2a9f8-108">Contrairement à l’appareil Direct3D 12, l’appareil DML n’est pas un singleton.</span><span class="sxs-lookup"><span data-stu-id="2a9f8-108">Unlike the Direct3D 12 device, the DML device is not a singleton.</span></span> <span data-ttu-id="2a9f8-109">Par conséquent, il est possible de créer plusieurs appareils DirectML sur le même appareil Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="2a9f8-109">Therefore, it's possible to create multiple DirectML devices over the same Direct3D 12 device.</span></span> <span data-ttu-id="2a9f8-110">Toutefois, cela n’est pas recommandé, car l’appareil DirectML n’a pas d’État mutable, donc il n’y a pas d’avantage à créer plusieurs appareils DML sur le même appareil Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="2a9f8-110">However, this isn't recommended as the DirectML device has no mutable state, so there's little advantage to creating multiple DML devices over the same Direct3D 12 device.</span></span>

<span data-ttu-id="2a9f8-111">Cet objet est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2a9f8-111">This object is thread-safe.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a9f8-112">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="2a9f8-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="2a9f8-113">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="2a9f8-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="availability"></a><span data-ttu-id="2a9f8-114">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="2a9f8-114">Availability</span></span>
<span data-ttu-id="2a9f8-115">Cette API a été introduite dans la version DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="2a9f8-115">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="2a9f8-116">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="2a9f8-116">Tensor constraints</span></span>
<span data-ttu-id="2a9f8-117">**Plateforme cible**: Windows</span><span class="sxs-lookup"><span data-stu-id="2a9f8-117">**Target Platform**: Windows</span></span>


## <a name="inheritance"></a><span data-ttu-id="2a9f8-118">Héritage</span><span class="sxs-lookup"><span data-stu-id="2a9f8-118">Inheritance</span></span>


<span data-ttu-id="2a9f8-119">L’interface IDMLDevice1 hérite de l’interface IDMLDevice.</span><span class="sxs-lookup"><span data-stu-id="2a9f8-119">The IDMLDevice1 interface inherits from the IDMLDevice interface.</span></span>



## <a name="methods"></a><span data-ttu-id="2a9f8-120">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2a9f8-120">Methods</span></span>

<p><span data-ttu-id="2a9f8-121">L’interface <b>IDMLDevice1</b> possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2a9f8-121">The <b>IDMLDevice1</b> interface has these methods.</span></span></p>

| <span data-ttu-id="2a9f8-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="2a9f8-122">Method</span></span> | <span data-ttu-id="2a9f8-123">Description</span><span class="sxs-lookup"><span data-stu-id="2a9f8-123">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="2a9f8-124">IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="2a9f8-124">IDMLDevice1::CompileGraph</span></span>](../directml/nf-directml-idmldevice1-compilegraph.md) | <span data-ttu-id="2a9f8-125">Compile un graphique d’opérateurs DirectML dans un objet qui peut être distribué au GPU.</span><span class="sxs-lookup"><span data-stu-id="2a9f8-125">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span> |


## <a name="requirements"></a><span data-ttu-id="2a9f8-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a9f8-126">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2a9f8-127">**Plateforme cible**</span><span class="sxs-lookup"><span data-stu-id="2a9f8-127">**Target Platform**</span></span> | <span data-ttu-id="2a9f8-128">Windows</span><span class="sxs-lookup"><span data-stu-id="2a9f8-128">Windows</span></span> |
| <span data-ttu-id="2a9f8-129">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="2a9f8-129">**Header**</span></span> | <span data-ttu-id="2a9f8-130">directml. h</span><span class="sxs-lookup"><span data-stu-id="2a9f8-130">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="2a9f8-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a9f8-131">See also</span></span>

[<span data-ttu-id="2a9f8-132">Interface IDMLDevice</span><span class="sxs-lookup"><span data-stu-id="2a9f8-132">IDMLDevice interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)