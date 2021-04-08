---
description: Définit la priorité de thread de base pour le lecteur source ou le writer de récepteur.
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: Attribut MF_READWRITE_MMCSS_PRIORITY (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7b83485b49e6ae584a38024e180f37c878d27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035191"
---
# <a name="mf_readwrite_mmcss_priority-attribute"></a><span data-ttu-id="d36d5-103">\_Attribut de \_ priorité MMCSS ReadWrite \_ MF</span><span class="sxs-lookup"><span data-stu-id="d36d5-103">MF\_READWRITE\_MMCSS\_PRIORITY attribute</span></span>

<span data-ttu-id="d36d5-104">Définit la priorité de thread de base pour le lecteur source ou le writer de récepteur.</span><span class="sxs-lookup"><span data-stu-id="d36d5-104">Sets the base thread priority for the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="d36d5-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="d36d5-105">Data type</span></span>

<span data-ttu-id="d36d5-106">**Int32** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d36d5-106">**INT32** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="d36d5-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="d36d5-107">Get/set</span></span>

<span data-ttu-id="d36d5-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="d36d5-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="d36d5-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="d36d5-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="d36d5-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d36d5-110">Remarks</span></span>

<span data-ttu-id="d36d5-111">Vous pouvez éventuellement définir cet attribut lorsque vous créez une instance du [lecteur source](source-reader.md) ou du [writer du récepteur](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="d36d5-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="d36d5-112">Si vous définissez cet attribut, définissez également l’attribut de classe de la [ \_ \_ \_ classe MMCSS ReadWrite MF](mf-readwrite-mmcss-class.md) .</span><span class="sxs-lookup"><span data-stu-id="d36d5-112">If you set this attribute, also set the [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md) attribute.</span></span> <span data-ttu-id="d36d5-113">Dans le cas contraire, cet attribut est ignoré.</span><span class="sxs-lookup"><span data-stu-id="d36d5-113">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="d36d5-114">Lorsque le lecteur source ou l’enregistreur du récepteur enregistre les threads avec le [service Planificateur de classes multimédias](../procthread/multimedia-class-scheduler-service.md), la valeur de cet attribut spécifie la priorité de thread de base.</span><span class="sxs-lookup"><span data-stu-id="d36d5-114">When the Source Reader or Sink Writer registers threads with the [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md), the value of this attribute specifies the base thread priority.</span></span> <span data-ttu-id="d36d5-115">Si cet attribut n’est pas défini, la valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="d36d5-115">If this attribute is not set, the default value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d36d5-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d36d5-116">Requirements</span></span>



| <span data-ttu-id="d36d5-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d36d5-117">Requirement</span></span> | <span data-ttu-id="d36d5-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d36d5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d36d5-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d36d5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d36d5-120">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d36d5-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="d36d5-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d36d5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d36d5-122">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="d36d5-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="d36d5-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d36d5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d36d5-124"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="d36d5-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d36d5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d36d5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d36d5-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d36d5-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
