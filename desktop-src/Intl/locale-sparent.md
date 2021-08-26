---
description: paramètres régionaux \_ sParent
ms.assetid: 3fa0bc36-7577-4b5a-b557-8ac42e8594a8
title: LOCALE_SPARENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11383e6fcdd216a1837d9f2f31e70a26821d394c3c56ea614b1df197bbe35c76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105919"
---
# <a name="locale_sparent"></a>paramètres régionaux \_ sParent

**Windows Vista et versions ultérieures :** Paramètres régionaux de secours, utilisés par le chargeur de ressources. Le nombre maximal de caractères autorisés pour cette chaîne est 85, y compris un caractère null de fin.

Les paramètres régionaux ont une hiérarchie dans laquelle le parent d’un paramètre régional spécifique est un paramètre régional neutre. Les paramètres régionaux spécifiques sont associés à une langue et à un pays/région, tandis qu’un paramètre régional neutre est associé à une langue, mais n’est associé à aucun pays ou région. Les paramètres régionaux parents sont utilisés pour décider du premier secours à essayer lorsqu’une ressource pour des paramètres régionaux spécifiques n’est pas disponible. Par exemple, les paramètres régionaux parents pour « en-US » (0x0409) sont « en » (0x0009). Lorsqu’une ressource n’est pas disponible pour les paramètres régionaux « en-US » spécifiques, le chargeur de ressources revient à utiliser la ressource qui est disponible pour les paramètres régionaux « en » neutres. Pour plus d’informations sur la stratégie de secours du chargeur de ressources, consultez Gestion de la langue de l' [interface utilisateur](user-interface-language-management.md) .

Ce modèle est cohérent pour les paramètres régionaux prédéfinis. Toutefois, les paramètres régionaux parents ne sont pas déterminés par les manipulations du nom des paramètres régionaux. Autrement dit, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) et [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) n’analysent pas une chaîne telle que « en-US » pour obtenir la valeur « fr ». Au lieu de cela, ils examinent les données des paramètres régionaux stockés. Pour les paramètres régionaux prédéfinis, la valeur suit le modèle attendu, dans lequel le parent des paramètres régionaux spécifiques correspond aux paramètres régionaux neutres correspondants et le parent des paramètres régionaux neutres correspond aux paramètres régionaux invariants. Bien qu’il soit recommandé que les paramètres régionaux personnalisés suivent une stratégie similaire en termes de définition de leurs paramètres régionaux parents, cela n’est pas appliqué. L’application qui implémente des paramètres régionaux personnalisés peut spécifier un parent approprié moins évidemment.

> [!Note]  
> Dans la mesure où aucune des fonctions décrites dans [appel des fonctions « nom des paramètres régionaux »](calling-the--locale-name--functions.md) n’accepte les paramètres régionaux neutres en tant qu’entrées, ces \_ données sParent sont très limitées. En particulier, ni [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ni [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) n’acceptent les paramètres régionaux neutres comme entrées.

 

 

 



