---
description: Définit la structure du fichier d’en-tête Moniteur réseau.
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: Structure de CAPTUREFILE_HEADER_VALUES (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILE_HEADER_VALUES
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b3f83a65dafd2da0198aade5243acc1184fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533638"
---
# <a name="capturefile_header_values-structure"></a><span data-ttu-id="8a2bd-103">\_Structure de valeurs d’en-tête CAPTUREFILE \_</span><span class="sxs-lookup"><span data-stu-id="8a2bd-103">CAPTUREFILE\_HEADER\_VALUES structure</span></span>

<span data-ttu-id="8a2bd-104">La structure des **\_ \_ valeurs d’en-tête CAPTUREFILE** définit la structure du fichier d’en-tête Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-104">The **CAPTUREFILE\_HEADER\_VALUES** structure defines the Network Monitor header file structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a2bd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a2bd-105">Syntax</span></span>


```C++
typedef struct _CAPTUREFILE_HEADER_VALUES {
  DWORD      Signature;
  BYTE       BCDVerMinor;
  BYTE       BCDVerMajor;
  WORD       MacType;
  SYSTEMTIME TimeStamp;
  DWORD      FrameTableOffset;
  DWORD      FrameTableLength;
  DWORD      UserDataOffset;
  DWORD      UserDataLength;
  DWORD      CommentDataOffset;
  DWORD      CommentDataLength;
  DWORD      StatisticsOffset;
  DWORD      StatisticsLength;
  DWORD      NetworkInfoOffset;
  DWORD      NetworkInfoLength;
  DWORD      ConversationStatsOffset;
  DWORD      ConversationStatsLength;
} CAPTUREFILE_HEADER_VALUES, *LPCAPTUREFILE_HEADER_VALUES;
```



## <a name="members"></a><span data-ttu-id="8a2bd-106">Membres</span><span class="sxs-lookup"><span data-stu-id="8a2bd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8a2bd-107">**Signature**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-107">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-108">Identificateur unique : 'GMBU.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-108">Unique identifier: 'GMBU.</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-109">**BCDVerMinor**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-109">**BCDVerMinor**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-110">Binaire, codé décimal (mineur).</span><span class="sxs-lookup"><span data-stu-id="8a2bd-110">Binary, coded decimal (minor).</span></span> <span data-ttu-id="8a2bd-111">La valeur de ce membre doit être égale à zéro (0).</span><span class="sxs-lookup"><span data-stu-id="8a2bd-111">The value of this member should be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-112">**BCDVerMajor**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-112">**BCDVerMajor**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-113">Décimale codée binaire (majeure).</span><span class="sxs-lookup"><span data-stu-id="8a2bd-113">Binary coded decimal (major).</span></span> <span data-ttu-id="8a2bd-114">Cette valeur doit être 2.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-114">This value should be 2.</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-115">**MacType**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-115">**MacType**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-116">Type de topologie.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-116">Topology type.</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-117">**Confirmé**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-117">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-118">Heure de la capture.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-118">Time of capture.</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-119">**FrameTableOffset**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-119">**FrameTableOffset**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-120">Table d’index de frames.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-120">Frame index table.</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-121">**FrameTableLength**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-121">**FrameTableLength**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-122">Taille de la table d’index de frames.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-122">Frame index table size.</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-123">**UserDataOffset**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-123">**UserDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-124">Décalage des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-124">User data offset.</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-125">**UserDataLength**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-125">**UserDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-126">Longueur des données de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-126">User data length.</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-127">**CommentDataOffset**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-127">**CommentDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-128">Décalage des données de commentaire.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-128">Comment data offset.</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-129">**CommentDataLength**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-129">**CommentDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-130">Longueur des données de commentaire.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-130">Length of comment data.</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-131">**StatisticsOffset**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-131">**StatisticsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-132">Décalage de la structure des **statistiques** .</span><span class="sxs-lookup"><span data-stu-id="8a2bd-132">Offset to the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-133">**StatisticsLength**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-133">**StatisticsLength**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-134">Longueur de la structure des **statistiques** .</span><span class="sxs-lookup"><span data-stu-id="8a2bd-134">Length of the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-135">**NetworkInfoOffset**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-135">**NetworkInfoOffset**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-136">Décalage de la structure **NETWORKINFO** .</span><span class="sxs-lookup"><span data-stu-id="8a2bd-136">Offset to the **NETWORKINFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-137">**NetworkInfoLength**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-137">**NetworkInfoLength**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-138">Longueur de la structure **NETWORKINFO** .</span><span class="sxs-lookup"><span data-stu-id="8a2bd-138">Length of the **NETWORKINFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-139">**ConversationStatsOffset**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-139">**ConversationStatsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-140">Ce membre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-140">This member is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8a2bd-141">**ConversationStatsLength**</span><span class="sxs-lookup"><span data-stu-id="8a2bd-141">**ConversationStatsLength**</span></span>
</dt> <dd>

<span data-ttu-id="8a2bd-142">Ce membre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-142">This member is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a2bd-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a2bd-143">Requirements</span></span>



| <span data-ttu-id="8a2bd-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a2bd-144">Requirement</span></span> | <span data-ttu-id="8a2bd-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a2bd-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8a2bd-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a2bd-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8a2bd-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a2bd-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8a2bd-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a2bd-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8a2bd-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a2bd-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8a2bd-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a2bd-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a2bd-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a2bd-151"><dt>Netmon.h</dt></span></span> </dl> |



 

 




