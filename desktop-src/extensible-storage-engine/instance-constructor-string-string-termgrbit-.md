---
description: 'En savoir plus sur : constructeur d’instance (String, String, TermGrbit)'
title: Constructeur d’instance (String, String, TermGrbit)
TOCTitle: Instance constructor (String, String, TermGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103289
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9cf90f9678db1074594c7772eb67d895a8a5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753301"
---
# <a name="instance-constructor-string-string-termgrbit"></a>Constructeur d’instance (String, String, TermGrbit)

Initialise une nouvelle instance de la classe d’instance. Le JET_INSTANCE sous-jacent est alloué, mais pas initialisé.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String, _
    termGrbit As TermGrbit _
)
'Usage
Dim name As String
Dim displayName As String
Dim termGrbit As TermGrbit

Dim instance As New Instance(name, displayName, _
    termGrbit)
```

``` csharp
public Instance(
    string name,
    string displayName,
    TermGrbit termGrbit
)
```

#### <a name="parameters"></a>Paramètres

  - name  
    Type : [System. String](/dotnet/api/system.string)  
    
    Nom de l'instance. Cette chaîne doit être unique au sein d’un processus donné hébergeant le moteur de base de données.

<!-- end list -->

  - displayName  
    Type : [System. String](/dotnet/api/system.string)  
    
    Nom complet de l’instance. Il sera utilisé dans les entrées du journal des événements.

<!-- end list -->

  - termGrbit  
    Type : [Microsoft. ISAM. esent. Interop. TermGrbit](./termgrbit-enumeration.md)  
    
    TermGrbit à utiliser au moment de la JetTerm.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’instance](./instance-class.md)

[Membres d’instance](./instance-members.md)

[Surcharge d’instance](./instance-constructor.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
