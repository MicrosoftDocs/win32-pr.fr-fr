---
description: 'En savoir plus sur : méthode API. TryGetLock'
title: API. TryGetLock, méthode
TOCTitle: 'TryGetLock method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryGetLock(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.GetLockGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trygetlock(v=EXCHG.10)
ms:contentKeyID: 55100934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryGetLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryGetLock
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a6a8d4ac8b5b81b1238e7847846a1e95122bc53cf8912d591acb221d666d6e24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738579"
---
# <a name="apitrygetlock-method"></a>API. TryGetLock, méthode

Réserver explicitement la possibilité de mettre à jour une ligne, un verrou en écriture ou d’empêcher explicitement une ligne d’être mise à jour par une autre session, verrou de lecture. Normalement, les verrous d’écriture de ligne sont acquis implicitement en raison de la mise à jour des lignes. Les verrous de lecture ne sont généralement pas requis en raison du contrôle de version des enregistrements. Toutefois, dans certains cas, une transaction peut souhaiter verrouiller explicitement une ligne pour appliquer la sérialisation, ou pour s’assurer qu’une opération suivante va être effectuée.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Function TryGetLock ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As GetLockGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As GetLockGrbit
Dim returnValue As Boolean

returnValue = Api.TryGetLock(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TryGetLock(
    JET_SESID sesid,
    JET_TABLEID tableid,
    GetLockGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Curseur à utiliser. Un verrou sera acquis sur l’enregistrement en cours.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. GetLockGrbit](./getlockgrbit-enumeration.md)  
    
    Options de verrouillage, utilisez cette option pour spécifier le type de verrou à obtenir.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si le verrou a été obtenu ; sinon, false. Une exception est levée si une erreur inattendue est rencontrée.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
