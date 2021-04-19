---
description: Substituts et caractères supplémentaires
ms.assetid: 0dea39e2-a2b4-47fc-b44a-56af8ba1e346
title: Substituts et caractères supplémentaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8d6b738955c8b8de4f6cb0ae43c78f86752a928
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513391"
---
# <a name="surrogates-and-supplementary-characters"></a>Substituts et caractères supplémentaires

Les applications Windows utilisent normalement UTF-16 pour représenter des données de caractères [Unicode](unicode.md) . L’utilisation de 16 bits permet la représentation directe de 65 536 caractères uniques, mais ce plan multilingue de base (BMP) n’est pas assez proche pour couvrir tous les symboles utilisés dans les langues humaines. La version Unicode 4,1 comprend plus de 97 000 caractères, avec plus de 70 000 caractères pour le chinois seul.

La norme Unicode a établi 16 « plans » supplémentaires de caractères, chacun ayant la même taille que le BMP. Naturellement, la plupart des points de code au-delà du BMP n’ont pas encore de caractères qui leur sont affectés, mais la définition des plans donne au Unicode le potentiel de définir 1 114 112 caractères (autrement dit, 2 ¹ ⁶ \* 17 caractères) dans la plage de points de code u + 0000 à u + 10FFFF. Pour qu’UTF-16 représente ce plus grand ensemble de caractères, la norme Unicode définit des « caractères supplémentaires ».

## <a name="about-supplementary-characters"></a>À propos des caractères supplémentaires

Un caractère supplémentaire est un caractère situé au-delà du BMP, et un « substitut » est une valeur de code UTF-16. Pour le format UTF-16, une « paire de substitution » est requise pour représenter un caractère supplémentaire unique. Le premier substitut (élevé) est une valeur de code de 16 bits comprise entre U + D800 et U + DBFF. Le deuxième substitut (faible) est une valeur de code de 16 bits dans la plage U + DC00 et à U + DFFF. En utilisant le mécanisme de substitution, UTF-16 peut prendre en charge tous les 1 114 112 caractères Unicode potentiels. Pour plus d’informations sur les caractères supplémentaires, les substituts et les paires de substitution, reportez-vous à [la norme Unicode](https://www.unicode.org/standard/standard.html).

> [!Note]  
> Windows 2000 introduit la prise en charge de l’entrée, de la sortie et du tri simple des caractères supplémentaires. Toutefois, tous les composants système ne sont pas compatibles avec les caractères supplémentaires.

 

Le système d’exploitation prend en charge les caractères supplémentaires des manières suivantes :

-   Le format 12 de la table CMAP de police OpenType prend directement en charge le code de caractère de 4 octets. Pour plus d’informations, consultez [spécification de police OpenType](/typography/opentype/spec/).
-   Windows prend en charge les [éditeurs de méthode d’entrée (IME)](../dxtecharts/installing-and-using-input-method-editors.md)activés pour la substitution.
-   L’API [GDI Windows](../gdi/windows-gdi.md) prend en charge les tables de format 12 CMAP dans les polices afin que les substituts puissent être affichés correctement.
-   L’API [Uniscribe](uniscribe.md) prend en charge les caractères supplémentaires.
-   Les [contrôles Windows](../controls/window-controls.md), y compris les fonctionnalités de [modification](../controls/edit-controls.md) et de [modification enrichie](../controls/rich-edit-controls.md), prennent en charge les caractères supplémentaires.
-   Le moteur HTML prend en charge les pages HTML qui incluent des caractères supplémentaires pour l’affichage, la modification (via Outlook Express) et l’envoi de formulaires.
-   La table de tri du système d’exploitation prend en charge les caractères supplémentaires.

## <a name="general-guidelines-for-software-development-using-supplementary-characters"></a>Instructions générales pour le développement de logiciels à l’aide de caractères supplémentaires

UTF-16 gère les caractères supplémentaires comme des paires de substitution. Le système d’exploitation traite une paire de substitution de la même manière qu’il traite les [marques sans espace](using-nonspacing-characters-and-diacritics.md). Au moment de l’affichage, la paire de substitution s’affiche comme un glyphe au moyen de Uniscribe, comme stipulé par la norme Unicode.

Windows Vista introduit trois nouvelles macros pour aider à identifier les substituts et les paires de substitution dans les chaînes UTF-16. Il s' [**agit d’un \_ \_ substitut étendu**](/windows/win32/api/Winnls/nf-winnls-is_high_surrogate), d’un [**\_ \_ substitut faible**](/windows/win32/api/Winnls/nf-winnls-is_low_surrogate)et d’une [**\_ \_ paire de substitution**](/windows/win32/api/Winnls/nf-winnls-is_surrogate_pair).

Les applications prennent automatiquement en charge les caractères supplémentaires s’ils prennent en charge Unicode et utilisent des contrôles système et des fonctions API standard, telles que [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) et [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). Par conséquent, si votre application utilise des contrôles système standard ou utilise des appels de type [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)généraux à afficher, les caractères supplémentaires doivent fonctionner sans code spécial.

Les applications qui implémentent leur propre prise en charge de la modification en utilisant des positions de glyphes de manière personnalisée peuvent utiliser Uniscribe pour tout traitement de texte. Uniscribe a des fonctions distinctes pour gérer le traitement des scripts complexes, tels que l’affichage du texte, le test de positionnement et le déplacement du curseur. Une application doit appeler les fonctions Uniscribe spécifiquement pour bénéficier de ces fonctionnalités avancées. Notez que les applications qui utilisent les fonctions Uniscribe sont entièrement multilingues, mais cela impose une baisse des performances. Par conséquent, certaines applications doivent effectuer leur propre traitement de caractères supplémentaires.

Étant donné que le mécanisme de substitution pour représenter des caractères supplémentaires est bien défini, votre application peut inclure du code pour gérer le traitement du texte de substitution UTF-16. Lorsque l’application rencontre une valeur UTF-16 séparée de la plage de substitution réservée inférieure (un substitut faible) ou de la plage de substitution réservée supérieure (un substitut étendu), la valeur doit être une moitié d’une paire de substitution. Ainsi, l’application peut détecter une paire de substitution en procédant à une vérification de plage simple. Si elle rencontre une valeur UTF-16 dans la plage inférieure ou supérieure, elle doit suivre la largeur 1 16 bits vers l’arrière ou vers l’avant pour obtenir le reste du caractère. Lors de l’écriture de votre application, gardez à l’esprit que [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta) et [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva) se déplacent par des points de code 16 bits, et non par paires de substitution.

> [!Note]  
> Les points de code de substitution autonomes ont un substitut étendu sans substitut faible adjacent, ou vice versa. Ces points de code ne sont pas valides et ne sont pas pris en charge. Leur comportement n’est pas défini.

 

Si vous développez une police ou un fournisseur IME, Notez que les systèmes d’exploitation antérieurs à Windows XP désactivent la prise en charge des caractères supplémentaires par défaut. Windows XP et versions ultérieures activent les caractères supplémentaires par défaut. Si vous fournissez une police et un package IME qui requièrent des caractères supplémentaires, votre application doit définir les valeurs de Registre suivantes :


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\LanguagePack]
SURROGATE=(REG_DWORD)0x00000002

[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\International\Scripts\42]
IEFixedFontName=[Surrogate Font Face Name]
IEPropFontName=[Surrogate Font Face Name]
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Jeux de caractères](character-sets.md)
</dt> </dl>

 

 
