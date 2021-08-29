---
title: Duration
description: L’attribut duration contient la durée d’exécution du fichier, en unités de 100 nanosecondes.
ms.assetid: 1d72f826-4087-45f5-a5b9-f31c4e98e9b1
keywords:
- Durée Windows Media format
topic_type:
- apiref
api_name:
- Duration
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fc6b32d34249fbbe94e629b9fea6ae40d9627d100d3c337efd74d5a2d2773f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119085861"
---
# <a name="duration"></a>Duration

L’attribut **Duration** contient la durée d’exécution du fichier, en unités de 100 nanosecondes.

## <a name="global-constant"></a>Constante globale

\_wszWMDuration g

## <a name="data-type"></a>Type de données

**\_type WMT \_ QWord**

## <a name="remarks"></a>Remarques

Il s’agit d’un attribut codé.

Cet attribut ne peut pas être dupliqué au niveau du fichier. si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) de Format multimédia Windows.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




