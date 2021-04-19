---
description: 'En savoir plus sur : méthode VistaApi. JetGetThreadStats'
title: Méthode VistaApi. JetGetThreadStats (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'JetGetThreadStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetthreadstats(v=EXCHG.10)
ms:contentKeyID: 55104192
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 92572fd538f0c6c2643e7b40a07ac168ae6980d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524966"
---
# <a name="vistaapijetgetthreadstats-method"></a>Méthode VistaApi. JetGetThreadStats

Récupère les informations de performance du moteur de base de données pour le thread actuel. Plusieurs appels peuvent être utilisés pour collecter des statistiques qui reflètent l’activité du moteur de base de données sur ce thread entre ces appels.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetGetThreadStats ( _
    <OutAttribute> ByRef threadstats As JET_THREADSTATS _
)
'Usage
Dim threadstats As JET_THREADSTATSVistaApi.JetGetThreadStats(threadstats)
```

``` csharp
public static void JetGetThreadStats(
    out JET_THREADSTATS threadstats
)
```

#### <a name="parameters"></a>Paramètres

  - threadstats  
    Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    Retourne les données de statistiques de thread.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[VistaApi, classe](./vistaapi-class.md)

[Membres VistaApi](./vistaapi-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
