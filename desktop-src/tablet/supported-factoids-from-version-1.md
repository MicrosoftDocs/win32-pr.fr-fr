---
description: La plateforme Tablet PC prend en charge un certain nombre de Factoids qui sont utilisés pour augmenter la précision de la reconnaissance.
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: Factoids pris en charge à partir de la version 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c24c192bcbda04be7ea25deb0c7b1cb7b392de57c43ce7a509e0ceaac31002
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934349"
---
# <a name="supported-factoids-from-version-1"></a>Factoids pris en charge à partir de la version 1

\[notez que la description suivante du factoids pris en charge dans la version 1 du kit de développement logiciel (SDK) de Microsoft Windows XP Tablet PC Edition est toujours prise en charge par les module de reconnaissance, mais il est recommandé que tout nouveau développement (pour les logiciels de reconnaissance du script Latin) utilise les valeurs définies dans l’énumération [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) .\]

La plateforme Tablet PC prend en charge un certain nombre de Factoids qui sont utilisés pour augmenter la précision de la reconnaissance. Lors de l’utilisation de Factoids, il est important que l’entrée attendue corresponde exactement à la définition du Factoid. Si l’entrée ne correspond pas à la définition du Factoid, la précision de la reconnaissance en souffre. Par exemple, si le **nombre** Factoid est défini et que l’utilisateur entre des lettres, la précision de la reconnaissance pour les lettres est médiocre.

Certaines Factoids, telles que la **messagerie électronique** et les **chiffres**, sont presque identiques d’un langage à l’autre. D’autres Factoids, tels que **Telephone** et **PostalCode**, varient selon la langue. Examinez le format de chaque Factoid pour la langue que vous utilisez. Vous trouverez une liste de formats pour chaque Factoid dans chaque langue dans les tableaux des rubriques qui suivent cette rubrique.

> [!Note]  
> Il existe une distinction subtile mais importante entre Factoids pour les langues occidentales et Factoids pour les langues d’Extrême-Orient. Les Factoids pour les langues occidentales sont implémentées à l’aide d’expressions qui décrivent le résultat souhaité. Le module de reconnaissance est ensuite biaisé pour produire des résultats qui correspondent à cette expression. Factoids pour les langues d’Extrême-Orient sont implémentées en spécifiant une plage acceptable de caractères Unicode. Par exemple, la **Date** Factoid pour les langues d’Asie orientale accepte uniquement les caractères Unicode dans une certaine plage.

 

Factoids pour les langues occidentales inclut Factoids pour l’anglais (Royaume-Uni), l’anglais (États-Unis), le français, l’allemand et l’espagnol. Factoids pour les langues d’Extrême-Orient incluent Factoids pour le chinois (simplifié), le chinois (traditionnel), le japonais et le coréen.

Les sections suivantes présentent les formats pris en charge pour chaque Factoid dans chaque langue :

-   [Factoids commun dans plusieurs langues](factoids-common-across-languages.md)
-   [Factoids pour les langues occidentales](factoids-for-western-languages.md)
-   [Factoids pour les langues d’Extrême-Orient](factoids-for-east-asian-languages.md)

Si vous prévoyez une entrée différente des formats énumérés dans les tableaux de ces sections, n’utilisez pas de Factoid. En outre, les Factoids sont intégrés dans le module de reconnaissance pour chaque langue. Vous ne pouvez pas utiliser Factoids dans une langue avec un module de reconnaissance d’une autre langue. Par exemple, vous ne pouvez pas utiliser le Factoid **téléphonique** français avec un module de reconnaissance japonais.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Constantes Factoid**](factoid-constants.md)
</dt> <dt>

[Classe Microsoft. Ink. Factoid](/previous-versions/ms583657(v=vs.100))
</dt> </dl>

 

 
