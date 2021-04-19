---
description: Contient les paramètres de configuration EAPOL.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: Structure EAPOL_INTF_PARAMS (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPOL_INTF_PARAMS
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: dd9e0664fe41b471162beccd31bf2c22fbfa1640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537036"
---
# <a name="eapol_intf_params-structure"></a><span data-ttu-id="a8b35-103">Structure de \_ paramètres EAPOL INTF \_</span><span class="sxs-lookup"><span data-stu-id="a8b35-103">EAPOL\_INTF\_PARAMS structure</span></span>

<span data-ttu-id="a8b35-104">\[**EAPOL \_ Les \_ paramètres INTF** ne sont plus pris en charge à partir de Windows Vista et windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a8b35-104">\[**EAPOL\_INTF\_PARAMS** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="a8b35-105">Utilisez plutôt l' [API WiFi Native](native-wifi-reference.md), qui offre des fonctionnalités similaires.</span><span class="sxs-lookup"><span data-stu-id="a8b35-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="a8b35-106">Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="a8b35-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="a8b35-107">Contient les paramètres de configuration EAPOL.</span><span class="sxs-lookup"><span data-stu-id="a8b35-107">Contains EAPOL configuration parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b35-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8b35-108">Syntax</span></span>


```C++
typedef struct _EAPOL_INTF_PARAMS {
  DWORD dwVersion;
  DWORD dwReserved2;
  DWORD dwEapFlags;
  DWORD dwEapType;
  DWORD dwSizeOfSSID;
  BYTE  bSSID[MAX_NETWORK_NAME_LENGTH];
} EAPOL_INTF_PARAMS, *PEAPOL_INTF_PARAMS;
```



## <a name="members"></a><span data-ttu-id="a8b35-109">Membres</span><span class="sxs-lookup"><span data-stu-id="a8b35-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="a8b35-110">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="a8b35-110">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="a8b35-111">Version de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="a8b35-111">Version of the caller.</span></span> <span data-ttu-id="a8b35-112">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="a8b35-112">Default is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-113">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="a8b35-113">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="a8b35-114">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="a8b35-114">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-115">**dwEapFlags**</span><span class="sxs-lookup"><span data-stu-id="a8b35-115">**dwEapFlags**</span></span>
</dt> <dd>

<span data-ttu-id="a8b35-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="a8b35-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-117">**dwEapType**</span><span class="sxs-lookup"><span data-stu-id="a8b35-117">**dwEapType**</span></span>
</dt> <dd>

<span data-ttu-id="a8b35-118">Type d’extension EAP à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a8b35-118">The EAP extension type to be used.</span></span> <span data-ttu-id="a8b35-119">Définissez sur 0x00000013 pour EAP-TLS et 0x00000026 pour PEAP.</span><span class="sxs-lookup"><span data-stu-id="a8b35-119">Set to 0x00000013 for EAP-TLS and 0x00000026 for PEAP.</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-120">**dwSizeOfSSID**</span><span class="sxs-lookup"><span data-stu-id="a8b35-120">**dwSizeOfSSID**</span></span>
</dt> <dd>

<span data-ttu-id="a8b35-121">Taille de l’identificateur réseau.</span><span class="sxs-lookup"><span data-stu-id="a8b35-121">Size of network identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-122">**bSSID**</span><span class="sxs-lookup"><span data-stu-id="a8b35-122">**bSSID**</span></span>
</dt> <dd>

<span data-ttu-id="a8b35-123">Identificateur réseau.</span><span class="sxs-lookup"><span data-stu-id="a8b35-123">Network identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8b35-124">Notes</span><span class="sxs-lookup"><span data-stu-id="a8b35-124">Remarks</span></span>

<span data-ttu-id="a8b35-125">Le fichier d’en-tête wzcsapi. h n’est pas disponible dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="a8b35-125">The header file wzcsapi.h is not available in the Windows SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b35-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8b35-126">Requirements</span></span>



| <span data-ttu-id="a8b35-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8b35-127">Requirement</span></span> | <span data-ttu-id="a8b35-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8b35-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b35-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8b35-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b35-130">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8b35-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a8b35-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8b35-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b35-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8b35-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a8b35-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a8b35-133">End of client support</span></span><br/>    | <span data-ttu-id="a8b35-134">Windows XP avec SP3</span><span class="sxs-lookup"><span data-stu-id="a8b35-134">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="a8b35-135">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="a8b35-135">End of server support</span></span><br/>    | <span data-ttu-id="a8b35-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8b35-136">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="a8b35-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8b35-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8b35-138"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b35-138"><dt>Wzcsapi.h</dt></span></span> </dl> |



 

 




