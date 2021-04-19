---
title: WMDMID, structure
description: La structure WMDMID décrit les numéros de série et les ID de groupe.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- Structure WMDMID Windows Media Gestionnaire de périphériques
- Pointeur de structure PWMDMID Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- WMDMID
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edc2a364bf29ead6aaf4fad8ad3a56fe80d7176
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534884"
---
# <a name="wmdmid-structure"></a><span data-ttu-id="72ce8-105">WMDMID, structure</span><span class="sxs-lookup"><span data-stu-id="72ce8-105">WMDMID structure</span></span>

<span data-ttu-id="72ce8-106">La structure **WMDMID** décrit les numéros de série et les ID de groupe.</span><span class="sxs-lookup"><span data-stu-id="72ce8-106">The **WMDMID** structure describes serial numbers and group IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="72ce8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72ce8-107">Syntax</span></span>


```C++
typedef struct __WMDMID {
  UINT  cbSize;
  DWORD dwVendorID;
  BYTE  pID[WMDMID_LENGTH];
  UINT  SerialNumberLength;
} WMDMID, *PWMDMID;
```



## <a name="members"></a><span data-ttu-id="72ce8-108">Membres</span><span class="sxs-lookup"><span data-stu-id="72ce8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="72ce8-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="72ce8-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="72ce8-110">Taille de la structure **WMDMID** , en octets.</span><span class="sxs-lookup"><span data-stu-id="72ce8-110">Size of the **WMDMID** structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="72ce8-111">**dwVendorID**</span><span class="sxs-lookup"><span data-stu-id="72ce8-111">**dwVendorID**</span></span>
</dt> <dd>

<span data-ttu-id="72ce8-112">**Valeur DWORD** contenant le numéro d’ID inscrit du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="72ce8-112">**DWORD** containing the registered ID number of the vendor.</span></span> <span data-ttu-id="72ce8-113">Contient zéro si la valeur n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="72ce8-113">Contains zero if not in use.</span></span>

</dd> <dt>

<span data-ttu-id="72ce8-114">**\[longueur WMDMID \_ PID\]**</span><span class="sxs-lookup"><span data-stu-id="72ce8-114">**pID\[WMDMID\_LENGTH\]**</span></span>
</dt> <dd>

<span data-ttu-id="72ce8-115">Pointeur vers un tableau d’octets contenant le numéro de série.</span><span class="sxs-lookup"><span data-stu-id="72ce8-115">Pointer to an array of bytes containing the serial number.</span></span> <span data-ttu-id="72ce8-116">Le numéro de série est une chaîne de valeurs d’octets qui n’ont pas de format standard.</span><span class="sxs-lookup"><span data-stu-id="72ce8-116">The serial number is a string of byte values that have no standard format.</span></span> <span data-ttu-id="72ce8-117">Notez qu’il ne s’agit pas d’une valeur à caractères larges.</span><span class="sxs-lookup"><span data-stu-id="72ce8-117">Note that this is not a wide-character value.</span></span> <span data-ttu-id="72ce8-118">**WMDMID \_ LENGTH** est une valeur constante définie dans mswmdm. h.</span><span class="sxs-lookup"><span data-stu-id="72ce8-118">**WMDMID\_LENGTH** is a constant value defined in mswmdm.h.</span></span>

</dd> <dt>

<span data-ttu-id="72ce8-119">**SerialNumberLength**</span><span class="sxs-lookup"><span data-stu-id="72ce8-119">**SerialNumberLength**</span></span>
</dt> <dd>

<span data-ttu-id="72ce8-120">Longueur réelle du numéro de série retourné, en octets.</span><span class="sxs-lookup"><span data-stu-id="72ce8-120">Actual length of the serial number returned, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72ce8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72ce8-121">Requirements</span></span>



| <span data-ttu-id="72ce8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72ce8-122">Requirement</span></span> | <span data-ttu-id="72ce8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="72ce8-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="72ce8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="72ce8-124">Header</span></span><br/> | <dl> <span data-ttu-id="72ce8-125"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="72ce8-125"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72ce8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72ce8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72ce8-127">**IMDSPDevice::GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="72ce8-127">**IMDSPDevice::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[<span data-ttu-id="72ce8-128">**IMDSPStorageGlobals::GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="72ce8-128">**IMDSPStorageGlobals::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[<span data-ttu-id="72ce8-129">**IWMDMDevice::GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="72ce8-129">**IWMDMDevice::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[<span data-ttu-id="72ce8-130">**IWMDMStorageGlobals::GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="72ce8-130">**IWMDMStorageGlobals::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[<span data-ttu-id="72ce8-131">**Structures**</span><span class="sxs-lookup"><span data-stu-id="72ce8-131">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





