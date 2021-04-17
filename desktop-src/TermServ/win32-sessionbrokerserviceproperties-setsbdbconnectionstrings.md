---
title: Méthode SetSBDbConnectionStrings de la classe Win32_SessionBrokerServiceProperties
description: Enregistre les chaînes de connexion de base de données, primaires et secondaires, dans le registre.
ms.assetid: a9a20eca-22d9-495c-b976-2952c97be67e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSBDbConnectionStrings
- Services Bureau à distance de la méthode SetSBDbConnectionStrings, classe Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de la classe Services Bureau à distance, méthode SetSBDbConnectionStrings
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetSBDbConnectionStrings
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4aa02cabe89e434fb8b24b308bbe2ec51fa5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465287"
---
# <a name="setsbdbconnectionstrings-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="8d20c-106">Méthode SetSBDbConnectionStrings de la \_ classe Win32 SessionBrokerServiceProperties</span><span class="sxs-lookup"><span data-stu-id="8d20c-106">SetSBDbConnectionStrings method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="8d20c-107">Enregistre les chaînes de connexion de base de données, primaires et secondaires, dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8d20c-107">Saves DB connection strings, both primary and secondary, in the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d20c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d20c-108">Syntax</span></span>


```mof
uint32 SetSBDbConnectionStrings(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms
);
```



## <a name="parameters"></a><span data-ttu-id="8d20c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d20c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d20c-110">*connStringToCentralDBRdcms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d20c-110">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d20c-111">Chaîne de connexion principale.</span><span class="sxs-lookup"><span data-stu-id="8d20c-111">The primary connection string.</span></span>

</dd> <dt>

<span data-ttu-id="8d20c-112">*secondaryConnStringToCentralDBRdcms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d20c-112">*secondaryConnStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d20c-113">Chaîne de connexion secondaire.</span><span class="sxs-lookup"><span data-stu-id="8d20c-113">The secondary connection string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d20c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d20c-114">Requirements</span></span>



| <span data-ttu-id="8d20c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d20c-115">Requirement</span></span> | <span data-ttu-id="8d20c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d20c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d20c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d20c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8d20c-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d20c-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8d20c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d20c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8d20c-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8d20c-120">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="8d20c-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8d20c-121">Namespace</span></span><br/>                | <span data-ttu-id="8d20c-122">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="8d20c-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="8d20c-123">MOF</span><span class="sxs-lookup"><span data-stu-id="8d20c-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d20c-124"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d20c-124"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d20c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8d20c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d20c-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d20c-126"><dt>RDMS.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8d20c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d20c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d20c-128">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="8d20c-128">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





