---
description: Stocke les informations clés relatives à une interface de réseau local sans fil gérée par le service de configuration sans fil.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: Structure INTF_KEY_ENTRY (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_KEY_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 91f25708e79be4f85c4200bd690404ff39f567d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318534"
---
# <a name="intf_key_entry-structure"></a><span data-ttu-id="b6615-103">Structure d’entrée de \_ clé INTF \_</span><span class="sxs-lookup"><span data-stu-id="b6615-103">INTF\_KEY\_ENTRY structure</span></span>

<span data-ttu-id="b6615-104">\[**INTF \_ L' \_ entrée de clé** n’est plus prise en charge à partir de Windows Vista et windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b6615-104">\[**INTF\_KEY\_ENTRY** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="b6615-105">Utilisez plutôt l' [API WiFi Native](native-wifi-reference.md), qui offre des fonctionnalités similaires.</span><span class="sxs-lookup"><span data-stu-id="b6615-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="b6615-106">Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="b6615-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="b6615-107">La structure d' **\_ \_ entrée de clé INTF** stocke les informations clés sur une interface de réseau local sans fil gérée par le service de configuration sans fil.</span><span class="sxs-lookup"><span data-stu-id="b6615-107">The **INTF\_KEY\_ENTRY** structure stores the key information about a wireless LAN interface managed by the Wireless Configuration Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6615-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6615-108">Syntax</span></span>


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a><span data-ttu-id="b6615-109">Membres</span><span class="sxs-lookup"><span data-stu-id="b6615-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="b6615-110">**wszGuid**</span><span class="sxs-lookup"><span data-stu-id="b6615-110">**wszGuid**</span></span>
</dt> <dd>

<span data-ttu-id="b6615-111">Pointeur vers le GUID d’interface représenté sous la forme d’une chaîne Unicode au format suivant : "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span><span class="sxs-lookup"><span data-stu-id="b6615-111">A pointer to the interface GUID represented as a Unicode string in the following format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6615-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b6615-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b6615-113">Le fichier d’en-tête *wzcsapi. h* n’est pas disponible dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="b6615-113">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b6615-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6615-114">Requirements</span></span>



| <span data-ttu-id="b6615-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6615-115">Requirement</span></span> | <span data-ttu-id="b6615-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6615-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b6615-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6615-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b6615-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6615-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b6615-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6615-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b6615-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6615-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b6615-121">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b6615-121">End of client support</span></span><br/>    | <span data-ttu-id="b6615-122">Windows XP avec SP3</span><span class="sxs-lookup"><span data-stu-id="b6615-122">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="b6615-123">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b6615-123">End of server support</span></span><br/>    | <span data-ttu-id="b6615-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b6615-124">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="b6615-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6615-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6615-126"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6615-126"><dt>Wzcsapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6615-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6615-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6615-128">**\_table de clé INTFS \_**</span><span class="sxs-lookup"><span data-stu-id="b6615-128">**INTFS\_KEY\_TABLE**</span></span>](intfs-key-table.md)
</dt> <dt>

[<span data-ttu-id="b6615-129">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="b6615-129">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> </dl>

 

 




