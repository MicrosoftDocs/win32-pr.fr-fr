---
description: Chaque paramètre régional a un identificateur unique, une valeur de 32 bits qui se compose d’un identificateur de langue et d’un identificateur d’ordre de tri.
ms.assetid: ea45b0e5-7df7-47fb-8dad-fccfbe53fec0
title: Identificateurs de paramètres régionaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3607a1dcbc97505a604a4dd8358c93af9d7c614a44192826030a4430d31c839
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106729"
---
# <a name="locale-identifiers"></a>Identificateurs de paramètres régionaux

Chaque [paramètre régional](locales-and-languages.md) a un identificateur unique, une valeur de 32 bits qui se compose d’un [identificateur de langue](language-identifiers.md) et d’un [identificateur d’ordre de tri](sort-order-identifiers.md). L’identificateur de paramètres régionaux est une abréviation numérique internationale standard et contient les composants nécessaires pour identifier de manière unique l’un des paramètres régionaux définis par le système d’exploitation installés. NLS prend en charge les identificateurs de paramètres régionaux prédéfinis et les identificateurs personnalisés.

> [!Note]  
> les noms de paramètres régionaux peuvent être utilisés avec les fonctions introduites dans Windows Vista qui acceptent un [nom de paramètres régionaux](locale-names.md) en tant que paramètre, au lieu d’un identificateur de paramètres régionaux. Pour plus d’informations, consultez [appel des fonctions « nom des paramètres régionaux »](calling-the--locale-name--functions.md). L’utilisation de noms de paramètres régionaux au lieu des identificateurs de paramètres régionaux est toujours préférable.

 

L’illustration suivante montre le format des bits dans un identificateur de paramètres régionaux.

``` syntax
+-------------+---------+-------------------------+
|   Reserved  | Sort ID |      Language ID        |
+-------------+---------+-------------------------+
31         20 19     16 15                      0   bit
```

## <a name="predefined-locale-identifiers"></a>Identificateurs de paramètres régionaux prédéfinis

Les identificateurs de paramètres régionaux prédéfinis pris en charge par NLS sont définis dans les informations de référence sur l' [API NLS (National Language Support)](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

NLS utilise les constantes d’informations de paramètres régionaux suivantes pour représenter les identificateurs de paramètres régionaux.

-   [Paramètres \_ régionaux SLANGUAGE](locale-slanguage.md) ou [paramètres régionaux \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)
-   [paramètres régionaux \_ SNAME](locale-sname.md)
-   [paramètres régionaux \_ SSCRIPTS](locale-sscripts.md)
-   [paramètres régionaux \_ IDEFAULTANSICODEPAGE](locale-idefault-constants.md)

## <a name="custom-locale-identifiers"></a>Identificateurs de paramètres régionaux personnalisés

**Windows Vista :** NLS prend en charge les identificateurs de paramètres régionaux personnalisés représentés par les constantes d’informations de paramètres régionaux suivantes.

-   [paramètres régionaux \_ personnalisés \_ par défaut](locale-custom-constants.md)
-   [paramètres régionaux \_ \_ par défaut de l’interface utilisateur personnalisée \_](locale-custom-constants.md)
-   [paramètres régionaux \_ personnalisés \_ non spécifiés](locale-custom-constants.md)

## <a name="building-a-locale"></a>Génération de paramètres régionaux

Vous pouvez utiliser l’utilitaire locale Builder fourni par NLS pour créer des paramètres régionaux. Pour plus d’informations, consultez [Microsoft locale Builder](https://www.microsoft.com/download/details.aspx?id=41158).

Votre application peut créer un identificateur de paramètres régionaux à l’aide de la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) . Vous pouvez également utiliser l’un des identificateurs par défaut correspondant aux constantes listées ci-dessous.

-   [paramètres régionaux \_ INvariants](locale-invariant.md)
-   [paramètres régionaux \_ \_ par défaut du système](locale-system-default.md)
-   [paramètres régionaux \_ par défaut de l’utilisateur \_](locale-user-default.md)

## <a name="retrieval-of-locale-identifiers"></a>Récupération des identificateurs de paramètres régionaux

Une application peut récupérer les identificateurs de paramètres régionaux actuels à l’aide des fonctions [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) et [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) . Chaque thread peut définir et récupérer ses propres paramètres régionaux avec [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) et [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres régionaux et langues](locales-and-languages.md)
</dt> <dt>

[Identificateurs de langue](language-identifiers.md)
</dt> <dt>

[Noms de paramètres régionaux](locale-names.md)
</dt> <dt>

[Identificateurs d’ordre de tri](sort-order-identifiers.md)
</dt> <dt>

[**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid)
</dt> </dl>

 

 
