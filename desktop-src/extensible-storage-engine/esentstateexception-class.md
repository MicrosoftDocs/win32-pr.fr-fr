---
description: 'En savoir plus sur : classe EsentStateException'
title: EsentStateException, classe
TOCTitle: EsentStateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102986
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5815c3b308874f69eab9dcc7b3803ee24f6831b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104211185"
---
# <a name="esentstateexception-class"></a><span data-ttu-id="1ad3a-103">EsentStateException, classe</span><span class="sxs-lookup"><span data-stu-id="1ad3a-103">EsentStateException class</span></span>

<span data-ttu-id="1ad3a-104">Classe de base pour les exceptions d’État.</span><span class="sxs-lookup"><span data-stu-id="1ad3a-104">Base class for State exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1ad3a-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="1ad3a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1ad3a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1ad3a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1ad3a-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="1ad3a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1ad3a-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1ad3a-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1ad3a-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="1ad3a-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>  
            

<span data-ttu-id="1ad3a-112">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1ad3a-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1ad3a-113">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1ad3a-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1ad3a-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ad3a-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentStateException _
    Inherits EsentApiException
'Usage
Dim instance As EsentStateException
```

``` csharp
[SerializableAttribute]
public abstract class EsentStateException : EsentApiException
```

## <a name="thread-safety"></a><span data-ttu-id="1ad3a-115">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="1ad3a-115">Thread safety</span></span>

<span data-ttu-id="1ad3a-116">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1ad3a-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1ad3a-117">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1ad3a-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ad3a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ad3a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ad3a-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="1ad3a-119">Reference</span></span>

[<span data-ttu-id="1ad3a-120">Membres EsentStateException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-120">EsentStateException members</span></span>](./esentstateexception-members.md)

[<span data-ttu-id="1ad3a-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1ad3a-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="1ad3a-122">Types dérivés</span><span class="sxs-lookup"><span data-stu-id="1ad3a-122">Derived types</span></span>

[<span data-ttu-id="1ad3a-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="1ad3a-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1ad3a-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="1ad3a-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1ad3a-125">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1ad3a-126">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1ad3a-127">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-127">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="1ad3a-128">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-128">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>  
            [<span data-ttu-id="1ad3a-129">Microsoft. ISAM. esent. Interop. EsentBackupInProgressException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-129">Microsoft.Isam.Esent.Interop.EsentBackupInProgressException</span></span>](./esentbackupinprogressexception-class.md)  
            [<span data-ttu-id="1ad3a-130">Microsoft. ISAM. esent. Interop. EsentBackupNotAllowedYetException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-130">Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException</span></span>](./esentbackupnotallowedyetexception-class.md)  
            [<span data-ttu-id="1ad3a-131">Microsoft. ISAM. esent. Interop. EsentBadItagSequenceException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-131">Microsoft.Isam.Esent.Interop.EsentBadItagSequenceException</span></span>](./esentbaditagsequenceexception-class.md)  
            [<span data-ttu-id="1ad3a-132">Microsoft. ISAM. esent. Interop. EsentBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-132">Microsoft.Isam.Esent.Interop.EsentBufferTooSmallException</span></span>](./esentbuffertoosmallexception-class.md)  
            [<span data-ttu-id="1ad3a-133">Microsoft. ISAM. esent. Interop. EsentCallbackFailedException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-133">Microsoft.Isam.Esent.Interop.EsentCallbackFailedException</span></span>](./esentcallbackfailedexception-class.md)  
            [<span data-ttu-id="1ad3a-134">Microsoft. ISAM. esent. Interop. EsentDatabaseAlreadyUpgradedException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-134">Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException</span></span>](./esentdatabasealreadyupgradedexception-class.md)  
            [<span data-ttu-id="1ad3a-135">Microsoft. ISAM. esent. Interop. EsentDatabaseFailedIncrementalReseedException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-135">Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException</span></span>](./esentdatabasefailedincrementalreseedexception-class.md)  
            [<span data-ttu-id="1ad3a-136">Microsoft. ISAM. esent. Interop. EsentDatabaseIncompleteUpgradeException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-136">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException</span></span>](./esentdatabaseincompleteupgradeexception-class.md)  
            [<span data-ttu-id="1ad3a-137">Microsoft. ISAM. esent. Interop. EsentDatabaseLeakInSpaceException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-137">Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException</span></span>](./esentdatabaseleakinspaceexception-class.md)  
            [<span data-ttu-id="1ad3a-138">Microsoft. ISAM. esent. Interop. EsentDirtyShutdownException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-138">Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException</span></span>](./esentdirtyshutdownexception-class.md)  
            [<span data-ttu-id="1ad3a-139">Microsoft. ISAM. esent. Interop. EsentFileNotFoundException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-139">Microsoft.Isam.Esent.Interop.EsentFileNotFoundException</span></span>](./esentfilenotfoundexception-class.md)  
            [<span data-ttu-id="1ad3a-140">Microsoft. ISAM. esent. Interop. EsentIndexInUseException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-140">Microsoft.Isam.Esent.Interop.EsentIndexInUseException</span></span>](./esentindexinuseexception-class.md)  
            [<span data-ttu-id="1ad3a-141">Microsoft. ISAM. esent. Interop. EsentIndexNotFoundException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-141">Microsoft.Isam.Esent.Interop.EsentIndexNotFoundException</span></span>](./esentindexnotfoundexception-class.md)  
            [<span data-ttu-id="1ad3a-142">Microsoft. ISAM. esent. Interop. EsentInvalidBufferSizeException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-142">Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException</span></span>](./esentinvalidbuffersizeexception-class.md)  
            [<span data-ttu-id="1ad3a-143">Microsoft. ISAM. esent. Interop. EsentInvalidLogDataSequenceException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-143">Microsoft.Isam.Esent.Interop.EsentInvalidLogDataSequenceException</span></span>](./esentinvalidlogdatasequenceexception-class.md)  
            [<span data-ttu-id="1ad3a-144">Microsoft. ISAM. esent. Interop. EsentKeyDuplicateException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-144">Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException</span></span>](./esentkeyduplicateexception-class.md)  
            [<span data-ttu-id="1ad3a-145">Microsoft. ISAM. esent. Interop. EsentKeyTruncatedException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-145">Microsoft.Isam.Esent.Interop.EsentKeyTruncatedException</span></span>](./esentkeytruncatedexception-class.md)  
            [<span data-ttu-id="1ad3a-146">Microsoft. ISAM. esent. Interop. EsentLogFileSizeMismatchDatabasesConsistentException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-146">Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchDatabasesConsistentException</span></span>](./esentlogfilesizemismatchdatabasesconsistentexception-class.md)  
            [<span data-ttu-id="1ad3a-147">Microsoft. ISAM. esent. Interop. EsentLogSectorSizeMismatchDatabasesConsistentException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-147">Microsoft.Isam.Esent.Interop.EsentLogSectorSizeMismatchDatabasesConsistentException</span></span>](./esentlogsectorsizemismatchdatabasesconsistentexception-class.md)  
            [<span data-ttu-id="1ad3a-148">Microsoft. ISAM. esent. Interop. EsentLSNotSetException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-148">Microsoft.Isam.Esent.Interop.EsentLSNotSetException</span></span>](./esentlsnotsetexception-class.md)  
            [<span data-ttu-id="1ad3a-149">Microsoft. ISAM. esent. Interop. EsentMissingFullBackupException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-149">Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException</span></span>](./esentmissingfullbackupexception-class.md)  
            [<span data-ttu-id="1ad3a-150">Microsoft. ISAM. esent. Interop. EsentMultiValuedDuplicateAfterTruncationException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-150">Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException</span></span>](./esentmultivaluedduplicateaftertruncationexception-class.md)  
            [<span data-ttu-id="1ad3a-151">Microsoft. ISAM. esent. Interop. EsentMultiValuedDuplicateException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-151">Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException</span></span>](./esentmultivaluedduplicateexception-class.md)  
            [<span data-ttu-id="1ad3a-152">Microsoft. ISAM. esent. Interop. EsentNoAttachmentsFailedIncrementalReseedException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-152">Microsoft.Isam.Esent.Interop.EsentNoAttachmentsFailedIncrementalReseedException</span></span>](./esentnoattachmentsfailedincrementalreseedexception-class.md)  
            [<span data-ttu-id="1ad3a-153">Microsoft. ISAM. esent. Interop. EsentNoBackupException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-153">Microsoft.Isam.Esent.Interop.EsentNoBackupException</span></span>](./esentnobackupexception-class.md)  
            [<span data-ttu-id="1ad3a-154">Microsoft. ISAM. esent. Interop. EsentNoCurrentRecordException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-154">Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException</span></span>](./esentnocurrentrecordexception-class.md)  
            [<span data-ttu-id="1ad3a-155">Microsoft. ISAM. esent. Interop. EsentObjectNotFoundException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-155">Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException</span></span>](./esentobjectnotfoundexception-class.md)  
            [<span data-ttu-id="1ad3a-156">Microsoft. ISAM. esent. Interop. EsentOSSnapshotNotAllowedException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-156">Microsoft.Isam.Esent.Interop.EsentOSSnapshotNotAllowedException</span></span>](./esentossnapshotnotallowedexception-class.md)  
            [<span data-ttu-id="1ad3a-157">Microsoft. ISAM. esent. Interop. EsentRecordDeletedException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-157">Microsoft.Isam.Esent.Interop.EsentRecordDeletedException</span></span>](./esentrecorddeletedexception-class.md)  
            [<span data-ttu-id="1ad3a-158">Microsoft. ISAM. esent. Interop. EsentRecordNotFoundException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-158">Microsoft.Isam.Esent.Interop.EsentRecordNotFoundException</span></span>](./esentrecordnotfoundexception-class.md)  
            [<span data-ttu-id="1ad3a-159">Microsoft. ISAM. esent. Interop. EsentRecordTooBigException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-159">Microsoft.Isam.Esent.Interop.EsentRecordTooBigException</span></span>](./esentrecordtoobigexception-class.md)  
            [<span data-ttu-id="1ad3a-160">Microsoft. ISAM. esent. Interop. EsentRecordTooBigForBackwardCompatibilityException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-160">Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException</span></span>](./esentrecordtoobigforbackwardcompatibilityexception-class.md)  
            [<span data-ttu-id="1ad3a-161">Microsoft. ISAM. esent. Interop. EsentRecoveredWithErrorsException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-161">Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException</span></span>](./esentrecoveredwitherrorsexception-class.md)  
            [<span data-ttu-id="1ad3a-162">Microsoft. ISAM. esent. Interop. EsentRecoveredWithoutUndoDatabasesConsistentException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-162">Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException</span></span>](./esentrecoveredwithoutundodatabasesconsistentexception-class.md)  
            [<span data-ttu-id="1ad3a-163">Microsoft. ISAM. esent. Interop. EsentRecoveredWithoutUndoException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-163">Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoException</span></span>](./esentrecoveredwithoutundoexception-class.md)  
            [<span data-ttu-id="1ad3a-164">Microsoft. ISAM. esent. Interop. EsentRestoreInProgressException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-164">Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException</span></span>](./esentrestoreinprogressexception-class.md)  
            [<span data-ttu-id="1ad3a-165">Microsoft. ISAM. esent. Interop. EsentSeparatedLongValueException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-165">Microsoft.Isam.Esent.Interop.EsentSeparatedLongValueException</span></span>](./esentseparatedlongvalueexception-class.md)  
            [<span data-ttu-id="1ad3a-166">Microsoft. ISAM. esent. Interop. EsentSurrogateBackupInProgressException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-166">Microsoft.Isam.Esent.Interop.EsentSurrogateBackupInProgressException</span></span>](./esentsurrogatebackupinprogressexception-class.md)  
            [<span data-ttu-id="1ad3a-167">Microsoft. ISAM. esent. Interop. EsentTableDuplicateException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-167">Microsoft.Isam.Esent.Interop.EsentTableDuplicateException</span></span>](./esenttableduplicateexception-class.md)  
            [<span data-ttu-id="1ad3a-168">Microsoft. ISAM. esent. Interop. EsentTableInUseException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-168">Microsoft.Isam.Esent.Interop.EsentTableInUseException</span></span>](./esenttableinuseexception-class.md)  
            [<span data-ttu-id="1ad3a-169">Microsoft. ISAM. esent. Interop. EsentTestInjectionNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-169">Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException</span></span>](./esenttestinjectionnotsupportedexception-class.md)  
            [<span data-ttu-id="1ad3a-170">Microsoft. ISAM. esent. Interop. EsentWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-170">Microsoft.Isam.Esent.Interop.EsentWriteConflictException</span></span>](./esentwriteconflictexception-class.md)  
            [<span data-ttu-id="1ad3a-171">Microsoft. ISAM. esent. Interop. EsentWriteConflictPrimaryIndexException</span><span class="sxs-lookup"><span data-stu-id="1ad3a-171">Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException</span></span>](./esentwriteconflictprimaryindexexception-class.md)