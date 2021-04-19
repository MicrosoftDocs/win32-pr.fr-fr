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
ms.openlocfilehash: 54e54576dfb1023ec4e3bc55ddd198a77f0ddf25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524898"
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

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Nom du membre</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Tous</td>
<td>Arrête tous les services ESE pour l’instance spécifiée.</td>
</tr>
<tr class="even">
<td></td>
<td>BackgroundUserTasks</td>
<td>Arrête les tâches de maintenance en arrière-plan spécifiques au client redémarrables (arbre B + arborescence).</td>
</tr>
<tr class="odd">
<td></td>
<td>QuiesceCaches</td>
<td>Quiesces tous les caches modifiés sur le disque. Asynchrone. La suspension est annulée si le bit de reprise est appelé par la suite.</td>
</tr>
<tr class="even">
<td></td>
<td>Reprendre</td>
<td>Reprend les opérations StopService précédemment émises, c.-à-d. &quot; redémarre le service &quot; . Peut être combiné avec les grbits ci-dessus pour reprendre des services spécifiques, ou avec 0x0 pour reprendre tous les services arrêtés précédemment.
<p>AVERTISSEMENT : ce bit ne peut être utilisé que pour reprendre JET_bitStopServiceBackground et JET_bitStopServiceQuiesceCaches, si vous avez effectué une JET_bitStopServiceAll ou une JET_bitStopServiceAPI, toute tentative d’utilisation de JET_bitStopServiceResume échouera.</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
