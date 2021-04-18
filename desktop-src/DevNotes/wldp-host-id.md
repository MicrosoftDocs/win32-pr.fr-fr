---
description: Identifie le type d’hôte de l’appelant WLDP.
ms.assetid: E8E603CC-9CB2-4C3B-9F06-9B06C7B5D752
title: Énumération WLDP_HOST_ID (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_ID
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 8914f93ff5936451b71b855473a09cb1d06584b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522924"
---
# <a name="wldp_host_id-enumeration"></a><span data-ttu-id="372c5-103">\_Énumération de l’ID d’hôte WLDP \_</span><span class="sxs-lookup"><span data-stu-id="372c5-103">WLDP\_HOST\_ID enumeration</span></span>

<span data-ttu-id="372c5-104">Identifie le type d’hôte de l’appelant WLDP.</span><span class="sxs-lookup"><span data-stu-id="372c5-104">Identifies the host type of the WLDP caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="372c5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="372c5-105">Syntax</span></span>


```C++
typedef enum _WLDP_HOST_ID { 
   WLDP_HOST_ID_UNKNOWN     = 0,
   WLDP_HOST_ID_GLOBAL      = 1,
  WLDP_HOST_ID_VBA          = 2,
   WLDP_HOST_ID_WSH         = 3,
   WLDP_HOST_ID_POWERSHELL  = 4,
   WLDP_HOST_ID_IE          = 5,
   WLDP_HOST_ID_MSI         = 6,
   WLDP_HOST_ID_MAX         = 7
} WLDP_HOST_ID, *PWLDP_HOST_ID;
```



## <a name="constants"></a><span data-ttu-id="372c5-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="372c5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="372c5-107"><span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span>**WLDP \_ ID d’hôte \_ \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="372c5-107"><span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span> **WLDP\_HOST\_ID\_UNKNOWN**</span></span> 
</dt> <dd>

<span data-ttu-id="372c5-108">Le type d’hôte est inconnu.</span><span class="sxs-lookup"><span data-stu-id="372c5-108">The host type is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="372c5-109"><span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span>**WLDP \_ ID d’hôte \_ \_ Global**</span><span class="sxs-lookup"><span data-stu-id="372c5-109"><span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span> **WLDP\_HOST\_ID\_GLOBAL**</span></span>
</dt> <dd>

<span data-ttu-id="372c5-110">Le type d’hôte est stratégie globale.</span><span class="sxs-lookup"><span data-stu-id="372c5-110">The host type is global policy.</span></span>

</dd> <dt>

<span data-ttu-id="372c5-111"><span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**\_ID d’hôte WLDP \_ \_ VBA**</span><span class="sxs-lookup"><span data-stu-id="372c5-111"><span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**WLDP\_HOST\_ID\_VBA**</span></span>
</dt> <dd>

<span data-ttu-id="372c5-112">Le type d’hôte est VBScript.</span><span class="sxs-lookup"><span data-stu-id="372c5-112">The host type is VBScript.</span></span>

</dd> <dt>

<span data-ttu-id="372c5-113"><span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span>**WLDP \_ ID d’hôte \_ \_ WSH**</span><span class="sxs-lookup"><span data-stu-id="372c5-113"><span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span> **WLDP\_HOST\_ID\_WSH**</span></span>
</dt> <dd>

<span data-ttu-id="372c5-114">Le type d’hôte est Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="372c5-114">The host type is Windows Script Host.</span></span>

</dd> <dt>

<span data-ttu-id="372c5-115"><span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span>**WLDP \_ ID d’hôte \_ \_ PowerShell**</span><span class="sxs-lookup"><span data-stu-id="372c5-115"><span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span> **WLDP\_HOST\_ID\_POWERSHELL**</span></span>
</dt> <dd>

<span data-ttu-id="372c5-116">Le type d’hôte est Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="372c5-116">The host type is Windows Powershell.</span></span>

</dd> <dt>

<span data-ttu-id="372c5-117"><span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span>**WLDP \_ ID d’hôte \_ \_ IE**</span><span class="sxs-lookup"><span data-stu-id="372c5-117"><span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span> **WLDP\_HOST\_ID\_IE**</span></span>
</dt> <dd>

<span data-ttu-id="372c5-118">Le type d’hôte est Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="372c5-118">The host type is Internet Explorer.</span></span>

</dd> <dt>

<span data-ttu-id="372c5-119"><span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span>**WLDP \_ ID d’hôte \_ \_ MSI**</span><span class="sxs-lookup"><span data-stu-id="372c5-119"><span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span> **WLDP\_HOST\_ID\_MSI**</span></span>
</dt> <dd>

<span data-ttu-id="372c5-120">Le type d’hôte est le Microsoft Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="372c5-120">The host type is the Microsoft Windows Installer.</span></span>

</dd> <dt>

<span data-ttu-id="372c5-121"><span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span>**WLDP \_ ID d’hôte \_ \_ Max** .</span><span class="sxs-lookup"><span data-stu-id="372c5-121"><span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span> **WLDP\_HOST\_ID\_MAX**</span></span> 
</dt> <dd>

<span data-ttu-id="372c5-122">Valeur d’énumération maximale.</span><span class="sxs-lookup"><span data-stu-id="372c5-122">The maximum enumeration value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="372c5-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="372c5-123">Requirements</span></span>



| <span data-ttu-id="372c5-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="372c5-124">Requirement</span></span> | <span data-ttu-id="372c5-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="372c5-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="372c5-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="372c5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="372c5-127">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="372c5-127">Windows 8 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="372c5-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="372c5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="372c5-129">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="372c5-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="372c5-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="372c5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="372c5-131"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="372c5-131"><dt>Wldp.h</dt></span></span> </dl> |



 

 




