---
description: L’événement InkPicture. NewInAirPackets se produit lorsqu’un paquet in-air est détecté.
ms.assetid: 30bc423d-0642-4515-9e51-a8b8b36aecad
title: InkPicture. NewInAirPackets, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0de8f2423817bada84f83b63de1517393740db4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086557"
---
# <a name="inkpicturenewinairpackets-event"></a><span data-ttu-id="bd868-103">InkPicture. NewInAirPackets, événement</span><span class="sxs-lookup"><span data-stu-id="bd868-103">InkPicture.NewInAirPackets event</span></span>

<span data-ttu-id="bd868-104">Se produit lorsqu’un paquet air est détecté.</span><span class="sxs-lookup"><span data-stu-id="bd868-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd868-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd868-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="bd868-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd868-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd868-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bd868-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd868-108">Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement **NewInAirPackets** .</span><span class="sxs-lookup"><span data-stu-id="bd868-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **NewInAirPackets** event.</span></span>

</dd> <dt>

<span data-ttu-id="bd868-109">*PacketCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bd868-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd868-110">Nombre de paquets in-air reçus.</span><span class="sxs-lookup"><span data-stu-id="bd868-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="bd868-111">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bd868-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd868-112">Tableau qui contient les données sélectionnées pour le paquet.</span><span class="sxs-lookup"><span data-stu-id="bd868-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="bd868-113">Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="bd868-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd868-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bd868-114">Return value</span></span>

<span data-ttu-id="bd868-115">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bd868-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd868-116">Notes </span><span class="sxs-lookup"><span data-stu-id="bd868-116">Remarks</span></span>

<span data-ttu-id="bd868-117">Un paquet aérien est créé lorsqu’un utilisateur déplace un stylet près de la tablette et que le curseur se trouve dans la fenêtre de l’objet du collecteur d’encre ou lorsque l’utilisateur déplace une souris dans la fenêtre associée de l’objet du collecteur.</span><span class="sxs-lookup"><span data-stu-id="bd868-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="bd868-118">Les événements **NewInAirPackets** sont générés rapidement et le gestionnaire d’événements doit être rapide ou en pâtit d’une performance.</span><span class="sxs-lookup"><span data-stu-id="bd868-118">**NewInAirPackets** events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="bd868-119">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ ICENewInAirPackets.</span><span class="sxs-lookup"><span data-stu-id="bd868-119">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="bd868-120">L’événement **NewInAirPackets** est déclenché même en mode SELECT ou Erase, pas uniquement lors de l’insertion d’une entrée manuscrite.</span><span class="sxs-lookup"><span data-stu-id="bd868-120">The **NewInAirPackets** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="bd868-121">Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement.</span><span class="sxs-lookup"><span data-stu-id="bd868-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="bd868-122">L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.</span><span class="sxs-lookup"><span data-stu-id="bd868-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="bd868-123">Pour définir les propriétés contenues dans ce tableau, utilisez la propriété [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) de l’objet Ink collector.</span><span class="sxs-lookup"><span data-stu-id="bd868-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="bd868-124">Le tableau retourné par le paramètre *PacketData* contient les données de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bd868-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="bd868-125">Bien que vous puissiez modifier les données du paquet, ces modifications ne sont pas conservées ou utilisées.</span><span class="sxs-lookup"><span data-stu-id="bd868-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bd868-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd868-126">Requirements</span></span>



| <span data-ttu-id="bd868-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd868-127">Requirement</span></span> | <span data-ttu-id="bd868-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd868-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd868-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd868-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bd868-130">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd868-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="bd868-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd868-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bd868-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd868-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="bd868-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd868-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd868-134"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bd868-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bd868-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bd868-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="bd868-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd868-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="bd868-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd868-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd868-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="bd868-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="bd868-139">**Propriété DesiredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="bd868-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="bd868-140">**Événement NewPackets**</span><span class="sxs-lookup"><span data-stu-id="bd868-140">**NewPackets Event**</span></span>](inkpicture-newpackets.md)
</dt> <dt>

[<span data-ttu-id="bd868-141">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="bd868-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




