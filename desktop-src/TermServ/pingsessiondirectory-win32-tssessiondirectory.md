---
title: Méthode PingSessionDirectory de la classe Win32_TSSessionDirectory
description: Vérifie si le serveur Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance) est disponible.
ms.assetid: 89243998-5ab2-4ea6-aa31-95ec63289055
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode PingSessionDirectory
- Services Bureau à distance de la méthode PingSessionDirectory, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode PingSessionDirectory
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.PingSessionDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4022a0c34094a19651522c3f8153038c6d9df503
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508750"
---
# <a name="pingsessiondirectory-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="5a0ec-106">Méthode PingSessionDirectory de la \_ classe Win32 TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="5a0ec-106">PingSessionDirectory method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="5a0ec-107">Vérifie si le serveur Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance) est disponible.</span><span class="sxs-lookup"><span data-stu-id="5a0ec-107">Checks whether the Remote Desktop Connection Broker (RD Connection Broker) server is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a0ec-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a0ec-108">Syntax</span></span>


```mof
uint32 PingSessionDirectory(
  [in] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="5a0ec-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a0ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a0ec-110">*Nom du serveur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a0ec-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a0ec-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a0ec-111">Type: **string**</span></span>

<span data-ttu-id="5a0ec-112">Nom du serveur du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="5a0ec-112">Name of the RD Connection Broker server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a0ec-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a0ec-113">Return value</span></span>

<span data-ttu-id="5a0ec-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a0ec-114">Type: **uint32**</span></span>

<span data-ttu-id="5a0ec-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="5a0ec-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="5a0ec-116">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="5a0ec-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a0ec-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5a0ec-117">Remarks</span></span>

<span data-ttu-id="5a0ec-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="5a0ec-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5a0ec-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5a0ec-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5a0ec-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="5a0ec-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5a0ec-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5a0ec-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a0ec-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a0ec-122">Requirements</span></span>



| <span data-ttu-id="5a0ec-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a0ec-123">Requirement</span></span> | <span data-ttu-id="5a0ec-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a0ec-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a0ec-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a0ec-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5a0ec-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a0ec-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5a0ec-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a0ec-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5a0ec-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a0ec-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5a0ec-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5a0ec-129">Namespace</span></span><br/>                | <span data-ttu-id="5a0ec-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="5a0ec-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5a0ec-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5a0ec-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a0ec-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a0ec-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a0ec-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5a0ec-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a0ec-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a0ec-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a0ec-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a0ec-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a0ec-136">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="5a0ec-136">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

