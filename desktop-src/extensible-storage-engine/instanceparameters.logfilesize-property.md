---
description: 'En savoir plus sur : InstanceParameters. LogFileSize, propriété'
title: InstanceParameters. LogFileSize, propriété
TOCTitle: 'LogFileSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logfilesize(v=EXCHG.10)
ms:contentKeyID: 55103312
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogFileSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogFileSize
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c141c76a92f49b4b5000cad65e302a7cf15d780f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535472"
---
# <a name="instanceparameterslogfilesize-property"></a>InstanceParameters. LogFileSize, propriété

Obtient ou définit la taille des fichiers du journal des transactions. Ce paramètre doit être défini en unités de 1024 octets (par exemple, un paramètre de 2048 donne des fichiers journaux de 2 Mo).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property LogFileSize As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogFileSize

instance.LogFileSize = value
```

``` csharp
public int LogFileSize { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[InstanceParameters, classe](./instanceparameters-class.md)

[Membres InstanceParameters](./instanceparameters-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
