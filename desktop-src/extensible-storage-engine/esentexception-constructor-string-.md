---
description: 'En savoir plus sur : constructeur EsentException (String)'
title: Constructeur EsentException (String) (Microsoft. ISAM. esent)
TOCTitle: EsentException constructor (String)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100720
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22a93625b7becbe083a42fbd6fcc71ad801173ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292150"
---
# <a name="esentexception-constructor-string"></a>Constructeur EsentException (String)

Initialise une nouvelle instance de la classe EsentException avec un message d’erreur spécifié.

**Espace de noms :**  [Microsoft. ISAM. esent](./microsoft.isam.esent-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Protected Sub New ( _
    message As String _
)
'Usage
Dim message As String

Dim instance As New EsentException(message)
```

``` csharp
protected EsentException(
    string message
)
```

#### <a name="parameters"></a>Paramètres

  - message  
    Type : [System. String](/dotnet/api/system.string)  
    
    Message décrivant l'erreur.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[EsentException, classe](./esentexception-class.md)

[Membres EsentException](./esentexception-members.md)

[Surcharge EsentException](./esentexception-constructor.md)

[Espace de noms Microsoft. ISAM. esent](./microsoft.isam.esent-namespace.md)
