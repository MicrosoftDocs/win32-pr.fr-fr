---
title: Méthode SetServerWeight de la classe Win32_TSSessionDirectory
description: Définit la valeur du poids du serveur pour l’équilibrage de charge de Connexion Bureau à distance Broker pour les connexions Bureau à distance.
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetServerWeight
- Services Bureau à distance de la méthode SetServerWeight, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode SetServerWeight
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetServerWeight
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e8456fa590de0c9d6236f96f3b09c16087d730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465974"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="9703b-106">Méthode SetServerWeight de la \_ classe Win32 TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="9703b-106">SetServerWeight method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="9703b-107">Définit la valeur du poids du serveur pour l’équilibrage de charge de Connexion Bureau à distance Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="9703b-107">Sets the server weight value for Remote Desktop Connection Broker (RD Connection Broker) load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="9703b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9703b-108">Syntax</span></span>


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a><span data-ttu-id="9703b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9703b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9703b-110">*ServerWeightValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9703b-110">*ServerWeightValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9703b-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9703b-111">Type: **uint32**</span></span>

<span data-ttu-id="9703b-112">Valeur de poids du serveur.</span><span class="sxs-lookup"><span data-stu-id="9703b-112">The server weight value.</span></span> <span data-ttu-id="9703b-113">La plage valide est comprise entre 1 et 10000.</span><span class="sxs-lookup"><span data-stu-id="9703b-113">The valid range is 1 to 10000.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9703b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9703b-114">Remarks</span></span>

<span data-ttu-id="9703b-115">Par défaut, dans l’interface utilisateur de Services Bureau à distance configuration, la valeur du poids du serveur est 100.</span><span class="sxs-lookup"><span data-stu-id="9703b-115">By default in the user interface of Remote Desktop Services Configuration, the server weight value is 100.</span></span> <span data-ttu-id="9703b-116">Le poids du serveur est relatif.</span><span class="sxs-lookup"><span data-stu-id="9703b-116">The server weight is relative.</span></span> <span data-ttu-id="9703b-117">Par conséquent, si vous affectez à un serveur la valeur 100 et une valeur de 200, le serveur avec un poids relatif de 200 recevra deux fois le nombre de sessions.</span><span class="sxs-lookup"><span data-stu-id="9703b-117">Therefore, if you assign one server a value of 100, and one a value of 200, the server with a relative weight of 200 will receive twice the number of sessions.</span></span>

<span data-ttu-id="9703b-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="9703b-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9703b-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9703b-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9703b-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="9703b-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9703b-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9703b-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9703b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9703b-122">Requirements</span></span>



| <span data-ttu-id="9703b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9703b-123">Requirement</span></span> | <span data-ttu-id="9703b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="9703b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9703b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9703b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9703b-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9703b-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="9703b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9703b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9703b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9703b-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9703b-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9703b-129">Namespace</span></span><br/>                | <span data-ttu-id="9703b-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="9703b-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9703b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9703b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9703b-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9703b-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9703b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9703b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9703b-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9703b-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9703b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9703b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9703b-136">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="9703b-136">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

