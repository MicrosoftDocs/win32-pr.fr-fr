---
title: Classe Win32_TSLicenseReportFailedPerUserSummaryEntry
description: Fournit des détails sur les domaines dans lesquels l’émission par utilisateur a échoué.
ms.assetid: f7265734-ac4d-439f-ae8b-3694e6f81f2a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportFailedPerUserSummaryEntry de la classe Services Bureau à distance
- Win32_TSLicenseReportFailedPerUserSummaryEntry de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserSummaryEntry
- Win32_TSLicenseReportFailedPerUserSummaryEntry.DomainName
- Win32_TSLicenseReportFailedPerUserSummaryEntry.FailedIssuanceCount
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f086d275c064f5df18ee01a3a38639a40913f3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941727"
---
# <a name="win32_tslicensereportfailedperusersummaryentry-class"></a><span data-ttu-id="3998f-105">\_Classe TSLicenseReportFailedPerUserSummaryEntry Win32</span><span class="sxs-lookup"><span data-stu-id="3998f-105">Win32\_TSLicenseReportFailedPerUserSummaryEntry class</span></span>

<span data-ttu-id="3998f-106">Fournit des détails sur les domaines dans lesquels l’émission par utilisateur a échoué.</span><span class="sxs-lookup"><span data-stu-id="3998f-106">Provides details of the domains to which Per User Issuance was failed.</span></span>

<span data-ttu-id="3998f-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3998f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3998f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3998f-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserSummaryEntry
{
  string DomainName;
  uint32 FailedIssuanceCount;
};
```

## <a name="members"></a><span data-ttu-id="3998f-109">Membres</span><span class="sxs-lookup"><span data-stu-id="3998f-109">Members</span></span>

<span data-ttu-id="3998f-110">La classe **Win32 \_ TSLicenseReportFailedPerUserSummaryEntry** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3998f-110">The **Win32\_TSLicenseReportFailedPerUserSummaryEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="3998f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3998f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3998f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3998f-112">Properties</span></span>

<span data-ttu-id="3998f-113">La classe **Win32 \_ TSLicenseReportFailedPerUserSummaryEntry** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3998f-113">The **Win32\_TSLicenseReportFailedPerUserSummaryEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3998f-114">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="3998f-114">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3998f-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3998f-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3998f-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3998f-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3998f-117">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3998f-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3998f-118">Spécifie le nom de domaine sur lequel l’émission de la licence a échoué.</span><span class="sxs-lookup"><span data-stu-id="3998f-118">Specifies the domain name to which the license issuance failed.</span></span>

</dd> <dt>

<span data-ttu-id="3998f-119">**FailedIssuanceCount**</span><span class="sxs-lookup"><span data-stu-id="3998f-119">**FailedIssuanceCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3998f-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3998f-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3998f-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3998f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3998f-122">Nombre d’émissions ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="3998f-122">The number of failed issuances.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3998f-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3998f-123">Requirements</span></span>



| <span data-ttu-id="3998f-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3998f-124">Requirement</span></span> | <span data-ttu-id="3998f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="3998f-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3998f-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3998f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3998f-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3998f-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="3998f-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3998f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3998f-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3998f-129">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="3998f-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3998f-130">Namespace</span></span><br/>                | <span data-ttu-id="3998f-131">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="3998f-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="3998f-132">MOF</span><span class="sxs-lookup"><span data-stu-id="3998f-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3998f-133"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3998f-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3998f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3998f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3998f-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3998f-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3998f-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3998f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3998f-137">**FetchReportFailedPerUserSummaryEntries**</span><span class="sxs-lookup"><span data-stu-id="3998f-137">**FetchReportFailedPerUserSummaryEntries**</span></span>](fetchreportfailedperusersummaryentries-win32-tslicensereport.md)
</dt> </dl>

 

