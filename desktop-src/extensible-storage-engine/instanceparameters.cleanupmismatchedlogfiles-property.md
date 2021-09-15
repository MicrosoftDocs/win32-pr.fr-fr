---
description: 'En savoir plus sur : InstanceParameters. CleanupMismatchedLogFiles, propriété'
title: InstanceParameters. CleanupMismatchedLogFiles, propriété
TOCTitle: 'CleanupMismatchedLogFiles property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cleanupmismatchedlogfiles(v=EXCHG.10)
ms:contentKeyID: 55103296
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e80bb8877335e26cb233a09b2fa3ec3a6f12615
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517285"
---
# <a name="instanceparameterscleanupmismatchedlogfiles-property"></a>InstanceParameters. CleanupMismatchedLogFiles, propriété

Obtient ou définit une valeur indiquant si JetInit échoue lorsque le moteur de base de données est configuré pour démarrer à l’aide des fichiers du journal des transactions sur un disque d’une taille différente de celle configurée. Normalement, [JetInit (JET_INSTANCE)](./api.jetinit-method.md) récupère les bases de données, mais échoue avec [LogFileSizeMismatchDatabasesConsistent](./jet-err-enumeration.md) pour indiquer que la taille du fichier journal n’est pas correctement configurée. Toutefois, lorsque ce paramètre est défini sur true, le moteur de base de données supprime silencieusement tous les anciens fichiers journaux, puis démarre un nouvel ensemble de fichiers journaux de transactions à l’aide de la taille de fichier journal configurée. Ce paramètre est utile lorsque l’application souhaite modifier en toute transparence la taille du fichier journal des transactions, tout en continuant à travailler de manière transparente dans les scénarios de mise à niveau et de restauration.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property CleanupMismatchedLogFiles As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CleanupMismatchedLogFiles

instance.CleanupMismatchedLogFiles = value
```

``` csharp
public bool CleanupMismatchedLogFiles { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[InstanceParameters, classe](./instanceparameters-class.md)

[Membres InstanceParameters](./instanceparameters-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
