---
description: 'En savoir plus sur : méthode API. JetRestoreInstance'
title: API. JetRestoreInstance, méthode
TOCTitle: 'JetRestoreInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrestoreinstance(v=EXCHG.10)
ms:contentKeyID: 55100787
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e2c2976eb8bf661dc53bdc86723bb21309ab973
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010323"
---
# <a name="apijetrestoreinstance-method"></a>API. JetRestoreInstance, méthode

Restaure et récupère une sauvegarde en continu d’une instance, y compris toutes les bases de données attachées. Il est conçu pour fonctionner avec une sauvegarde créée avec la fonction [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md) . Il s’agit de la fonction de restauration la plus simple et la plus encapsulée.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetRestoreInstance ( _
    instance As JET_INSTANCE, _
    source As String, _
    destination As String, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim source As String
Dim destination As String
Dim statusCallback As JET_PFNSTATUSApi.JetRestoreInstance(instance, _
    source, destination, statusCallback)
```

``` csharp
public static void JetRestoreInstance(
    JET_INSTANCE instance,
    string source,
    string destination,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a>Paramètres

  - instance  
    Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instance à utiliser. L’instance ne doit pas être initialisée. La restauration des fichiers va initialiser l’instance.

<!-- end list -->

  - source  
    Type : [System. String](/dotnet/api/system.string)  
    
    Emplacement de la sauvegarde. La sauvegarde doit avoir été créée avec [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).

<!-- end list -->

  - destination  
    Type : [System. String](/dotnet/api/system.string)  
    
    Nom du dossier dans lequel les fichiers de base de données du jeu de sauvegarde seront copiés et récupérés. Si la valeur est null, les fichiers de base de données sont copiés et récupérés à leur emplacement d’origine.

<!-- end list -->

  - statusCallback  
    Type : [Microsoft.ISAM.esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Rappel de notification d’État facultatif.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
