---
description: La \_ propriété AudioEngine \_ OEMFormat spécifie le format par défaut de l’appareil utilisé pour le rendu ou la capture d’un flux. Les valeurs sont remplies par le fabricant d’ordinateurs OEM dans un fichier. inf.
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: PKEY_AudioEngine_OEMFormat (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7ed65ae8a7bd717992b13dc7b5517a5725b241
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111311"
---
# <a name="pkey_audioengine_oemformat"></a><span data-ttu-id="d711d-104">\_AudioEngine \_ OEMFormat</span><span class="sxs-lookup"><span data-stu-id="d711d-104">PKEY\_AudioEngine\_OEMFormat</span></span>

<span data-ttu-id="d711d-105">La \_ propriété AudioEngine \_ OEMFormat spécifie le format par défaut de l’appareil utilisé pour le rendu ou la capture d’un flux.</span><span class="sxs-lookup"><span data-stu-id="d711d-105">The PKEY\_AudioEngine\_OEMFormat property specifies the default format of the device that is used for rendering or capturing a stream.</span></span> <span data-ttu-id="d711d-106">Les valeurs sont remplies par le fabricant d’ordinateurs OEM dans un fichier. inf.</span><span class="sxs-lookup"><span data-stu-id="d711d-106">The values are populated by the OEM in an .inf file.</span></span>

<span data-ttu-id="d711d-107">Le membre **VT** de la structure **PROPVARIANT** est défini sur l' \_ objet BLOB VT.</span><span class="sxs-lookup"><span data-stu-id="d711d-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_BLOB.</span></span>

<span data-ttu-id="d711d-108">Le membre **BLOB** de la structure **PROPVARIANT** est une structure de type **BLOB** qui contient deux membres.</span><span class="sxs-lookup"><span data-stu-id="d711d-108">The **blob** member of the **PROPVARIANT** structure is a structure of type **BLOB** that contains two members.</span></span> <span data-ttu-id="d711d-109">BLOB de membre **. cbSize** est une **valeur DWORD** qui spécifie le nombre d’octets dans la description de format.</span><span class="sxs-lookup"><span data-stu-id="d711d-109">Member **blob.cbSize** is a **DWORD** that specifies the number of bytes in the format description.</span></span> <span data-ttu-id="d711d-110">BLOB de membre **. pBlobData** pointe vers une structure **WAVEFORMATEX** qui contient la description de format.</span><span class="sxs-lookup"><span data-stu-id="d711d-110">Member **blob.pBlobData** points to a **WAVEFORMATEX** structure that contains the format description.</span></span> <span data-ttu-id="d711d-111">Pour plus d’informations sur les objets BLOB, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="d711d-111">For more information about BLOB, see the Windows SDK documentation.</span></span> <span data-ttu-id="d711d-112">Pour plus d’informations sur **WAVEFORMATEX**, consultez la documentation de Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="d711d-112">For more information about **WAVEFORMATEX**, see the Windows DDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="d711d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d711d-113">Requirements</span></span>



| <span data-ttu-id="d711d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d711d-114">Requirement</span></span> | <span data-ttu-id="d711d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d711d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d711d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d711d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d711d-117">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d711d-117">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d711d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d711d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d711d-119">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d711d-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d711d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d711d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d711d-121"><dt>MMDeviceAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d711d-121"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d711d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d711d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d711d-123">**Propriétés du point de terminaison audio**</span><span class="sxs-lookup"><span data-stu-id="d711d-123">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="d711d-124">Propriétés audio principales</span><span class="sxs-lookup"><span data-stu-id="d711d-124">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




