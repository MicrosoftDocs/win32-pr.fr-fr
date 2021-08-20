---
description: 'En savoir plus sur : méthode API. JetGetTableInfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)'
title: Méthode API. JetGetTableInfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, String, JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String@,Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100745
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a742aaa8ee6bd8c296f0a6aa912a9a4ca8f4ed48cf560e77ce469a13a2712fb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117603"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-string-jet_tblinfo"></a>Méthode API. JetGetTableInfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)

Récupère différents éléments d’informations sur une table dans une base de données.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef result As String, _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As String
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out string result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Table dont les informations doivent être récupérées.

<!-- end list -->

  - result  
    Type : [System. String](/dotnet/api/system.string)  
    
    Informations récupérées.

<!-- end list -->

  - infoLevel  
    Type : [Microsoft.ISAM.esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)  
    
    Type d’informations à récupérer.

## <a name="remarks"></a>Remarques

Cette surcharge est utilisée avec [Name](./jet-tblinfo-enumeration.md) et [TemplateTableName](./jet-tblinfo-enumeration.md).

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Surcharge JetGetTableInfo](./api.jetgettableinfo-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
