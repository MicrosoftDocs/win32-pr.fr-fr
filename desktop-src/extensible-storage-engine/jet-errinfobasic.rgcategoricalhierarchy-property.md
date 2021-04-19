---
description: 'En savoir plus sur : propriété JET_ERRINFOBASIC. rgCategoricalHierarchy'
title: JET_ERRINFOBASIC. rgCategoricalHierarchy, propriété (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'rgCategoricalHierarchy property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.rgCategoricalHierarchy
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errinfobasic.rgcategoricalhierarchy(v=EXCHG.10)
ms:contentKeyID: 55104314
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.rgCategoricalHierarchy
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.set_rgCategoricalHierarchy
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.get_rgCategoricalHierarchy
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.rgCategoricalHierarchy
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37034ca35427c9470d69f5e90dd43a4640601574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522030"
---
# <a name="jet_errinfobasicrgcategoricalhierarchy-property"></a>JET_ERRINFOBASIC. rgCategoricalHierarchy, propriété

Obtient ou définit la hiérarchie des erreurs. La position 0 est le niveau le plus élevé dans la hiérarchie, tandis que le reste est JET_errcatUnknown.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property rgCategoricalHierarchy As JET_ERRCAT()
    Get
    Set
'Usage
Dim instance As JET_ERRINFOBASIC
Dim value As JET_ERRCAT()

value = instance.rgCategoricalHierarchy

instance.rgCategoricalHierarchy = value
```

``` csharp
public JET_ERRCAT[] rgCategoricalHierarchy { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Entrer \[\]  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_ERRINFOBASIC](./jet-errinfobasic-class.md)

[Membres JET_ERRINFOBASIC](./jet-errinfobasic-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
