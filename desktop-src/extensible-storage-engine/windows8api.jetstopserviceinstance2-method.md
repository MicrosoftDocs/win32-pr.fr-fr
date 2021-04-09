---
description: 'En savoir plus sur : méthode Windows8Api. JetStopServiceInstance2'
title: Méthode Windows8Api. JetStopServiceInstance2 (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetStopServiceInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetstopserviceinstance2(v=EXCHG.10)
ms:contentKeyID: 55104460
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0821a00016eb9cd2c511ee37889e0ddaa0b76edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034133"
---
# <a name="windows8apijetstopserviceinstance2-method"></a>Méthode Windows8Api. JetStopServiceInstance2

Prépare une instance pour l’arrêt. Peut également être utilisé pour reprendre une suspension précédente.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetStopServiceInstance2 ( _
    instance As JET_INSTANCE, _
    grbit As StopServiceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As StopServiceGrbitWindows8Api.JetStopServiceInstance2(instance, _
    grbit)
```

``` csharp
public static void JetStopServiceInstance2(
    JET_INSTANCE instance,
    StopServiceGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - instance  
    Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instance (en cours d’exécution) à utiliser.

<!-- end list -->

  - grbit  
    Tapez : [Microsoft. ISAM. esent. Interop. Windows8. StopServiceGrbit](./stopservicegrbit-enumeration.md)  
    
    Options permettant d’arrêter ou de reprendre l’instance.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Windows8Api, classe](./windows8api-class.md)

[Membres Windows8Api](./windows8api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
