---
description: Paramètres régionaux personnalisés
ms.assetid: 110efeab-c02f-4244-8950-a975cfc91e8a
title: Paramètres régionaux personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50108750fb1209aa210b04d8be9adcd48e5fd308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952818"
---
# <a name="custom-locales"></a>Paramètres régionaux personnalisés

**Windows Vista et versions ultérieures :** Les paramètres régionaux personnalisés prennent en charge des propriétés internationales qui fournissent une expérience utilisateur plus culturellement appropriée que celles fournies avec les paramètres régionaux standard fournis par Microsoft avec le système d’exploitation. L’utilisation de paramètres régionaux personnalisés permet aux administrateurs d’étendre l’ensemble de paramètres régionaux fournis par Microsoft ou de remplacer les données dans des paramètres régionaux fournis avec Windows, par exemple, les symboles monétaires ou les noms des mois de l’année.

Les deux types de paramètres régionaux personnalisés sont les paramètres régionaux supplémentaires et les paramètres régionaux de remplacement. Les paramètres régionaux supplémentaires sont des paramètres régionaux personnalisés qui permettent aux entreprises, aux universités, aux gouvernements et à d’autres tiers de créer des données de paramètres régionaux qui ne sont pas disponibles dans le système d’exploitation d’expédition. Les paramètres régionaux de remplacement sont des paramètres régionaux personnalisés fournis avec le système d’exploitation sans modification des [identificateurs](locale-identifiers.md) de paramètres régionaux ou des [noms de paramètres](locale-names.md)régionaux.

Vous pouvez utiliser l’utilitaire locale Builder fourni par NLS pour créer des paramètres régionaux personnalisés. Pour plus d’informations, consultez [Microsoft locale Builder](https://www.microsoft.com/download/details.aspx?id=41158). Les instructions relatives à l’utilisation de paramètres régionaux personnalisés dans vos applications sont fournies dans [utilisation de paramètres régionaux personnalisés](working-with-custom-locales.md).

## <a name="comparison-of-custom-locale-types"></a>Comparaison des types de paramètres régionaux personnalisés

Le tableau suivant décrit les différences entre les paramètres régionaux supplémentaires et les paramètres régionaux de remplacement.



| Élément                                                                                                                           | Paramètres régionaux supplémentaires                                                                                                                                                                                                                   | Paramètres régionaux de remplacement                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Calendriers                                                                                                                      | Peut inclure l’un des calendriers fournis par Microsoft. Au moins l’un des calendriers fournis doit être le calendrier localisé grégorien.                                                                                              | Peut inclure l’un des calendriers fournis par Microsoft. Au moins l’un des calendriers fournis doit être le calendrier localisé grégorien, et la collection doit inclure le calendrier par défaut des paramètres régionaux remplacés. |
| Tri                                                                                                                        | Peut utiliser n’importe lequel des tris fournis par Microsoft.                                                                                                                                                                                          | Conserve le comportement de tri des paramètres régionaux remplacés.                                                                                                                                                            |
| Noms des jours et des mois                                                                                                            | Peut être personnalisé uniquement pour le calendrier grégorien standard, et non pour les calendriers non grégoriens, et non pour les calendriers grégoriens spécialisés, tels que le calendrier grégorien du Moyen-Orient.                                           | Identique à pour les paramètres régionaux supplémentaires.                                                                                                                                                                                      |
| Nom de la langue ([paramètres régionaux \_ SLANGUAGE](locale-slanguage.md) ou [paramètres régionaux \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)) | Retourne les [paramètres régionaux \_ SNATIVELANGNAME](locale-snative-constants.md) ou [locale \_ SNATIVELANGUAGENAME](locale-snative-constants.md).                                                                                                       | Conserve le nom de langue des paramètres régionaux remplacés.                                                                                                                                                                 |
| Identificateur de paramètres régionaux                                                                                                              | Défini sur [paramètres régionaux \_ personnalisés \_ non spécifiés](locale-custom-constants.md) , sauf si les paramètres régionaux sont les normes et formats de paramètres régionaux actuellement sélectionnés par l’utilisateur. dans ce cas, il est défini sur [paramètres régionaux \_ personnalisés \_ par défaut](locale-custom-constants.md). | Conserve l’identificateur de paramètres régionaux des paramètres régionaux remplacés.                                                                                                                                                             |
| Nom des paramètres régionaux                                                                                                                    | Arbitraire doit correspondre au modèle abordé dans [noms de paramètres régionaux](locale-names.md).                                                                                                                                                      | Conserve le nom des paramètres régionaux des paramètres régionaux remplacés.                                                                                                                                                                   |



 

## <a name="supplemental-locale-examples"></a>Exemples de paramètres régionaux supplémentaires



| Nom des paramètres régionaux    | Description                                                                                                                                                                                                                                                                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en-Californie-fabricam | Fabricam est un fabricant de PC canadien avec des bureaux dans le monde entier. Pour fournir un comportement d’interface utilisateur cohérent pour tous ses ordinateurs, l’entreprise développe des paramètres régionaux pour utiliser l’ensemble de l’entreprise.                                                                                                                                                          |
| fr-US          | Woodlawn Bank utilise Windows XP Embedded pour ses distributeurs automatisés (DAB), que la Banque expédie sur Amérique du Nord avec des interfaces utilisateur en français, en anglais et en espagnol. Pour fournir une expérience cohérente, la Banque crée des paramètres régionaux pour le français dans le États-Unis qui a des formats de États-Unis, mais des noms de jours et de mois français. |



 

## <a name="replacement-locale-example"></a>Exemple de paramètres régionaux de remplacement



| Nom des paramètres régionaux | Description                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fr-FR       | Fabricam est un fabricant de PC canadien avec des bureaux dans le monde entier. Pour fournir un comportement d’interface utilisateur cohérent pour tous ses ordinateurs, l’entreprise développe des paramètres régionaux pour utiliser l’ensemble de l’entreprise. Elle utilise une horloge de 24 heures, mais se comporte sinon comme les paramètres régionaux anglais (États-Unis) pris en charge. Étant donné que les paramètres régionaux personnalisés sont similaires aux paramètres régionaux pris en charge, fabricam décide de les implémenter comme paramètres régionaux de remplacement au lieu de paramètres régionaux supplémentaires. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres régionaux et langues](locales-and-languages.md)
</dt> <dt>

[Utilisation de paramètres régionaux personnalisés](working-with-custom-locales.md)
</dt> </dl>

 

 



