---
description: 'En savoir plus sur : structure JET_INDEXID'
title: Structure JET_INDEXID
TOCTitle: JET_INDEXID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_INDEXID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid(v=EXCHG.10)
ms:contentKeyID: 39510071
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13ff0984926fe821d666d18c1907c9bd1bf93b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536865"
---
# <a name="jet_indexid-structure"></a>Structure JET_INDEXID

Contient un ID d’index. Un ID d’index est un indicateur utilisé pour accélérer la sélection de l’index actuel à l’aide de JetSetCurrentIndex. Elle est particulièrement utile lorsqu’il existe un très grand nombre d’index sur une table. L’ID d’index peut être récupéré à l’aide de JetGetIndexInfo ou JetGetTableIndexInfo.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Structure JET_INDEXID _
    Implements IEquatable(Of JET_INDEXID)
'Usage
Dim instance As JET_INDEXID
```

``` csharp
public struct JET_INDEXID : IEquatable<JET_INDEXID>
```

## <a name="remarks"></a>Notes

L’attribut Pack est nécessaire, car la version C++ est définie en tant que tableau d’octets. Si le \# compilateur C insère le remplissage habituel entre le cbStruct uint et le IntPtr, la structure finit par être trop grande.

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres JET_INDEXID](./jet-indexid-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
