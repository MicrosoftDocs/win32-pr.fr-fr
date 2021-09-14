---
description: 'En savoir plus sur : classe EsentCorruptionException'
title: EsentCorruptionException, classe
TOCTitle: EsentCorruptionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCorruptionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a6914c2bf133a1050e3e3800e5c113c6cac1a11f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126914963"
---
# <a name="esentcorruptionexception-class"></a>EsentCorruptionException, classe

Classe de base pour les exceptions d’altération.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentCorruptionException  
            

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentCorruptionException _
    Inherits EsentDataException
'Usage
Dim instance As EsentCorruptionException
```

``` csharp
[SerializableAttribute]
public abstract class EsentCorruptionException : EsentDataException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentCorruptionException](./esentcorruptionexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Types dérivés

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentCorruptionException  
            [Microsoft. ISAM. esent. Interop. EsentBadEmptyPageException](./esentbademptypageexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBadPageLinkException](./esentbadpagelinkexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBadParentPageLinkException](./esentbadparentpagelinkexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCatalogCorruptedException](./esentcatalogcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCheckpointCorruptException](./esentcheckpointcorruptexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCommittedLogFileCorruptException](./esentcommittedlogfilecorruptexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCommittedLogFilesMissingException](./esentcommittedlogfilesmissingexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseBufferDependenciesCorruptedException](./esentdatabasebufferdependenciescorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseCorruptedException](./esentdatabasecorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDbTimeCorruptedException](./esentdbtimecorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDecompressionFailedException](./esentdecompressionfailedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDerivedColumnCorruptionException](./esentderivedcolumncorruptionexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDiskReadVerificationFailureException](./esentdiskreadverificationfailureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFileIOBeyondEOFException](./esentfileiobeyondeofexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFileSystemCorruptionException](./esentfilesystemcorruptionexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexBuildCorruptedException](./esentindexbuildcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidLogSequenceException](./esentinvalidlogsequenceexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogCorruptDuringHardRecoveryException](./esentlogcorruptduringhardrecoveryexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogCorruptDuringHardRestoreException](./esentlogcorruptduringhardrestoreexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogCorruptedException](./esentlogcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogFileCorruptException](./esentlogfilecorruptexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogReadVerifyFailureException](./esentlogreadverifyfailureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogTornWriteDuringHardRecoveryException](./esentlogtornwriteduringhardrecoveryexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogTornWriteDuringHardRestoreException](./esentlogtornwriteduringhardrestoreexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLVCorruptedException](./esentlvcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMissingLogFileException](./esentmissinglogfileexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMissingPreviousLogFileException](./esentmissingpreviouslogfileexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentPageNotInitializedException](./esentpagenotinitializedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentPrimaryIndexCorruptedException](./esentprimaryindexcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentReadLostFlushVerifyFailureException](./esentreadlostflushverifyfailureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentReadPgnoVerifyFailureException](./esentreadpgnoverifyfailureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentReadVerifyFailureException](./esentreadverifyfailureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRecordFormatConversionFailedException](./esentrecordformatconversionfailedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRecoveryVerifyFailureException](./esentrecoveryverifyfailureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRedoAbruptEndedException](./esentredoabruptendedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSecondaryIndexCorruptedException](./esentsecondaryindexcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSPAvailExtCorruptedException](./esentspavailextcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSPOwnExtCorruptedException](./esentspownextcorruptedexception-class.md)