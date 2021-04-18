---
title: Structure RECORD_HEADER
description: En-tête d’enregistrement utilisé par \_ l' \_ entrée du journal des modifications et les \_ structures d’en-tête du journal des modifications \_ .
ms.assetid: f8d2147c-ad13-4be4-94d7-ae0ca26511da
keywords:
- Restauration du système de la structure RECORD_HEADER
- PRECORD_HEADER de la restauration du système du pointeur de structure
topic_type:
- apiref
api_name:
- RECORD_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fd304d2f1b6a5ece08d3d3535aacd7a1abcf614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466358"
---
# <a name="record_header-structure"></a><span data-ttu-id="fc8c8-105">\_Structure d’en-tête d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="fc8c8-105">RECORD\_HEADER structure</span></span>

<span data-ttu-id="fc8c8-106">\[Ces informations s’appliquent uniquement à Windows XP avec Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="fc8c8-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="fc8c8-107">En-tête d’enregistrement utilisé par l' [**\_ \_ entrée du journal des modifications**](change-log-entry.md) et les structures d' [**\_ \_ en-tête du journal des modifications**](change-log-header.md) .</span><span class="sxs-lookup"><span data-stu-id="fc8c8-107">The record header used by the [**CHANGE\_LOG\_ENTRY**](change-log-entry.md) and [**CHANGE\_LOG\_HEADER**](change-log-header.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc8c8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc8c8-108">Syntax</span></span>


```C++
typedef struct _RECORD_HEADER {
  DWORD dwRecordSize;
  DWORD dwRecordType;
} RECORD_HEADER, *PRECORD_HEADER;
```



## <a name="members"></a><span data-ttu-id="fc8c8-109">Membres</span><span class="sxs-lookup"><span data-stu-id="fc8c8-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="fc8c8-110">**dwRecordSize**</span><span class="sxs-lookup"><span data-stu-id="fc8c8-110">**dwRecordSize**</span></span>
</dt> <dd>

<span data-ttu-id="fc8c8-111">Taille totale de l’enregistrement, y compris l’en-tête, en octets.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-111">The total size of the record, including the header, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="fc8c8-112">**dwRecordType**</span><span class="sxs-lookup"><span data-stu-id="fc8c8-112">**dwRecordType**</span></span>
</dt> <dd>

<span data-ttu-id="fc8c8-113">Type d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-113">The record type.</span></span> <span data-ttu-id="fc8c8-114">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-114">This member may be one of the following values.</span></span>



| <span data-ttu-id="fc8c8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc8c8-115">Value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="fc8c8-116">Signification</span><span class="sxs-lookup"><span data-stu-id="fc8c8-116">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RecordTypeLogHeader"></span><span id="recordtypelogheader"></span><span id="RECORDTYPELOGHEADER"></span><dl> <span data-ttu-id="fc8c8-117"><dt>**RecordTypeLogHeader**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fc8c8-117"><dt>**RecordTypeLogHeader**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="fc8c8-118">L’enregistrement est l’en-tête du journal des modifications.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-118">The record is the header for the change log.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="RecordTypeLogEntry"></span><span id="recordtypelogentry"></span><span id="RECORDTYPELOGENTRY"></span><dl> <span data-ttu-id="fc8c8-119"><dt>**RecordTypeLogEntry**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fc8c8-119"><dt>**RecordTypeLogEntry**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="fc8c8-120">L’enregistrement est l’en-tête d’une entrée de journal des modifications.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-120">The record is the header for a change log entry.</span></span><br/>                                                                                                                                                                                                                        |
| <span id="RecordTypeVolumePath"></span><span id="recordtypevolumepath"></span><span id="RECORDTYPEVOLUMEPATH"></span><dl> <span data-ttu-id="fc8c8-121"><dt>**RecordTypeVolumePath**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fc8c8-121"><dt>**RecordTypeVolumePath**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="fc8c8-122">Les données sont le chemin d’accès du volume pour l’entrée du journal des modifications.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-122">The data is the volume path for the change log entry.</span></span><br/>                                                                                                                                                                                                                   |
| <span id="RecordTypeFirstPath"></span><span id="recordtypefirstpath"></span><span id="RECORDTYPEFIRSTPATH"></span><dl> <span data-ttu-id="fc8c8-123"><dt>**RecordTypeFirstPath**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fc8c8-123"><dt>**RecordTypeFirstPath**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="fc8c8-124">Les données sont le chemin de fichier de l’entrée du journal des modifications.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-124">The data is the file path for the change log entry.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="RecordTypeSecondPath"></span><span id="recordtypesecondpath"></span><span id="RECORDTYPESECONDPATH"></span><dl> <span data-ttu-id="fc8c8-125"><dt>**RecordTypeSecondPath**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fc8c8-125"><dt>**RecordTypeSecondPath**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="fc8c8-126">Les données sont utilisées lors de l’attribution d’un nouveau nom aux entrées du journal des modifications. ce chemin d’accès est l’emplacement où le fichier renommé est stocké.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-126">The data is used when renaming change log entries; this path is where the renamed file is stored.</span></span><br/>                                                                                                                                                                       |
| <span id="RecordTypeTempPath"></span><span id="recordtypetemppath"></span><span id="RECORDTYPETEMPPATH"></span><dl> <span data-ttu-id="fc8c8-127"><dt>**RecordTypeTempPath**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="fc8c8-127"><dt>**RecordTypeTempPath**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="fc8c8-128">Les données sont le nom du fichier de sauvegarde utilisé pour restaurer l’entrée du journal des modifications.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-128">The data is the name of the backup file used to restore the change log entry.</span></span> <span data-ttu-id="fc8c8-129">Les fichiers de sauvegarde se trouvent dans le dossier RP *n* .</span><span class="sxs-lookup"><span data-stu-id="fc8c8-129">The backup files are located in the RP *n* folder.</span></span> <span data-ttu-id="fc8c8-130">Le nom de fichier a le format suivant : a *xxxxxxx*. *ext*, où *xxxxxxx* est un nombre à sept chiffres et *ext* est l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-130">The file name has the following format: A *xxxxxxx*.*ext*, where *xxxxxxx* is a seven-digit number and *ext* is the file name extension.</span></span><br/> |
| <span id="RecordTypeAclInline"></span><span id="recordtypeaclinline"></span><span id="RECORDTYPEACLINLINE"></span><dl> <span data-ttu-id="fc8c8-131"><dt>**RecordTypeAclInline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="fc8c8-131"><dt>**RecordTypeAclInline**</dt> <dt>6</dt></span></span> </dl>     | <span data-ttu-id="fc8c8-132">Les données sont une liste de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-132">The data is an ACL.</span></span> <span data-ttu-id="fc8c8-133">Le format de données est une structure de [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="fc8c8-133">The data format is a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure.</span></span> <br/> <span data-ttu-id="fc8c8-134">Cette valeur ne peut pas être supérieure à 8 192 octets.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-134">This value cannot be larger than 8,192 bytes.</span></span> <span data-ttu-id="fc8c8-135">Pour spécifier une valeur supérieure à 8 192 octets, utilisez le membre **RecordTypeAclFile** .</span><span class="sxs-lookup"><span data-stu-id="fc8c8-135">To specify a value larger than 8,192 bytes, use the **RecordTypeAclFile** member.</span></span><br/>                |
| <span id="RecordTypeAclFile"></span><span id="recordtypeaclfile"></span><span id="RECORDTYPEACLFILE"></span><dl> <span data-ttu-id="fc8c8-136"><dt>**RecordTypeAclFile**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="fc8c8-136"><dt>**RecordTypeAclFile**</dt> <dt>7</dt></span></span> </dl>             | <span data-ttu-id="fc8c8-137">Les données sont le nom du fichier ACL utilisé pour stocker la liste de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-137">The data is the name of the ACL file used to store the ACL.</span></span> <span data-ttu-id="fc8c8-138">Les fichiers ACL se trouvent dans le dossier RP *n* .</span><span class="sxs-lookup"><span data-stu-id="fc8c8-138">The ACL files are located in the RP *n* folder.</span></span> <span data-ttu-id="fc8c8-139">Le nom de fichier est au format suivant : S *xxxxxxx*. ACL, où *xxxxxxx* est un nombre à sept chiffres.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-139">The file name has the following format: S *xxxxxxx*.acl, where *xxxxxxx* is a seven-digit number.</span></span><br/>                                                             |
| <span id="RecordTypeDebugInfo"></span><span id="recordtypedebuginfo"></span><span id="RECORDTYPEDEBUGINFO"></span><dl> <span data-ttu-id="fc8c8-140"><dt>**RecordTypeDebugInfo**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="fc8c8-140"><dt>**RecordTypeDebugInfo**</dt> <dt>8</dt></span></span> </dl>     | <span data-ttu-id="fc8c8-141">Les données sont des informations de débogage pour l’entrée du journal des modifications.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-141">The data is debug information for the change log entry.</span></span> <span data-ttu-id="fc8c8-142">Le format de données est une structure d' **\_ \_ \_ informations de débogage du journal SR** .</span><span class="sxs-lookup"><span data-stu-id="fc8c8-142">The data format is a **SR\_LOG\_DEBUG\_INFO** structure.</span></span> <span data-ttu-id="fc8c8-143">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-143">For more information, see Remarks.</span></span><br/>                                                                                                                     |
| <span id="RecordTypeShortName"></span><span id="recordtypeshortname"></span><span id="RECORDTYPESHORTNAME"></span><dl> <span data-ttu-id="fc8c8-144"><dt>**RecordTypeShortName**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="fc8c8-144"><dt>**RecordTypeShortName**</dt> <dt>9</dt></span></span> </dl>     | <span data-ttu-id="fc8c8-145">Les données sont le nom abrégé du fichier de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-145">The data is the short name of the backup file.</span></span><br/>                                                                                                                                                                                                                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc8c8-146">Notes</span><span class="sxs-lookup"><span data-stu-id="fc8c8-146">Remarks</span></span>

<span data-ttu-id="fc8c8-147">La structure des **\_ \_ \_ informations de débogage du journal SR** est définie comme suit.</span><span class="sxs-lookup"><span data-stu-id="fc8c8-147">The **SR\_LOG\_DEBUG\_INFO** structure is defined as follows.</span></span>

``` syntax
typedef struct _SR_LOG_DEBUG_INFO {
    RECORD_HEADER Header;         // log entry header
    HANDLE ThreadId;              // thread identifier
    HANDLE ProcessId;             // process identifier
    ULARGER_INTEGER TimeStamp;    // event time stamp
    CHAR ProcesName[13];          // process name
} SR_LOG_DEBUG_INFO, *PSR_LOG_DEBUG_INFO;
```

## <a name="requirements"></a><span data-ttu-id="fc8c8-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc8c8-148">Requirements</span></span>



| <span data-ttu-id="fc8c8-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc8c8-149">Requirement</span></span> | <span data-ttu-id="fc8c8-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc8c8-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc8c8-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc8c8-151">Minimum supported client</span></span><br/> | <span data-ttu-id="fc8c8-152">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc8c8-152">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fc8c8-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc8c8-153">Minimum supported server</span></span><br/> | <span data-ttu-id="fc8c8-154">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc8c8-154">None supported</span></span><br/>                            |
| <span data-ttu-id="fc8c8-155">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="fc8c8-155">End of client support</span></span><br/>    | <span data-ttu-id="fc8c8-156">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="fc8c8-156">Windows XP with SP2</span></span><br/>                       |



 

