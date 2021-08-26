---
description: 'En savoir plus sur : constructeur d’instance (String, String)'
title: Constructeur d’instance (String, String)
TOCTitle: Instance constructor (String, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103267
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d93a5799a646a90688261bdd55bc9dfe929ef6bd074a51e15cabdcee768ffa2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116439"
---
# <a name="instance-constructor-string-string"></a>Constructeur d’instance (String, String)

Initialise une nouvelle instance de la classe d’instance. Le JET_INSTANCE sous-jacent est alloué, mais pas initialisé.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String _
)
'Usage
Dim name As String
Dim displayName As String

Dim instance As New Instance(name, displayName)
```

``` csharp
public Instance(
    string name,
    string displayName
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

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’instance](./instance-class.md)

[Membres d’instance](./instance-members.md)

[Surcharge d’instance](./instance-constructor.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
