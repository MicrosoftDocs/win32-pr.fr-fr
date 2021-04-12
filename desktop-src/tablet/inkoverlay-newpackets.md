---
description: Se produit lorsque la collecte d’encre rreceives un paquet.
ms.assetid: 26d5a3eb-430a-4e21-8a3f-fdec5005cd6e
title: InkOverlay. NewPackets, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43743b47d007b44d4f2460266e7198266c36afd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210297"
---
# <a name="inkoverlaynewpackets-event"></a><span data-ttu-id="f1ca7-103">Événement InkOverlay. NewPackets</span><span class="sxs-lookup"><span data-stu-id="f1ca7-103">InkOverlay.NewPackets event</span></span>

<span data-ttu-id="f1ca7-104">Se produit lorsque la collecte d’encre rreceives un paquet</span><span class="sxs-lookup"><span data-stu-id="f1ca7-104">Occurs when the ink collecto rreceives a packet</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ca7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1ca7-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="f1ca7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1ca7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1ca7-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f1ca7-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1ca7-108">Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**NewInAirPackets**](inkcollector-newinairpackets.md) .</span><span class="sxs-lookup"><span data-stu-id="f1ca7-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="f1ca7-109">*Trait* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f1ca7-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1ca7-110">Spécifie l’objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="f1ca7-110">Specifies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="f1ca7-111">*PacketCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f1ca7-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1ca7-112">Nombre de paquets reçus pour un objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="f1ca7-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="f1ca7-113">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f1ca7-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1ca7-114">Tableau qui contient les données sélectionnées pour le paquet.</span><span class="sxs-lookup"><span data-stu-id="f1ca7-114">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="f1ca7-115">Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="f1ca7-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1ca7-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f1ca7-116">Return value</span></span>

<span data-ttu-id="f1ca7-117">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f1ca7-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1ca7-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f1ca7-118">Remarks</span></span>

<span data-ttu-id="f1ca7-119">Les paquets sont reçus lorsqu’un trait est collecté.</span><span class="sxs-lookup"><span data-stu-id="f1ca7-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="f1ca7-120">Les événements de paquets se produisent rapidement et un gestionnaire d’événements [**NewPackets**](inkcollector-newpackets.md) doit être rapide ou subir des performances.</span><span class="sxs-lookup"><span data-stu-id="f1ca7-120">Packet events occur rapidly, and a [**NewPackets**](inkcollector-newpackets.md) event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="f1ca7-121">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICENewPackets.</span><span class="sxs-lookup"><span data-stu-id="f1ca7-121">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="f1ca7-122">Cet événement doit être utilisé avec précaution, car il peut avoir un effet néfaste sur les performances de l’encre si un trop grand nombre de code est exécuté dans les gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="f1ca7-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="f1ca7-123">Pour définir les propriétés contenues dans ce tableau, utilisez la propriété [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) de l’objet Ink collector.</span><span class="sxs-lookup"><span data-stu-id="f1ca7-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="f1ca7-124">Le tableau retourné par le paramètre *PacketData* contient les données de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f1ca7-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="f1ca7-125">Bien que vous puissiez modifier les données du paquet, ces modifications ne sont pas conservées ou utilisées.</span><span class="sxs-lookup"><span data-stu-id="f1ca7-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f1ca7-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1ca7-126">Requirements</span></span>



| <span data-ttu-id="f1ca7-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1ca7-127">Requirement</span></span> | <span data-ttu-id="f1ca7-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1ca7-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ca7-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1ca7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f1ca7-130">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1ca7-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f1ca7-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1ca7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f1ca7-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1ca7-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f1ca7-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1ca7-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1ca7-134"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f1ca7-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f1ca7-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f1ca7-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="f1ca7-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1ca7-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f1ca7-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1ca7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1ca7-138">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="f1ca7-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="f1ca7-139">**Événement NewInAirPackets**</span><span class="sxs-lookup"><span data-stu-id="f1ca7-139">**NewInAirPackets Event**</span></span>](inkcollector-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="f1ca7-140">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="f1ca7-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="f1ca7-141">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="f1ca7-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




