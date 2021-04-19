---
title: Méthode SetVirtualIPMode de la classe Win32_TSVirtualIP
description: Définit la valeur de la propriété VirtualIPMode.
ms.assetid: d4b39566-ad2a-493b-8022-c006a857043d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetVirtualIPMode
- Services Bureau à distance de la méthode SetVirtualIPMode, classe Win32_TSVirtualIP
- Win32_TSVirtualIP de la classe Services Bureau à distance, méthode SetVirtualIPMode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250633f5d41f5a4a7cb06a17ba9ae45bb444a018
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513616"
---
# <a name="setvirtualipmode-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="018b3-106">Méthode SetVirtualIPMode de la \_ classe Win32 TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="018b3-106">SetVirtualIPMode method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="018b3-107">Définit la valeur de la propriété **VirtualIPMode** .</span><span class="sxs-lookup"><span data-stu-id="018b3-107">Sets the **VirtualIPMode** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="018b3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="018b3-108">Syntax</span></span>


```mof
uint32 SetVirtualIPMode(
  [in] uint32 VirtualIPMode
);
```



## <a name="parameters"></a><span data-ttu-id="018b3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="018b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="018b3-110">*VirtualIPMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="018b3-110">*VirtualIPMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="018b3-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="018b3-111">Type: **uint32**</span></span>

<span data-ttu-id="018b3-112">Spécifie le mode de virtualisation IP utilisé sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="018b3-112">Specifies which IP virtualization mode is being used on the server.</span></span> <span data-ttu-id="018b3-113">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="018b3-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="018b3-114">0</span><span class="sxs-lookup"><span data-stu-id="018b3-114">0</span></span>
</dt> <dd>

<span data-ttu-id="018b3-115">Le mode de virtualisation IP est par session.</span><span class="sxs-lookup"><span data-stu-id="018b3-115">The IP virtualization mode is per-session.</span></span>

</dd> <dt>

<span data-ttu-id="018b3-116">1</span><span class="sxs-lookup"><span data-stu-id="018b3-116">1</span></span>
</dt> <dd>

<span data-ttu-id="018b3-117">Le mode de virtualisation IP est par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="018b3-117">The IP virtualization mode is per-user.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="018b3-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="018b3-118">Return value</span></span>

<span data-ttu-id="018b3-119">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="018b3-119">Type: **uint32**</span></span>

<span data-ttu-id="018b3-120">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="018b3-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="018b3-121">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="018b3-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="018b3-122">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="018b3-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="018b3-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="018b3-123">Requirements</span></span>



| <span data-ttu-id="018b3-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="018b3-124">Requirement</span></span> | <span data-ttu-id="018b3-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="018b3-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="018b3-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="018b3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="018b3-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="018b3-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="018b3-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="018b3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="018b3-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="018b3-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="018b3-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="018b3-130">Namespace</span></span><br/>                | <span data-ttu-id="018b3-131">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="018b3-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="018b3-132">MOF</span><span class="sxs-lookup"><span data-stu-id="018b3-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="018b3-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="018b3-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="018b3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="018b3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="018b3-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="018b3-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="018b3-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="018b3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="018b3-137">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="018b3-137">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





