---
description: 'En savoir plus sur : classe EsentQuotaException'
title: Classe EsentQuotaException
TOCTitle: EsentQuotaException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentQuotaException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102495
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6350dfa9cbdddcf935b4f87fab964d40c1fc65765a254219c542d29b676fed36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782269"
---
# <a name="esentquotaexception-class"></a>Classe EsentQuotaException

Classe de base pour les exceptions de quota.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentResourceException](./esentresourceexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentQuotaException  
              [Microsoft. ISAM. esent. Interop. EsentOutOfDatabaseSpaceException](./esentoutofdatabasespaceexception-class.md)  
              [Microsoft. ISAM. esent. Interop. EsentTooManyInstancesException](./esenttoomanyinstancesexception-class.md)  
              [Microsoft. ISAM. esent. Interop. EsentTooManyOpenTablesException](./esenttoomanyopentablesexception-class.md)  
              [Microsoft. ISAM. esent. Interop. EsentVersionStoreOutOfMemoryException](./esentversionstoreoutofmemoryexception-class.md)  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentQuotaException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentQuotaException
```

``` csharp
[SerializableAttribute]
public abstract class EsentQuotaException : EsentResourceException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentQuotaException](./esentquotaexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
