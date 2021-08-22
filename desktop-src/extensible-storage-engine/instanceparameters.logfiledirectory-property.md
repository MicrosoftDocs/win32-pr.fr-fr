---
description: 'En savoir plus sur : InstanceParameters. répertoire, propriété'
title: InstanceParameters. répertoire, propriété
TOCTitle: 'LogFileDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logfiledirectory(v=EXCHG.10)
ms:contentKeyID: 55103562
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogFileDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogFileDirectory
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55020b6c0f9e3a4b970242de2e43fe771b4c90550fe65f1585a2ab67c4211182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119039427"
---
# <a name="instanceparameterslogfiledirectory-property"></a>InstanceParameters. répertoire, propriété

Obtient ou définit le chemin d’accès relatif ou absolu du système de fichiers du dossier qui contiendra les journaux des transactions pour l’instance.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property LogFileDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.LogFileDirectory

instance.LogFileDirectory = value
```

``` csharp
public string LogFileDirectory { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. String](/dotnet/api/system.string)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[InstanceParameters, classe](./instanceparameters-class.md)

[Membres InstanceParameters](./instanceparameters-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
