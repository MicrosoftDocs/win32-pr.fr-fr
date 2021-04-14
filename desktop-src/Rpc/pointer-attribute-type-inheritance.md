---
title: Héritage de type de Pointer-Attribute
description: Selon la spécification DCE, chaque fichier IDL doit définir des attributs pour ses pointeurs.
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182b7d46774484a9520424fd82bcff2d7103aa3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382496"
---
# <a name="pointer-attribute-type-inheritance"></a>Héritage de type de Pointer-Attribute

Selon la spécification DCE, chaque fichier IDL doit définir des attributs pour ses pointeurs. Si un attribut explicite n’est pas assigné à un pointeur, le pointeur utilise la valeur spécifiée par le \[ mot clé [ \_ par défaut du pointeur](/windows/desktop/Midl/pointer-default) \] . Certaines implémentations de DCE n’autorisent pas les pointeurs non attributs. Si un pointeur n’a pas d’attribut explicite, le fichier IDL doit avoir une spécification de **\[ pointeur \_ par défaut \]** afin que l’attribut de pointeur puisse être défini.

En mode par défaut (extensions Microsoft), vous pouvez spécifier l’attribut d’un pointeur dans le fichier IDL qui importe le fichier IDL de définition. Les pointeurs définis dans un fichier IDL peuvent hériter des attributs spécifiés dans d’autres fichiers IDL. En outre, dans le mode par défaut, les fichiers IDL peuvent inclure des pointeurs non attributs. Si ni la base ni les fichiers IDL importés ne spécifient un attribut de pointeur ou un **\[ pointeur \_ par défaut \]**, les pointeurs non attributs sont interprétés comme des pointeurs uniques.

Le compilateur MIDL assigne des attributs de pointeur aux pointeurs à l’aide des règles de priorité suivantes (1 est le plus élevé).



| Priority | Description                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| 1        | Les attributs de pointeur explicites sont appliqués au pointeur au niveau de la définition ou de l’utilisation du site.                                      |
| 2        | La valeur par défaut est l’attribut **\[ \_ par défaut \] du pointeur** dans le fichier IDL qui définit le type.                               |
| 3        | La valeur par défaut est l’attribut **\[ \_ par défaut \] du pointeur** dans le fichier IDL qui importe le type.                               |
| 4        | La valeur par défaut est \[ [ptr](/windows/desktop/Midl/ptr) \] dans le mode de compatibilité DCE, ou \[ [unique](/windows/desktop/Midl/unique) \] en mode extensions Microsoft. |



 

 

 