---
description: 'En savoir plus sur : constructeur EsentUsageException (String, JET_err)'
title: Constructeur EsentUsageException (String, JET_err)
TOCTitle: EsentUsageException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentUsageException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103223
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e446d01cd2df11e89c6bf2b4803b810fa1255e8553ae11eddc81faf190e8131c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891372"
---
# <a name="esentusageexception-constructor-string-jet_err"></a>Constructeur EsentUsageException (String, JET_err)

Initialise une nouvelle instance de la classe EsentUsageException.

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

Dim instance As New EsentUsageException(description, _
    err)
```

``` csharp
protected EsentUsageException(
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

[EsentUsageException, classe](./esentusageexception-class.md)

[Membres EsentUsageException](./esentusageexception-members.md)

[Surcharge EsentUsageException](./esentusageexception-constructor.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
