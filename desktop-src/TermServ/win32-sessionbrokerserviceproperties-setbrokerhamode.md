---
title: Méthode SetBrokerHAMode de la classe Win32_SessionBrokerServiceProperties
description: Migre les données d’une base de données WID locale vers la nouvelle base de données SQL Server. Il configure également le serveur Broker pour utiliser le serveur SQL Server central.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetBrokerHAMode
- Services Bureau à distance de la méthode SetBrokerHAMode, classe Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de la classe Services Bureau à distance, méthode SetBrokerHAMode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4526f8ded96086ccf223b3c8e5aad72d9e0262cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103672"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="dc800-107">Méthode SetBrokerHAMode de la \_ classe Win32 SessionBrokerServiceProperties</span><span class="sxs-lookup"><span data-stu-id="dc800-107">SetBrokerHAMode method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="dc800-108">Migre les données d’une base de données WID locale vers la nouvelle base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dc800-108">Migrates data from a local WID database to the new SQL server-based database.</span></span> <span data-ttu-id="dc800-109">Il configure également le serveur Broker pour utiliser le serveur SQL Server central.</span><span class="sxs-lookup"><span data-stu-id="dc800-109">It also configures the broker server to use the central SQL server.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc800-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc800-110">Syntax</span></span>


```mof
uint32 SetBrokerHAMode(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms,
  [in] string brokerDnsRRName,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a><span data-ttu-id="dc800-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc800-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc800-112">*connStringToCentralDBRdcms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc800-112">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc800-113">Chaîne de connexion à la base de données centrale.</span><span class="sxs-lookup"><span data-stu-id="dc800-113">Connection string to the central database.</span></span>

</dd> <dt>

<span data-ttu-id="dc800-114">*secondaryConnStringToCentralDBRdcms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc800-114">*secondaryConnStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc800-115">Chaîne de connexion secondaire à la base de données centrale.</span><span class="sxs-lookup"><span data-stu-id="dc800-115">Secondary connection string to the central database.</span></span>

<span data-ttu-id="dc800-116">**Windows server 2012 R2 et Windows server 2012 :** Ce paramètre n’est pas disponible avant Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="dc800-116">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="dc800-117">*brokerDnsRRName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc800-117">*brokerDnsRRName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc800-118">Nom DNS du Service Broker.</span><span class="sxs-lookup"><span data-stu-id="dc800-118">Broker DNS name.</span></span>

</dd> <dt>

<span data-ttu-id="dc800-119">*activeBrokerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc800-119">*activeBrokerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc800-120">Nom de service Broker actif.</span><span class="sxs-lookup"><span data-stu-id="dc800-120">Active broker name.</span></span>

<span data-ttu-id="dc800-121">**Windows server 2012 R2 et Windows server 2012 :** Ce paramètre n’est pas disponible avant Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="dc800-121">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc800-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc800-122">Requirements</span></span>



| <span data-ttu-id="dc800-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc800-123">Requirement</span></span> | <span data-ttu-id="dc800-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc800-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc800-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc800-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dc800-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc800-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dc800-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc800-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dc800-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dc800-128">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="dc800-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dc800-129">Namespace</span></span><br/>                | <span data-ttu-id="dc800-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="dc800-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="dc800-131">MOF</span><span class="sxs-lookup"><span data-stu-id="dc800-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc800-132"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc800-132"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc800-133">DLL</span><span class="sxs-lookup"><span data-stu-id="dc800-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc800-134"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc800-134"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc800-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc800-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc800-136">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="dc800-136">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





