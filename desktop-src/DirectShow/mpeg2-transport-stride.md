---
description: La \_ \_ structure Stride transport MPEG2 décrit le format des paquets de flux de transport MPEG-2 (TS).
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: Structure MPEG2_TRANSPORT_STRIDE (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MPEG2_TRANSPORT_STRIDE
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 5153f6f79c2807634149222a126a7256a65ffe8a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908487"
---
# <a name="mpeg2_transport_stride-structure"></a><span data-ttu-id="4d82e-103">\_Structure Stride de transport MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="4d82e-103">MPEG2\_TRANSPORT\_STRIDE structure</span></span>

<span data-ttu-id="4d82e-104">La `MPEG2_TRANSPORT_STRIDE` structure décrit le format des paquets de flux de transport MPEG-2 (TS).</span><span class="sxs-lookup"><span data-stu-id="4d82e-104">The `MPEG2_TRANSPORT_STRIDE` structure describes the format of MPEG-2 transport stream (TS) packets.</span></span> <span data-ttu-id="4d82e-105">Cette structure autorise les flux de transport dans lesquels les paquets de transport de 188 octets ne sont pas contigus.</span><span class="sxs-lookup"><span data-stu-id="4d82e-105">This structure allows for transports streams in which the 188-byte transport packets are not contiguous.</span></span> <span data-ttu-id="4d82e-106">Dans le cadre de cette documentation, ces paquets sont appelés *paquets Stride*.</span><span class="sxs-lookup"><span data-stu-id="4d82e-106">For the purpose of this documentation, such packets are referred to as *stride packets*.</span></span>

<span data-ttu-id="4d82e-107">Les paquets Stride sont identifiés par le type de média suivant :</span><span class="sxs-lookup"><span data-stu-id="4d82e-107">Stride packets are identified by the following media type:</span></span>



| <span data-ttu-id="4d82e-108">Étiquette</span><span class="sxs-lookup"><span data-stu-id="4d82e-108">Label</span></span> | <span data-ttu-id="4d82e-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d82e-109">Value</span></span> |
|-------------|----------------------------------------|
| <span data-ttu-id="4d82e-110">Type principal</span><span class="sxs-lookup"><span data-stu-id="4d82e-110">Major Type</span></span>  | <span data-ttu-id="4d82e-111">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="4d82e-111">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="4d82e-112">Subtype</span><span class="sxs-lookup"><span data-stu-id="4d82e-112">Subtype</span></span>     | <span data-ttu-id="4d82e-113">\_Stride de \_ transport MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="4d82e-113">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="4d82e-114">Type de format</span><span class="sxs-lookup"><span data-stu-id="4d82e-114">Format Type</span></span> | <span data-ttu-id="4d82e-115">FORMAT \_ aucun</span><span class="sxs-lookup"><span data-stu-id="4d82e-115">FORMAT\_None</span></span>                           |



 

<span data-ttu-id="4d82e-116">Le bloc de format (**pbFormat**) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="4d82e-116">The format block (**pbFormat**) is optional.</span></span> <span data-ttu-id="4d82e-117">Si le bloc de format est inclus, il doit commencer par une structure **\_ \_ Stride de transport MPEG2** .</span><span class="sxs-lookup"><span data-stu-id="4d82e-117">If the format block is included, it must begin with an **MPEG2\_TRANSPORT\_STRIDE** structure.</span></span> <span data-ttu-id="4d82e-118">Cette structure définit la disposition du paquet de transport dans le paquet Stride.</span><span class="sxs-lookup"><span data-stu-id="4d82e-118">This structure defines the layout of the transport packet within the stride packet.</span></span> <span data-ttu-id="4d82e-119">Si le bloc de format est **null**, les paquets sont supposés utiliser un ensemble de valeurs par défaut ; Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4d82e-119">If the format block is **NULL**, the packets are assumed to use a set of default values; see the Remarks section for details.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d82e-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d82e-120">Syntax</span></span>


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a><span data-ttu-id="4d82e-121">Membres</span><span class="sxs-lookup"><span data-stu-id="4d82e-121">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d82e-122">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="4d82e-122">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="4d82e-123">Spécifie l’offset, en octets, entre le début du paquet et le premier octet du paquet de transport incorporé.</span><span class="sxs-lookup"><span data-stu-id="4d82e-123">Specifies the offset, in bytes, from the beginning of the packet to the first byte of the embedded transport packet.</span></span> <span data-ttu-id="4d82e-124">La valeur doit être comprise entre zéro et `(dwStride - dwPacketLength)` , inclus.</span><span class="sxs-lookup"><span data-stu-id="4d82e-124">The value must range from zero to `(dwStride - dwPacketLength)`, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="4d82e-125">**dwPacketLength**</span><span class="sxs-lookup"><span data-stu-id="4d82e-125">**dwPacketLength**</span></span>
</dt> <dd>

<span data-ttu-id="4d82e-126">Spécifie la longueur, en octets, du paquet de transport incorporé.</span><span class="sxs-lookup"><span data-stu-id="4d82e-126">Specifies the length of the embedded transport packet, in bytes.</span></span> <span data-ttu-id="4d82e-127">Pour les paquets de transport MPEG-2 standard, la valeur doit être de 188 octets.</span><span class="sxs-lookup"><span data-stu-id="4d82e-127">For standard MPEG-2 transport packets, the value must be 188 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4d82e-128">**dwStride**</span><span class="sxs-lookup"><span data-stu-id="4d82e-128">**dwStride**</span></span>
</dt> <dd>

<span data-ttu-id="4d82e-129">Spécifie la longueur de l’ensemble du paquet Stride, en octets.</span><span class="sxs-lookup"><span data-stu-id="4d82e-129">Specifies the length of the entire stride packet, in bytes.</span></span> <span data-ttu-id="4d82e-130">La valeur doit être au moins égale à `(dwOffset + dwPacketLength)` .</span><span class="sxs-lookup"><span data-stu-id="4d82e-130">The value must be at least `(dwOffset + dwPacketLength)`.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d82e-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="4d82e-131">Remarks</span></span>

<span data-ttu-id="4d82e-132">Le diagramme suivant illustre les relations entre les membres de structure.</span><span class="sxs-lookup"><span data-stu-id="4d82e-132">The following diagram illustrates the relations between the structure members.</span></span>

![paquet Stride MPEG-2](images/mpeg2-stride-packet.png)

<span data-ttu-id="4d82e-134">Les mémoires tampons d’entrée qui contiennent des paquets Stride multiplexés présentent des restrictions :</span><span class="sxs-lookup"><span data-stu-id="4d82e-134">Input buffers that contain multiplexed stride packets have some restrictions:</span></span>

-   <span data-ttu-id="4d82e-135">Les paquets Stride doivent être empaquetés de façon contiguë dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="4d82e-135">Stride packets must be packed contiguously within the buffer.</span></span>
-   <span data-ttu-id="4d82e-136">Aucun octet ne peut précéder le premier paquet Stride ou suivre le dernier paquet Stride.</span><span class="sxs-lookup"><span data-stu-id="4d82e-136">No bytes may precede the first stride packet or follow the last stride packet.</span></span>
-   <span data-ttu-id="4d82e-137">Un nombre entier de paquets Stride doit tenir dans la mémoire tampon ; autrement dit, la longueur de la mémoire tampon% dwStride est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="4d82e-137">An integral number of stride packets must fit in the buffer; that is, buffer length % dwStride equals zero.</span></span>

<span data-ttu-id="4d82e-138">Il n’existe aucune restriction sur le nombre de paquets Stride par mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="4d82e-138">There is no restriction on the number of stride packets per buffer.</span></span>

<span data-ttu-id="4d82e-139">Si le type de média ne contient pas de bloc de format (**pbFormat** a la **valeur null**), les valeurs par défaut suivantes sont utilisées :</span><span class="sxs-lookup"><span data-stu-id="4d82e-139">If the media type does not contain a format block (**pbFormat** is **NULL**), the following default values are used:</span></span>

-   <span data-ttu-id="4d82e-140">**dwOffset**: 0</span><span class="sxs-lookup"><span data-stu-id="4d82e-140">**dwOffset**: 0</span></span>
-   <span data-ttu-id="4d82e-141">**dwPacketLength**: 188</span><span class="sxs-lookup"><span data-stu-id="4d82e-141">**dwPacketLength**: 188</span></span>
-   <span data-ttu-id="4d82e-142">**dwStride**: 188</span><span class="sxs-lookup"><span data-stu-id="4d82e-142">**dwStride**: 188</span></span>

## <a name="requirements"></a><span data-ttu-id="4d82e-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d82e-143">Requirements</span></span>



| <span data-ttu-id="4d82e-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d82e-144">Requirement</span></span> | <span data-ttu-id="4d82e-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d82e-145">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d82e-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d82e-146">Header</span></span><br/> | <dl> <span data-ttu-id="4d82e-147"><dt>Bdatypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d82e-147"><dt>Bdatypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d82e-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d82e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d82e-149">Structures DirectShow</span><span class="sxs-lookup"><span data-stu-id="4d82e-149">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="4d82e-150">Types de média MPEG-2</span><span class="sxs-lookup"><span data-stu-id="4d82e-150">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




