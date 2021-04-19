---
description: 'En savoir plus sur : constructeur EsentOperationException (String, JET_err)'
title: Constructeur EsentOperationException (String, JET_err)
TOCTitle: EsentOperationException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentOperationException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102376
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb25ea404e4581b369f9d81e772ba4b2e95f7fc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527429"
---
# <a name="esentoperationexception-constructor-string-jet_err"></a>Constructeur EsentOperationException (String, JET_err)

Initialise une nouvelle instance de la classe EsentOperationException.

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

Dim instance As New EsentOperationException(description, _
    err)
```

``` csharp
protected EsentOperationException(
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

[EsentOperationException, classe](./esentoperationexception-class.md)

[Membres EsentOperationException](./esentoperationexception-members.md)

[Surcharge EsentOperationException](./esentoperationexception-constructor.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
