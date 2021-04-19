---
title: Méthode SetVirtualizeLoopbackAddressesEnabled de la classe Win32_TSVirtualIP
description: Définit la valeur de la propriété VirtualizeLoopbackAddressesEnabled.
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetVirtualizeLoopbackAddressesEnabled
- Services Bureau à distance de la méthode SetVirtualizeLoopbackAddressesEnabled, classe Win32_TSVirtualIP
- Win32_TSVirtualIP de la classe Services Bureau à distance, méthode SetVirtualizeLoopbackAddressesEnabled
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed74e74a9f0fcbcd070a50743e6182649c2dca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510525"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="66ac9-106">Méthode SetVirtualizeLoopbackAddressesEnabled de la \_ classe Win32 TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="66ac9-106">SetVirtualizeLoopbackAddressesEnabled method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="66ac9-107">Définit la valeur de la propriété **VirtualizeLoopbackAddressesEnabled** .</span><span class="sxs-lookup"><span data-stu-id="66ac9-107">Sets the **VirtualizeLoopbackAddressesEnabled** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="66ac9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66ac9-108">Syntax</span></span>


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="66ac9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66ac9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66ac9-110">*VirtualizeLoopbackAddressesEnabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="66ac9-110">*VirtualizeLoopbackAddressesEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66ac9-111">Spécifie s’il faut activer la virtualisation des adresses de bouclage.</span><span class="sxs-lookup"><span data-stu-id="66ac9-111">Specifies whether to enable loopback address virtualization.</span></span> <span data-ttu-id="66ac9-112">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="66ac9-112">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="66ac9-113">0</span><span class="sxs-lookup"><span data-stu-id="66ac9-113">0</span></span>
</dt> <dd>

<span data-ttu-id="66ac9-114">N’activez pas la virtualisation des adresses de bouclage.</span><span class="sxs-lookup"><span data-stu-id="66ac9-114">Do not enable loopback address virtualization.</span></span>

</dd> <dt>

<span data-ttu-id="66ac9-115">1</span><span class="sxs-lookup"><span data-stu-id="66ac9-115">1</span></span>
</dt> <dd>

<span data-ttu-id="66ac9-116">Activez la virtualisation des adresses de bouclage.</span><span class="sxs-lookup"><span data-stu-id="66ac9-116">Enable loopback address virtualization.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66ac9-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66ac9-117">Return value</span></span>

<span data-ttu-id="66ac9-118">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="66ac9-118">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="66ac9-119">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="66ac9-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="66ac9-120">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="66ac9-120">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="66ac9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66ac9-121">Requirements</span></span>



| <span data-ttu-id="66ac9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66ac9-122">Requirement</span></span> | <span data-ttu-id="66ac9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="66ac9-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66ac9-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66ac9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="66ac9-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="66ac9-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="66ac9-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66ac9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="66ac9-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="66ac9-127">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="66ac9-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="66ac9-128">Namespace</span></span><br/>                | <span data-ttu-id="66ac9-129">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="66ac9-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="66ac9-130">MOF</span><span class="sxs-lookup"><span data-stu-id="66ac9-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66ac9-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66ac9-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="66ac9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="66ac9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66ac9-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66ac9-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66ac9-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66ac9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66ac9-135">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="66ac9-135">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





