---
description: L’événement InkPicture. NewPackets-se produit lorsque le collecteur d’encres reçoit un paquet.
ms.assetid: 7d120198-c016-4452-b8a8-22c4ad87d526
title: InkPicture. NewPackets, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194fb9bffae07cca561fbfc11ff8a185d63bb9e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086477"
---
# <a name="inkpicturenewpackets-event"></a><span data-ttu-id="8405a-103">InkPicture. NewPackets, événement</span><span class="sxs-lookup"><span data-stu-id="8405a-103">InkPicture.NewPackets event</span></span>

<span data-ttu-id="8405a-104">Se produit lorsque le collecteur d’encres reçoit un paquet.</span><span class="sxs-lookup"><span data-stu-id="8405a-104">Occurs when the ink collector receives a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="8405a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8405a-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="8405a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8405a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8405a-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8405a-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8405a-108">Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**NewInAirPackets**](inkpicture-newinairpackets.md) .</span><span class="sxs-lookup"><span data-stu-id="8405a-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkpicture-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="8405a-109">*Trait* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8405a-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8405a-110">Objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="8405a-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="8405a-111">*PacketCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8405a-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8405a-112">Nombre de paquets reçus pour un objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="8405a-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="8405a-113">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8405a-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8405a-114">Tableau qui contient les données sélectionnées pour le paquet.</span><span class="sxs-lookup"><span data-stu-id="8405a-114">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="8405a-115">Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="8405a-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8405a-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8405a-116">Return value</span></span>

<span data-ttu-id="8405a-117">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8405a-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8405a-118">Notes </span><span class="sxs-lookup"><span data-stu-id="8405a-118">Remarks</span></span>

<span data-ttu-id="8405a-119">Les paquets sont reçus lorsqu’un trait est collecté.</span><span class="sxs-lookup"><span data-stu-id="8405a-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="8405a-120">Les événements de paquets se produisent rapidement et un gestionnaire d’événements **NewPackets** doit être rapide ou subir des performances.</span><span class="sxs-lookup"><span data-stu-id="8405a-120">Packet events occur rapidly, and a **NewPackets** event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="8405a-121">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ ICENewPackets.</span><span class="sxs-lookup"><span data-stu-id="8405a-121">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="8405a-122">Cet événement doit être utilisé avec précaution, car il peut avoir un effet néfaste sur les performances de l’encre si un trop grand nombre de code est exécuté dans les gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="8405a-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="8405a-123">Pour définir les propriétés contenues dans ce tableau, utilisez la propriété [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) de l’objet Ink collector.</span><span class="sxs-lookup"><span data-stu-id="8405a-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="8405a-124">Le tableau retourné par le paramètre *PacketData* contient les données de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8405a-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="8405a-125">Bien que vous puissiez modifier les données du paquet, ces modifications ne sont pas conservées ou utilisées.</span><span class="sxs-lookup"><span data-stu-id="8405a-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8405a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8405a-126">Requirements</span></span>



| <span data-ttu-id="8405a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8405a-127">Requirement</span></span> | <span data-ttu-id="8405a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="8405a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8405a-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8405a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8405a-130">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8405a-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8405a-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8405a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8405a-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8405a-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8405a-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="8405a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8405a-134"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8405a-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8405a-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8405a-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="8405a-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8405a-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8405a-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8405a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8405a-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="8405a-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="8405a-139">**Événement NewInAirPackets**</span><span class="sxs-lookup"><span data-stu-id="8405a-139">**NewInAirPackets Event**</span></span>](inkpicture-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="8405a-140">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="8405a-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="8405a-141">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="8405a-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




