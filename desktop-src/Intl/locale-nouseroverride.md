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
# <a name="locale_nouseroverride"></a><span data-ttu-id="2e0dd-103">paramètres régionaux \_ NOUSEROVERRIDE</span><span class="sxs-lookup"><span data-stu-id="2e0dd-103">LOCALE\_NOUSEROVERRIDE</span></span>

> [!Caution]  
> <span data-ttu-id="2e0dd-104">Étant donné que \_ les paramètres régionaux NOUSEROVERRIDE désactive les préférences utilisateur, son utilisation est fortement déconseillée.</span><span class="sxs-lookup"><span data-stu-id="2e0dd-104">Since LOCALE\_NOUSEROVERRIDE disables user preferences, its use is strongly discouraged.</span></span> <span data-ttu-id="2e0dd-105">Cette constante ne garantit pas la stabilité des données dans la mesure où les [paramètres régionaux personnalisés](custom-locales.md), les mises à jour du service, les différentes versions de système d’exploitation et d’autres scénarios peuvent modifier les données de manière inattendue.</span><span class="sxs-lookup"><span data-stu-id="2e0dd-105">This constant does not guarantee data stability since [custom locales](custom-locales.md), service updates, different operating system versions, and other scenarios can change data in unexpected ways.</span></span> <span data-ttu-id="2e0dd-106">Pour plus d’informations, consultez [utilisation de données de paramètres régionaux persistants](using-persistent-locale-data.md).</span><span class="sxs-lookup"><span data-stu-id="2e0dd-106">For more information, see [Using Persistent Locale Data](using-persistent-locale-data.md).</span></span>

 

<span data-ttu-id="2e0dd-107">Aucun remplacement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2e0dd-107">No user override.</span></span> <span data-ttu-id="2e0dd-108">Dans plusieurs fonctions, par exemple, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) et [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), cette constante force la fonction à contourner tout remplacement d’utilisateur et à utiliser la valeur système par défaut pour toute autre constante spécifiée dans l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="2e0dd-108">In several functions, for example, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) and [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), this constant causes the function to bypass any user override and use the system default value for any other constant specified in the function call.</span></span> <span data-ttu-id="2e0dd-109">Les informations sont récupérées de la base de données locale, même si l’identificateur indique les paramètres régionaux actuels et si l’utilisateur a modifié certaines des valeurs à l’aide du panneau de configuration, ou si une application a modifié ces valeurs à l’aide de [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="2e0dd-109">The information is retrieved from the locale database, even if the identifier indicates the current locale and the user has changed some of the values using the Control Panel, or if an application has changed these values by using [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="2e0dd-110">Si cette constante n’est pas spécifiée, toutes les valeurs que l’utilisateur a configurées à partir du panneau de configuration ou qu’une application a configurées à l’aide de [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) sont prioritaires sur les paramètres de base de données pour les paramètres régionaux par défaut du système actuel.</span><span class="sxs-lookup"><span data-stu-id="2e0dd-110">If this constant is not specified, any values that the user has configured from the Control Panel or that an application has configured using [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) take precedence over the database settings for the current system default locale.</span></span>

 

 



