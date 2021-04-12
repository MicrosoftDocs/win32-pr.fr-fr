---
title: Méthode IsDbReachable de la classe Win32_SessionBrokerServiceProperties
description: Vérifie si la base de données est accessible.
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsDbReachable
- Services Bureau à distance de la méthode IsDbReachable, classe Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de la classe Services Bureau à distance, méthode IsDbReachable
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.IsDbReachable
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a59b8b0eba80dd832b3967b5e626642684f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465290"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="d3ccc-106">Méthode IsDbReachable de la \_ classe Win32 SessionBrokerServiceProperties</span><span class="sxs-lookup"><span data-stu-id="d3ccc-106">IsDbReachable method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="d3ccc-107">Vérifie si la base de données est accessible.</span><span class="sxs-lookup"><span data-stu-id="d3ccc-107">Checks if the database is reachable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ccc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3ccc-108">Syntax</span></span>


```mof
uint32 IsDbReachable(
  [in] string connStringToDb,
  [in] string connSecondaryStringToDb,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a><span data-ttu-id="d3ccc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3ccc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3ccc-110">*connStringToDb* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3ccc-110">*connStringToDb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3ccc-111">Chaîne de connexion à la base de données.</span><span class="sxs-lookup"><span data-stu-id="d3ccc-111">The connection string to the database.</span></span>

</dd> <dt>

<span data-ttu-id="d3ccc-112">*connSecondaryStringToDb* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3ccc-112">*connSecondaryStringToDb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3ccc-113">Chaîne de connexion secondaire à la base de données centrale.</span><span class="sxs-lookup"><span data-stu-id="d3ccc-113">Secondary connection string to the central database.</span></span>

<span data-ttu-id="d3ccc-114">**Windows server 2012 R2 et Windows server 2012 :** Ce paramètre n’est pas disponible avant Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d3ccc-114">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="d3ccc-115">*activeBrokerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3ccc-115">*activeBrokerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3ccc-116">Nom de service Broker actif.</span><span class="sxs-lookup"><span data-stu-id="d3ccc-116">Active broker name.</span></span>

<span data-ttu-id="d3ccc-117">**Windows server 2012 R2 et Windows server 2012 :** Ce paramètre n’est pas disponible avant Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d3ccc-117">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3ccc-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3ccc-118">Requirements</span></span>



| <span data-ttu-id="d3ccc-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3ccc-119">Requirement</span></span> | <span data-ttu-id="d3ccc-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3ccc-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ccc-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3ccc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ccc-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3ccc-122">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d3ccc-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3ccc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ccc-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d3ccc-124">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="d3ccc-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d3ccc-125">Namespace</span></span><br/>                | <span data-ttu-id="d3ccc-126">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="d3ccc-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="d3ccc-127">MOF</span><span class="sxs-lookup"><span data-stu-id="d3ccc-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3ccc-128"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3ccc-128"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3ccc-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d3ccc-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3ccc-130"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3ccc-130"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3ccc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3ccc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3ccc-132">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="d3ccc-132">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





