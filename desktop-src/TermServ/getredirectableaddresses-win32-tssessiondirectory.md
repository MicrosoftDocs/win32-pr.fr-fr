---
title: Méthode GetRedirectableAddresses de la classe Win32_TSSessionDirectory
description: Obtient la liste complète des adresses DNS éligibles.
ms.assetid: 828079e7-472c-4428-97a0-2d5dedcdae91
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetRedirectableAddresses
- Services Bureau à distance de la méthode GetRedirectableAddresses, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode GetRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd5348c11b5f2aba442f7f13ef06488c6d849be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032378"
---
# <a name="getredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="2ad12-106">Méthode GetRedirectableAddresses de la \_ classe Win32 TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="2ad12-106">GetRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="2ad12-107">Obtient la liste complète des adresses DNS éligibles.</span><span class="sxs-lookup"><span data-stu-id="2ad12-107">Obtains the entire list of DNS eligible addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ad12-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ad12-108">Syntax</span></span>


```mof
uint32 GetRedirectableAddresses(
  [in]  uint32 fTokenRedirection,
  [out] string IPAddresses[],
  [out] string AdapterNames[],
  [out] string NetConName[]
);
```



## <a name="parameters"></a><span data-ttu-id="2ad12-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ad12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ad12-110">*fTokenRedirection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ad12-110">*fTokenRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ad12-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2ad12-111">Type: **uint32**</span></span>

<span data-ttu-id="2ad12-112">Indicateur qui signale si la redirection des jetons doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="2ad12-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="2ad12-113">*AdressesIP* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ad12-113">*IPAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ad12-114">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="2ad12-114">Type: **string\[\]**</span></span>

<span data-ttu-id="2ad12-115">Liste complète des adresses IP disponibles pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="2ad12-115">The entire list of IP addresses that are available for redirection.</span></span>

</dd> <dt>

<span data-ttu-id="2ad12-116">*AdapterNames* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ad12-116">*AdapterNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ad12-117">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="2ad12-117">Type: **string\[\]**</span></span>

<span data-ttu-id="2ad12-118">Liste des noms de cartes réseau qui sont associés aux adresses disponibles pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="2ad12-118">The list of network adapter names that are associated with the addresses that are available for redirection.</span></span>

</dd> <dt>

<span data-ttu-id="2ad12-119">*NetConName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ad12-119">*NetConName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ad12-120">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="2ad12-120">Type: **string\[\]**</span></span>

<span data-ttu-id="2ad12-121">Liste des noms de connexion réseau associés aux adresses disponibles pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="2ad12-121">The list of network connection names that are associated with the addresses that are available for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ad12-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2ad12-122">Return value</span></span>

<span data-ttu-id="2ad12-123">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2ad12-123">Type: **uint32**</span></span>

<span data-ttu-id="2ad12-124">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="2ad12-124">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2ad12-125">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2ad12-125">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ad12-126">Notes</span><span class="sxs-lookup"><span data-stu-id="2ad12-126">Remarks</span></span>

<span data-ttu-id="2ad12-127">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="2ad12-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2ad12-128">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2ad12-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2ad12-129">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="2ad12-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2ad12-130">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2ad12-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ad12-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ad12-131">Requirements</span></span>



| <span data-ttu-id="2ad12-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ad12-132">Requirement</span></span> | <span data-ttu-id="2ad12-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ad12-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ad12-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ad12-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2ad12-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ad12-135">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2ad12-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ad12-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2ad12-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ad12-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2ad12-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2ad12-138">Namespace</span></span><br/>                | <span data-ttu-id="2ad12-139">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="2ad12-139">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2ad12-140">MOF</span><span class="sxs-lookup"><span data-stu-id="2ad12-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ad12-141"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ad12-141"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ad12-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2ad12-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ad12-143"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ad12-143"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ad12-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ad12-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ad12-145">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="2ad12-145">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

