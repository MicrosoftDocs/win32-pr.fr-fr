---
title: Collection de compteurs (Isysmon. h)
description: Utilisez cette classe pour gérer la collection d’objets CounterItem. Pour récupérer cet objet, appelez SystemMonitor. Counters.
ms.assetid: 01542569-3fee-440a-8722-db377380b73c
keywords:
- Compteurs de collecte de compteurs
- Compteurs collection SysMon, Description
topic_type:
- apiref
api_name:
- Counters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8349c1425450491c3fc658f6ac1ac3c5fcf75d3e617a92f6e34b91f2f5802e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883336"
---
# <a name="counters-collection"></a>Compteurs, collection

Utilisez cette classe pour gérer la collection d’objets [**CounterItem**](counteritem.md) .

Pour récupérer cet objet, appelez [**systemmonitor. Counters**](systemmonitor-counters.md).

## <a name="members"></a>Membres

La collection de **compteurs** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La collection de **compteurs** possède ces méthodes.



| Méthode                            | Description                                                                           |
|:----------------------------------|:--------------------------------------------------------------------------------------|
| [**Complémentaires**](counters-add.md)       | Ajoute une instance [**CounterItem**](counteritem.md) à la collection.<br/>      |
| [**Installez**](counters-remove.md) | Supprime une instance [**CounterItem**](counteritem.md) de la collection.<br/> |



 

### <a name="properties"></a>Propriétés

La collection de **compteurs** possède ces propriétés.



| Propriété                                   | Description                                                                                         |
|:-------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Count**](counters-count.md)<br/> | Récupère le nombre d’instances de [**CounterItem**](counteritem.md) dans la collection.<br/>  |
| [**Élément**](counters-item.md)<br/>   | Récupère l’instance [**CounterItem**](counteritem.md) spécifiée de la collection.<br/> |



 

## <a name="remarks"></a>Remarques

L’objet **Counters** est la propriété par défaut de l’objet [**systemmonitor**](systemmonitor.md) .

Ajoutez à ce regroupement les compteurs que vous souhaitez représenter graphiquement. SYSMON récupère les valeurs de compteur à partir du système ou d’un fichier journal, en fonction de la [**source de données**](systemmonitor-datasourcetype.md) que vous spécifiez.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





