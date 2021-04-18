---
title: Méthode SetBrokerNonHAMode de la classe Win32_SessionBrokerServiceProperties
description: Migre les données du SQL Server central vers une base de données locale. Il configure également le serveur Broker pour utiliser la base de données locale.
ms.assetid: a73908be-0cc8-4512-842c-439d5cf18ed4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetBrokerNonHAMode
- Services Bureau à distance de la méthode SetBrokerNonHAMode, classe Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de la classe Services Bureau à distance, méthode SetBrokerNonHAMode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerNonHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef811bf8024f8e89f9739461dfa8499891077f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512164"
---
# <a name="setbrokernonhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="fe92d-107">Méthode SetBrokerNonHAMode de la \_ classe Win32 SessionBrokerServiceProperties</span><span class="sxs-lookup"><span data-stu-id="fe92d-107">SetBrokerNonHAMode method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="fe92d-108">Migre les données du SQL Server central vers une base de données locale.</span><span class="sxs-lookup"><span data-stu-id="fe92d-108">Migrates data from central SQL Server to a local database.</span></span> <span data-ttu-id="fe92d-109">Il configure également le serveur Broker pour utiliser la base de données locale.</span><span class="sxs-lookup"><span data-stu-id="fe92d-109">It also configures the broker server to use the local database.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe92d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe92d-110">Syntax</span></span>


```mof
uint32 SetBrokerNonHAMode(
  [in] string connStringToCentralDBRdcms
);
```



## <a name="parameters"></a><span data-ttu-id="fe92d-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe92d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe92d-112">*connStringToCentralDBRdcms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe92d-112">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe92d-113">Chaîne de connexion à la base de données centrale.</span><span class="sxs-lookup"><span data-stu-id="fe92d-113">Connection string to the central database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe92d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe92d-114">Requirements</span></span>



| <span data-ttu-id="fe92d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe92d-115">Requirement</span></span> | <span data-ttu-id="fe92d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe92d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe92d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe92d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fe92d-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe92d-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fe92d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe92d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fe92d-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fe92d-120">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="fe92d-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fe92d-121">Namespace</span></span><br/>                | <span data-ttu-id="fe92d-122">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="fe92d-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="fe92d-123">MOF</span><span class="sxs-lookup"><span data-stu-id="fe92d-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe92d-124"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe92d-124"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe92d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fe92d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe92d-126"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe92d-126"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe92d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe92d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe92d-128">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="fe92d-128">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





