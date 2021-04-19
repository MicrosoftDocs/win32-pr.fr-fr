---
description: 'En savoir plus sur : classe EsentOperationException'
title: EsentOperationException, classe
TOCTitle: EsentOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102414
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 314ae88a674f6bd59b0111d40ff3ca5a9eab8a2f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106539368"
---
# <a name="esentoperationexception-class"></a>EsentOperationException, classe

Classe de base pour les exceptions d’opération.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        Microsoft. ISAM. esent. Interop. EsentOperationException  
          

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentOperationException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentOperationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentOperationException : EsentErrorException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentOperationException](./esentoperationexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Types dérivés

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        Microsoft. ISAM. esent. Interop. EsentOperationException  
          [Microsoft. ISAM. esent. Interop. EsentBackupAbortByServerException](./esentbackupabortbyserverexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentCheckpointDepthTooDeepException](./esentcheckpointdepthtoodeepexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentClientRequestToStopJetServiceException](./esentclientrequesttostopjetserviceexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentFatalException](./esentfatalexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentInitInProgressException](./esentinitinprogressexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentInternalErrorException](./esentinternalerrorexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentIOException](./esentioexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentNTSystemCallFailedException](./esentntsystemcallfailedexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentOSSnapshotTimeOutException](./esentossnapshottimeoutexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentRecordNotDeletedException](./esentrecordnotdeletedexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentResourceException](./esentresourceexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentTermInProgressException](./esentterminprogressexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUnicodeLanguageValidationFailureException](./esentunicodelanguagevalidationfailureexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUnicodeTranslationFailException](./esentunicodetranslationfailexception-class.md)