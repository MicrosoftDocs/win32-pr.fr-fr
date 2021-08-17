---
description: Au fil du temps, différentes versions peuvent exister pour l’interface TAPI, les applications et les fournisseurs de services pour une ligne ou un téléphone.
ms.assetid: 36a17ae8-31db-4db9-a401-097d47aa26ad
title: Négociation de version TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cd6d816c07cb1c6c93d9cc219509f257d9a2695671b5197002171f0f819f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404064"
---
# <a name="tapi-version-negotiation"></a>Négociation de version TAPI

Au fil du temps, différentes versions peuvent exister pour l’interface TAPI, les applications et les fournisseurs de services pour une ligne ou un téléphone. Les nouvelles versions peuvent définir de nouvelles fonctionnalités, de nouveaux champs aux structures de données, et ainsi de suite. Les numéros de version indiquent donc comment interpréter diverses structures de données.

Pour permettre une interopérabilité optimale des différentes versions d’applications, des versions de l’interface TAPI elle-même et des versions de fournisseurs de services par différents fournisseurs, TAPI fournit un mécanisme de négociation de version simple et en deux étapes pour les applications. Deux versions différentes doivent être approuvées par l’application, l’interface TAPI et le fournisseur de services pour chaque périphérique de ligne. La première est le numéro de version pour la téléphonie de base et supplémentaire, et est appelée version d’API. L’autre est pour les extensions spécifiques au fournisseur, le cas échéant, et est appelée version de l’extension. Le format des structures de données et des types de données utilisés par les fonctionnalités de base et supplémentaires de l’interface TAPI est défini par la version de l’API, tandis que la version de l’extension détermine le format des structures de données définies par les extensions spécifiques au fournisseur.

La négociation de version se poursuit en deux phases. Dans la première phase, le numéro de version de l’API est négocié et l’identificateur d’extension associé aux extensions spécifiques au fournisseur prises en charge sur l’appareil est obtenu. Dans la deuxième phase, la version de l’extension est négociée. Si l’application n’utilise pas d’extensions d’API, elle ignore la deuxième phase et les extensions ne sont pas activées par le fournisseur de services. Si l’application souhaite utiliser des extensions, mais que les extensions du fournisseur de services (l’identificateur d’extension) ne sont pas reconnues par l’application, l’application doit également ignorer la négociation pour la version de l’extension. Chaque fournisseur dispose de son propre ensemble de versions juridiques (reconnues) pour chaque ensemble de spécifications d’extension qu’il distribue.

La fonction [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) est utilisée pour négocier le numéro de version de l’API à utiliser. Il récupère également l’identificateur d’extension pris en charge par le périphérique de ligne, en retournant des zéros si aucune extension n’est prise en charge. Avec cet appel de fonction, l’application fournit la plage de versions de l’API avec laquelle elle est compatible. TAPI à son tour négocie avec le fournisseur de services de la ligne pour déterminer la plage de versions d’API qu’il prend en charge. L’interface TAPI sélectionne ensuite un numéro de version (généralement, mais pas nécessairement, le numéro de version le plus élevé) dans la plage de versions qui se chevauche, que l’application, la DLL et le fournisseur de services ont fourni. Ce nombre est renvoyé à l’application, avec l’identificateur d’extension qui définit les extensions disponibles à partir du fournisseur de services de cette ligne.

Si l’application souhaite utiliser les extensions définies par l’identificateur d’extension retourné, elle doit d’abord appeler [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) pour négocier la version de l’extension. Dans une phase de négociation similaire, l’application spécifie la version d’API déjà convenue et la plage de versions d’extension qu’elle prend en charge. L’interface TAPI transmet ces informations au fournisseur de services de la ligne. Le fournisseur de services vérifie la version de l’API et la plage de versions d’extension par rapport à sa propre valeur, et sélectionne le numéro de version de l’extension appropriée, le cas échéant.

Lorsque l’application appelle ensuite [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps), elle retourne un ensemble de fonctionnalités d’appareil pour la ligne qui correspondent aux résultats de la négociation de version. Celles-ci incluent les fonctionnalités d’appareil de la ligne qui sont cohérentes avec la version de l’API et les fonctionnalités spécifiques à l’appareil de la ligne qui sont cohérentes avec la version de l’extension. L’application doit spécifier les deux numéros de version lors de l’ouverture d’une ligne. À ce stade, l’application, la DLL et le fournisseur de services s’engagent à utiliser les versions convenues. Si les extensions spécifiques à l’appareil ne sont pas à utiliser, la version de l’extension doit être spécifiée comme zéro.

Dans un environnement où plusieurs applications ouvrent le même périphérique de ligne, la première application à ouvrir le périphérique de ligne sélectionne les versions de toutes les futures applications qui souhaitent utiliser la ligne (les fournisseurs de services ne prennent pas en charge plusieurs versions simultanément). De même, une application qui ouvre plusieurs périphériques de ligne peut trouver plus facile d’utiliser tous les périphériques de ligne sous le même numéro de version d’API.

Chaque fonction qui accepte un paramètre *dwAPIVersion* ou similaire doit définir ce paramètre sur la version d’API la plus élevée prise en charge par l’application ou la version de l’API négociée à l’aide de la fonction [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) ou [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) sur un appareil particulier. Utilisez le tableau suivant comme guide :



| Fonction                                                     | Signification                                                                               |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)             | Utilisez la version retournée par [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineGetCountry**](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)                     | Utilisez la version la plus récente prise en charge par l’application.                                     |
| [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)                     | Utilisez la version retournée par [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineGetProviderList**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist)           | Utilisez la version la plus récente prise en charge par l’application.                                     |
| [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)         | Utilisez la version la plus récente prise en charge par l’application.                                     |
| [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)   | Utilisez la version la plus récente prise en charge par l’application.                                     |
| [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion)   | Utilisez la version retournée par [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)                                 | Utilisez la version retournée par [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)         | Utilisez la version la plus récente prise en charge par l’application.                                     |
| [**lineTranslateDialog**](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog)           | Utilisez la version la plus récente prise en charge par l’application.                                     |
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)                   | Utilisez la version retournée par [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Utilisez la version la plus récente prise en charge par l’application.                                     |
| [**phoneNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | Utilisez la version retournée par [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)                               | Utilisez la version retournée par [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |



 

> [!IMPORTANT]
> Lors de la négociation d’une version d’API, définissez toujours les numéros de version haute et basse sur la plage de versions que votre application peut prendre en charge. Par exemple, n’utilisez jamais 0x00000000 pour la version basse ou 0xFFFFFFFF pour la valeur élevée, car ces valeurs requièrent que votre application prenne en charge toutes les versions de TAPI, à la fois passées et futures.

 

 

 



