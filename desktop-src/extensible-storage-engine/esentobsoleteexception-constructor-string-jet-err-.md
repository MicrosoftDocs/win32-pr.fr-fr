---
description: 'En savoir plus sur : constructeur EsentObsoleteException (String, JET_err)'
title: Constructeur EsentObsoleteException (String, JET_err)
TOCTitle: EsentObsoleteException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentObsoleteException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102363
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 435a3db75cb09a47bccc311733b90fae30563c86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126917688"
---
# <a name="esentobsoleteexception-constructor-string-jet_err"></a>Constructeur EsentObsoleteException (String, JET_err)

Initialise une nouvelle instance de la classe EsentObsoleteException.

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

Dim instance As New EsentObsoleteException(description, _
    err)
```

``` csharp
protected EsentObsoleteException(
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

[EsentObsoleteException, classe](./esentobsoleteexception-class.md)

[Membres EsentObsoleteException](./esentobsoleteexception-members.md)

[Surcharge EsentObsoleteException](./esentobsoleteexception-constructor.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
