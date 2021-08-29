---
description: L’objet GetFiles récupère les fichiers nécessaires dans une langue particulière du module. Certaines actions doivent être effectuées par le biais de l’objet de fusion avant que toutes les parties de cette interface ne retournent des résultats valides.
ms.assetid: f3bf64ec-75f7-43a6-bbd8-a51508c57002
title: Objet GetFiles (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles
- IMsmGetFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c8e5848b04b5b87a09d43f1705c48c34adc13eb99017b14260f89357226750c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044239"
---
# <a name="getfiles-object"></a>GetFiles (objet)

L’objet **GetFiles** récupère les fichiers nécessaires dans une langue particulière du module. Certaines actions doivent être effectuées par le biais de l' [objet de fusion](merge-object.md) avant que toutes les parties de cette interface ne retournent des résultats valides.

## <a name="members"></a>Membres

L’objet **GetFiles** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **GetFiles** possède ces propriétés.



| Propriété                                               | Description                                                                                                                                                     |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ModuleFiles**](getfiles-modulefiles.md)<br/> | La propriété [**ModuleFiles**](getfiles-modulefiles.md) retourne toutes les clés primaires de la [table de fichiers](file-table.md) pour le module actuellement ouvert.<br/> |



 

## <a name="c"></a>C++

interface **IMsmGetFiles : IDispatch**

## <a name="interface-id"></a>ID d’interface



| Constante              | Valeur                                  |
|-----------------------|----------------------------------------|
| **IID \_ IMsmGetFiles** | {7041AE26-2D78-11D2-888A-00A0C981B015} |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




