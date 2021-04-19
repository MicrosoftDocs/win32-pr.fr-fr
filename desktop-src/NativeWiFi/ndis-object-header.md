---
description: Empaquette les informations relatives au type d’objet, à la version et à la taille requises dans de nombreuses structures NDIS 6,0.
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: Structure NDIS_OBJECT_HEADER (Ntddndis. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDIS_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- ntddndis.h
ms.openlocfilehash: fe28a87eeb1457bace0b72a386bcb07667b24a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544836"
---
# <a name="ndis_object_header-structure"></a><span data-ttu-id="18c3e-103">\_Structure d' \_ en-tête d’objet NDIS</span><span class="sxs-lookup"><span data-stu-id="18c3e-103">NDIS\_OBJECT\_HEADER structure</span></span>

<span data-ttu-id="18c3e-104">La structure d' **\_ \_ en-tête d’objet NDIS** conditionne le type d’objet, la version et les informations de taille requis dans de nombreuses structures NDIS 6,0.</span><span class="sxs-lookup"><span data-stu-id="18c3e-104">The **NDIS\_OBJECT\_HEADER** structure packages the object type, version, and size information that is required in many NDIS 6.0 structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="18c3e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18c3e-105">Syntax</span></span>


```C++
typedef struct _NDIS_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Size;
} NDIS_OBJECT_HEADER, *PNDIS_OBJECT_HEADER;
```



## <a name="members"></a><span data-ttu-id="18c3e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="18c3e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="18c3e-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="18c3e-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="18c3e-108">Spécifie le type d’objet NDIS décrit par une structure.</span><span class="sxs-lookup"><span data-stu-id="18c3e-108">Specifies the type of NDIS object that a structure describes.</span></span>

</dd> <dt>

<span data-ttu-id="18c3e-109">**Faisant**</span><span class="sxs-lookup"><span data-stu-id="18c3e-109">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="18c3e-110">Spécifie le numéro de révision de cette structure.</span><span class="sxs-lookup"><span data-stu-id="18c3e-110">Specifies the revision number of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="18c3e-111">**Taille**</span><span class="sxs-lookup"><span data-stu-id="18c3e-111">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="18c3e-112">Spécifie la taille totale, en octets, de la structure NDIS qui contient **l' \_ \_ en-tête d’objet NDIS**.</span><span class="sxs-lookup"><span data-stu-id="18c3e-112">Specifies the total size, in bytes, of the NDIS structure that contains the **NDIS\_OBJECT\_HEADER**.</span></span> <span data-ttu-id="18c3e-113">Cette taille comprend la taille du membre **d' \_ \_ en-tête d’objet NDIS** et de tous les autres membres de la structure.</span><span class="sxs-lookup"><span data-stu-id="18c3e-113">This size includes the size of the **NDIS\_OBJECT\_HEADER** member and all other members of the structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18c3e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18c3e-114">Requirements</span></span>



| <span data-ttu-id="18c3e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18c3e-115">Requirement</span></span> | <span data-ttu-id="18c3e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="18c3e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18c3e-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18c3e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="18c3e-118">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18c3e-118">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="18c3e-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18c3e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="18c3e-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18c3e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="18c3e-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="18c3e-121">Redistributable</span></span><br/>          | <span data-ttu-id="18c3e-122">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="18c3e-122">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="18c3e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="18c3e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="18c3e-124"><dt>Ntddndis. h (inclure Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18c3e-124"><dt>Ntddndis.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18c3e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18c3e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18c3e-126">**\_Liste des BSSID DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="18c3e-126">**DOT11\_BSSID\_LIST**</span></span>](dot11-bssid-list.md)
</dt> </dl>

 

 




