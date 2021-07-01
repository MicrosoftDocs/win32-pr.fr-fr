---
title: Obtention d’informations d’État
description: Obtention d’informations d’État
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, informations d’État
- OpenGL, variables d’État
- informations d’État OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8329fd34fc68122be8d63e4dc28756f88faf7797
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120684"
---
# <a name="obtaining-state-information"></a>Obtention d’informations d’État

OpenGL gère de nombreuses variables d’État qui affectent le comportement de nombreuses fonctions. Certaines de ces variables ont des fonctions de requête spécialisées.

:::row:::
    :::column:::
        [**glGetClipPlane**](glgetclipplane.md)
    :::column-end:::
    :::column:::
        [**glGetPixelMap**](glgetpixelmap.md)
    :::column-end:::
    :::column:::
        [**glGetTexImage**](glgetteximage.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetLight**](glgetlight.md)
    :::column-end:::
    :::column:::
        [**glGetPolygonStipple**](glgetpolygonstipple.md)
    :::column-end:::
    :::column:::
        [**glGetTexLevelParameter**](glgettexlevelparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetMap**](glgetmap.md)
    :::column-end:::
    :::column:::
        [**glGetTexEnv**](glgettexenv.md)
    :::column-end:::
    :::column:::
        [**glGetTexParameter**](glgettexparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetMaterial**](glgetmaterial.md)
    :::column-end:::
    :::column:::
        [**glGetTexGen**](glgettexgen.md)
    :::column-end:::
    :::column:::

    :::column-end:::
:::row-end:::

Pour obtenir la valeur d’autres variables d’État, utilisez [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md)ou [**glGetIntegerv**](glgetintegerv.md), selon le cas. Pour plus d’informations sur l’utilisation de ces fonctions, consultez [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) . Les autres fonctions de requête que vous pouvez utiliser sont [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md)et [**glIsEnabled**](glisenabled.md). (Pour plus d’informations sur les fonctions liées à la gestion des erreurs, consultez [gestion des erreurs](handling-errors.md) .) Pour enregistrer et restaurer des ensembles de variables d’État, utilisez [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md).

-   [Utilisation des fonctions de requête](using-the-query-functions.md)
-   [Gestion des erreurs](error-handling.md)
-   [Codes d’erreur OpenGL](opengl-error-codes.md)
-   [Enregistrement et restauration de jeux de variables d’État](saving-and-restoring-sets-of-state-variables.md)
-   [Variables d’État OpenGL](opengl-state-variables.md)
-   [Informations de référence sur l’État](state-information-reference.md)

 

 




