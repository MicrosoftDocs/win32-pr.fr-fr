---
description: 'En savoir plus sur : propriété InstanceParameters. BaseName'
title: InstanceParameters. BaseName, propriété
TOCTitle: 'BaseName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.BaseName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.basename(v=EXCHG.10)
ms:contentKeyID: 55103315
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.BaseName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.BaseName
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_BaseName
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_BaseName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe441036dbd4ae4b6c861e17e73596ef194cd05f2ad7fa46eb5c8fd8f5d8dbcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112462"
---
# <a name="instanceparametersbasename-property"></a>InstanceParameters. BaseName, propriété

Obtient ou définit le préfixe à trois lettres utilisé pour la plupart des fichiers utilisés par le moteur de base de données. Par exemple, le fichier de point de contrôle est appelé EDB. CHK par défaut, car EDB est le nom de base par défaut.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property BaseName As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.BaseName

instance.BaseName = value
```

``` csharp
public string BaseName { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. String](/dotnet/api/system.string)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[InstanceParameters, classe](./instanceparameters-class.md)

[Membres InstanceParameters](./instanceparameters-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
