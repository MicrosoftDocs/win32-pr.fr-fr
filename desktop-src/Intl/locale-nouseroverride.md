---
description: paramètres régionaux \_ NOUSEROVERRIDE
ms.assetid: ab68d16b-5e1e-4af3-b048-43975cded00a
title: LOCALE_NOUSEROVERRIDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28c2f59358bf71936e3a812c10e061d7a169387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527922"
---
# <a name="locale_nouseroverride"></a>paramètres régionaux \_ NOUSEROVERRIDE

> [!Caution]  
> Étant donné que \_ les paramètres régionaux NOUSEROVERRIDE désactive les préférences utilisateur, son utilisation est fortement déconseillée. Cette constante ne garantit pas la stabilité des données dans la mesure où les [paramètres régionaux personnalisés](custom-locales.md), les mises à jour du service, les différentes versions de système d’exploitation et d’autres scénarios peuvent modifier les données de manière inattendue. Pour plus d’informations, consultez [utilisation de données de paramètres régionaux persistants](using-persistent-locale-data.md).

 

Aucun remplacement de l’utilisateur. Dans plusieurs fonctions, par exemple, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) et [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), cette constante force la fonction à contourner tout remplacement d’utilisateur et à utiliser la valeur système par défaut pour toute autre constante spécifiée dans l’appel de fonction. Les informations sont récupérées de la base de données locale, même si l’identificateur indique les paramètres régionaux actuels et si l’utilisateur a modifié certaines des valeurs à l’aide du panneau de configuration, ou si une application a modifié ces valeurs à l’aide de [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Si cette constante n’est pas spécifiée, toutes les valeurs que l’utilisateur a configurées à partir du panneau de configuration ou qu’une application a configurées à l’aide de [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) sont prioritaires sur les paramètres de base de données pour les paramètres régionaux par défaut du système actuel.

 

 



