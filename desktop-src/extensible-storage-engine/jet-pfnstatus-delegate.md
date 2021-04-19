---
description: 'En savoir plus sur : JET_PFNSTATUS délégué'
title: Délégué JET_PFNSTATUS
TOCTitle: JET_PFNSTATUS delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnstatus(v=EXCHG.10)
ms:contentKeyID: 39515654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.BeginInvoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16cc5807d858f964f995b449a0a0eee78659aefd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521876"
---
# <a name="jet_pfnstatus-delegate"></a>Délégué JET_PFNSTATUS

Reçoit des informations sur la progression des opérations de longue durée, telles que les opérations de défragmentation, de sauvegarde ou de restauration. Pendant ces opérations, le moteur de base de données appelle cette fonction de rappel pour fournir une mise à jour de la progression de l’opération.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Delegate Function JET_PFNSTATUS ( _
    sesid As JET_SESID, _
    snp As JET_SNP, _
    snt As JET_SNT, _
    data As Object _
) As JET_err
'Usage
Dim instance As New JET_PFNSTATUS(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNSTATUS(
    JET_SESID sesid,
    JET_SNP snp,
    JET_SNT snt,
    Object data
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session avec laquelle l’opération de longue durée a été appelée.

<!-- end list -->

  - SNP  
    Type : [Microsoft.ISAM.esent.Interop.JET_SNP](./jet-snp-enumeration.md)  
    
    Type d’opération.

<!-- end list -->

  - SNT  
    Type : [Microsoft.ISAM.esent.Interop.JET_SNT](./jet-snt-enumeration.md)  
    
    L’état de l’opération.

<!-- end list -->

  - data  
    Type : [System. Object](/dotnet/api/system.object)  
    
    Données facultatives. Peut être un [JET_SNPROG](./jet-snprog-class.md).

#### <a name="return-value"></a>Valeur retournée

Type : [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
