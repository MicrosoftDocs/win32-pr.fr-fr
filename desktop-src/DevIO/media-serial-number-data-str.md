---
description: Contient le numéro de série d’un périphérique USB. Elle est utilisée par le \_ Code de contrôle du numéro de série du support de stockage IOCTL \_ \_ \_ \_ .
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: Structure MEDIA_SERIAL_NUMBER_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SERIAL_NUMBER_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 843c445a29bcce9e6dc26b66b0c6738831e9b79c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106539788"
---
# <a name="media_serial_number_data-structure"></a><span data-ttu-id="bfc3c-104">\_Structure de \_ données du numéro de série du support \_</span><span class="sxs-lookup"><span data-stu-id="bfc3c-104">MEDIA\_SERIAL\_NUMBER\_DATA structure</span></span>

<span data-ttu-id="bfc3c-105">Contient le numéro de série d’un périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="bfc3c-105">Contains the serial number of a USB device.</span></span> <span data-ttu-id="bfc3c-106">Elle est utilisée par le code de contrôle du [**\_ numéro de \_ \_ \_ série \_ du support de stockage IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) .</span><span class="sxs-lookup"><span data-stu-id="bfc3c-106">It is used by the [**IOCTL\_STORAGE\_GET\_MEDIA\_SERIAL\_NUMBER**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfc3c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfc3c-107">Syntax</span></span>


```C++
typedef struct _MEDIA_SERIAL_NUMBER_DATA {
  ULONG SerialNumberLength;
  ULONG Result;
  ULONG Reserved[2];
  UCHAR SerialNumberData[];
} MEDIA_SERIAL_NUMBER_DATA, *PMEDIA_SERIAL_NUMBER_DATA;
```



## <a name="members"></a><span data-ttu-id="bfc3c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="bfc3c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="bfc3c-109">**SerialNumberLength**</span><span class="sxs-lookup"><span data-stu-id="bfc3c-109">**SerialNumberLength**</span></span>
</dt> <dd>

<span data-ttu-id="bfc3c-110">Taille de la chaîne **SerialNumberData** , en octets.</span><span class="sxs-lookup"><span data-stu-id="bfc3c-110">The size of the **SerialNumberData** string, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="bfc3c-111">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="bfc3c-111">**Result**</span></span>
</dt> <dd>

<span data-ttu-id="bfc3c-112">État de la demande.</span><span class="sxs-lookup"><span data-stu-id="bfc3c-112">The status of the request.</span></span>

</dd> <dt>

<span data-ttu-id="bfc3c-113">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="bfc3c-113">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="bfc3c-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="bfc3c-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bfc3c-115">**SerialNumberData**</span><span class="sxs-lookup"><span data-stu-id="bfc3c-115">**SerialNumberData**</span></span>
</dt> <dd>

<span data-ttu-id="bfc3c-116">Numéro de série de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bfc3c-116">The serial number of the device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfc3c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="bfc3c-117">Remarks</span></span>

<span data-ttu-id="bfc3c-118">Aucun fichier d’en-tête n’est disponible pour la structure de **données du numéro de série du support \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="bfc3c-118">No header file is available for the **MEDIA\_SERIAL\_NUMBER\_DATA** structure.</span></span> <span data-ttu-id="bfc3c-119">Incluez la définition de la structure en haut de cette page dans votre code source.</span><span class="sxs-lookup"><span data-stu-id="bfc3c-119">Include the structure definition at the top of this page in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfc3c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfc3c-120">Requirements</span></span>



| <span data-ttu-id="bfc3c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfc3c-121">Requirement</span></span> | <span data-ttu-id="bfc3c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfc3c-122">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="bfc3c-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfc3c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bfc3c-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bfc3c-124">Windows XP</span></span><br/>          |
| <span data-ttu-id="bfc3c-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfc3c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bfc3c-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bfc3c-126">Windows Server 2003</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bfc3c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfc3c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfc3c-128">**\_numéro de \_ série du support d’extraction du stockage IOCTL \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bfc3c-128">**IOCTL\_STORAGE\_GET\_MEDIA\_SERIAL\_NUMBER**</span></span>](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




