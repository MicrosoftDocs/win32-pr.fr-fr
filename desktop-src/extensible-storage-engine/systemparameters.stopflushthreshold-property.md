---
description: 'En savoir plus sur : SystemParameters. StopFlushThreshold, propriété'
title: Propriété SystemParameters. StopFlushThreshold
TOCTitle: 'StopFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.stopflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104130
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b79a9e5894de6539e8ab7dc0db4218b5f6cb3bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320162"
---
# <a name="systemparametersstopflushthreshold-property"></a>Propriété SystemParameters. StopFlushThreshold

Obtient ou définit le seuil auquel le cache de la page de base de données met fin à la suppression des pages du cache pour libérer de l’espace pour les pages qui ne sont pas mises en cache. Lorsque le nombre de tampons de page dans le cache dépasse ce seuil, le processus en arrière-plan qui a démarré pour réapprovisionner ce pool de mémoires tampons disponibles est arrêté. Ce seuil est toujours relatif à la taille maximale du cache définie par JET_paramCacheSizeMax. Ce seuil doit également être toujours supérieur au seuil de démarrage défini par JET_paramStartFlushThreshold. La distance entre le seuil de démarrage et le seuil d’arrêt affecte l’efficacité avec laquelle les pages de base de données sont vidées par le processus en arrière-plan. Un plus grand fossé rendra plus probable l’Association des écritures aux pages voisines. Toutefois, un seuil d’arrêt élevé réduit la taille effective du cache des pages de la base de données.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Property StopFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StopFlushThreshold

SystemParameters.StopFlushThreshold = value
```

``` csharp
public static int StopFlushThreshold { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[SystemParameters (classe)](./systemparameters-class.md)

[Membres SystemParameters](./systemparameters-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
