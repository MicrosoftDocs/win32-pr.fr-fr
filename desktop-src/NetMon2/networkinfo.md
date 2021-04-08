---
description: La structure NETWORKINFO décrit une carte réseau.
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: NETWORKINFO, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8917966d2e090417a95a9ca20158c6c5935bda3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760131"
---
# <a name="networkinfo-structure"></a><span data-ttu-id="be6ea-103">NETWORKINFO, structure</span><span class="sxs-lookup"><span data-stu-id="be6ea-103">NETWORKINFO structure</span></span>

<span data-ttu-id="be6ea-104">La structure NETWORKINFO décrit une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="be6ea-104">The NETWORKINFO structure describes a NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="be6ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be6ea-105">Syntax</span></span>


```C++
typedef struct _NETWORKINFO {
  BYTE    PermanentAddr[6];
  BYTE    CurrentAddr[6];
  ADDRESS OtherAddress;
  DWORD   LinkSpeed;
  DWORD   MacType;
  DWORD   MaxFrameSize;
  DWORD   Flags;
  DWORD   TimestampScaleFactor;
  BYTE    NodeName[32];
  BOOL    PModeSupported;
  BYTE    Comment[ADAPTER_COMMENT_LENGTH];
} NETWORKINFO, *LPNETWORKINFO;
```



## <a name="members"></a><span data-ttu-id="be6ea-106">Membres</span><span class="sxs-lookup"><span data-stu-id="be6ea-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="be6ea-107">**PermanentAddr**</span><span class="sxs-lookup"><span data-stu-id="be6ea-107">**PermanentAddr**</span></span>
</dt> <dd>

<span data-ttu-id="be6ea-108">Adresse MAC permanente.</span><span class="sxs-lookup"><span data-stu-id="be6ea-108">Permanent MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="be6ea-109">**CurrentAddr**</span><span class="sxs-lookup"><span data-stu-id="be6ea-109">**CurrentAddr**</span></span>
</dt> <dd>

<span data-ttu-id="be6ea-110">Adresse MAC actuelle.</span><span class="sxs-lookup"><span data-stu-id="be6ea-110">Current MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="be6ea-111">**OtherAddress**</span><span class="sxs-lookup"><span data-stu-id="be6ea-111">**OtherAddress**</span></span>
</dt> <dd>

<span data-ttu-id="be6ea-112">Autre adresse qui la prend en charge (par exemple, IP, IPX).</span><span class="sxs-lookup"><span data-stu-id="be6ea-112">Other address that support this (for example IP, IPX).</span></span>

</dd> <dt>

<span data-ttu-id="be6ea-113">**LinkSpeed**</span><span class="sxs-lookup"><span data-stu-id="be6ea-113">**LinkSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="be6ea-114">Vitesse de liaison, en Mbits/s.</span><span class="sxs-lookup"><span data-stu-id="be6ea-114">Link speed, in Mbps.</span></span>

</dd> <dt>

<span data-ttu-id="be6ea-115">**MacType**</span><span class="sxs-lookup"><span data-stu-id="be6ea-115">**MacType**</span></span>
</dt> <dd>

<span data-ttu-id="be6ea-116">Type de média.</span><span class="sxs-lookup"><span data-stu-id="be6ea-116">Media type.</span></span>

</dd> <dt>

<span data-ttu-id="be6ea-117">**MaxFrameSize**</span><span class="sxs-lookup"><span data-stu-id="be6ea-117">**MaxFrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="be6ea-118">Taille de trame maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="be6ea-118">Maximum frame size allowed.</span></span>

</dd> <dt>

<span data-ttu-id="be6ea-119">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="be6ea-119">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="be6ea-120">Ce paramètre peut être l’un des indicateurs d’informations suivants :</span><span class="sxs-lookup"><span data-stu-id="be6ea-120">This parameter can be one of the following informational flags:</span></span>



| <span data-ttu-id="be6ea-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="be6ea-121">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="be6ea-122">Signification</span><span class="sxs-lookup"><span data-stu-id="be6ea-122">Meaning</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <span data-ttu-id="be6ea-123"><dt>**\_indicateurs NETWORKINFO \_ PMODE \_ non \_ pris en charge**</dt></span><span class="sxs-lookup"><span data-stu-id="be6ea-123"><dt>**NETWORKINFO\_FLAGS\_PMODE\_NOT\_SUPPORTED**</dt></span></span> </dl>    | <span data-ttu-id="be6ea-124">La carte réseau ne prend pas en charge le mode de promiscuité, ce qui signifie qu’elle ne capturera que le trafic qui est diffusé par nature ou qui implique uniquement l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="be6ea-124">The network card does not support promiscuous mode, meaning that it will only capture traffic which is broadcast in nature or only involves the local machine.</span></span><br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <span data-ttu-id="be6ea-125"><dt>**NETWORKINFO \_ indicateurs \_ RAS**</dt></span><span class="sxs-lookup"><span data-stu-id="be6ea-125"><dt>**NETWORKINFO\_FLAGS\_RAS**</dt></span></span> </dl>                                                      | <span data-ttu-id="be6ea-126">Il s’agit d’une carte réseau virtuelle qui est une connexion RAS (serveur d’accès à distance) par le biais d’un modem ou d’une autre carte réseau.</span><span class="sxs-lookup"><span data-stu-id="be6ea-126">This is a virtual network card that is a RAS (Remote Access Server) connection through a modem or another network card.</span></span><br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <span data-ttu-id="be6ea-127"><dt>**\_ \_ carte à distance drapeaux NETWORKINFO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="be6ea-127"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_CARD**</dt></span></span> </dl>                             | <span data-ttu-id="be6ea-128">La carte réseau ne se trouve pas sur l’ordinateur local, mais elle est capturée sur un ordinateur distant à l’Bequest de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="be6ea-128">The network card is not on the local computer, but is capturing on a remote machine at the bequest of the local computer.</span></span><br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <span data-ttu-id="be6ea-129"><dt>**\_indicateurs NETWORKINFO \_ distants \_ nal**</dt></span><span class="sxs-lookup"><span data-stu-id="be6ea-129"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_NAL**</dt></span></span> </dl>                                | <span data-ttu-id="be6ea-130">Périmé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="be6ea-130">Obsolete; do not use.</span></span><br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <span data-ttu-id="be6ea-131"><dt>**\_drapeaux NETWORKINFO \_ distants \_ \_ connectés**</dt></span><span class="sxs-lookup"><span data-stu-id="be6ea-131"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_NAL\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="be6ea-132">Périmé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="be6ea-132">Obsolete; do not use.</span></span><br/>                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="be6ea-133">**TimestampScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="be6ea-133">**TimestampScaleFactor**</span></span>
</dt> <dd>

<span data-ttu-id="be6ea-134">Par exemple, la valeur 1 indique 1/1 ms, 10 indique 1/10 ms, 100 indique 1/100 ms, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="be6ea-134">For example, a value of 1 indicates 1/1 ms, 10 indicates 1/10 ms, 100 indicates 1/100 ms, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="be6ea-135">**NodeName**</span><span class="sxs-lookup"><span data-stu-id="be6ea-135">**NodeName**</span></span>
</dt> <dd>

<span data-ttu-id="be6ea-136">Nom de la station de travail distante.</span><span class="sxs-lookup"><span data-stu-id="be6ea-136">Name of remote workstation.</span></span>

</dd> <dt>

<span data-ttu-id="be6ea-137">**PModeSupported**</span><span class="sxs-lookup"><span data-stu-id="be6ea-137">**PModeSupported**</span></span>
</dt> <dd>

<span data-ttu-id="be6ea-138">Indicateur de prise en charge du mode P de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="be6ea-138">NIC P-mode support indicator.</span></span>

</dd> <dt>

<span data-ttu-id="be6ea-139">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="be6ea-139">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="be6ea-140">Champ de commentaire de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="be6ea-140">Adapter comment field.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be6ea-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be6ea-141">Requirements</span></span>



| <span data-ttu-id="be6ea-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be6ea-142">Requirement</span></span> | <span data-ttu-id="be6ea-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="be6ea-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="be6ea-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be6ea-144">Minimum supported client</span></span><br/> | <span data-ttu-id="be6ea-145">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be6ea-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="be6ea-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be6ea-146">Minimum supported server</span></span><br/> | <span data-ttu-id="be6ea-147">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be6ea-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="be6ea-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="be6ea-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="be6ea-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="be6ea-149"><dt>Netmon.h</dt></span></span> </dl> |



 

 




