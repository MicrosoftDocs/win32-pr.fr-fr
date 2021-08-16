---
description: 'En savoir plus sur : méthode API. JetCompact'
title: API. JetCompact, méthode
TOCTitle: 'JetCompact method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCompact(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS,Microsoft.Isam.Esent.Interop.JET_CONVERT,Microsoft.Isam.Esent.Interop.CompactGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcompact(v=EXCHG.10)
ms:contentKeyID: 55100666
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8aecd3ec6120a93edb19b06d1f86c9573c1404f8dc1feb95c1acfec2d0077bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983459"
---
# <a name="apijetcompact-method"></a>API. JetCompact, méthode

Effectue une copie d’une base de données existante. La copie est compactée dans un état optimal pour l’utilisation. Les données dans les données copiées seront empaquetées en fonction des mesures choisies pour les index lors de la création de l’index. De cette façon, les données compactées peuvent être stockées aussi denses que possible. Les données compactées peuvent également réserver de l’espace pour la croissance des enregistrements ou les insertions d’index suivantes.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetCompact ( _
    sesid As JET_SESID, _
    sourceDatabase As String, _
    destinationDatabase As String, _
    statusCallback As JET_PFNSTATUS, _
    ignored As JET_CONVERT, _
    grbit As CompactGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim sourceDatabase As String
Dim destinationDatabase As String
Dim statusCallback As JET_PFNSTATUS
Dim ignored As JET_CONVERT
Dim grbit As CompactGrbitApi.JetCompact(sesid, sourceDatabase, _
    destinationDatabase, statusCallback, _
    ignored, grbit)
```

``` csharp
public static void JetCompact(
    JET_SESID sesid,
    string sourceDatabase,
    string destinationDatabase,
    JET_PFNSTATUS statusCallback,
    JET_CONVERT ignored,
    CompactGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser pour l’appel.

<!-- end list -->

  - sourceDatabase  
    Type : [System. String](/dotnet/api/system.string)  
    
    Base de données source qui sera compactée.

<!-- end list -->

  - destinationDatabase  
    Type : [System. String](/dotnet/api/system.string)  
    
    Nom à utiliser pour la base de données compactée.

<!-- end list -->

  - statusCallback  
    Type : [Microsoft.ISAM.esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Fonction de rappel qui peut être appelée régulièrement via l’opération de compactage de la base de données pour signaler la progression.

<!-- end list -->

  - ignoré  
    Type : [Microsoft.ISAM.esent.Interop.JET_CONVERT](./jet-convert-class.md)  
    
    Ce paramètre est ignoré et doit avoir la valeur null.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. CompactGrbit](./compactgrbit-enumeration.md)  
    
    Options de compactage.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
