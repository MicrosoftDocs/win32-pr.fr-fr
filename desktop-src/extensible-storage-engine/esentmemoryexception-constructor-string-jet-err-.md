---
description: 'En savoir plus sur : constructeur EsentMemoryException (String, JET_err)'
title: Constructeur EsentMemoryException (String, JET_err)
TOCTitle: EsentMemoryException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentMemoryException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102199
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60cdb6fda03695a4afb41d82e83aaeeb9415f421
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007884"
---
# <a name="esentmemoryexception-constructor-string-jet_err"></a>Constructeur EsentMemoryException (String, JET_err)

Initialise une nouvelle instance de la classe EsentMemoryException.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentMemoryException(description, _
    err)
```

``` csharp
protected EsentMemoryException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a>Paramètres

  - description  
    Type : [System. String](/dotnet/api/system.string)  
    
    Description de l'erreur.

<!-- end list -->

  - Raise  
    Type : [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)  
    
    Code d’erreur de l’exception.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe EsentMemoryException](./esentmemoryexception-class.md)

[Membres EsentMemoryException](./esentmemoryexception-members.md)

[Surcharge EsentMemoryException](./esentmemoryexception-constructor.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
