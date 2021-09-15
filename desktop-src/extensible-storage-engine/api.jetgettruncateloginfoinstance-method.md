---
description: 'En savoir plus sur : méthode API. JetGetTruncateLogInfoInstance'
title: API. JetGetTruncateLogInfoInstance, méthode
TOCTitle: 'JetGetTruncateLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettruncateloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100743
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc54d12796a724b382343c4a3514f03102df305f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530101"
---
# <a name="apijetgettruncateloginfoinstance-method"></a>API. JetGetTruncateLogInfoInstance, méthode

Utilisé lors d’une sauvegarde initiée par [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) pour interroger une instance pour connaître les noms des fichiers du journal des transactions qui peuvent être supprimés en toute sécurité une fois la sauvegarde terminée.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetGetTruncateLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetTruncateLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetTruncateLogInfoInstance(
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
    
    Retourne une liste de chaînes terminées par null qui décrivent l’ensemble des fichiers journaux de base de données qui peuvent être supprimés en toute sécurité une fois la sauvegarde terminée. La liste de chaînes retournée dans cette mémoire tampon est dans le même format qu’une chaîne multiple utilisée par le registre. Chaque chaîne se terminant par un caractère NULL est retournée dans la séquence suivie d’une marque de fin null finale.

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

#### <a name="reference"></a>Référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
