---
description: Décrit les architectures d’ordinateur possibles.
ms.assetid: 1E5E4F98-925B-424D-9B3D-BC6716FBF990
title: Constantes d’ordinateur de fichier image (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c43767ce0d86edf2285241772ea060573efc1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193723"
---
# <a name="image-file-machine-constants"></a>Constantes d’ordinateur de fichier image

Décrit les architectures d’ordinateur possibles. Utilisé dans [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) et [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).

<dl> <dt>

<span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**\_ordinateur de fichier image \_ \_ inconnu**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Unknown


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**IMAGE de l' \_ \_ ordinateur \_ \_ hôte cible de l’ordinateur**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Interagit avec l’hôte et non un invité WOW64

> [!Note]  
> cette constante est disponible à partir de Windows 10, version 1607 et Windows Server 2016.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**\_Fichier image \_ ordinateur \_ i386**
</dt> <dd> <dl> <dt>

0x014c
</dt> <dt>



Intel 386


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**\_Ordinateur de fichier image \_ \_ R3000**
</dt> <dd> <dl> <dt>

0x0162
</dt> <dt>



Big endian de MIPS, 0x160 Big-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**\_Ordinateur de fichier image \_ \_ R4000**
</dt> <dd> <dl> <dt>

0x0166
</dt> <dt>



Big-endian MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**\_Ordinateur de fichier image \_ \_ R10000**
</dt> <dd> <dl> <dt>

0x0168
</dt> <dt>



Big-endian MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**\_Ordinateur de fichier image \_ \_ WCEMIPSV2**
</dt> <dd> <dl> <dt>

0x0169
</dt> <dt>



minimum de MIPS-endian WCE v2


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**\_ordinateur de fichier image \_ \_ alpha**
</dt> <dd> <dl> <dt>

0x0184
</dt> <dt>



Alpha \_ AXP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**\_Ordinateur du fichier image \_ \_ SH3**
</dt> <dd> <dl> <dt>

0x01a2
</dt> <dt>



SH3 Little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**\_Ordinateur de fichier image \_ \_ SH3DSP**
</dt> <dd> <dl> <dt>

0x01a3
</dt> <dt>



SH3DSP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**\_Ordinateur de fichier image \_ \_ SH3E**
</dt> <dd> <dl> <dt>

0x01a4
</dt> <dt>



SH3E Little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**\_Machine fichier \_ image \_ sh4**
</dt> <dd> <dl> <dt>

0x01a6
</dt> <dt>



SH4 Little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**\_Ordinateur de fichier image \_ \_ SH5**
</dt> <dd> <dl> <dt>

0x01a8
</dt> <dt>



SH5


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**fichier IMAGE bras de l' \_ \_ ordinateur \_**
</dt> <dd> <dl> <dt>

0x01c0
</dt> <dt>



Little-Endian ARM


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**curseur de l' \_ ordinateur du fichier image \_ \_**
</dt> <dd> <dl> <dt>

0x01c2
</dt> <dt>



Little-Endian ARM/Thumb-2


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**\_ordinateur de fichier image \_ \_ ARMNT**
</dt> <dd> <dl> <dt>

0x01c4
</dt> <dt>



ARM Thumb-2 Little-Endian

> [!Note]  
> cette constante est disponible à partir de Windows 7 et Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**\_Ordinateur de fichier image \_ \_ AM33**
</dt> <dd> <dl> <dt>

0x01d3
</dt> <dt>



TAM33BD


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**\_fichier image \_ ordinateur \_ powerpc**
</dt> <dd> <dl> <dt>

0x01F0
</dt> <dt>



Little-Endian IBM PowerPC


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**\_ordinateur de fichier image \_ \_ POWERPCFP**
</dt> <dd> <dl> <dt>

0x01f1
</dt> <dt>



POWERPCFP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**\_Machine de fichier image \_ \_ ia64**
</dt> <dd> <dl> <dt>

0x0200
</dt> <dt>



Intel 64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**\_Ordinateur de fichier image \_ \_ MIPS16**
</dt> <dd> <dl> <dt>

0x0266
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**\_Ordinateur de fichier image \_ \_ ALPHA64**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



ALPHA64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**\_ordinateur de fichier image \_ \_ MIPSFPU**
</dt> <dd> <dl> <dt>

0x0366
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**\_Ordinateur de fichier image \_ \_ MIPSFPU16**
</dt> <dd> <dl> <dt>

0x0466
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**\_Ordinateur de fichier image \_ \_ AXP64**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



AXP64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**\_ordinateur de fichier image \_ \_ TriCore**
</dt> <dd> <dl> <dt>

0x0520
</dt> <dt>



Infineon


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**\_ordinateur de fichier image \_ \_ CEF**
</dt> <dd> <dl> <dt>

0x0CEF
</dt> <dt>



CEF


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**\_fichier d' \_ image \_ EBC machine**
</dt> <dd> <dl> <dt>

0x0EBC
</dt> <dt>



Code d’octet EFI


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**\_Machine de fichier image \_ \_ amd64**
</dt> <dd> <dl> <dt>

0x8664
</dt> <dt>



AMD64 (K8)


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**\_Ordinateur de fichier image \_ \_ m32r**
</dt> <dd> <dl> <dt>

0x9041
</dt> <dt>



M32R Little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**\_Ordinateur de fichier image \_ \_ ARM64**
</dt> <dd> <dl> <dt>

0xAA64
</dt> <dt>



ARM64 Little-Endian

> [!Note]  
> cette constante est disponible à partir de Windows 8.1 et Windows Server 2012 R2.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**\_machine de fichier image \_ \_ CEE**
</dt> <dd> <dl> <dt>

0xC0EE
</dt> <dt>



CEE


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

 




