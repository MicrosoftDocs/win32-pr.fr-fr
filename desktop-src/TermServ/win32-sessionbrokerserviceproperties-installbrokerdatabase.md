---
title: Méthode InstallBrokerDatabase de la classe Win32_SessionBrokerServiceProperties
description: Installe une base de données du Service Broker pour les connexions Bureau à distance sur un serveur SQL Server central.
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode InstallBrokerDatabase
- Services Bureau à distance de la méthode InstallBrokerDatabase, classe Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de la classe Services Bureau à distance, méthode InstallBrokerDatabase
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.InstallBrokerDatabase
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da560bd4746c41864b3c56438f841efebe71ecd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740197"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="a66b8-106">Méthode InstallBrokerDatabase de la \_ classe Win32 SessionBrokerServiceProperties</span><span class="sxs-lookup"><span data-stu-id="a66b8-106">InstallBrokerDatabase method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="a66b8-107">Installe une base de données du Service Broker pour les connexions Bureau à distance sur un serveur SQL Server central.</span><span class="sxs-lookup"><span data-stu-id="a66b8-107">Installs an RD connection broker database on a central SQL server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a66b8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a66b8-108">Syntax</span></span>


```mof
uint32 InstallBrokerDatabase(
  [in] string newDbFilePath,
  [in] string connStringToCentralDBMaster,
  [in] string centralRdcmsDbName
);
```



## <a name="parameters"></a><span data-ttu-id="a66b8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a66b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a66b8-110">*newDbFilePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a66b8-110">*newDbFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a66b8-111">nouveau chemin d’accès au fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="a66b8-111">new database file path.</span></span>

</dd> <dt>

<span data-ttu-id="a66b8-112">*connStringToCentralDBMaster* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a66b8-112">*connStringToCentralDBMaster* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a66b8-113">Chaîne de connexion à la base de données principale centrale.</span><span class="sxs-lookup"><span data-stu-id="a66b8-113">Connection string to the central database master.</span></span>

</dd> <dt>

<span data-ttu-id="a66b8-114">*centralRdcmsDbName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a66b8-114">*centralRdcmsDbName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a66b8-115">Nom de la base de données centrale.</span><span class="sxs-lookup"><span data-stu-id="a66b8-115">Name of the central database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a66b8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a66b8-116">Requirements</span></span>



| <span data-ttu-id="a66b8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a66b8-117">Requirement</span></span> | <span data-ttu-id="a66b8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a66b8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a66b8-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a66b8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a66b8-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a66b8-120">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a66b8-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a66b8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a66b8-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a66b8-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="a66b8-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a66b8-123">Namespace</span></span><br/>                | <span data-ttu-id="a66b8-124">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="a66b8-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="a66b8-125">MOF</span><span class="sxs-lookup"><span data-stu-id="a66b8-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a66b8-126"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a66b8-126"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a66b8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a66b8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a66b8-128"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a66b8-128"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a66b8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a66b8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a66b8-130">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="a66b8-130">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





