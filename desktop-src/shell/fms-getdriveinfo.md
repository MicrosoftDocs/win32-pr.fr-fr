---
description: Contient des informations sur le lecteur sélectionné dans la fenêtre Gestionnaire de fichiers active (la fenêtre du répertoire ou la fenêtre des résultats de la recherche).
title: Structure FMS_GETDRIVEINFO (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 14f8a90b-d0ed-4818-a719-8fc4ea617bef
ms.openlocfilehash: b19b54d89f74fa122effa5853beb2961e0ddf1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973222"
---
# <a name="fms_getdriveinfo-structure"></a><span data-ttu-id="1b067-103">\_GETDRIVEINFO-structure FMS</span><span class="sxs-lookup"><span data-stu-id="1b067-103">FMS\_GETDRIVEINFO structure</span></span>

<span data-ttu-id="1b067-104">Contient des informations sur le lecteur sélectionné dans la fenêtre Gestionnaire de fichiers active (la fenêtre du répertoire ou la fenêtre des résultats de la recherche).</span><span class="sxs-lookup"><span data-stu-id="1b067-104">Contains information about the drive selected in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b067-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b067-105">Syntax</span></span>


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a><span data-ttu-id="1b067-106">Membres</span><span class="sxs-lookup"><span data-stu-id="1b067-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b067-107">**dwTotalSpace**</span><span class="sxs-lookup"><span data-stu-id="1b067-107">**dwTotalSpace**</span></span>
</dt> <dd>

<span data-ttu-id="1b067-108">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1b067-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1b067-109">Quantité totale d’espace de stockage, en octets, sur le disque associé au lecteur.</span><span class="sxs-lookup"><span data-stu-id="1b067-109">The total amount of storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="1b067-110">**dwFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="1b067-110">**dwFreeSpace**</span></span>
</dt> <dd>

<span data-ttu-id="1b067-111">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1b067-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1b067-112">Quantité d’espace de stockage disponible, en octets, sur le disque associé au lecteur.</span><span class="sxs-lookup"><span data-stu-id="1b067-112">The amount of free storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="1b067-113">**szPath**</span><span class="sxs-lookup"><span data-stu-id="1b067-113">**szPath**</span></span>
</dt> <dd>

<span data-ttu-id="1b067-114">Type : **TCHAR \[ 260 \]**</span><span class="sxs-lookup"><span data-stu-id="1b067-114">Type: **TCHAR\[260\]**</span></span>

</dd> <dd>

<span data-ttu-id="1b067-115">chemin d’accès se terminant par un caractère null du répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="1b067-115">the null-terminated path of the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="1b067-116">**szVolume**</span><span class="sxs-lookup"><span data-stu-id="1b067-116">**szVolume**</span></span>
</dt> <dd>

<span data-ttu-id="1b067-117">Type : **TCHAR \[ 14 \]**</span><span class="sxs-lookup"><span data-stu-id="1b067-117">Type: **TCHAR\[14\]**</span></span>

</dd> <dd>

<span data-ttu-id="1b067-118">Nom de volume terminé par le caractère null du disque associé au lecteur.</span><span class="sxs-lookup"><span data-stu-id="1b067-118">The null-terminated volume label of the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="1b067-119">**szShare**</span><span class="sxs-lookup"><span data-stu-id="1b067-119">**szShare**</span></span>
</dt> <dd>

<span data-ttu-id="1b067-120">Type : **TCHAR \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="1b067-120">Type: **TCHAR\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="1b067-121">Nom se terminant par un caractère null de la ressource réseau (si le lecteur est accessible via un réseau).</span><span class="sxs-lookup"><span data-stu-id="1b067-121">The null-terminated name of the network resource (if the drive is being accessed through a network).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b067-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1b067-122">Requirements</span></span>



| <span data-ttu-id="1b067-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b067-123">Requirement</span></span> | <span data-ttu-id="1b067-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b067-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1b067-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b067-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1b067-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b067-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1b067-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b067-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1b067-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b067-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1b067-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b067-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b067-130"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b067-130"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b067-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b067-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b067-132">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="1b067-132">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="1b067-133">**\_GETDRIVEINFO FM**</span><span class="sxs-lookup"><span data-stu-id="1b067-133">**FM\_GETDRIVEINFO**</span></span>](fm-getdriveinfo.md)
</dt> </dl>

 

 




