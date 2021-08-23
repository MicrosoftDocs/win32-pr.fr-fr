---
title: ControlTypeRequiredPatternNotSupported
description: ControlTypeRequiredPatternNotSupported
ms.assetid: D3DFB577-0F46-4598-A90F-C91A6A360AAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498d477ef06e369f0ebb14b370953914b37c7d124ed18bcdcb6042d8f27fb32e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614769"
---
# <a name="controltyperequiredpatternnotsupported"></a>ControlTypeRequiredPatternNotSupported

## <a name="text"></a>Texte

L’élément avec un ControlType de {0} doit prendre en charge, {1} mais ce n’est pas le cas de cet élément

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

La prise en charge d’UI Automation de l’élément n’est pas conforme à la spécification UI Automation, car l’élément doit prendre en charge la liste de modèles de contrôle fournie, mais ce n’est pas le cas. Par conséquent, cet élément peut ne pas être exposé correctement aux technologies d’assistance, ce qui peut avoir un impact sérieux sur l’expérience utilisateur.

## <a name="possible-causes"></a>Causes possibles

-   Implémentation d’UI Automation incomplète.
-   La propriété ControlType n’est pas définie correctement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




