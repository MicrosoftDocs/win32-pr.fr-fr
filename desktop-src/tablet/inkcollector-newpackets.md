---
description: Se produit lorsque le collecteur d’encres reçoit un paquet.
ms.assetid: 2682e7ba-dabd-497e-aea4-6d3f837f4f10
title: Événement InkCollector. NewPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b03e1a561a61c9b291bca8e59f990dc12b4e2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318101"
---
# <a name="inkcollectornewpackets-event"></a><span data-ttu-id="1a698-103">Événement InkCollector. NewPackets</span><span class="sxs-lookup"><span data-stu-id="1a698-103">InkCollector.NewPackets event</span></span>

<span data-ttu-id="1a698-104">Se produit lorsque le collecteur d’encres reçoit un paquet.</span><span class="sxs-lookup"><span data-stu-id="1a698-104">Occurs when the ink collector receives a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a698-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a698-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="1a698-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a698-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a698-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a698-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a698-108">Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**NewInAirPackets**](inkcollector-newinairpackets.md) .</span><span class="sxs-lookup"><span data-stu-id="1a698-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="1a698-109">*Trait* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a698-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a698-110">Spécifie l’objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="1a698-110">Specifies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="1a698-111">*PacketCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a698-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a698-112">Nombre de paquets reçus pour un objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="1a698-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="1a698-113">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1a698-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a698-114">Lorsque cette méthode est retournée, contient un tableau qui contient les données sélectionnées pour le paquet.</span><span class="sxs-lookup"><span data-stu-id="1a698-114">When this method returns, contains an array that contains the selected data for the packet.</span></span>

<span data-ttu-id="1a698-115">Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="1a698-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a698-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a698-116">Return value</span></span>

<span data-ttu-id="1a698-117">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1a698-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a698-118">Notes</span><span class="sxs-lookup"><span data-stu-id="1a698-118">Remarks</span></span>

<span data-ttu-id="1a698-119">Les paquets sont reçus lorsqu’un trait est collecté.</span><span class="sxs-lookup"><span data-stu-id="1a698-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="1a698-120">Les événements de paquets se produisent rapidement et un gestionnaire d’événements **NewPackets** doit être rapide ou subir des performances.</span><span class="sxs-lookup"><span data-stu-id="1a698-120">Packet events occur rapidly, and a **NewPackets** event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="1a698-121">La méthode d’événement TCet est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IINKPICTUREEVENTS avec l’ID DISPID \_ ICENewPackets.</span><span class="sxs-lookup"><span data-stu-id="1a698-121">TThis event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="1a698-122">Cet événement doit être utilisé avec précaution, car il peut avoir un effet néfaste sur les performances de l’encre si un trop grand nombre de code est exécuté dans les gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="1a698-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="1a698-123">Pour définir les propriétés contenues dans ce tableau, utilisez la propriété [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) de l’objet Ink collector.</span><span class="sxs-lookup"><span data-stu-id="1a698-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="1a698-124">Le tableau retourné par le paramètre *PacketData* contient les données de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1a698-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="1a698-125">Bien que vous puissiez modifier les données du paquet, ces modifications ne sont pas conservées ou utilisées.</span><span class="sxs-lookup"><span data-stu-id="1a698-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1a698-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a698-126">Requirements</span></span>



| <span data-ttu-id="1a698-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a698-127">Requirement</span></span> | <span data-ttu-id="1a698-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a698-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a698-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a698-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1a698-130">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a698-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1a698-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a698-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1a698-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a698-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1a698-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a698-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a698-134"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1a698-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1a698-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1a698-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a698-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a698-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1a698-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a698-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a698-138">**InkCollector (classe)**</span><span class="sxs-lookup"><span data-stu-id="1a698-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="1a698-139">**Événement NewInAirPackets**</span><span class="sxs-lookup"><span data-stu-id="1a698-139">**NewInAirPackets Event**</span></span>](inkcollector-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="1a698-140">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="1a698-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="1a698-141">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="1a698-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




