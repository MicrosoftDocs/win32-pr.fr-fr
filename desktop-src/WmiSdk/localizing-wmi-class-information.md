---
description: WMI implémente une technique qui permet de stocker plusieurs versions localisées de la même classe dans le référentiel.
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: Localisation des informations de classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9f1a7e34c3ba230655ebba4c070981a8dab901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320334"
---
# <a name="localizing-wmi-class-information"></a>Localisation des informations de classe WMI

WMI implémente une technique qui permet de stocker plusieurs versions localisées de la même classe dans le référentiel.

La définition de classe est divisée en versions suivantes :

-   Version indépendante du langage qui contient uniquement une définition de classe de base.
-   Version spécifique à un langage qui contient des informations localisées, telles que des descriptions de propriété spécifiques à des paramètres régionaux.

Les définitions de classe spécifiques à une langue sont stockées dans un espace de noms enfant sous l’espace de noms qui contient une définition de classe de base indépendante du langage.

Lorsque vous demandez une définition de classe localisée pour des paramètres régionaux spécifiques, WMI combine la définition de la classe de base et les informations de classe localisées pour former une classe localisée complète. Vous pouvez obtenir une version localisée d’une classe WMI en spécifiant des paramètres régionaux lorsque vous vous connectez à WMI et en définissant un indicateur qui indique que vous souhaitez des informations localisées. WMI fusionne ensuite les informations à partir des versions indépendantes du langage et des versions spécifiques à la langue de la définition de classe pour former une classe localisée.

Les classes WMI qui contiennent des informations localisées sont marquées avec le qualificateur d' **Amendement** et sont appelées classes modifiées ; une classe prend en charge les informations localisées si elle possède ce qualificateur. Vous pouvez déterminer les paramètres régionaux pour lesquels la classe a été localisée en recherchant un autre qualificateur appelé [**paramètres régionaux**](swbemobjectpath-locale.md). Le qualificateur de paramètres régionaux contient un identificateur de localisation (LCID Windows) qui identifie des paramètres régionaux. Par exemple, les paramètres régionaux pour l’anglais américain sont 0x40C. Si un qualificateur dans une classe modifiée contient des informations localisées, il contient la version de qualificateur **modifiée** .

La localisation WMI comprend les tâches suivantes :

-   [Création de définitions de classes localisées](creating-localized-class-definitions.md)
-   [Compilation des fichiers MOF localisés](compiling-localized-mof-files.md)
-   [Localiser des valeurs de propriété](localizing-property-values.md)
-   [Récupération des classes modifiées](retrieving-amended-classes.md)

Pour plus d’informations, consultez [Considérations sur les classes modifiées](amended-class-considerations.md).

 

 



