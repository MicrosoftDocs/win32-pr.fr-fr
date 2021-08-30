---
description: '\_Constantes personnalisées de paramètres régionaux \*'
ms.assetid: a41a7f55-8905-47a1-86c3-74ed40b3834c
title: Constantes LOCALE_CUSTOM *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc2bebc121ad2db797a2ff80b1fee925fc529cd3129ce6b906a579788789899
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106889"
---
# <a name="locale_custom-constants"></a>\_Constantes personnalisées de paramètres régionaux \*

Cette rubrique définit les \_ constantes personnalisées de paramètres régionaux \* utilisées par nls pour représenter des [paramètres régionaux personnalisés](custom-locales.md).



| Valeur                       | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| paramètres régionaux \_ personnalisés \_ par défaut     | **Windows Vista et versions ultérieures :** Paramètres régionaux personnalisés par défaut. Lorsqu’une fonction NLS doit retourner un identificateur de paramètres régionaux pour les [paramètres régionaux supplémentaires](custom-locales.md) de l’utilisateur actuel, la fonction retourne cette valeur au lieu des [paramètres régionaux \_ \_ par défaut](locale-user-default.md)de l’utilisateur. La valeur \_ par défaut personnalisée des paramètres régionaux \_ est 0x0C00.                                                                                                                                                                  |
| paramètres régionaux \_ \_ par défaut de l’interface utilisateur personnalisée \_ | **Windows Vista et versions ultérieures :** Paramètres régionaux personnalisés par défaut pour MUI. les langues d’interface utilisateur préférées de l’utilisateur et les langues d’interface utilisateur préférées du système peuvent inclure au maximum une seule langue implémentée par un Pack linguistique LIP (Language Interface Pack) (LIP) et pour lesquelles l’identificateur de langue correspond à des paramètres régionaux supplémentaires. S’il existe une telle langue dans une liste, la constante est utilisée pour faire référence à cette langue dans certains contextes. La valeur \_ par défaut de l' \_ interface utilisateur personnalisée locale \_ est 0x1400.                    |
| paramètres régionaux \_ personnalisés \_ non spécifiés | **Windows Vista et versions ultérieures :** Paramètres régionaux personnalisés non spécifiés, utilisés pour identifier tous les paramètres régionaux supplémentaires, à l’exception des paramètres régionaux de l’utilisateur actuel. Les paramètres régionaux supplémentaires ne peuvent pas être distingués les uns des autres par leurs identificateurs de paramètres régionaux, mais peuvent être distingués par leurs [noms de paramètres régionaux](locale-names.md). Certaines fonctions NLS peuvent retourner cette constante pour indiquer qu’elles ne peuvent pas fournir un identificateur utile pour des paramètres régionaux particuliers. La valeur des paramètres régionaux \_ personnalisés non \_ spécifiés est 0x1000. |



 

 

 



