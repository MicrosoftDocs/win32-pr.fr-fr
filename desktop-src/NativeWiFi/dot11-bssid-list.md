---
description: Contient une liste d’identificateurs BSS (Service Set) de base.
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: Structure DOT11_BSSID_LIST (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSSID_LIST
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 345053a8d39ea37bea2fa2350dcc426420aed422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518745"
---
# <a name="dot11_bssid_list-structure"></a><span data-ttu-id="915d3-103">Structure de liste des \_ BSSID DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="915d3-103">DOT11\_BSSID\_LIST structure</span></span>

<span data-ttu-id="915d3-104">La structure de **\_ \_ liste des BSSID DOT11** contient une liste d’identificateurs BSS (Basic Service Set).</span><span class="sxs-lookup"><span data-stu-id="915d3-104">The **DOT11\_BSSID\_LIST** structure contains a list of basic service set (BSS) identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="915d3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="915d3-105">Syntax</span></span>


```C++
typedef struct _DOT11_BSSID_LIST {
  NDIS_OBJECT_HEADER Header;
  ULONG              uNumOfEntries;
  ULONG              uTotalNumOfEntries;
  DOT11_MAC_ADDRESS  BSSIDs[1];
} DOT11_BSSID_LIST, *PDOT11_BSSID_LIST;
```



## <a name="members"></a><span data-ttu-id="915d3-106">Membres</span><span class="sxs-lookup"><span data-stu-id="915d3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="915d3-107">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="915d3-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="915d3-108">Structure [**d' \_ \_ en-tête d’objet NDIS**](ndis-object-header.md) qui contient le type, la version et les informations de taille d’une structure NDIS.</span><span class="sxs-lookup"><span data-stu-id="915d3-108">An [**NDIS\_OBJECT\_HEADER**](ndis-object-header.md) structure that contains the type, version, and, size information of an NDIS structure.</span></span> <span data-ttu-id="915d3-109">Pour la plupart des structures de **\_ \_ liste des BSSID dot11** , définissez **le type de membre sur** **NDIS \_ \_ \_ par défaut**, définissez le membre de **révision** sur **DOT11 \_ BSSID \_ List \_ révision \_ 1**, puis définissez le membre **Size** sur **sizeof ( \_ liste des BSSID dot11 \_ )**.</span><span class="sxs-lookup"><span data-stu-id="915d3-109">For most **DOT11\_BSSID\_LIST** structures, set the **Type** member to **NDIS\_OBJECT\_TYPE\_DEFAULT**, set the **Revision** member to **DOT11\_BSSID\_LIST\_REVISION\_1**, and set the **Size** member to **sizeof(DOT11\_BSSID\_LIST)**.</span></span>

</dd> <dt>

<span data-ttu-id="915d3-110">**uNumOfEntries**</span><span class="sxs-lookup"><span data-stu-id="915d3-110">**uNumOfEntries**</span></span>
</dt> <dd>

<span data-ttu-id="915d3-111">Nombre d’entrées dans cette structure.</span><span class="sxs-lookup"><span data-stu-id="915d3-111">The number of entries in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="915d3-112">**uTotalNumOfEntries**</span><span class="sxs-lookup"><span data-stu-id="915d3-112">**uTotalNumOfEntries**</span></span>
</dt> <dd>

<span data-ttu-id="915d3-113">Nombre total d’entrées prises en charge.</span><span class="sxs-lookup"><span data-stu-id="915d3-113">The total number of entries supported.</span></span>

</dd> <dt>

<span data-ttu-id="915d3-114">**BSSIDs**</span><span class="sxs-lookup"><span data-stu-id="915d3-114">**BSSIDs**</span></span>
</dt> <dd>

<span data-ttu-id="915d3-115">Liste d’identificateurs BSS.</span><span class="sxs-lookup"><span data-stu-id="915d3-115">A list of BSS identifiers.</span></span> <span data-ttu-id="915d3-116">Un identificateur BSS est stocké en tant que type d' [**\_ \_ adresse Mac DOT11**](dot11-mac-address-type.md) .</span><span class="sxs-lookup"><span data-stu-id="915d3-116">A BSS identifier is stored as a [**DOT11\_MAC\_ADDRESS**](dot11-mac-address-type.md) type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="915d3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="915d3-117">Requirements</span></span>



| <span data-ttu-id="915d3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="915d3-118">Requirement</span></span> | <span data-ttu-id="915d3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="915d3-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="915d3-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="915d3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="915d3-121">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="915d3-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="915d3-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="915d3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="915d3-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="915d3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="915d3-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="915d3-124">Redistributable</span></span><br/>          | <span data-ttu-id="915d3-125">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="915d3-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="915d3-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="915d3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="915d3-127"><dt>Windot11. h (inclure Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="915d3-127"><dt>Windot11.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="915d3-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="915d3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="915d3-129">**\_paramètres de connexion WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="915d3-129">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




