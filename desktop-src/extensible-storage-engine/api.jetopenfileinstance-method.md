---
description: 'En savoir plus sur : méthode API. JetOpenFileInstance'
title: API. JetOpenFileInstance, méthode
TOCTitle: 'JetOpenFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.JET_HANDLE@,System.Int64@,System.Int64@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopenfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100767
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b58b3a426fd2eb7e33cce1f5f539418bcc993ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522423"
---
# <a name="apijetopenfileinstance-method"></a>API. JetOpenFileInstance, méthode

Ouvre une base de données attachée, un fichier de correctif de base de données ou un fichier journal de transactions d’une instance active pour effectuer une sauvegarde de diffusion en continu floue. Les données de ces fichiers peuvent ensuite être lues par le handle retourné à l’aide de JetReadFileInstance. Le handle retourné doit être fermé à l’aide de JetCloseFileInstance. Une sauvegarde externe de l’instance doit avoir été précédemment lancée à l’aide de JetBeginExternalBackupInstance.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetOpenFileInstance ( _
    instance As JET_INSTANCE, _
    file As String, _
    <OutAttribute> ByRef handle As JET_HANDLE, _
    <OutAttribute> ByRef fileSizeLow As Long, _
    <OutAttribute> ByRef fileSizeHigh As Long _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As String
Dim handle As JET_HANDLE
Dim fileSizeLow As Long
Dim fileSizeHigh As LongApi.JetOpenFileInstance(instance, _
    file, handle, fileSizeLow, fileSizeHigh)
```

``` csharp
public static void JetOpenFileInstance(
    JET_INSTANCE instance,
    string file,
    out JET_HANDLE handle,
    out long fileSizeLow,
    out long fileSizeHigh
)
```

#### <a name="parameters"></a>Paramètres

  - instance  
    Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instance à utiliser.

<!-- end list -->

  - fichier  
    Type : [System. String](/dotnet/api/system.string)  
    
    Fichier à ouvrir.

<!-- end list -->

  - traitée  
    Type : [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    Retourne un handle au fichier.

<!-- end list -->

  - fileSizeLow  
    Type : [System. Int64](/dotnet/api/system.int64)  
    
    Retourne les 32 bits les moins significatifs de la taille du fichier.

<!-- end list -->

  - fileSizeHigh  
    Type : [System. Int64](/dotnet/api/system.int64)  
    
    Retourne les 32 bits les plus significatifs de la taille du fichier.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
