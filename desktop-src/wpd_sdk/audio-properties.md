---
description: Appareils mobiles Windows prend en charge les propriétés audio suivantes.
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: Propriétés audio (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Audio
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1bdab201fc987d5bc1aff3638fbb57358115fdce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523522"
---
# <a name="audio-properties"></a><span data-ttu-id="6c654-103">Propriétés audio</span><span class="sxs-lookup"><span data-stu-id="6c654-103">Audio Properties</span></span>

<span data-ttu-id="6c654-104">Appareils mobiles Windows prend en charge les propriétés audio suivantes.</span><span class="sxs-lookup"><span data-stu-id="6c654-104">Windows Portable Devices supports the following audio properties.</span></span>



| <span data-ttu-id="6c654-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="6c654-105">Property</span></span>                         | <span data-ttu-id="6c654-106">VarType</span><span class="sxs-lookup"><span data-stu-id="6c654-106">VarType</span></span>     | <span data-ttu-id="6c654-107">Description</span><span class="sxs-lookup"><span data-stu-id="6c654-107">Description</span></span>                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c654-108">**\_profondeur de \_ bits \_ audio wpd**</span><span class="sxs-lookup"><span data-stu-id="6c654-108">**WPD\_AUDIO\_BIT\_DEPTH**</span></span>       | <span data-ttu-id="6c654-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="6c654-109">**VT\_UI4**</span></span> | <span data-ttu-id="6c654-110">Profondeur du bit de l’audio.</span><span class="sxs-lookup"><span data-stu-id="6c654-110">The bit-depth of the audio.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="6c654-111">**\_ \_ débit binaire wpd**</span><span class="sxs-lookup"><span data-stu-id="6c654-111">**WPD\_AUDIO\_BITRATE**</span></span>          | <span data-ttu-id="6c654-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="6c654-112">**VT\_UI4**</span></span> | <span data-ttu-id="6c654-113">Vitesse de transmission de l’audio, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="6c654-113">The bit rate of the audio, in bits per second.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="6c654-114">**\_alignement des \_ blocs \_ audio wpd**</span><span class="sxs-lookup"><span data-stu-id="6c654-114">**WPD\_AUDIO\_BLOCK\_ALIGNMENT**</span></span> | <span data-ttu-id="6c654-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="6c654-115">**VT\_UI4**</span></span> | <span data-ttu-id="6c654-116">Alignement de bloc du fichier audio, en octets.</span><span class="sxs-lookup"><span data-stu-id="6c654-116">The block alignment of the audio file, in bytes.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="6c654-117">**\_nombre de \_ canaux \_ audio wpd**</span><span class="sxs-lookup"><span data-stu-id="6c654-117">**WPD\_AUDIO\_CHANNEL\_COUNT**</span></span>   | <span data-ttu-id="6c654-118">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="6c654-118">**VT\_R4**</span></span>  | <span data-ttu-id="6c654-119">Nombre de canaux dans ce fichier audio, par exemple 1, 2 ou 5,1.</span><span class="sxs-lookup"><span data-stu-id="6c654-119">The number of channels in this audio file, for example, 1, 2, or 5.1.</span></span>                                                                                                                                              |
| <span data-ttu-id="6c654-120">**\_Code de \_ format \_ audio wpd**</span><span class="sxs-lookup"><span data-stu-id="6c654-120">**WPD\_AUDIO\_FORMAT\_CODE**</span></span>     | <span data-ttu-id="6c654-121">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="6c654-121">**VT\_UI4**</span></span> | <span data-ttu-id="6c654-122">Numéro de code du format WAVE enregistré.</span><span class="sxs-lookup"><span data-stu-id="6c654-122">The registered WAVE format code number.</span></span> <span data-ttu-id="6c654-123">Pour obtenir la liste des formats WAVE inscrits, consultez l’article sur les [codes FourCC et les formats Wave inscrits](https://msdn2.microsoft.com/library/ms867195.aspx) sur le site Web MSDN.</span><span class="sxs-lookup"><span data-stu-id="6c654-123">For a listing of registered WAVE formats, see the article [Registered FOURCC Codes and WAVE Formats](https://msdn2.microsoft.com/library/ms867195.aspx) on the MSDN Web site.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6c654-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c654-124">Requirements</span></span>



| <span data-ttu-id="6c654-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c654-125">Requirement</span></span> | <span data-ttu-id="6c654-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c654-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c654-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c654-127">Header</span></span><br/> | <dl> <span data-ttu-id="6c654-128"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c654-128"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c654-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c654-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c654-130">**Propriétés et attributs WPD**</span><span class="sxs-lookup"><span data-stu-id="6c654-130">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




