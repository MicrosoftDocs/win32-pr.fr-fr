---
description: 'En savoir plus sur : SystemParameters. StartFlushThreshold, propriété'
title: Propriété SystemParameters. StartFlushThreshold
TOCTitle: 'StartFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.startflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104050
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StartFlushThreshold
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 49a868bf06f6994d61e3f901d5d9a447d2ef63c7909c33db3689fda343e16c27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118484858"
---
# <a name="systemparametersstartflushthreshold-property"></a>Propriété SystemParameters. StartFlushThreshold

Obtient ou définit le seuil auquel le cache de la page de base de données commence à supprimer les pages du cache pour libérer de l’espace pour les pages qui ne sont pas mises en cache. Lorsque le nombre de tampons de page dans le cache descend sous ce seuil, un processus en arrière-plan est démarré pour réapprovisionner ce pool de mémoires tampons disponibles. Ce seuil est toujours relatif à la taille maximale du cache définie par JET_paramCacheSizeMax. Ce seuil doit également toujours être inférieur au seuil d’arrêt défini par JET_paramStopFlushThreshold. La hauteur de distance du seuil de démarrage détermine le temps de réponse que le cache de page de la base de données doit avoir pour produire des tampons disponibles avant que l’application en ait besoin. Un seuil de démarrage élevé donnera plus de temps au processus en arrière-plan. Toutefois, un seuil de démarrage élevé implique un seuil d’arrêt plus élevé et réduit la taille effective du cache des pages de la base de données.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Property StartFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StartFlushThreshold

SystemParameters.StartFlushThreshold = value
```

``` csharp
public static int StartFlushThreshold { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[SystemParameters (classe)](./systemparameters-class.md)

[Membres SystemParameters](./systemparameters-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
