---
description: L’objet Merge permet d’accéder à d’autres objets de niveau supérieur. Un objet de fusion doit être créé avant le chargement de la prise en charge d’Automation requise par COM pour accéder aux fonctions dans Mergemod.dll.
ms.assetid: 3f76ee8a-d195-4a69-99a3-31ef2c1c72d5
title: Objet Merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8382fd3c0b94e3e450d56a62fdd9d0a330cdd37fad72a6da926581b6336bc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869249"
---
# <a name="merge-object"></a>Objet Merge

L’objet **Merge** permet d’accéder à d’autres objets de niveau supérieur. Un objet de **fusion** doit être créé avant le chargement de la prise en charge d’Automation requise par com pour accéder aux fonctions dans Mergemod.dll.

Mergemod.dll permet d’accéder aux fonctionnalités étendues au moment de la génération par le biais d’une deuxième version du CLSID existant. Ce CLSID prend en charge les fonctionnalités existantes disponibles via l’interface [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) , mais l’interface par défaut sur l’objet (et l’interface double associée) est l’interface [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) au lieu de l’interface **IMsmMerge** .

 

 
