---
title: ControlTypeNoExpectedPatternsSupported
description: ControlTypeNoExpectedPatternsSupported
ms.assetid: 2C9CEFEA-8207-47A7-B100-A56CFBFB792D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c40f9f094589b312a033d6bdadf3fbf3b5020b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310161"
---
# <a name="controltypenoexpectedpatternssupported"></a>ControlTypeNoExpectedPatternsSupported

## <a name="text"></a>Texte

L’élément avec un ControlType de {0} doit prendre en charge au moins l’un de ces modèles : {1} mais cet élément ne le fait pas

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

La prise en charge d’UI Automation de l’élément n’est pas conforme à la spécification UI Automation, car l’élément doit prendre en charge au moins une des listes de modèles de contrôle fournies, mais ce n’est pas le cas. Par conséquent, cet élément peut ne pas être exposé correctement aux technologies d’assistance, ce qui peut avoir un impact sérieux sur l’expérience utilisateur.

## <a name="possible-causes"></a>Causes possibles

-   Implémentation d’UI Automation incomplète.
-   La propriété ControlType n’est pas définie correctement.

## <a name="remarks"></a>Notes

AccChecker enregistre ce message d’erreur pour une barre de progression indéterminée. Vous pouvez ignorer ce message et/ou l’ajouter à la liste des suppressions.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




