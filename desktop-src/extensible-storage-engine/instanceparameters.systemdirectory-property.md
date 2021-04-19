---
description: 'En savoir plus sur les éléments suivants : InstanceParameters.Syspropriété temDirectory'
title: InstanceParameters.Syspropriété temDirectory
TOCTitle: 'SystemDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.SystemDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.systemdirectory(v=EXCHG.10)
ms:contentKeyID: 55103561
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.SystemDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_SystemDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.SystemDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_SystemDirectory
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c0478b4b9d626610549240d58f3289fc24d10aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523696"
---
# <a name="instanceparameterssystemdirectory-property"></a>InstanceParameters.Syspropriété temDirectory

Obtient ou définit le chemin d’accès relatif ou absolu du système de fichiers du dossier qui contiendra le fichier de point de contrôle de l’instance.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property SystemDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.SystemDirectory

instance.SystemDirectory = value
```

``` csharp
public string SystemDirectory { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. String](/dotnet/api/system.string)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[InstanceParameters, classe](./instanceparameters-class.md)

[Membres InstanceParameters](./instanceparameters-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
