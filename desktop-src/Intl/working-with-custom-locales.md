---
description: Cette rubrique fournit des instructions pour la gestion des paramètres régionaux personnalisés dans vos applications.
ms.assetid: 2622e2b3-b952-4666-a440-85d73d11c5e0
title: Utilisation de paramètres régionaux personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab0e59446496ae2985860c0fd6b1bd5bddde084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951470"
---
# <a name="working-with-custom-locales"></a>Utilisation de paramètres régionaux personnalisés

Cette rubrique fournit des instructions pour la gestion des [paramètres régionaux personnalisés](custom-locales.md) dans vos applications. Il est préférable de préparer l’ensemble de votre code source avec ces considérations à l’esprit, car votre application ne contrôle pas si les paramètres régionaux personnalisés sont installés sur le système d’exploitation.

## <a name="handle-locale_stime-constant-correctly"></a>Gérer correctement les paramètres régionaux \_ stime constant

Si vous disposez d’une application plus ancienne qui utilise [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) pour obtenir le séparateur d’heure obsolète indiqué par les [paramètres régionaux \_ stime](locale-stime-constants.md), l’application peut ne pas réussir à analyser le format d’heure. N’oubliez pas que le caractère qui sépare les heures des minutes est différent du caractère qui sépare les minutes des secondes.

> [!Note]  
> Lorsque vous programmez pour des paramètres régionaux personnalisés, n’oubliez pas qu’ils sont inhabituels. Pratiquement tous les champs disponibles dans NLS doivent faire face à un comportement inhabituel. Par exemple, le format d’heure 12H34 « 12 » est légitime et généralement compréhensible. Pourtant, de nombreuses applications font des hypothèses sur les séparateurs de temps qui peuvent rompre les longueurs de mémoire tampon ou afficher les champs.

 

## <a name="distinguish-among-supplemental-locales"></a>Faire la distinction entre les paramètres régionaux supplémentaires

Tous les paramètres régionaux supplémentaires utilisent la constante [ \_ personnalisée \_ non spécifiée de paramètres régionaux](locale-custom-constants.md) pour l’identificateur de [paramètres régionaux](locale-identifiers.md). En règle générale, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ne peut pas faire la distinction entre les paramètres régionaux supplémentaires, mais [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) peut être parce qu’il utilise des [noms de paramètres régionaux](locale-names.md) au lieu des identificateurs de paramètres régionaux. Votre application peut récupérer des informations sur un paramètre régional supplémentaire particulier uniquement lorsque ces paramètres régionaux sont les paramètres régionaux actuellement sélectionnés. Ensuite, l’application peut appeler [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) et passer l' [utilisateur de paramètres régionaux constants \_ \_ par défaut](locale-user-default.md) comme identificateur de paramètres régionaux.

## <a name="handle-replacement-locales"></a>Gérer les paramètres régionaux de remplacement

Pour préserver la fiabilité de Windows, n’oubliez pas qu’un paramètre régional de remplacement pris en charge par votre application ne peut pas modifier l’identificateur de paramètres régionaux des paramètres régionaux remplacés. Aucun des paramètres régionaux de remplacement ne peut modifier les propriétés de tri de Windows.

Bien qu’un paramètre régional de remplacement puisse modifier le calendrier par défaut, il doit conserver la valeur par défaut d’origine dans la liste des calendriers disponibles. Par exemple, les paramètres régionaux thaï (Thaïlande) utilisent le calendrier thaï bouddhiste comme valeur par défaut. Un administrateur peut créer des paramètres régionaux de remplacement qui utilisent le calendrier grégorien localisé. Toutefois, la liste des calendriers disponibles continue à contenir une entrée pour le calendrier thaï bouddhiste.

Pour les paramètres régionaux de remplacement, votre application doit généralement consulter les informations spécifiques aux paramètres régionaux au lieu de tenter un « raccourci » basé sur la connaissance d’un certain nombre de paramètres régionaux. Par exemple, lorsque [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) récupère les paramètres régionaux actuels en anglais (États-Unis), il peut en fait s’agir de paramètres régionaux de remplacement qui doivent être autorisés à prendre effet.

## <a name="customize-calendars"></a>Personnaliser les calendriers

Vos applications peuvent personnaliser les noms des jours et des mois pour les calendriers grégoriens, mais pas pour les calendriers non grégoriens. De même, NLS ne prend pas en charge la création de calendriers personnalisés définis par l’utilisateur. Pour plus d’informations, consultez [date et calendrier](date-and-calendar.md).

## <a name="handle-sorting-sequences"></a>Gérer les séquences de tri

Les paramètres régionaux supplémentaires peuvent utiliser n’importe quelle séquence de tri définie par Microsoft. Les paramètres régionaux de remplacement doivent utiliser la même séquence de tri que les paramètres régionaux qu’il remplace. NLS ne prend pas en charge la création de séquences de tri définies par l’utilisateur. Pour plus d’informations, consultez [gestion du tri dans vos applications](handling-sorting-in-your-applications.md).

## <a name="localize-custom-locale-information"></a>Localiser les informations de paramètres régionaux personnalisés

NLS ne fournit pas de mécanisme pour localiser les informations de paramètres régionaux personnalisés. Ainsi, les paramètres [régionaux \_ SLANGUAGE](locale-slanguage.md) ou les [paramètres régionaux \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md) utilisés comme identificateurs de paramètres régionaux pour les paramètres régionaux personnalisés récupèrent toujours les valeurs associées aux paramètres [régionaux \_ SNATIVELANGNAME](locale-snative-constants.md) ou [locale \_ SNATIVELANGUAGENAME](locale-snative-constants.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la prise en charge linguistique nationale](using-national-language-support.md)
</dt> <dt>

[Paramètres régionaux personnalisés](custom-locales.md)
</dt> <dt>

[Date et calendrier](date-and-calendar.md)
</dt> <dt>

[Gestion du tri dans vos applications](handling-sorting-in-your-applications.md)
</dt> </dl>

 

 



