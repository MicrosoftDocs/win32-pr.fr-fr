---
description: 'En savoir plus sur : JET_BKLOGTIME. ToDateTime, méthode'
title: JET_BKLOGTIME. ToDateTime, méthode
TOCTitle: 'ToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.ToDateTime
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.todatetime(v=EXCHG.10)
ms:contentKeyID: 39515201
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.ToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.ToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88319fb0e179e84322bfd5badab8234e323615a9bb6681852d2ab09ac3146b35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721069"
---
# <a name="jet_bklogtimetodatetime-method"></a>JET_BKLOGTIME. ToDateTime, méthode

Génère une représentation DateTime de cette JET_BKLOGTIME.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Function ToDateTime As Nullable(Of DateTime)
'Usage
Dim instance As JET_BKLOGTIME
Dim returnValue As Nullable(Of DateTime)

returnValue = instance.ToDateTime()
```

``` csharp
public Nullable<DateTime> ToDateTime()
```

#### <a name="return-value"></a>Valeur de retour

Type : [System. Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\>  
Valeur DateTime représentant le JET_BKLOGTIME. Si le JET_BKLOGTIME a la valeur null, la valeur null est retournée.  

#### <a name="implements"></a>Implémente

[IJET_LOGTIME. ToDateTime ()](./ijet-logtime.todatetime-method.md)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_BKLOGTIME](./jet-bklogtime-structure2.md)

[Membres JET_BKLOGTIME](./jet-bklogtime-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
