---
title: Méthode DeleteEx de la classe Win32_SessionBrokerFarmAccount
description: La \_ classe SessionBrokerFarmAccount Win32 n’est plus disponible pour une utilisation à partir de Windows Server 2012. | Méthode DeleteEx de la classe Win32_SessionBrokerFarmAccount
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DeleteEx
- Services Bureau à distance de la méthode DeleteEx, classe Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount de la classe Services Bureau à distance, méthode DeleteEx
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount.DeleteEx
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdad7b1c7af85337ace59690bb44f4309254eb76
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531272"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a><span data-ttu-id="e6a91-107">Méthode DeleteEx de la \_ classe Win32 SessionBrokerFarmAccount</span><span class="sxs-lookup"><span data-stu-id="e6a91-107">DeleteEx method of the Win32\_SessionBrokerFarmAccount class</span></span>

<span data-ttu-id="e6a91-108">\[La [**classe \_ SessionBrokerFarmAccount Win32**](win32-sessionbrokerfarmaccount.md) n’est plus disponible pour une utilisation à partir de Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="e6a91-108">\[The [**Win32\_SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md) class is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="e6a91-109">Supprime le compte de batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="e6a91-109">Deletes the farm account.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a91-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6a91-110">Syntax</span></span>


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a><span data-ttu-id="e6a91-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6a91-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6a91-112">*DeleteComputerObject* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6a91-112">*DeleteComputerObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6a91-113">Indique si l’objet ordinateur associé à la batterie de serveurs doit être supprimé de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e6a91-113">Indicates whether the computer object associated with the farm is to be removed from Active Directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6a91-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6a91-114">Return value</span></span>

<span data-ttu-id="e6a91-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="e6a91-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e6a91-116">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e6a91-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a91-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6a91-117">Requirements</span></span>



| <span data-ttu-id="e6a91-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6a91-118">Requirement</span></span> | <span data-ttu-id="e6a91-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6a91-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a91-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6a91-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e6a91-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6a91-121">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e6a91-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6a91-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e6a91-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e6a91-123">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="e6a91-124">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e6a91-124">End of client support</span></span><br/>    | <span data-ttu-id="e6a91-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6a91-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e6a91-126">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e6a91-126">End of server support</span></span><br/>    | <span data-ttu-id="e6a91-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e6a91-127">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="e6a91-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e6a91-128">Namespace</span></span><br/>                | <span data-ttu-id="e6a91-129">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="e6a91-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="e6a91-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e6a91-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6a91-131"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6a91-131"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6a91-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e6a91-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6a91-133"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6a91-133"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6a91-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6a91-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a91-135">**\_SessionBrokerFarmAccount Win32**</span><span class="sxs-lookup"><span data-stu-id="e6a91-135">**Win32\_SessionBrokerFarmAccount**</span></span>](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





