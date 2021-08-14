---
description: 'En savoir plus sur : méthode API. JetCreateInstance2'
title: API. JetCreateInstance2, méthode
TOCTitle: 'JetCreateInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,System.String,System.String,Microsoft.Isam.Esent.Interop.CreateInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateinstance2(v=EXCHG.10)
ms:contentKeyID: 55100675
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46313c3307db53084b88cd1d8b495a4368abe4412ed9ab99f76430d48435dfed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117719257"
---
# <a name="apijetcreateinstance2-method"></a>API. JetCreateInstance2, méthode

Allouez une nouvelle instance du moteur de base de données pour une utilisation dans un processus unique, avec un nom d’affichage spécifié.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetCreateInstance2 ( _
    <OutAttribute> ByRef instance As JET_INSTANCE, _
    name As String, _
    displayName As String, _
    grbit As CreateInstanceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim name As String
Dim displayName As String
Dim grbit As CreateInstanceGrbitApi.JetCreateInstance2(instance, _
    name, displayName, grbit)
```

``` csharp
public static void JetCreateInstance2(
    out JET_INSTANCE instance,
    string name,
    string displayName,
    CreateInstanceGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - instance  
    Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Retourne l’instance nouvellement créée.

<!-- end list -->

  - name  
    Type : [System. String](/dotnet/api/system.string)  
    
    Spécifie un identificateur de chaîne unique pour l’instance à créer. Cette chaîne doit être unique au sein d’un processus donné hébergeant le moteur de base de données.

<!-- end list -->

  - displayName  
    Type : [System. String](/dotnet/api/system.string)  
    
    Nom complet de l’instance à créer. Il sera utilisé dans les entrées du journal des événements.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. CreateInstanceGrbit](./createinstancegrbit-enumeration.md)  
    
    Options de création.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
