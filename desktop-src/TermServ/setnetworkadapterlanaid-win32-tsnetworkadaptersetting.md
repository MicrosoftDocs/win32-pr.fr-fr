---
title: Méthode SetNetworkAdapterLanaID de la classe Win32_TSNetworkAdapterSetting
description: Spécifie le numéro de carte réseau local (LANA) de la carte réseau à définir.
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetNetworkAdapterLanaID
- Services Bureau à distance de la méthode SetNetworkAdapterLanaID, classe Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting de la classe Services Bureau à distance, méthode SetNetworkAdapterLanaID
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SetNetworkAdapterLanaID
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00675ae6378041e6c06b82a7de3c1ccf27620f4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743493"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="d3214-106">Méthode SetNetworkAdapterLanaID de la \_ classe Win32 TSNetworkAdapterSetting</span><span class="sxs-lookup"><span data-stu-id="d3214-106">SetNetworkAdapterLanaID method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="d3214-107">La méthode **SetNetworkAdapterLanaID** spécifie le numéro de carte réseau local (Lana) de la carte réseau à définir.</span><span class="sxs-lookup"><span data-stu-id="d3214-107">The **SetNetworkAdapterLanaID** method specifies the Local Area Network Adapter (LANA) number of the network adapter to set.</span></span> <span data-ttu-id="d3214-108">Si l’ID de LANA spécifié n’est pas valide ou n’existe pas, une erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="d3214-108">If the LANA ID specified is not valid or does not exist, an error is returned.</span></span> <span data-ttu-id="d3214-109">La liste disponible des ID de carte LANA est obtenue en énumérant la propriété **DeviceIDList** dans la classe [**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md) .</span><span class="sxs-lookup"><span data-stu-id="d3214-109">The available list of LANA IDs is obtained by enumerating the property **DeviceIDList** in the [**Win32\_TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3214-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3214-110">Syntax</span></span>


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a><span data-ttu-id="d3214-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3214-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3214-112">*NetworkAdapterLanaID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3214-112">*NetworkAdapterLanaID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3214-113">Numéro LANA de la carte réseau à définir.</span><span class="sxs-lookup"><span data-stu-id="d3214-113">LANA number of the network adapter to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3214-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3214-114">Return value</span></span>

<span data-ttu-id="d3214-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="d3214-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d3214-116">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d3214-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3214-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d3214-117">Remarks</span></span>

<span data-ttu-id="d3214-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="d3214-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d3214-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d3214-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d3214-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="d3214-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d3214-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d3214-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3214-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3214-122">Requirements</span></span>



| <span data-ttu-id="d3214-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3214-123">Requirement</span></span> | <span data-ttu-id="d3214-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3214-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3214-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3214-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d3214-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3214-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d3214-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3214-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d3214-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3214-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d3214-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d3214-129">Namespace</span></span><br/>                | <span data-ttu-id="d3214-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="d3214-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d3214-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d3214-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3214-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3214-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3214-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d3214-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3214-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3214-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3214-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3214-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3214-136">**\_TSNetworkAdapterSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="d3214-136">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

