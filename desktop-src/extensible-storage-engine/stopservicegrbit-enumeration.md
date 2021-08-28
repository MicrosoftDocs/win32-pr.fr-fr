---
description: 'En savoir plus sur : énumération StopServiceGrbit'
title: Énumération StopServiceGrbit (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c8280bf4abfbc9eb5818d1aab460a17298db7b0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477455"
---
# <a name="stopservicegrbit-enumeration"></a>Énumération StopServiceGrbit

Options pour [JetStopServiceInstance2 (JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a>Membres


|  | Nom du membre | Description | 
|--|-------------|-------------|
|  | Tous | Arrête tous les services ESE pour l’instance spécifiée. | 
|  | BackgroundUserTasks | Arrête les tâches de maintenance en arrière-plan spécifiques au client redémarrables (arbre B + arborescence). | 
|  | QuiesceCaches | Quiesces tous les caches modifiés sur le disque. Asynchrone. La suspension est annulée si le bit de reprise est appelé par la suite. | 
|  | Reprendre | Reprend les opérations StopService précédemment émises, par exemple « redémarre le service ». Peut être combiné avec les grbits ci-dessus pour reprendre des services spécifiques, ou avec 0x0 pour reprendre tous les services arrêtés précédemment.<p>AVERTISSEMENT : ce bit ne peut être utilisé que pour reprendre JET_bitStopServiceBackground et JET_bitStopServiceQuiesceCaches, si vous avez effectué une JET_bitStopServiceAll ou une JET_bitStopServiceAPI, toute tentative d’utilisation de JET_bitStopServiceResume échouera.</p> | 



## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Espace de noms Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
