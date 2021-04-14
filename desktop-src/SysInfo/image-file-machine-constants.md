---
description: Décrit les architectures d’ordinateur possibles.
ms.assetid: 1E5E4F98-925B-424D-9B3D-BC6716FBF990
title: Constantes d’ordinateur de fichier image (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c43767ce0d86edf2285241772ea060573efc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526985"
---
# <a name="image-file-machine-constants"></a><span data-ttu-id="30b1c-103">Constantes d’ordinateur de fichier image</span><span class="sxs-lookup"><span data-stu-id="30b1c-103">Image File Machine Constants</span></span>

<span data-ttu-id="30b1c-104">Décrit les architectures d’ordinateur possibles.</span><span class="sxs-lookup"><span data-stu-id="30b1c-104">Describes possible machine architectures.</span></span> <span data-ttu-id="30b1c-105">Utilisé dans [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) et [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).</span><span class="sxs-lookup"><span data-stu-id="30b1c-105">Used in [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) and [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).</span></span>

<dl> <dt>

<span data-ttu-id="30b1c-106"><span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**\_ordinateur de fichier image \_ \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="30b1c-106"><span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**IMAGE\_FILE\_MACHINE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-107">0</span><span class="sxs-lookup"><span data-stu-id="30b1c-107">0</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-108">Unknown</span><span class="sxs-lookup"><span data-stu-id="30b1c-108">Unknown</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-109"><span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**IMAGE de l' \_ \_ ordinateur \_ \_ hôte cible de l’ordinateur**</span><span class="sxs-lookup"><span data-stu-id="30b1c-109"><span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**IMAGE\_FILE\_MACHINE\_TARGET\_HOST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="30b1c-110">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-111">Interagit avec l’hôte et non un invité WOW64</span><span class="sxs-lookup"><span data-stu-id="30b1c-111">Interacts with the host and not a WOW64 guest</span></span>

> [!Note]  
> <span data-ttu-id="30b1c-112">Cette constante est disponible à partir de Windows 10, version 1607 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="30b1c-112">This constant is available starting with Windows 10, version 1607 and Windows Server 2016.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-113"><span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**\_Fichier image \_ ordinateur \_ i386**</span><span class="sxs-lookup"><span data-stu-id="30b1c-113"><span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**IMAGE\_FILE\_MACHINE\_I386**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-114">0x014c</span><span class="sxs-lookup"><span data-stu-id="30b1c-114">0x014c</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-115">Intel 386</span><span class="sxs-lookup"><span data-stu-id="30b1c-115">Intel 386</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-116"><span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**\_Ordinateur de fichier image \_ \_ R3000**</span><span class="sxs-lookup"><span data-stu-id="30b1c-116"><span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**IMAGE\_FILE\_MACHINE\_R3000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-117">0x0162</span><span class="sxs-lookup"><span data-stu-id="30b1c-117">0x0162</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-118">Big endian de MIPS, 0x160 Big-endian</span><span class="sxs-lookup"><span data-stu-id="30b1c-118">MIPS little-endian, 0x160 big-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-119"><span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**\_Ordinateur de fichier image \_ \_ R4000**</span><span class="sxs-lookup"><span data-stu-id="30b1c-119"><span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**IMAGE\_FILE\_MACHINE\_R4000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-120">0x0166</span><span class="sxs-lookup"><span data-stu-id="30b1c-120">0x0166</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-121">Big-endian MIPS</span><span class="sxs-lookup"><span data-stu-id="30b1c-121">MIPS little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-122"><span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**\_Ordinateur de fichier image \_ \_ R10000**</span><span class="sxs-lookup"><span data-stu-id="30b1c-122"><span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**IMAGE\_FILE\_MACHINE\_R10000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-123">0x0168</span><span class="sxs-lookup"><span data-stu-id="30b1c-123">0x0168</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-124">Big-endian MIPS</span><span class="sxs-lookup"><span data-stu-id="30b1c-124">MIPS little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-125"><span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**\_Ordinateur de fichier image \_ \_ WCEMIPSV2**</span><span class="sxs-lookup"><span data-stu-id="30b1c-125"><span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**IMAGE\_FILE\_MACHINE\_WCEMIPSV2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-126">0x0169</span><span class="sxs-lookup"><span data-stu-id="30b1c-126">0x0169</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-127">MIPS Little-endian WCE v2</span><span class="sxs-lookup"><span data-stu-id="30b1c-127">MIPS little-endian WCE v2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-128"><span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**\_ordinateur de fichier image \_ \_ alpha**</span><span class="sxs-lookup"><span data-stu-id="30b1c-128"><span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**IMAGE\_FILE\_MACHINE\_ALPHA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-129">0x0184</span><span class="sxs-lookup"><span data-stu-id="30b1c-129">0x0184</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-130">Alpha \_ AXP</span><span class="sxs-lookup"><span data-stu-id="30b1c-130">Alpha\_AXP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-131"><span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**\_Ordinateur du fichier image \_ \_ SH3**</span><span class="sxs-lookup"><span data-stu-id="30b1c-131"><span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**IMAGE\_FILE\_MACHINE\_SH3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-132">0x01a2</span><span class="sxs-lookup"><span data-stu-id="30b1c-132">0x01a2</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-133">SH3 Little-endian</span><span class="sxs-lookup"><span data-stu-id="30b1c-133">SH3 little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-134"><span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**\_Ordinateur de fichier image \_ \_ SH3DSP**</span><span class="sxs-lookup"><span data-stu-id="30b1c-134"><span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**IMAGE\_FILE\_MACHINE\_SH3DSP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-135">0x01a3</span><span class="sxs-lookup"><span data-stu-id="30b1c-135">0x01a3</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-136">SH3DSP</span><span class="sxs-lookup"><span data-stu-id="30b1c-136">SH3DSP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-137"><span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**\_Ordinateur de fichier image \_ \_ SH3E**</span><span class="sxs-lookup"><span data-stu-id="30b1c-137"><span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**IMAGE\_FILE\_MACHINE\_SH3E**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-138">0x01a4</span><span class="sxs-lookup"><span data-stu-id="30b1c-138">0x01a4</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-139">SH3E Little-endian</span><span class="sxs-lookup"><span data-stu-id="30b1c-139">SH3E little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-140"><span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**\_Machine fichier \_ image \_ sh4**</span><span class="sxs-lookup"><span data-stu-id="30b1c-140"><span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**IMAGE\_FILE\_MACHINE\_SH4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-141">0x01a6</span><span class="sxs-lookup"><span data-stu-id="30b1c-141">0x01a6</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-142">SH4 Little-endian</span><span class="sxs-lookup"><span data-stu-id="30b1c-142">SH4 little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-143"><span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**\_Ordinateur de fichier image \_ \_ SH5**</span><span class="sxs-lookup"><span data-stu-id="30b1c-143"><span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**IMAGE\_FILE\_MACHINE\_SH5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-144">0x01a8</span><span class="sxs-lookup"><span data-stu-id="30b1c-144">0x01a8</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-145">SH5</span><span class="sxs-lookup"><span data-stu-id="30b1c-145">SH5</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-146"><span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**fichier IMAGE bras de l' \_ \_ ordinateur \_**</span><span class="sxs-lookup"><span data-stu-id="30b1c-146"><span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**IMAGE\_FILE\_MACHINE\_ARM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-147">0x01c0</span><span class="sxs-lookup"><span data-stu-id="30b1c-147">0x01c0</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-148">Little-Endian ARM</span><span class="sxs-lookup"><span data-stu-id="30b1c-148">ARM Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-149"><span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**curseur de l' \_ ordinateur du fichier image \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30b1c-149"><span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**IMAGE\_FILE\_MACHINE\_THUMB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-150">0x01c2</span><span class="sxs-lookup"><span data-stu-id="30b1c-150">0x01c2</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-151">Little-Endian ARM/Thumb-2</span><span class="sxs-lookup"><span data-stu-id="30b1c-151">ARM Thumb/Thumb-2 Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-152"><span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**\_ordinateur de fichier image \_ \_ ARMNT**</span><span class="sxs-lookup"><span data-stu-id="30b1c-152"><span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**IMAGE\_FILE\_MACHINE\_ARMNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-153">0x01c4</span><span class="sxs-lookup"><span data-stu-id="30b1c-153">0x01c4</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-154">ARM Thumb-2 Little-Endian</span><span class="sxs-lookup"><span data-stu-id="30b1c-154">ARM Thumb-2 Little-Endian</span></span>

> [!Note]  
> <span data-ttu-id="30b1c-155">Cette constante est disponible à partir de Windows 7 et de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="30b1c-155">This constant is available starting with Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-156"><span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**\_Ordinateur de fichier image \_ \_ AM33**</span><span class="sxs-lookup"><span data-stu-id="30b1c-156"><span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**IMAGE\_FILE\_MACHINE\_AM33**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-157">0x01d3</span><span class="sxs-lookup"><span data-stu-id="30b1c-157">0x01d3</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-158">TAM33BD</span><span class="sxs-lookup"><span data-stu-id="30b1c-158">TAM33BD</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-159"><span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**\_fichier image \_ ordinateur \_ powerpc**</span><span class="sxs-lookup"><span data-stu-id="30b1c-159"><span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**IMAGE\_FILE\_MACHINE\_POWERPC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-160">0x01F0</span><span class="sxs-lookup"><span data-stu-id="30b1c-160">0x01F0</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-161">Little-Endian IBM PowerPC</span><span class="sxs-lookup"><span data-stu-id="30b1c-161">IBM PowerPC Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-162"><span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**\_ordinateur de fichier image \_ \_ POWERPCFP**</span><span class="sxs-lookup"><span data-stu-id="30b1c-162"><span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**IMAGE\_FILE\_MACHINE\_POWERPCFP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-163">0x01f1</span><span class="sxs-lookup"><span data-stu-id="30b1c-163">0x01f1</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-164">POWERPCFP</span><span class="sxs-lookup"><span data-stu-id="30b1c-164">POWERPCFP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-165"><span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**\_Machine de fichier image \_ \_ ia64**</span><span class="sxs-lookup"><span data-stu-id="30b1c-165"><span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**IMAGE\_FILE\_MACHINE\_IA64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-166">0x0200</span><span class="sxs-lookup"><span data-stu-id="30b1c-166">0x0200</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-167">Intel 64</span><span class="sxs-lookup"><span data-stu-id="30b1c-167">Intel 64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-168"><span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**\_Ordinateur de fichier image \_ \_ MIPS16**</span><span class="sxs-lookup"><span data-stu-id="30b1c-168"><span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**IMAGE\_FILE\_MACHINE\_MIPS16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-169">0x0266</span><span class="sxs-lookup"><span data-stu-id="30b1c-169">0x0266</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-170">MIPS</span><span class="sxs-lookup"><span data-stu-id="30b1c-170">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-171"><span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**\_Ordinateur de fichier image \_ \_ ALPHA64**</span><span class="sxs-lookup"><span data-stu-id="30b1c-171"><span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**IMAGE\_FILE\_MACHINE\_ALPHA64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-172">0x0284</span><span class="sxs-lookup"><span data-stu-id="30b1c-172">0x0284</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-173">ALPHA64</span><span class="sxs-lookup"><span data-stu-id="30b1c-173">ALPHA64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-174"><span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**\_ordinateur de fichier image \_ \_ MIPSFPU**</span><span class="sxs-lookup"><span data-stu-id="30b1c-174"><span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**IMAGE\_FILE\_MACHINE\_MIPSFPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-175">0x0366</span><span class="sxs-lookup"><span data-stu-id="30b1c-175">0x0366</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-176">MIPS</span><span class="sxs-lookup"><span data-stu-id="30b1c-176">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-177"><span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**\_Ordinateur de fichier image \_ \_ MIPSFPU16**</span><span class="sxs-lookup"><span data-stu-id="30b1c-177"><span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**IMAGE\_FILE\_MACHINE\_MIPSFPU16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-178">0x0466</span><span class="sxs-lookup"><span data-stu-id="30b1c-178">0x0466</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-179">MIPS</span><span class="sxs-lookup"><span data-stu-id="30b1c-179">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-180"><span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**\_Ordinateur de fichier image \_ \_ AXP64**</span><span class="sxs-lookup"><span data-stu-id="30b1c-180"><span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**IMAGE\_FILE\_MACHINE\_AXP64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-181">0x0284</span><span class="sxs-lookup"><span data-stu-id="30b1c-181">0x0284</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-182">AXP64</span><span class="sxs-lookup"><span data-stu-id="30b1c-182">AXP64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-183"><span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**\_ordinateur de fichier image \_ \_ TriCore**</span><span class="sxs-lookup"><span data-stu-id="30b1c-183"><span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**IMAGE\_FILE\_MACHINE\_TRICORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-184">0x0520</span><span class="sxs-lookup"><span data-stu-id="30b1c-184">0x0520</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-185">Infineon</span><span class="sxs-lookup"><span data-stu-id="30b1c-185">Infineon</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-186"><span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**\_ordinateur de fichier image \_ \_ CEF**</span><span class="sxs-lookup"><span data-stu-id="30b1c-186"><span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**IMAGE\_FILE\_MACHINE\_CEF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-187">0x0CEF</span><span class="sxs-lookup"><span data-stu-id="30b1c-187">0x0CEF</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-188">CEF</span><span class="sxs-lookup"><span data-stu-id="30b1c-188">CEF</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-189"><span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**\_fichier d' \_ image \_ EBC machine**</span><span class="sxs-lookup"><span data-stu-id="30b1c-189"><span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**IMAGE\_FILE\_MACHINE\_EBC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-190">0x0EBC</span><span class="sxs-lookup"><span data-stu-id="30b1c-190">0x0EBC</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-191">Code d’octet EFI</span><span class="sxs-lookup"><span data-stu-id="30b1c-191">EFI Byte Code</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-192"><span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**\_Machine de fichier image \_ \_ amd64**</span><span class="sxs-lookup"><span data-stu-id="30b1c-192"><span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**IMAGE\_FILE\_MACHINE\_AMD64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-193">0x8664</span><span class="sxs-lookup"><span data-stu-id="30b1c-193">0x8664</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-194">AMD64 (K8)</span><span class="sxs-lookup"><span data-stu-id="30b1c-194">AMD64 (K8)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-195"><span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**\_Ordinateur de fichier image \_ \_ m32r**</span><span class="sxs-lookup"><span data-stu-id="30b1c-195"><span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**IMAGE\_FILE\_MACHINE\_M32R**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-196">0x9041</span><span class="sxs-lookup"><span data-stu-id="30b1c-196">0x9041</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-197">M32R Little-endian</span><span class="sxs-lookup"><span data-stu-id="30b1c-197">M32R little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-198"><span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**\_Ordinateur de fichier image \_ \_ ARM64**</span><span class="sxs-lookup"><span data-stu-id="30b1c-198"><span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**IMAGE\_FILE\_MACHINE\_ARM64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-199">0xAA64</span><span class="sxs-lookup"><span data-stu-id="30b1c-199">0xAA64</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-200">ARM64 Little-Endian</span><span class="sxs-lookup"><span data-stu-id="30b1c-200">ARM64 Little-Endian</span></span>

> [!Note]  
> <span data-ttu-id="30b1c-201">Cette constante est disponible à partir de Windows 8.1 et de Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="30b1c-201">This constant is available starting with Windows 8.1 and Windows Server 2012 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="30b1c-202"><span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**\_machine de fichier image \_ \_ CEE**</span><span class="sxs-lookup"><span data-stu-id="30b1c-202"><span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**IMAGE\_FILE\_MACHINE\_CEE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b1c-203">0xC0EE</span><span class="sxs-lookup"><span data-stu-id="30b1c-203">0xC0EE</span></span>
</dt> <dt>



<span data-ttu-id="30b1c-204">CEE</span><span class="sxs-lookup"><span data-stu-id="30b1c-204">CEE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30b1c-205">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30b1c-205">Requirements</span></span>



| <span data-ttu-id="30b1c-206">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30b1c-206">Requirement</span></span> | <span data-ttu-id="30b1c-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="30b1c-207">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="30b1c-208">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30b1c-208">Minimum supported client</span></span><br/> | <span data-ttu-id="30b1c-209">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30b1c-209">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30b1c-210">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30b1c-210">Minimum supported server</span></span><br/> | <span data-ttu-id="30b1c-211">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30b1c-211">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="30b1c-212">En-tête</span><span class="sxs-lookup"><span data-stu-id="30b1c-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="30b1c-213"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="30b1c-213"><dt>Winnt.h</dt></span></span> </dl> |



 

 




