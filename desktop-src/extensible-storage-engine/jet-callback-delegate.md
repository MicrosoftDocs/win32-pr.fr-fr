---
description: 'En savoir plus sur : JET_CALLBACK délégué'
title: Délégué JET_CALLBACK
TOCTitle: JET_CALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_callback(v=EXCHG.10)
ms:contentKeyID: 39515752
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK..ctor
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.Invoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 617cbefba047f822b338627a782be7e016c2a16f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012531"
---
# <a name="jet_callback-delegate"></a>Délégué JET_CALLBACK

Fonction de rappel polyvalente utilisée par le moteur de base de données pour informer l’application d’un événement impliquant la défragmentation en ligne et les notifications de l’état du curseur.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Delegate Function JET_CALLBACK ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    arg1 As Object, _
    arg2 As Object, _
    context As IntPtr, _
    unused As IntPtr _
) As JET_err
'Usage
Dim instance As New JET_CALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_CALLBACK(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    Object arg1,
    Object arg2,
    IntPtr context,
    IntPtr unused
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session pour laquelle le rappel est effectué.

<!-- end list -->

  - dbid  
    Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de données pour laquelle le rappel est effectué.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Curseur pour lequel le rappel est effectué.

<!-- end list -->

  - cbtyp  
    Type : [Microsoft.ISAM.esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)  
    
    Opération pour laquelle le rappel est effectué.

<!-- end list -->

  - arg1  
    Type : [System. Object](/dotnet/api/system.object)  
    
    Premier argument spécifique au rappel.

<!-- end list -->

  - arg2  
    Type : [System. Object](/dotnet/api/system.object)  
    
    Deuxième argument spécifique au rappel.

<!-- end list -->

  - contexte  
    Type : [System. IntPtr](/dotnet/api/system.intptr)  
    
    Contexte de rappel.

<!-- end list -->

  - unused  
    Type : [System. IntPtr](/dotnet/api/system.intptr)  
    
    Ce paramètre n'est pas utilisé.

#### <a name="return-value"></a>Valeur de retour

Type : [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
