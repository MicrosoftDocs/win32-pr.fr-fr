---
title: Méthode SelectNetworkAdapterIP de la classe Win32_TSNetworkAdapterSetting
description: Sélectionne une carte réseau en fonction de l’adresse IP de la carte.
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SelectNetworkAdapterIP
- Services Bureau à distance de la méthode SelectNetworkAdapterIP, classe Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting de la classe Services Bureau à distance, méthode SelectNetworkAdapterIP
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectNetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9590bab26b3cda2e20a3dc74c5e201a2f7f86f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518075"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="3c8cd-106">Méthode SelectNetworkAdapterIP de la \_ classe Win32 TSNetworkAdapterSetting</span><span class="sxs-lookup"><span data-stu-id="3c8cd-106">SelectNetworkAdapterIP method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="3c8cd-107">Sélectionne une carte réseau en fonction de l’adresse IP de la carte.</span><span class="sxs-lookup"><span data-stu-id="3c8cd-107">Selects a network adapter based on the adapter's IP address.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c8cd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c8cd-108">Syntax</span></span>


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a><span data-ttu-id="3c8cd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c8cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c8cd-110">*NetworkAdapterIP* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c8cd-110">*NetworkAdapterIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c8cd-111">Adresse IP de la carte réseau à définir.</span><span class="sxs-lookup"><span data-stu-id="3c8cd-111">The IP address of the network adapter to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c8cd-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c8cd-112">Return value</span></span>

<span data-ttu-id="3c8cd-113">Retourne zéro si l’adresse IP spécifiée est valide et retourne un code d’erreur WMI si l’adresse IP n’est pas valide ou n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="3c8cd-113">Returns zero if the specified IP address is valid, and returns a WMI error code if the IP address is invalid or does not exist.</span></span> <span data-ttu-id="3c8cd-114">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="3c8cd-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c8cd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3c8cd-115">Remarks</span></span>

<span data-ttu-id="3c8cd-116">Vous pouvez récupérer l’adresse IP d’une carte réseau en énumérant les propriétés de la classe [**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="3c8cd-116">You can retrieve the IP address of a network adapter by enumerating the properties of the [**Win32\_TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md) class.</span></span>

<span data-ttu-id="3c8cd-117">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="3c8cd-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3c8cd-118">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3c8cd-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3c8cd-119">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="3c8cd-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3c8cd-120">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3c8cd-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c8cd-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c8cd-121">Requirements</span></span>



| <span data-ttu-id="3c8cd-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c8cd-122">Requirement</span></span> | <span data-ttu-id="3c8cd-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c8cd-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c8cd-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c8cd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3c8cd-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c8cd-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c8cd-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c8cd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3c8cd-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c8cd-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c8cd-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c8cd-128">Namespace</span></span><br/>                | <span data-ttu-id="3c8cd-129">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="3c8cd-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3c8cd-130">MOF</span><span class="sxs-lookup"><span data-stu-id="3c8cd-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c8cd-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c8cd-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c8cd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3c8cd-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c8cd-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c8cd-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c8cd-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c8cd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c8cd-135">**\_TSNetworkAdapterSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="3c8cd-135">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

