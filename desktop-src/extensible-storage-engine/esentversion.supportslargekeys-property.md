---
description: 'En savoir plus sur : EsentVersion. SupportsLargeKeys, propriété'
title: EsentVersion. SupportsLargeKeys, propriété
TOCTitle: 'SupportsLargeKeys property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversion.supportslargekeys(v=EXCHG.10)
ms:contentKeyID: 55103180
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
- Microsoft.Isam.Esent.Interop.EsentVersion.get_SupportsLargeKeys
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43ee88b7c0e190d9c717c087deeb5fc4556e6575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535644"
---
# <a name="esentversionsupportslargekeys-property"></a>EsentVersion. SupportsLargeKeys, propriété

Obtient une valeur qui indique si les clés volumineuses ( \> 255 octets) sont prises en charge. La taille de la clé d’un index peut être spécifiée dans l’objet [JET_INDEXCREATE](./jet-indexcreate-class.md) .

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared ReadOnly Property SupportsLargeKeys As Boolean
    Get
'Usage
Dim value As Boolean

value = EsentVersion.SupportsLargeKeys
```

``` csharp
public static bool SupportsLargeKeys { get; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[EsentVersion, classe](./esentversion-class.md)

[Membres EsentVersion](./esentversion-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
