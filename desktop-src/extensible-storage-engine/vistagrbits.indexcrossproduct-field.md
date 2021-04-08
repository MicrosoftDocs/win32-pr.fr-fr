---
description: 'En savoir plus sur : champ VistaGrbits. IndexCrossProduct'
title: Champ VistaGrbits. IndexCrossProduct (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: IndexCrossProduct field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits.indexcrossproduct(v=EXCHG.10)
ms:contentKeyID: 55104426
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1b16f741c63d455d18a887331505080aef62990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953201"
---
# <a name="vistagrbitsindexcrossproduct-field"></a>Champ VistaGrbits. IndexCrossProduct

La spécification de cet indicateur pour un index qui a plusieurs colonnes clés qui est une colonne à plusieurs valeurs entraîne la création d’une entrée d’index pour chaque résultat d’un produit croisé de toutes les valeurs dans ces colonnes clés. Dans le cas contraire, l’index comporte une seule entrée pour chaque valeur multiple dans la colonne clé la plus significative qui est une colonne à valeurs multiples et chacune de ces entrées d’index utilise la première valeur multiple de toutes les autres colonnes clés qui sont des colonnes à valeurs multiples. Par exemple, si vous avez spécifié cet indicateur pour un index sur la colonne a qui a les valeurs « Red » et « Blue » et sur la colonne B qui a les valeurs « 1 » et « 2 », les entrées d’index suivantes sont créées : « Red », « 1 »; « Red », « 2 »; "Blue", "1"; « Blue », « 2 ». Dans le cas contraire, les entrées d’index suivantes sont créées : « Red », « 1 »; « Blue », « 1 ».

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Const IndexCrossProduct As CreateIndexGrbit
'Usage
Dim value As CreateIndexGrbit

value = VistaGrbits.IndexCrossProduct
```

``` csharp
public const CreateIndexGrbit IndexCrossProduct
```

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[VistaGrbits, classe](./vistagrbits-class.md)

[Membres VistaGrbits](./vistagrbits-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
