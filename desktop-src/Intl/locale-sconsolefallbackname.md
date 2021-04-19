---
description: paramètres régionaux \_ SCONSOLEFALLBACKNAME
ms.assetid: 36465a1c-085f-4f80-ad3d-5be6eaefe943
title: LOCALE_SCONSOLEFALLBACKNAME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09536167c68a4ec9156a1558960c48778019ae97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531992"
---
# <a name="locale_sconsolefallbackname"></a>paramètres régionaux \_ SCONSOLEFALLBACKNAME

**Windows Vista et versions ultérieures :** Paramètres régionaux par défaut à utiliser pour l’affichage de la console. Le nombre maximal de caractères autorisés pour cette chaîne est 85, y compris un caractère null de fin.

> [!Note]  
> En général, les applications ne doivent pas utiliser directement les \_ données locales SCONSOLEFALLBACKNAME. Pour déterminer les ressources de langue à utiliser dans une fenêtre de console, une application doit appeler [SetThreadUILanguage](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) ou [SetThreadPreferredUILanguages](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). Ces fonctions utilisent les données de secours de la console comme facteur de choix d’une langue lisible dans la console, mais ce n’est pas le seul déterminant. En particulier, la console est limitée à l’affichage des caractères à partir d’une page de codes unique. Par exemple, El-GR pour le grec (Grèce) est une langue de console valide, mais si la page de codes de la console actuelle est latin-1 (page de codes 1252), la console affiche le texte grec principalement comme une série de symboles de caractères introuvables.

 

Si la langue correspondant à ces paramètres régionaux est prise en charge dans la console, la valeur est la même que pour les [paramètres régionaux \_ sName](locale-sname.md), autrement dit, les paramètres régionaux peuvent être utilisés pour l’affichage de la console. Toutefois, la console ne peut pas afficher les langues qui peuvent être rendues uniquement avec [Uniscribe](uniscribe.md). Par exemple, la console ne peut pas afficher l’arabe ou les différentes langues indiennes. Par conséquent, les paramètres régionaux \_ SCONSOLEFALLBACKNAME pour les paramètres régionaux correspondant à ces langues diffèrent de la valeur de paramètres régionaux \_ sName.

Pour les paramètres régionaux prédéfinis, si la valeur de secours est différente de la valeur des paramètres régionaux lui-même, la valeur des paramètres régionaux neutres est utilisée. Les paramètres régionaux spécifiques sont associés à une langue et à un pays/région, tandis qu’un paramètre régional neutre est associé à une langue, mais n’est associé à aucun pays ou région. Par exemple, ar-SA revient à « fr », et non à « en-US ». Cette stratégie d’utilisation de paramètres régionaux neutres est implémentée de manière cohérente pour les paramètres régionaux prédéfinis et est fortement recommandée pour les paramètres régionaux personnalisés. Toutefois, la stratégie n’est pas appliquée. Pour les paramètres régionaux personnalisés, votre application peut utiliser des paramètres régionaux spécifiques au lieu de paramètres régionaux neutres comme secours.

> [!Note]  
> Aucune des fonctions décrites dans [appel des fonctions « nom des paramètres régionaux »](calling-the--locale-name--functions.md) n’accepte les paramètres régionaux neutres en tant qu’entrées. Par conséquent, les \_ données de SCONSOLEFALLBACKNAME de paramètres régionaux sont très limitées. En particulier, ni [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ni [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) n’acceptent les paramètres régionaux neutres comme entrées.

 

 

 



