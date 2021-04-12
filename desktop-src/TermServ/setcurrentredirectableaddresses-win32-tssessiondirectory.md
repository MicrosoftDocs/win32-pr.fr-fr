---
title: Méthode SetCurrentRedirectableAddresses de la classe Win32_TSSessionDirectory
description: Définit la liste configurée des adresses DNS éligibles qui peuvent être utilisées pour la redirection.
ms.assetid: cad6a8a8-fdf1-406e-abeb-37acb396ac16
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetCurrentRedirectableAddresses
- Services Bureau à distance de la méthode SetCurrentRedirectableAddresses, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode SetCurrentRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e70f8d108e908155b5db3e6800f4be26811c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384968"
---
# <a name="setcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="f9395-106">Méthode SetCurrentRedirectableAddresses de la \_ classe Win32 TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="f9395-106">SetCurrentRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="f9395-107">La méthode **SetCurrentRedirectableAddresses** définit la liste configurée des adresses DNS éligibles qui peuvent être utilisées pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="f9395-107">The **SetCurrentRedirectableAddresses** method sets the configured list of DNS eligible addresses that can be used for redirection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9395-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9395-108">Syntax</span></span>


```mof
uint32 SetCurrentRedirectableAddresses(
  [in] uint32 fTokenRedirection,
  [in] string IPAddresses[]
);
```



## <a name="parameters"></a><span data-ttu-id="f9395-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9395-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9395-110">*fTokenRedirection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9395-110">*fTokenRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9395-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9395-111">Type: **uint32**</span></span>

<span data-ttu-id="f9395-112">Indicateur qui signale si la redirection des jetons doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f9395-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="f9395-113">*AdressesIP* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9395-113">*IPAddresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9395-114">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="f9395-114">Type: **string\[\]**</span></span>

<span data-ttu-id="f9395-115">Tableau de chaînes qui représente la liste des adresses IP éligibles DNS qui peuvent être utilisées pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="f9395-115">An array of strings that represents the list of DNS eligible IP addresses that can be used for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9395-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9395-116">Return value</span></span>

<span data-ttu-id="f9395-117">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9395-117">Type: **uint32**</span></span>

<span data-ttu-id="f9395-118">Retourne 0 en cas de réussite ; Sinon, retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="f9395-118">Returns 0 on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="f9395-119">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f9395-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9395-120">Notes</span><span class="sxs-lookup"><span data-stu-id="f9395-120">Remarks</span></span>

<span data-ttu-id="f9395-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="f9395-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f9395-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f9395-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f9395-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="f9395-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f9395-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f9395-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9395-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9395-125">Requirements</span></span>



| <span data-ttu-id="f9395-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9395-126">Requirement</span></span> | <span data-ttu-id="f9395-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9395-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9395-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9395-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f9395-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9395-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f9395-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9395-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f9395-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9395-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9395-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f9395-132">Namespace</span></span><br/>                | <span data-ttu-id="f9395-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="f9395-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f9395-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f9395-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9395-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9395-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9395-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f9395-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9395-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9395-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9395-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9395-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9395-139">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="f9395-139">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

