---
description: La structure STATIONQUERY fournit des informations sur un ordinateur spécifique à l’aide de Moniteur réseau.
ms.assetid: b7202c6b-e2b9-4a6f-8b87-3d11879f1d69
title: STATIONQUERY, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONQUERY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: de76c4da7bc27d76c04aeeaa7a46d69134e411ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527410"
---
# <a name="stationquery-structure"></a><span data-ttu-id="9a4dd-103">STATIONQUERY, structure</span><span class="sxs-lookup"><span data-stu-id="9a4dd-103">STATIONQUERY structure</span></span>

<span data-ttu-id="9a4dd-104">La structure **STATIONQUERY** fournit des informations sur un ordinateur spécifique à l’aide de moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-104">The **STATIONQUERY** structure provides information about a specific computer using Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a4dd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a4dd-105">Syntax</span></span>


```C++
typedef struct _STATIONQUERY {
  DWORD Flags;
  BYTE  BCDVerMinor;
  BYTE  BCDVerMajor;
  DWORD LicenseNumber;
  BYTE  MachineName[MACHINE_NAME_LENGTH];
  BYTE  UserName[USER_NAME_LENGTH];
  BYTE  Reserved[32];
  BYTE  AdapterAddress[6];
  WCHAR WMachineName[MACHINE_NAME_LENGTH];
  WCHAR WUserName[USER_NAME_LENGTH];
} STATIONQUERY, *LPSTATIONQUERY;
```



## <a name="members"></a><span data-ttu-id="9a4dd-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9a4dd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9a4dd-107">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="9a4dd-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="9a4dd-108">Indicateurs identifiant l’état actuel de Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-108">Flags that Identify the current state of Network Monitor.</span></span>



| <span data-ttu-id="9a4dd-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a4dd-109">Value</span></span>                                                                                                                                                                                                                | <span data-ttu-id="9a4dd-110">Signification</span><span class="sxs-lookup"><span data-stu-id="9a4dd-110">Meaning</span></span>                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="STATIONQUERY_FLAGS_LOADED"></span><span id="stationquery_flags_loaded"></span><dl> <span data-ttu-id="9a4dd-111"><dt>**\_indicateurs STATIONQUERY \_ chargés**</dt></span><span class="sxs-lookup"><span data-stu-id="9a4dd-111"><dt>**STATIONQUERY\_FLAGS\_LOADED**</dt></span></span> </dl>                   | <span data-ttu-id="9a4dd-112">Le pilote est chargé, mais pas le noyau.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-112">The driver is loaded, but the kernel is not.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_RUNNING"></span><span id="stationquery_flags_running"></span><dl> <span data-ttu-id="9a4dd-113"><dt>**\_indicateurs STATIONQUERY \_ en cours d’exécution**</dt></span><span class="sxs-lookup"><span data-stu-id="9a4dd-113"><dt>**STATIONQUERY\_FLAGS\_RUNNING**</dt></span></span> </dl>                | <span data-ttu-id="9a4dd-114">Le pilote est chargé mais ne capture pas les données.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-114">The driver is loaded but not capturing data.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_CAPTURING"></span><span id="stationquery_flags_capturing"></span><dl> <span data-ttu-id="9a4dd-115"><dt>**\_capture d’indicateurs STATIONQUERY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9a4dd-115"><dt>**STATIONQUERY\_FLAGS\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="9a4dd-116">Le pilote est activement engagé dans une capture.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-116">The driver is actively engaged in a capture.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_TRANSMITTING"></span><span id="stationquery_flags_transmitting"></span><dl> <span data-ttu-id="9a4dd-117"><dt>**\_indicateurs STATIONQUERY \_ transmettant**</dt></span><span class="sxs-lookup"><span data-stu-id="9a4dd-117"><dt>**STATIONQUERY\_FLAGS\_TRANSMITTING**</dt></span></span> </dl> | <span data-ttu-id="9a4dd-118">Cet indicateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-118">This flag is obsolete.</span></span><br/>                       |



 

</dd> <dt>

<span data-ttu-id="9a4dd-119">**BCDVerMinor**</span><span class="sxs-lookup"><span data-stu-id="9a4dd-119">**BCDVerMinor**</span></span>
</dt> <dd>

<span data-ttu-id="9a4dd-120">Numéro de version mineure de Moniteur réseau installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-120">Minor version number of Network Monitor installed on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="9a4dd-121">**BCDVerMajor**</span><span class="sxs-lookup"><span data-stu-id="9a4dd-121">**BCDVerMajor**</span></span>
</dt> <dd>

<span data-ttu-id="9a4dd-122">Numéro de version principale de Moniteur réseau installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-122">Major version number of Network Monitor installed on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="9a4dd-123">**LicenseNumber**</span><span class="sxs-lookup"><span data-stu-id="9a4dd-123">**LicenseNumber**</span></span>
</dt> <dd>

<span data-ttu-id="9a4dd-124">Numéro de licence du logiciel.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-124">Software license number.</span></span>

</dd> <dt>

<span data-ttu-id="9a4dd-125">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="9a4dd-125">**MachineName**</span></span>
</dt> <dd>

<span data-ttu-id="9a4dd-126">Nom du fabricant de l’ordinateur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-126">Computer manufacturer name, if any.</span></span>

</dd> <dt>

<span data-ttu-id="9a4dd-127">**UserName**</span><span class="sxs-lookup"><span data-stu-id="9a4dd-127">**UserName**</span></span>
</dt> <dd>

<span data-ttu-id="9a4dd-128">Nom d’utilisateur ou identificateur système.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-128">User name or system identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9a4dd-129">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="9a4dd-129">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="9a4dd-130">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-130">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="9a4dd-131">**AdapterAddress**</span><span class="sxs-lookup"><span data-stu-id="9a4dd-131">**AdapterAddress**</span></span>
</dt> <dd>

<span data-ttu-id="9a4dd-132">Adresse de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-132">NIC address.</span></span>

</dd> <dt>

<span data-ttu-id="9a4dd-133">**WMachineName**</span><span class="sxs-lookup"><span data-stu-id="9a4dd-133">**WMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="9a4dd-134">Nom de l’ordinateur Unicode.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-134">Unicode computer name.</span></span> <span data-ttu-id="9a4dd-135">Ce membre s’applique à Moniteur réseau 2,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-135">This member applies to Network Monitor 2.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="9a4dd-136">**WUserName**</span><span class="sxs-lookup"><span data-stu-id="9a4dd-136">**WUserName**</span></span>
</dt> <dd>

<span data-ttu-id="9a4dd-137">Nom d’utilisateur Unicode.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-137">Unicode user name.</span></span> <span data-ttu-id="9a4dd-138">Ce membre s’applique à Moniteur réseau 2,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-138">This member applies to Network Monitor 2.0 or later.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a4dd-139">Notes</span><span class="sxs-lookup"><span data-stu-id="9a4dd-139">Remarks</span></span>

<span data-ttu-id="9a4dd-140">Un tableau de ces structures est utilisé par la structure [QUERYTABLE](querytable.md) pour fournir une liste des ordinateurs qui utilisent actuellement Moniteur réseau pour capturer des données.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-140">An array of these structures is used by the [QUERYTABLE](querytable.md) structure to provide a list of the computers that are currently using Network Monitor to capture data.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a4dd-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a4dd-141">Requirements</span></span>



| <span data-ttu-id="9a4dd-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a4dd-142">Requirement</span></span> | <span data-ttu-id="9a4dd-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a4dd-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9a4dd-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a4dd-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9a4dd-145">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a4dd-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9a4dd-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a4dd-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9a4dd-147">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a4dd-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9a4dd-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a4dd-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a4dd-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a4dd-149"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a4dd-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a4dd-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a4dd-151">QUERYTABLE</span><span class="sxs-lookup"><span data-stu-id="9a4dd-151">QUERYTABLE</span></span>](querytable.md)
</dt> </dl>

 

 




