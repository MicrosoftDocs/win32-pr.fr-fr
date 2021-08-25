---
description: 'En savoir plus sur : InstanceParameters. EventSourceKey, propriété'
title: InstanceParameters. EventSourceKey, propriété
TOCTitle: 'EventSourceKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.eventsourcekey(v=EXCHG.10)
ms:contentKeyID: 55107449
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EventSourceKey
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EventSourceKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84d39ada06b0155c350da062eed6fffd23fa07b4866e7b94079019703247fef8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850269"
---
# <a name="instanceparameterseventsourcekey-property"></a>InstanceParameters. EventSourceKey, propriété

Obtient ou définit le nom du journal des événements que le moteur de base de données utilise pour ses messages de journal des événements. Par défaut, tous les messages du journal des événements sont envoyés dans le journal des événements de l’application. Si le nom de la clé de registre d’un autre journal des événements est configuré, les messages du journal des événements y seront à la place.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property EventSourceKey As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.EventSourceKey

instance.EventSourceKey = value
```

``` csharp
public string EventSourceKey { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. String](/dotnet/api/system.string)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[InstanceParameters, classe](./instanceparameters-class.md)

[Membres InstanceParameters](./instanceparameters-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
