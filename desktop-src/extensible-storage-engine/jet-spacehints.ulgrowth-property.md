---
description: 'En savoir plus sur : propriété JET_SPACEHINTS. ulGrowth'
title: JET_SPACEHINTS. ulGrowth, propriété
TOCTitle: 'ulGrowth property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ulGrowth
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_spacehints.ulgrowth(v=EXCHG.10)
ms:contentKeyID: 55103929
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ulGrowth
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.set_ulGrowth
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ulGrowth
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.get_ulGrowth
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 946975a1777778871ecb8ae66c8e567e7c2ffcd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749764"
---
# <a name="jet_spacehintsulgrowth-property"></a>JET_SPACEHINTS. ulGrowth, propriété

Obtient ou définit le pourcentage de croissance de la dernière croissance ou taille initiale (éventuellement arrondie à la taille d’allocation JET Native la plus proche). Les valeurs valides sont 0 et \[ 100, 50000).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property ulGrowth As Integer
    Get
    Set
'Usage
Dim instance As JET_SPACEHINTS
Dim value As Integer

value = instance.ulGrowth

instance.ulGrowth = value
```

``` csharp
public int ulGrowth { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_SPACEHINTS](./jet-spacehints-class.md)

[Membres JET_SPACEHINTS](./jet-spacehints-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
