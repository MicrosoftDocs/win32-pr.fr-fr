---
description: 'En savoir plus sur : InstanceParameters. DbExtensionSize, propriété'
title: InstanceParameters. DbExtensionSize, propriété
TOCTitle: 'DbExtensionSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.DbExtensionSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.dbextensionsize(v=EXCHG.10)
ms:contentKeyID: 55107443
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.DbExtensionSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_DbExtensionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.DbExtensionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_DbExtensionSize
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 402c37ca649a9e9ff70435c8a8ef58f79376842b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520438"
---
# <a name="instanceparametersdbextensionsize-property"></a>InstanceParameters. DbExtensionSize, propriété

Obtient ou définit le nombre de pages qui sont ajoutées à un fichier de base de données chaque fois qu’il doit croître pour accueillir davantage de données.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property DbExtensionSize As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.DbExtensionSize

instance.DbExtensionSize = value
```

``` csharp
public int DbExtensionSize { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[InstanceParameters, classe](./instanceparameters-class.md)

[Membres InstanceParameters](./instanceparameters-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
