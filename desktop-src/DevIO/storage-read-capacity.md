---
description: Contient des informations sur la taille d’un appareil. Elle est retournée à partir du \_ Code de contrôle de capacité de lecture du stockage IOCTL \_ \_ .
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: Structure STORAGE_READ_CAPACITY (Ntddstor. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_READ_CAPACITY
api_type:
- HeaderDef
api_location:
- Ntddstor.h
ms.openlocfilehash: e57a9f4420b977598e15f9aae219c060665c9d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392991"
---
# <a name="storage_read_capacity-structure"></a><span data-ttu-id="3e820-104">Structure de la capacité de lecture du stockage \_ \_</span><span class="sxs-lookup"><span data-stu-id="3e820-104">STORAGE\_READ\_CAPACITY structure</span></span>

<span data-ttu-id="3e820-105">Contient des informations sur la taille d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="3e820-105">Contains information about the size of a device.</span></span> <span data-ttu-id="3e820-106">Elle est retournée à partir du code de contrôle de [**\_ capacité de \_ lecture \_ du stockage IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) .</span><span class="sxs-lookup"><span data-stu-id="3e820-106">This is returned from the [**IOCTL\_STORAGE\_READ\_CAPACITY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e820-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e820-107">Syntax</span></span>


```C++
typedef struct _STORAGE_READ_CAPACITY {
  ULONG         Version;
  ULONG         Size;
  ULONG         BlockLength;
  LARGE_INTEGER NumberOfBlocks;
  LARGE_INTEGER DiskLength;
} STORAGE_READ_CAPACITY, *PSTORAGE_READ_CAPACITY;
```



## <a name="members"></a><span data-ttu-id="3e820-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3e820-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3e820-109">**Version**</span><span class="sxs-lookup"><span data-stu-id="3e820-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="3e820-110">Version de cette structure.</span><span class="sxs-lookup"><span data-stu-id="3e820-110">The version of this structure.</span></span> <span data-ttu-id="3e820-111">L’appelant doit affecter à ce membre la valeur `sizeof(STORAGE_READ_CAPACITY)` .</span><span class="sxs-lookup"><span data-stu-id="3e820-111">The caller must set this member to `sizeof(STORAGE_READ_CAPACITY)`.</span></span>

</dd> <dt>

<span data-ttu-id="3e820-112">**Taille**</span><span class="sxs-lookup"><span data-stu-id="3e820-112">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="3e820-113">Taille des données retournées.</span><span class="sxs-lookup"><span data-stu-id="3e820-113">The size of the data returned.</span></span>

</dd> <dt>

<span data-ttu-id="3e820-114">**BlockLength**</span><span class="sxs-lookup"><span data-stu-id="3e820-114">**BlockLength**</span></span>
</dt> <dd>

<span data-ttu-id="3e820-115">Nombre d’octets par bloc.</span><span class="sxs-lookup"><span data-stu-id="3e820-115">The number of bytes per block.</span></span>

</dd> <dt>

<span data-ttu-id="3e820-116">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="3e820-116">**NumberOfBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="3e820-117">Nombre total de blocs sur le disque.</span><span class="sxs-lookup"><span data-stu-id="3e820-117">The total number of blocks on the disk.</span></span>

</dd> <dt>

<span data-ttu-id="3e820-118">**DiskLength**</span><span class="sxs-lookup"><span data-stu-id="3e820-118">**DiskLength**</span></span>
</dt> <dd>

<span data-ttu-id="3e820-119">Taille du disque en octets.</span><span class="sxs-lookup"><span data-stu-id="3e820-119">The disk size in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e820-120">Notes</span><span class="sxs-lookup"><span data-stu-id="3e820-120">Remarks</span></span>

<span data-ttu-id="3e820-121">Le fichier d’en-tête Ntddstor. h est disponible dans le kit WDK (Windows Driver Kit).</span><span class="sxs-lookup"><span data-stu-id="3e820-121">The header file Ntddstor.h is available in the Windows Driver Kit (WDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e820-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e820-122">Requirements</span></span>



| <span data-ttu-id="3e820-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e820-123">Requirement</span></span> | <span data-ttu-id="3e820-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e820-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e820-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e820-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3e820-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e820-126">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="3e820-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e820-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3e820-128">Windows Server 2008, Windows Server 2003 avec SP1</span><span class="sxs-lookup"><span data-stu-id="3e820-128">Windows Server 2008, Windows Server 2003 with SP1</span></span><br/>                          |
| <span data-ttu-id="3e820-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e820-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e820-130"><dt>Ntddstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e820-130"><dt>Ntddstor.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e820-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e820-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e820-132">**\_capacité de \_ lecture du stockage IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="3e820-132">**IOCTL\_STORAGE\_READ\_CAPACITY**</span></span>](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




