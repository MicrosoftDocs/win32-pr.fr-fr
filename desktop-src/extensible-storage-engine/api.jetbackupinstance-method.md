---
description: 'En savoir plus sur : méthode API. JetBackupInstance'
title: API. JetBackupInstance, méthode
TOCTitle: 'JetBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.BackupGrbit,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55107221
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a4b9ef9fbedce13b9c68940fc45204a35c1113e9551034fa57ed6948f4fa5e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983649"
---
# <a name="apijetbackupinstance-method"></a>API. JetBackupInstance, méthode

Effectue une sauvegarde en continu d’une instance de, y compris toutes les bases de données attachées, vers un répertoire. Avec plusieurs méthodes de sauvegarde prises en charge par le moteur, il s’agit de la fonction la plus simple et la plus encapsulée.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetBackupInstance ( _
    instance As JET_INSTANCE, _
    destination As String, _
    grbit As BackupGrbit, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim destination As String
Dim grbit As BackupGrbit
Dim statusCallback As JET_PFNSTATUSApi.JetBackupInstance(instance, _
    destination, grbit, statusCallback)
```

``` csharp
public static void JetBackupInstance(
    JET_INSTANCE instance,
    string destination,
    BackupGrbit grbit,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a>Paramètres

  - instance  
    Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instance à sauvegarder.

<!-- end list -->

  - destination  
    Type : [System. String](/dotnet/api/system.string)  
    
    Répertoire dans lequel la sauvegarde doit être stockée. Si le chemin d’accès de sauvegarde a la valeur null pour utiliser, la fonction tronque les journaux, si possible.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. BackupGrbit](./backupgrbit-enumeration.md)  
    
    Options de sauvegarde.

<!-- end list -->

  - statusCallback  
    Type : [Microsoft.ISAM.esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Rappel de notification d’État facultatif.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
