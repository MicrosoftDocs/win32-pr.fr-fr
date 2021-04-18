---
description: 'En savoir plus sur : classe EsentStreamingDataNotLoggedException'
title: EsentStreamingDataNotLoggedException, classe
TOCTitle: EsentStreamingDataNotLoggedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStreamingDataNotLoggedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstreamingdatanotloggedexception(v=EXCHG.10)
ms:contentKeyID: 55102942
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStreamingDataNotLoggedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStreamingDataNotLoggedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e46d57bdadd07cafe37dfb59460504cc58b34975
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519984"
---
# <a name="esentstreamingdatanotloggedexception-class"></a>EsentStreamingDataNotLoggedException, classe

Classe de base pour JET_err. Exceptions StreamingDataNotLogged.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentStreamingDataNotLoggedException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentStreamingDataNotLoggedException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentStreamingDataNotLoggedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentStreamingDataNotLoggedException : EsentObsoleteException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentStreamingDataNotLoggedException](./esentstreamingdatanotloggedexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
