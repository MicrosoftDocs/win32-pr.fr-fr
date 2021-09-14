---
description: 'En savoir plus sur : méthode API. JetGetAttachInfoInstance'
title: API. JetGetAttachInfoInstance, méthode
TOCTitle: 'JetGetAttachInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetattachinfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100704
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94865042edf8b049b7140673a8aee1b4e2d91573
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921155"
---
# <a name="apijetgetattachinfoinstance-method"></a>API. JetGetAttachInfoInstance, méthode

Utilisé lors d’une sauvegarde initiée par [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) pour interroger une instance pour obtenir les noms des fichiers de base de données qui doivent faire partie du jeu de fichiers de sauvegarde. Seules les bases de données qui sont actuellement attachées à l’instance à l’aide de [JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) sont prises en compte. Ces fichiers peuvent ensuite être ouverts à l’aide de [JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) et lus à l’aide de [JetReadFileInstance (JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32)](./api.jetreadfileinstance-method.md).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetGetAttachInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetAttachInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetAttachInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a>Paramètres

  - instance  
    Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instance pour laquelle obtenir les informations.

<!-- end list -->

  - files  
    Type : [System. String](/dotnet/api/system.string)  
    
    Retourne une liste de chaînes terminées par le caractère null qui décrivent l’ensemble des fichiers de base de données qui doivent faire partie du jeu de fichiers de sauvegarde. La liste de chaînes retournée dans cette mémoire tampon est dans le même format qu’une chaîne multiple utilisée par le registre. Chaque chaîne se terminant par un caractère NULL est retournée dans la séquence suivie d’une marque de fin null finale.

<!-- end list -->

  - maxChars  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Nombre maximal de caractères à récupérer.

<!-- end list -->

  - actualChars  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Taille réelle de la liste de fichiers. Si cette valeur est supérieure à maxChars, la liste a été tronquée.

## <a name="remarks"></a>Notes

Il est important de noter que cette API ne retourne pas d’erreur ou d’avertissement si la mémoire tampon de sortie est trop petite pour accepter la liste complète des fichiers qui doivent faire partie du jeu de fichiers de sauvegarde.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
