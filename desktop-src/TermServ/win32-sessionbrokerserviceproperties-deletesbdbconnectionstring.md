---
title: Méthode DeleteSBDbConnectionString de la classe Win32_SessionBrokerServiceProperties
description: Supprime du registre les chaînes de connexion à la base de données (primaire ou secondaire).
ms.assetid: 275dd790-bdc7-46d1-a07d-54ec6fa33e44
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DeleteSBDbConnectionString
- Services Bureau à distance de la méthode DeleteSBDbConnectionString, classe Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de la classe Services Bureau à distance, méthode DeleteSBDbConnectionString
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.DeleteSBDbConnectionString
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a9701afebe150f0c8dc0e4bf437dd23586c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513780"
---
# <a name="deletesbdbconnectionstring-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="7d87b-106">Méthode DeleteSBDbConnectionString de la \_ classe Win32 SessionBrokerServiceProperties</span><span class="sxs-lookup"><span data-stu-id="7d87b-106">DeleteSBDbConnectionString method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="7d87b-107">Supprime du registre les chaînes de connexion à la base de données (primaire ou secondaire).</span><span class="sxs-lookup"><span data-stu-id="7d87b-107">Deletes DB connection strings (primary or secondary) from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d87b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d87b-108">Syntax</span></span>


```mof
uint32 DeleteSBDbConnectionString(
  [in] boolean IsSecondaryConnString
);
```



## <a name="parameters"></a><span data-ttu-id="7d87b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d87b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d87b-110">*IsSecondaryConnString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7d87b-110">*IsSecondaryConnString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d87b-111">Si la **valeur est true**, la chaîne de connexion secondaire est supprimée.</span><span class="sxs-lookup"><span data-stu-id="7d87b-111">If **True**, secondary connection string is removed.</span></span> <span data-ttu-id="7d87b-112">Si la **valeur est false**, la chaîne de connexion principale est supprimée.</span><span class="sxs-lookup"><span data-stu-id="7d87b-112">If **False**, primary connection string is removed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d87b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d87b-113">Requirements</span></span>



| <span data-ttu-id="7d87b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d87b-114">Requirement</span></span> | <span data-ttu-id="7d87b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d87b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d87b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d87b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7d87b-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d87b-117">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7d87b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d87b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7d87b-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7d87b-119">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="7d87b-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7d87b-120">Namespace</span></span><br/>                | <span data-ttu-id="7d87b-121">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="7d87b-121">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="7d87b-122">MOF</span><span class="sxs-lookup"><span data-stu-id="7d87b-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d87b-123"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d87b-123"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d87b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7d87b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d87b-125"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d87b-125"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d87b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d87b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d87b-127">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="7d87b-127">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





