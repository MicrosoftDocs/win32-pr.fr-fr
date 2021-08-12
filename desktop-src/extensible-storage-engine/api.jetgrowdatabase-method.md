---
description: 'En savoir plus sur : méthode API. JetGrowDatabase'
title: API. JetGrowDatabase, méthode
TOCTitle: 'JetGrowDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgrowdatabase(v=EXCHG.10)
ms:contentKeyID: 55100754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80652f60e7c7bf8afad3e3dd6bc36d1998dc64b989c307e130ec9d664a7949f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118271913"
---
# <a name="apijetgrowdatabase-method"></a>API. JetGrowDatabase, méthode

Étend la taille d’une base de données qui est actuellement ouverte.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetGrowDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim desiredPages As Integer
Dim actualPages As IntegerApi.JetGrowDatabase(sesid, dbid, _
    desiredPages, actualPages)
```

``` csharp
public static void JetGrowDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    int desiredPages,
    out int actualPages
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - dbid  
    Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de données à augmenter.

<!-- end list -->

  - desiredPages  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Taille souhaitée de la base de données, en pages.

<!-- end list -->

  - actualPages  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Taille de la base de données, en pages, après l’appel.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
