---
description: 'En savoir plus sur : propriété JET_INDEXCREATE. cbKeyMost'
title: JET_INDEXCREATE. cbKeyMost, propriété
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55103646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_cbKeyMost
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 321704f88da59af33f4dab99d7d681fbcbd96e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866846"
---
# <a name="jet_indexcreatecbkeymost-property"></a>JET_INDEXCREATE. cbKeyMost, propriété

Obtient ou définit la taille maximale autorisée, en octets, pour les clés dans l’index. La taille de clé maximale prise en charge minimale est JET_cbKeyMostMin (255) qui est la taille de clé maximale héritée. La taille de clé maximale dépend de la taille de page de la base de données [DatabasePageSize](./jet-param-enumeration.md). La [taille de clé](./systemparameters.keymost-property.md)maximale peut être récupérée avec. Ce paramètre est ignoré sur Windows XP et Windows Server 2003. Contrairement à l’API non managée, **IndexKeyMost ()** (JET_bitIndexKeyMost) n’est pas nécessaire, elle est ajoutée automatiquement.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_INDEXCREATE](./jet-indexcreate-class.md)

[Membres JET_INDEXCREATE](./jet-indexcreate-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
