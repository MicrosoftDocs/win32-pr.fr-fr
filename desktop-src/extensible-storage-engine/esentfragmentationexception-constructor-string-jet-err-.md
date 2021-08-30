---
description: 'En savoir plus sur : constructeur EsentFragmentationException (String, JET_err)'
title: Constructeur EsentFragmentationException (String, JET_err)
TOCTitle: EsentFragmentationException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFragmentationException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101778
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3343957dd19fc67d13fd46d5e64281c7d056993493d002691d08daa0f000664
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065299"
---
# <a name="esentfragmentationexception-constructor-string-jet_err"></a>Constructeur EsentFragmentationException (String, JET_err)

Initialise une nouvelle instance de la classe EsentFragmentationException.

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

Dim instance As New EsentFragmentationException(description, _
    err)
```

``` csharp
protected EsentFragmentationException(
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

[EsentFragmentationException, classe](./esentfragmentationexception-class.md)

[Membres EsentFragmentationException](./esentfragmentationexception-members.md)

[Surcharge EsentFragmentationException](./esentfragmentationexception-constructor.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
