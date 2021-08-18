---
description: 'En savoir plus sur : InstanceParameters. CreatePathIfNotExist, propriété'
title: InstanceParameters. CreatePathIfNotExist, propriété
TOCTitle: 'CreatePathIfNotExist property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CreatePathIfNotExist
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.createpathifnotexist(v=EXCHG.10)
ms:contentKeyID: 55103321
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CreatePathIfNotExist
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CreatePathIfNotExist
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CreatePathIfNotExist
- Microsoft.Isam.Esent.Interop.InstanceParameters.CreatePathIfNotExist
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cf48149548a21cc225816d307f65ac7c24bdaba4bfd090def9951e773f251c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112418"
---
# <a name="instanceparameterscreatepathifnotexist-property"></a>InstanceParameters. CreatePathIfNotExist, propriété

Obtient ou définit une valeur indiquant si ESENT crée sans assistance des dossiers manquants dans ses chemins d’accès de système de fichiers.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property CreatePathIfNotExist As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CreatePathIfNotExist

instance.CreatePathIfNotExist = value
```

``` csharp
public bool CreatePathIfNotExist { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[InstanceParameters, classe](./instanceparameters-class.md)

[Membres InstanceParameters](./instanceparameters-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
