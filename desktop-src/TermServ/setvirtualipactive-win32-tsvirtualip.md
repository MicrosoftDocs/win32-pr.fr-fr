---
title: Méthode SetVirtualIPActive de la classe Win32_TSVirtualIP
description: Définit la valeur de la propriété VirtualIPActive.
ms.assetid: e485aeb1-afdf-4572-bac7-daa80d903edc
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetVirtualIPActive
- Services Bureau à distance de la méthode SetVirtualIPActive, classe Win32_TSVirtualIP
- Win32_TSVirtualIP de la classe Services Bureau à distance, méthode SetVirtualIPActive
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06534c967c5d86a7a19c060254b3b988ff98b17e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942324"
---
# <a name="setvirtualipactive-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="a82db-106">Méthode SetVirtualIPActive de la \_ classe Win32 TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="a82db-106">SetVirtualIPActive method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="a82db-107">Définit la valeur de la propriété **VirtualIPActive** .</span><span class="sxs-lookup"><span data-stu-id="a82db-107">Sets the **VirtualIPActive** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a82db-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a82db-108">Syntax</span></span>


```mof
uint32 SetVirtualIPActive(
  [in] uint32 VirtualIPActive
);
```



## <a name="parameters"></a><span data-ttu-id="a82db-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a82db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a82db-110">*VirtualIPActive* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a82db-110">*VirtualIPActive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a82db-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a82db-111">Type: **uint32**</span></span>

<span data-ttu-id="a82db-112">Spécifie si la virtualisation IP est active sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="a82db-112">Specifies if IP virtualization is active on the server.</span></span> <span data-ttu-id="a82db-113">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a82db-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="a82db-114">zéro</span><span class="sxs-lookup"><span data-stu-id="a82db-114">zero</span></span>
</dt> <dd>

<span data-ttu-id="a82db-115">La virtualisation IP n’est pas active.</span><span class="sxs-lookup"><span data-stu-id="a82db-115">IP virtualization is not active.</span></span>

</dd> <dt>

<span data-ttu-id="a82db-116">différente</span><span class="sxs-lookup"><span data-stu-id="a82db-116">nonzero</span></span>
</dt> <dd>

<span data-ttu-id="a82db-117">La virtualisation IP est active.</span><span class="sxs-lookup"><span data-stu-id="a82db-117">IP virtualization is active.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a82db-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a82db-118">Return value</span></span>

<span data-ttu-id="a82db-119">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a82db-119">Type: **uint32**</span></span>

<span data-ttu-id="a82db-120">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="a82db-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a82db-121">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a82db-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="a82db-122">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="a82db-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a82db-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a82db-123">Requirements</span></span>



| <span data-ttu-id="a82db-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a82db-124">Requirement</span></span> | <span data-ttu-id="a82db-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a82db-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a82db-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a82db-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a82db-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a82db-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a82db-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a82db-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a82db-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a82db-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="a82db-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a82db-130">Namespace</span></span><br/>                | <span data-ttu-id="a82db-131">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="a82db-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a82db-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a82db-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a82db-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a82db-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a82db-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a82db-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a82db-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a82db-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a82db-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a82db-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a82db-137">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="a82db-137">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





