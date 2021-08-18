---
description: 'En savoir plus sur : champ Server2003Grbits. EnumerateIgnoreUserDefinedDefault'
title: Champ Server2003Grbits. EnumerateIgnoreUserDefinedDefault (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: EnumerateIgnoreUserDefinedDefault field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.enumerateignoreuserdefineddefault(v=EXCHG.10)
ms:contentKeyID: 55104099
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b3c110e1aeb54d38805b5ee6ad116ed8fcbbdc7274d0548b582fd88b0e8ac1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978559"
---
# <a name="server2003grbitsenumerateignoreuserdefineddefault-field"></a>Champ Server2003Grbits. EnumerateIgnoreUserDefinedDefault

Si une colonne donnée n’est pas présente dans l’enregistrement et qu’elle a une valeur par défaut définie par l’utilisateur, aucune valeur de colonne n’est retournée. Cette option empêchera le rappel qui calcule la valeur par défaut définie par l’utilisateur pour la colonne à être appelée lors de l’énumération des valeurs de cette colonne.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Const EnumerateIgnoreUserDefinedDefault As EnumerateColumnsGrbit
'Usage
Dim value As EnumerateColumnsGrbit

value = Server2003Grbits.EnumerateIgnoreUserDefinedDefault
```

``` csharp
public const EnumerateColumnsGrbit EnumerateIgnoreUserDefinedDefault
```

## <a name="remarks"></a>Notes

cette option est disponible uniquement pour les systèmes d’exploitation Windows Server 2003 SP1 et versions ultérieures.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Server2003Grbits, classe](./server2003grbits-class.md)

[Membres Server2003Grbits](./server2003grbits-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
