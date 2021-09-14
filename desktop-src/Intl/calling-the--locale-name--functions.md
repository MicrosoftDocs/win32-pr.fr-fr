---
description: Windows Vista introduit un grand nombre de fonctions qui utilisent des noms de paramètres régionaux plutôt que des identificateurs de paramètres régionaux.
ms.assetid: e88c31b2-b1da-40ae-b512-67b8ad409b95
title: Appel des fonctions « nom des paramètres régionaux »
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58c15d2d9fe7721eb162f8c7cf96084bd4afa2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240438"
---
# <a name="calling-the-locale-name-functions"></a>Appel des fonctions « nom des paramètres régionaux »

Windows Vista introduit un grand nombre de fonctions qui utilisent des [noms de paramètres régionaux](locale-names.md) plutôt que des [identificateurs de paramètres régionaux](locale-identifiers.md). Ces nouvelles fonctions offrent une bonne prise en charge des [paramètres régionaux supplémentaires](custom-locales.md), et plusieurs d’entre elles offrent des fonctionnalités supplémentaires non disponibles dans les anciennes fonctions nls. Certaines d’entre elles, telles que les nouvelles fonctions d’énumération, représentent également des améliorations de conception.

> [!Note]  
> les Applications qui sont destinées à s’exécuter uniquement sur Windows Vista et versions ultérieures doivent utiliser les fonctions « nom des paramètres régionaux » de préférence aux fonctions NLS qui utilisent des identificateurs de paramètres régionaux.

 

Le tableau suivant répertorie les fonctions des noms de paramètres régionaux, ainsi que les fonctions plus anciennes qu’elles peuvent remplacer.



| Fonctions utilisant des noms de paramètres régionaux                                     | Fonctions utilisant des identificateurs de paramètres régionaux                                                             |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)                       | [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)                                                         |
| [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)             | [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [ **EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) |
| [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)               | [**EnumDateFormats**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [ **EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)     |
| [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)               | [**EnumSystemLocales**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesa)                                                 |
| [**EnumTimeFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumtimeformatsex)                   | [**EnumTimeFormats**](/windows/desktop/api/Winnls/nf-winnls-enumtimeformatsa)                                                     |
| [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)                       | [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)                                                         |
| [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)                   | [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)                                                     |
| [**GetCurrencyFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getcurrencyformatex)               | [**GetCurrencyFormat**](/windows/desktop/api/Winnls/nf-winnls-getcurrencyformata)                                                 |
| [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)                       | [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)                                                         |
| [**GetDurationFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getdurationformatex)               | [**GetDurationFormat**](/windows/desktop/api/Winnls/nf-winnls-getdurationformat)                                                 |
| [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)                       | [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)                                                         |
| [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex)                       | [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion)                                                         |
| [**GetNumberFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getnumberformatex)                   | [**GetNumberFormat**](/windows/desktop/api/Winnls/nf-winnls-getnumberformata)                                                     |
| [**GetSystemDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) | [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid)                                           |
| [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex)                       | [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata)                                                         |
| [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename)     | [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid)                                               |
| [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)                   | [**IsValidLocale**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocale)                                                         |
| [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)                           | [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                                                             |



 

## <a name="example"></a>Exemple

Vous trouverez un exemple d’utilisation de plusieurs fonctions basées sur les noms de paramètres régionaux dans l' [exemple d’API nls : basée](nls--name-based-apis-sample.md)sur des noms.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la prise en charge linguistique nationale](using-national-language-support.md)
</dt> </dl>

 

 
