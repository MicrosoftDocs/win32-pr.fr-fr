---
description: 'En savoir plus sur : méthode API. TryMoveNext'
title: API. TryMoveNext, méthode
TOCTitle: 'TryMoveNext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMoveNext(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymovenext(v=EXCHG.10)
ms:contentKeyID: 55100887
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMoveNext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMoveNext
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e0f44caef2cef6d168668525b8dbd4066d1519f7e3d80ee5de9baec5a10d10c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738379"
---
# <a name="apitrymovenext-method"></a>API. TryMoveNext, méthode

Essayez de vous déplacer vers l’enregistrement suivant dans la table. Si aucun enregistrement suivant n’est présent, la valeur false est retournée, si une erreur différente est rencontrée, une exception est levée.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Function TryMoveNext ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMoveNext(sesid, _
    tableid)
```

``` csharp
public static bool TryMoveNext(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Curseur à positionner.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si le déplacement a réussi.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
