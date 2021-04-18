---
description: Contient la table d’informations clés de toutes les interfaces de réseau local sans fil gérées par le service de configuration sans fil.
ms.assetid: 5d5fe222-6ca1-4778-9f64-1c6a63467a6c
title: Structure INTFS_KEY_TABLE (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTFS_KEY_TABLE
api_type:
- HeaderDef
api_location:
- Wzcsapi.h
ms.openlocfilehash: 4ef38f2317c763eaa6c7e0379be5c8b00c0ed6b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513005"
---
# <a name="intfs_key_table-structure"></a><span data-ttu-id="94b7b-103">Structure de table de \_ clés INTFS \_</span><span class="sxs-lookup"><span data-stu-id="94b7b-103">INTFS\_KEY\_TABLE structure</span></span>

<span data-ttu-id="94b7b-104">\[**INTFS \_ La \_ table de clés** n’est plus prise en charge à partir de Windows Vista et windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="94b7b-104">\[**INTFS\_KEY\_TABLE** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="94b7b-105">Utilisez plutôt l' [API WiFi Native](native-wifi-reference.md), qui offre des fonctionnalités similaires.</span><span class="sxs-lookup"><span data-stu-id="94b7b-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="94b7b-106">Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="94b7b-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="94b7b-107">La structure de **\_ \_ table de clés INTFS** contient la table d’informations de clé pour toutes les interfaces de réseau local sans fil gérées par le service de configuration sans fil.</span><span class="sxs-lookup"><span data-stu-id="94b7b-107">The **INTFS\_KEY\_TABLE** structure contains the table of key information for all wireless LAN interfaces managed by the Wireless Configuration Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="94b7b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94b7b-108">Syntax</span></span>


```C++
typedef struct {
  DWORD           dwNumIntfs;
  PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;
```



## <a name="members"></a><span data-ttu-id="94b7b-109">Membres</span><span class="sxs-lookup"><span data-stu-id="94b7b-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="94b7b-110">**dwNumIntfs**</span><span class="sxs-lookup"><span data-stu-id="94b7b-110">**dwNumIntfs**</span></span>
</dt> <dd>

<span data-ttu-id="94b7b-111">Nombre total d’interfaces.</span><span class="sxs-lookup"><span data-stu-id="94b7b-111">Total number of interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="94b7b-112">**pIntfs**</span><span class="sxs-lookup"><span data-stu-id="94b7b-112">**pIntfs**</span></span>
</dt> <dd>

<span data-ttu-id="94b7b-113">Pointeur vers la structure d' [**\_ \_ entrée de clé INTF**](intf-key-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="94b7b-113">Pointer to the [**INTF\_KEY\_ENTRY**](intf-key-entry.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94b7b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="94b7b-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="94b7b-115">Le fichier d’en-tête *wzcsapi. h* n’est pas disponible dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="94b7b-115">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="94b7b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94b7b-116">Requirements</span></span>



| <span data-ttu-id="94b7b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94b7b-117">Requirement</span></span> | <span data-ttu-id="94b7b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="94b7b-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="94b7b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94b7b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="94b7b-120">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94b7b-120">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="94b7b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94b7b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="94b7b-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94b7b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="94b7b-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="94b7b-123">End of client support</span></span><br/>    | <span data-ttu-id="94b7b-124">Windows XP avec SP3</span><span class="sxs-lookup"><span data-stu-id="94b7b-124">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="94b7b-125">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="94b7b-125">End of server support</span></span><br/>    | <span data-ttu-id="94b7b-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="94b7b-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="94b7b-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="94b7b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="94b7b-128"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="94b7b-128"><dt>Wzcsapi.h</dt></span></span> </dl> |



 

 




