---
description: 'En savoir plus sur : JET_THREADSTATS. Ajouter une méthode'
title: JET_THREADSTATS. Add, méthode (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'Add method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.add(v=EXCHG.10)
ms:contentKeyID: 39514259
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2a824249fde43de92c65d64d02fbab4097b7dc34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513969"
---
# <a name="jet_threadstatsadd-method"></a>JET_THREADSTATS. Ajouter une méthode

Ajoutez les statistiques dans deux structures JET_THREADSTATS.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Function Add ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Add(t1, t2)
```

``` csharp
public static JET_THREADSTATS Add(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a>Paramètres

  - t1  
    Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    Premier JET_THREADSTATS.

<!-- end list -->

  - H2  
    Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    Deuxième JET_THREADSTATS.

#### <a name="return-value"></a>Valeur retournée

Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
JET_THREADSTATS contenant le résultat de l’ajout des statistiques dans T1 et T2.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_THREADSTATS](./jet-threadstats-structure2.md)

[Membres JET_THREADSTATS](./jet-threadstats-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
