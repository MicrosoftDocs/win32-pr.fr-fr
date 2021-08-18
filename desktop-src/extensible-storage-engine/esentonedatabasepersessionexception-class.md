---
description: 'En savoir plus sur : classe EsentOneDatabasePerSessionException'
title: EsentOneDatabasePerSessionException, classe
TOCTitle: EsentOneDatabasePerSessionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOneDatabasePerSessionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentonedatabasepersessionexception(v=EXCHG.10)
ms:contentKeyID: 55102432
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOneDatabasePerSessionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOneDatabasePerSessionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7473add15117f7912abbb66aee5cfc407c07cba45d8281a2b74aea02108abeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782509"
---
# <a name="esentonedatabasepersessionexception-class"></a>EsentOneDatabasePerSessionException, classe

Classe de base pour JET_err. Exceptions OneDatabasePerSession.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentOneDatabasePerSessionException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOneDatabasePerSessionException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentOneDatabasePerSessionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOneDatabasePerSessionException : EsentUsageException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentOneDatabasePerSessionException](./esentonedatabasepersessionexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
