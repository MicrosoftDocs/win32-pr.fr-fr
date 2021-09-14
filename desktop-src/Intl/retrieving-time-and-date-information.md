---
description: Cette rubrique contient des instructions sur l’utilisation des fonctions NLS dans vos applications pour récupérer des informations de date et d’heure, ainsi que des données de durée. Si votre application doit rendre les données persistantes, consultez Utilisation de données de paramètres régionaux persistants.
ms.assetid: 1880ff8f-110c-4661-8b1f-afe1d8d2a38d
title: Récupération des informations de date et d’heure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2c2fa1d15de2c1ba5587a981373ff14b1c1c7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121897"
---
# <a name="retrieving-time-and-date-information"></a>Récupération des informations de date et d’heure

Cette rubrique contient des instructions sur l’utilisation des fonctions NLS dans vos applications pour récupérer des informations de [date et d’heure](time-and-date.md) , ainsi que des données de durée. Si votre application doit rendre les données persistantes, consultez [utilisation de données de paramètres régionaux persistants](using-persistent-locale-data.md).

**Windows Vista et versions ultérieures :** Les fonctions présentées dans cette rubrique peuvent récupérer des données de [paramètres régionaux personnalisés](custom-locales.md). En particulier, elles peuvent être utilisées pour personnaliser les formats de date et d’heure. Par exemple, il est possible d’avoir un format d’heure tel que « hhHmm’ss », ce qui génère des chaînes de temps comme « 12H34 » « 12 ».

## <a name="retrieve-time-information"></a>Récupérer les informations d’heure

Votre application peut obtenir des chaînes à tout moment dans un format approprié pour les paramètres régionaux actuels à l’aide des fonctions [**getTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) et [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) . L’une ou l’autre des fonctions vérifie chacune des valeurs d’heure dans une structure [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) valide pour déterminer qu’elle se trouve dans la plage de valeurs appropriée, en ignorant les parties de date de la structure. Si l’une des valeurs d’heure n’est pas comprise dans la plage correcte, la fonction échoue avec le paramètre erreur de code \_ non valide \_ . La fonction ne retourne aucune erreur pour une chaîne de format incorrecte, mais forme simplement la meilleure chaîne horaire possible.

> [!Note]  
> Les fonctions d’heure NLS n’incluent pas de millisecondes dans le cadre d’une chaîne de temps mise en forme.

 

Pour obtenir le format d’heure sans effectuer de mise en forme réelle, l’application peut utiliser la fonction [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) , en spécifiant la constante [ \_ sTimeFormat par des paramètres régionaux](locale-stime-constants.md) dans l’appel.

**Utiliser des marqueurs horaires**

Exemples d’indicateurs de temps : « AM » et « PM » pour l’anglais (États-Unis) et « de ». et « du ». pour l’espagnol (Mexique). Si TIME \_ NOTIMEMARKER est spécifié dans l’appel à [**getTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) ou [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex), la fonction supprime le ou les séparateurs qui précèdent et suivent le marqueur d’heure. Si un marqueur d’heure existe et que l' \_ indicateur NOTIMEMARKER n’est pas défini dans l’appel, la fonction localise le marqueur d’heure en fonction de l’identificateur de paramètres régionaux spécifié.

**Supprimer les séparateurs précédant les minutes et les secondes**

Votre application peut appeler [**getTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) ou [**GETTIMEFORMATEX**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) avec l’heure \_ NOMINUTESORSECONDS ou \_ les nosecondts de temps spécifiés pour supprimer les séparateurs qui précèdent les minutes et/ou les secondes.

**Utiliser le format 24 heures**

Si votre application prend en charge une heure au format 24 heures, elle peut appeler [**getTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) ou [**GETTIMEFORMATEX**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) avec l’heure \_ FORCE24HOURFORMAT. À moins que l' \_ indicateur Time NOTIMEMARKER ne soit défini, la fonction affiche tout marqueur d’heure existant.

## <a name="retrieve-date-information"></a>Récupérer les informations de date

Une application peut récupérer des chaînes pour toute date dans un format approprié pour les paramètres régionaux actuels à l’aide des fonctions [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) et [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) . L’une ou l’autre des fonctions vérifie chacune des valeurs de date année, mois, jour et jour de la semaine dans une structure [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) valide, en ignorant les portions heure de la structure. Le nom du jour, le nom du jour abrégé, le nom du mois et le nom du mois abrégé sont tous localisés en fonction de l’identificateur de paramètres régionaux. Si le jour de la semaine est incorrect, la fonction utilise la valeur correcte et ne retourne aucune erreur. Si l’une des autres valeurs de date n’est pas comprise dans la plage correcte, la fonction échoue avec le paramètre erreur de code \_ non valide \_ . La fonction ne retourne aucune erreur pour une chaîne de format incorrecte, mais forme simplement la meilleure chaîne de date possible.

Si l’application requiert le format de date pour un calendrier particulier, elle doit utiliser [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) ou [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex), en transmettant l' [**identificateur de calendrier**](calendar-identifiers.md)approprié. Pour retourner tous les formats de date d’un calendrier particulier, l’application peut utiliser [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)ou [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).

**Spécifier un autre calendrier**

L’application peut appeler [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) ou [**GETDATEFORMATEX**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) avec la date de l’indicateur \_ use \_ Alt \_ Calendar pour utiliser le format par défaut pour le calendrier de remplacement spécifié. S’il n’existe pas de format par défaut pour l’autre calendrier, la fonction utilise les remplacements de l’utilisateur.

Pour obtenir le format de date d’un autre calendrier, l’application peut utiliser [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) avec la constante [ \_ IOPTIONALCALENDAR locale](locale-ioptionalcalendar.md) .

**Spécifier le type de date**

Si l’application souhaite utiliser le format de date abrégé, elle spécifie \_ la date SHORTDATE dans l’appel à [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) ou [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex). Un format de date longue peut être obtenu en spécifiant \_ la date LONGDATE dans l’appel de fonction. Si aucun indicateur n’est spécifié et que *lpFormat* a la valeur **null**, la fonction utilise \_ la date SHORTDATE comme valeur par défaut.

Pour obtenir le format de date short et long pour le calendrier de paramètres régionaux par défaut, l’application doit utiliser la fonction [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) avec la constante [locale \_ SSHORTDATE](locale-sshortdate.md) ou [locale \_ SLONGDATE](locale-slongdate.md) .

**Spécifier l’image de format de date**

L’application peut spécifier une image de format de date que [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) ou [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) utilise pour former la chaîne de date. Si le format de date pour les paramètres régionaux spécifiés est requis, l’application peut appeler la fonction avec *lpFormat* ayant la valeur **null**. Si le paramètre n’a pas la valeur **null**, la fonction utilise les paramètres régionaux uniquement pour les informations non spécifiées dans la chaîne de format d’image, par exemple, les noms de jour et de mois des paramètres régionaux.

L’application peut placer tout texte qui doit rester dans sa forme exacte à l’intérieur de guillemets simples. Un guillemet simple peut également être utilisé comme caractère d’échappement pour permettre l’affichage de la marque elle-même dans la chaîne de date. Toutefois, la séquence d’échappement doit être placée entre deux guillemets simples. Par exemple, pour afficher la date sous la forme « 93 », la chaîne de format est : « MMMM » « ' 'AA ».

## <a name="retrieve-duration-information"></a>Récupérer les informations sur la durée

**Windows Vista et versions ultérieures :** Les fonctions [**GetDurationFormat**](/windows/desktop/api/Winnls/nf-winnls-getdurationformat) et [**GetDurationFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getdurationformatex) sont disponibles pour obtenir des formats de durée pour les paramètres régionaux, y compris des paramètres régionaux personnalisés. Pour obtenir le format de durée par défaut pour les paramètres régionaux, l’application doit utiliser la fonction [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) avec la constante [ \_ SDURATION locale](locale-sduration.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la prise en charge linguistique nationale](about-national-language-support.md)
</dt> <dt>

[Date et heure](time-and-date.md)
</dt> <dt>

[Utilisation des données de paramètres régionaux persistants](using-persistent-locale-data.md)
</dt> </dl>

 

 
