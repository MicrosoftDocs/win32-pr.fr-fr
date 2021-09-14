---
description: 'En savoir plus sur : méthode API. JetEndSession'
title: API. JetEndSession, méthode
TOCTitle: 'JetEndSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndSession(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.EndSessionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendsession(v=EXCHG.10)
ms:contentKeyID: 55100690
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndSession
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10412f6b01b14d63557bf024d65975c271bbe31b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921175"
---
# <a name="apijetendsession-method"></a>API. JetEndSession, méthode

Met fin à une session.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetEndSession ( _
    sesid As JET_SESID, _
    grbit As EndSessionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As EndSessionGrbitApi.JetEndSession(sesid, grbit)
```

``` csharp
public static void JetEndSession(
    JET_SESID sesid,
    EndSessionGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à terminer.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. EndSessionGrbit](./endsessiongrbit-enumeration.md)  
    
    Ce paramètre n'est pas utilisé.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
