---
description: 'En savoir plus sur : méthode JET_LGPOS. CompareTo'
title: JET_LGPOS. CompareTo, méthode
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo(Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.compareto(v=EXCHG.10)
ms:contentKeyID: 39514516
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 83012ed755ab876618147c013e99868927e16f1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126850899"
---
# <a name="jet_lgposcompareto-method"></a>JET_LGPOS. CompareTo, méthode

Compare cette position du journal à une autre position du journal et détermine si cette instance est antérieure, identique ou postérieure à l’autre instance.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_LGPOS _
) As Integer
'Usage
Dim instance As JET_LGPOS
Dim other As JET_LGPOS
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_LGPOS other
)
```

#### <a name="parameters"></a>Paramètres

  - other  
    Type : [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    Position du journal à comparer à l’instance actuelle.

#### <a name="return-value"></a>Valeur de retour

Type : [System. Int32](/dotnet/api/system.int32)  
Nombre signé indiquant les positions relatives de cette instance et du paramètre de valeur.  

#### <a name="implements"></a>Implémente

[IComparable \<T\> . CompareTo (T)](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_LGPOS](./jet-lgpos-structure2.md)

[Membres JET_LGPOS](./jet-lgpos-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
