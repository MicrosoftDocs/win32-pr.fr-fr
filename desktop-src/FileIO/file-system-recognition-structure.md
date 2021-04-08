---
description: Contient les informations de reconnaissance du système de fichiers sur disque stockées dans le secteur de démarrage des volumes (secteur du disque logique zéro).
ms.assetid: d9c19e01-ff82-4bbc-9eb6-aac9dc5c34ac
title: STRUCTURE FILE_SYSTEM_RECOGNITION_STRUCTURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_SYSTEM_RECOGNITION_STRUCTURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c542b2b9ee1cd1696c7c95797c7df20aa02180cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034273"
---
# <a name="file_system_recognition_structure-structure"></a><span data-ttu-id="7a872-103">Structure de la structure de reconnaissance du système de fichiers \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="7a872-103">FILE\_SYSTEM\_RECOGNITION\_STRUCTURE structure</span></span>

<span data-ttu-id="7a872-104">Contient les informations de reconnaissance du système de fichiers sur disque stockées dans le secteur de démarrage du volume (secteur du disque logique zéro).</span><span class="sxs-lookup"><span data-stu-id="7a872-104">Contains the on-disk file system recognition information stored in the volume's boot sector (logical disk sector zero).</span></span>

<span data-ttu-id="7a872-105">Il s’agit d’une structure de données définie en interne qui n’est pas disponible dans un en-tête public et est fournie ici pour les développeurs de système de fichiers qui souhaitent tirer parti de la reconnaissance du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7a872-105">This is an internally-defined data structure not available in a public header and is provided here for file system developers who want to take advantage of file system recognition.</span></span> <span data-ttu-id="7a872-106">Pour plus d’informations, consultez [reconnaissance du système de fichiers](file-system-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="7a872-106">For more information, see [File System Recognition](file-system-recognition.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a872-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a872-107">Syntax</span></span>


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE;
```



## <a name="members"></a><span data-ttu-id="7a872-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7a872-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a872-109">**JMP**</span><span class="sxs-lookup"><span data-stu-id="7a872-109">**Jmp**</span></span>
</dt> <dd>

<span data-ttu-id="7a872-110">Instruction JMP.</span><span class="sxs-lookup"><span data-stu-id="7a872-110">The JMP instruction.</span></span> <span data-ttu-id="7a872-111">Ce membre de données n’est pas inclus dans la valeur contenue dans le membre de la **somme de contrôle** .</span><span class="sxs-lookup"><span data-stu-id="7a872-111">This data member is not included in the value contained in the **Checksum** data member.</span></span>

</dd> <dt>

<span data-ttu-id="7a872-112">**FsName**</span><span class="sxs-lookup"><span data-stu-id="7a872-112">**FsName**</span></span>
</dt> <dd>

<span data-ttu-id="7a872-113">Nom du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7a872-113">The file system name.</span></span> <span data-ttu-id="7a872-114">Il s’agit d’une séquence de 8 caractères ASCII qui représente le nom explicite non localisable du système de fichiers avec lequel le volume est mis en forme.</span><span class="sxs-lookup"><span data-stu-id="7a872-114">This is a sequence of 8 ASCII characters that represents the nonlocalizable human-readable name of the file system the volume is formatted with.</span></span>

<span data-ttu-id="7a872-115">Cette chaîne se trouve au même emplacement que le nom du système de fichiers OEM sur un disque avec une structure de bloc de paramètres BIOS normale (BPB).</span><span class="sxs-lookup"><span data-stu-id="7a872-115">This string is in the same place as the OEM file system name on a disk with a normal BIOS parameter block (BPB) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7a872-116">**MustBeZero**</span><span class="sxs-lookup"><span data-stu-id="7a872-116">**MustBeZero**</span></span>
</dt> <dd>

<span data-ttu-id="7a872-117">Espace réservé qui contient des zéros.</span><span class="sxs-lookup"><span data-stu-id="7a872-117">Reserved space that contains all zeros.</span></span>

<span data-ttu-id="7a872-118">Ce membre de données chevauche ce qui est normalement les membres de données suivants dans un BPB :</span><span class="sxs-lookup"><span data-stu-id="7a872-118">This data member overlaps what normally are the following data members in a BPB:</span></span>

-   <span data-ttu-id="7a872-119">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="7a872-119">**BytesPerSector**</span></span>
-   <span data-ttu-id="7a872-120">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="7a872-120">**SectorsPerCluster**</span></span>
-   <span data-ttu-id="7a872-121">**ReservedSectorCount**</span><span class="sxs-lookup"><span data-stu-id="7a872-121">**ReservedSectorCount**</span></span>

<span data-ttu-id="7a872-122">Étant donné que ces membres de données ont la valeur zéro, cela doit être suffisant pour obliger les OSs antérieurs à conclure qu’il ne s’agit pas d’un BPB valide et donc de reconnaître le volume.</span><span class="sxs-lookup"><span data-stu-id="7a872-122">Because these data members are set to zero, this should be sufficient to cause earlier OSs to conclude that this is not a valid BPB and therefore recognize the volume.</span></span>

</dd> <dt>

<span data-ttu-id="7a872-123">**Identificateur**</span><span class="sxs-lookup"><span data-stu-id="7a872-123">**Identifier**</span></span>
</dt> <dd>

<span data-ttu-id="7a872-124">Identificateur de la structure</span><span class="sxs-lookup"><span data-stu-id="7a872-124">A structure identifier.</span></span> <span data-ttu-id="7a872-125">Doit contenir la valeur 0x53525346 organisée dans un ordre d’octet Little endian.</span><span class="sxs-lookup"><span data-stu-id="7a872-125">Must contain the value 0x53525346 arranged in little-endian byte order.</span></span>

<span data-ttu-id="7a872-126">À ce stade de la structure, les données sont alignées sur 16 octets.</span><span class="sxs-lookup"><span data-stu-id="7a872-126">At this point in the structure, the data is aligned to 16 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7a872-127">**Durée**</span><span class="sxs-lookup"><span data-stu-id="7a872-127">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="7a872-128">Nombre d’octets dans cette structure, du début à la fin, y compris le membre de données **JMP** .</span><span class="sxs-lookup"><span data-stu-id="7a872-128">The number of bytes in this structure, from the beginning to the end, including the **Jmp** data member.</span></span>

</dd> <dt>

<span data-ttu-id="7a872-129">**EEPROM**</span><span class="sxs-lookup"><span data-stu-id="7a872-129">**Checksum**</span></span>
</dt> <dd>

<span data-ttu-id="7a872-130">Somme de contrôle de deux octets calculée sur les octets à partir du membre de données **FsName** et se terminant au dernier octet de cette structure, à l’exclusion des membres de données **JMP** et **checksum** .</span><span class="sxs-lookup"><span data-stu-id="7a872-130">A two-byte checksum calculated over the bytes starting at the **FsName** data member and ending at the last byte of this structure, excluding the **Jmp** and **Checksum** data members.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a872-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a872-131">Requirements</span></span>



| <span data-ttu-id="7a872-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a872-132">Requirement</span></span> | <span data-ttu-id="7a872-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a872-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7a872-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a872-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7a872-135">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a872-135">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="7a872-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a872-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7a872-137">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a872-137">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a872-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a872-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a872-139">Calcul d’une somme de contrôle de reconnaissance du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="7a872-139">Computing a File System Recognition Checksum</span></span>](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[<span data-ttu-id="7a872-140">Reconnaissance du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="7a872-140">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="7a872-141">**\_ \_ informations sur la reconnaissance du système de fichiers \_**</span><span class="sxs-lookup"><span data-stu-id="7a872-141">**FILE\_SYSTEM\_RECOGNITION\_INFORMATION**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-file_system_recognition_information)
</dt> <dt>

[<span data-ttu-id="7a872-142">**\_reconnaissance du \_ système de fichiers de requête FSCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7a872-142">**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

