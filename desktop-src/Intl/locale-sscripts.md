---
description: paramètres régionaux \_ SSCRIPTS
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb79f78626e7afb54229d8e0619e26d94250f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516912"
---
# <a name="locale_sscripts"></a>paramètres régionaux \_ SSCRIPTS

**Windows Vista et versions ultérieures :** Chaîne représentant une liste de scripts, à l’aide de la notation à 4 caractères utilisée dans [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html). Chaque nom de script se compose de quatre caractères latins et la liste est triée par ordre alphabétique avec chaque nom, y compris le dernier, suivi d’un point-virgule.

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) peut être appelé avec *LCTYPE* défini sur locale \_ SSCRIPTS dans le cadre d’une stratégie visant à limiter les problèmes de sécurité liés aux noms de domaine internationaux (IDNs). Voici quelques exemples de valeurs :



| Paramètres régionaux                  | Nom de paramètres régionaux/langue | Valeur                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| Anglais (États-Unis) | fr-FR                | LATN                                                                                                  |
| Hindi (Inde)           | hi-IN                | Deva                                                                                                  |
| Japonais (Japon)        | ja-JP                | **Windows 7 et versions ultérieures :** Hani; Hira; Jpan; Caractères Kana<br/> **Windows Vista :** Hani; Hira; Caractères Kana<br/> |



 

Une valeur de script composé n’inclut pas le script latin, sauf s’il s’agit d’une partie essentielle du système d’écriture utilisé pour les paramètres régionaux spécifiques. Les caractères latins sont souvent utilisés dans le contexte des paramètres régionaux pour lesquels ils ne sont pas natifs, par exemple, pour un nom d’entreprise étranger. Dans l’exemple ci-dessus pour l’hindi en Inde, la seule valeur de script est « Deva » (pour « DÉVANÂGARÎ »), bien que les caractères latins puissent également apparaître dans le texte hindi. La fonction [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) a un indicateur spécial pour traiter ce cas.

 

 




