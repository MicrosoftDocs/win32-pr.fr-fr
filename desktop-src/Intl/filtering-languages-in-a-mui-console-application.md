---
description: Une application console MUI peut prendre en charge les paramètres système ou les paramètres spécifiques à l’application pour ses langues d’interface utilisateur. Cette rubrique décrit le filtrage des langues pour ce type d’application.
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: Filtrage des langues dans une application console MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcdd8fc0f7f63b5771f5b75b86ce5e76ab2420d407832d77b731ad952174cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041319"
---
# <a name="filtering-languages-in-a-mui-console-application"></a>Filtrage des langues dans une application console MUI

Une application console MUI peut prendre en charge les paramètres système ou les paramètres spécifiques à l’application pour ses langues d’interface utilisateur. Cette rubrique décrit le filtrage des langues pour ce type d’application.

## <a name="limit-the-languages-to-display"></a>Limiter les langues à afficher

contrairement à une fenêtre graphique, la console Windows ne peut pas afficher des [scripts complexes](uniscribe-glossary.md), tels que l’arabe, l’hébreu, le persan, l’Hindi, l’ourdou, le thaï et bien d’autres. Par conséquent, la console ne peut en aucun cas afficher de nombreuses langues d’interface utilisateur.

La console peut afficher uniquement les caractères de la [page de codes OEM](code-pages.md) unique associée à la langue actuelle pour les applications non-Unicode. Pour chaque page de codes OEM, la console utilise une police particulière et cela peut ne pas fournir une couverture complète pour cette page de codes.

Ces limitations liées à la console réduisent le nombre de langues de l’interface utilisateur que la console peut afficher sur un ordinateur particulier. Par exemple, si la langue actuelle pour les applications non-Unicode est le japonais et que l’utilisateur essaie d’afficher du texte en allemand dans la console, les caractères avec les trémas ne s’affichent pas correctement. Si la langue actuelle pour les applications non-Unicode est l’allemand et que l’utilisateur souhaite afficher du texte en japonais dans la console, les résultats sont beaucoup pires, ce qui rend le texte presque incompréhensible.

> [!Note]  
> Lorsque vous fournissez une prise en charge de la console pour vos applications MUI, n’oubliez pas que la console fournit uniquement une prise en charge limitée des [éditeurs de méthode d’entrée](input-method-manager.md).

 

## <a name="set-the-language-for-console-output"></a>Définir la langue de la sortie de la console

sur Windows Vista et versions ultérieures, une application console définit la langue pour prendre en charge l’affichage de la console en appelant [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). Dans cet appel, l’application transmet le \_ filtre de la console MUI \_ dans le paramètre *DwFlags* et la **valeur null** pour *pwszLanguagesBuffer*. Une alternative consiste à appeler [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) avec un identificateur de langue de 0. Ce paramètre force la fonction à sélectionner la langue qui prend le mieux en charge l’affichage de la console.

sur Windows XP, l’application peut uniquement définir la langue de sortie de la console en appelant [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) avec un identificateur de langue de 0.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition des préférences linguistiques de l’application](setting-application-language-preferences.md)
</dt> </dl>

 

 
