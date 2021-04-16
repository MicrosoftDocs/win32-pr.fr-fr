---
description: 'En savoir plus sur : classe EsentDatabaseAlreadyUpgradedException'
title: EsentDatabaseAlreadyUpgradedException, classe
TOCTitle: EsentDatabaseAlreadyUpgradedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasealreadyupgradedexception(v=EXCHG.10)
ms:contentKeyID: 55101322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27ad5a37676ef0b8e4a450619c19a45f3bdee1b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530363"
---
# <a name="esentdatabasealreadyupgradedexception-class"></a>EsentDatabaseAlreadyUpgradedException, classe

Classe de base pour JET_err. Exceptions DatabaseAlreadyUpgraded.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentStateException](./esentstateexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentDatabaseAlreadyUpgradedException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseAlreadyUpgradedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseAlreadyUpgradedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseAlreadyUpgradedException : EsentStateException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentDatabaseAlreadyUpgradedException](./esentdatabasealreadyupgradedexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
