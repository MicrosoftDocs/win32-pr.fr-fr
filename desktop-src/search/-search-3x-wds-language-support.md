---
description: Cette rubrique décrit comment Windows Search prend en charge plusieurs langues.
ms.assetid: a800d2ac-3aee-4e74-a29a-a70355138ebc
title: Langues prises en charge par Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350a8861a5817a8ac5710214ccd35c780f2c9dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750436"
---
# <a name="languages-supported-by-windows-search"></a>Langues prises en charge par Windows Search

Cette rubrique décrit comment Windows Search prend en charge plusieurs langues.

## <a name="tokenization-wordbreakers-and-language-resources"></a>Jetons, séparateurs et ressources de langage

La recherche Windows est indépendante du langage, mais la précision de la recherche dans les différentes langues peut varier en raison de la façon dont séparateurs le texte de jeton. Séparateurs implémente diverses règles de création de jetons pour les langues et découpent le texte en jetons individuels, ou mots, à indexer ou Rechercher.

La langue du texte indexé et de la chaîne de requête est divisée en jetons. Étant donné que les règles de création de jetons varient selon la langue, il existe des séparateurs distincts pour chaque langue ou famille de langues. En cas de discordance entre le langage de requête et le langage indexé, les résultats peuvent être imprévisibles.

Windows Search est fourni avec un ensemble bien défini de séparateurs. Les composants de séparateur de formes classique et générateur de formes dérivées sont pris en charge dans Windows Vista et versions ultérieures. Si la langue d’un document ne peut pas être déterminée, Windows Search tente de détecter la langue pour identifier le séparateur de séparateur le plus approprié. Windows Search tente de détecter la langue en appelant la fonction [**GetSystemPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getsystempreferreduilanguages) pour déterminer la première langue de l’interface utilisateur (MUI) (généralement la langue de l’interface utilisateur système, sauf si les modules linguistiques MUI sont installés). Si cet appel a échoué, le séparateur de la première langue MUI est utilisé. Si l’appel à **GetSystemPreferredUILanguages** échoue, la recherche Windows récupère les paramètres régionaux système en appelant la fonction [**GetSystemDefaultLCID**](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlcid) et utilise le séparateur de paramètres associé à ces paramètres régionaux.

Si aucun séparateur n’est installé pour une langue, la recherche Windows s’arrête sur les espaces blancs à l’aide du séparateur de césure **neutre** .

Vous pouvez supprimer une langue par le biais du Registre, comme illustré dans l’exemple suivant.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            ContentIndex
               Language
                  Dutch_Dutch
                     (Default)
                     Locale
                     NoiseFile
                     StemmerClass = CLSID
                     WBreakerClass = CLSID
```

> [!TIP]
> Si vous apportez des modifications au registre, redémarrez Windows Search.

 

Lorsque la recherche Windows requiert un nouveau séparateur de points, l’identificateur de classe (CLSID) est lu et le séparateur de date instancié est mis en cache.

Vous pouvez créer un séparateur de passe personnalisé pour une langue en implémentant l’interface [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) . Windows Search appelle ensuite les méthodes **IWordBreaker** lors de la création d’index de contenu et d’exécution de requêtes.

Les informations de paramètres régionaux pour le contenu indexé sont extraites de la source du contenu. Si l’implémenteur source ne connaît pas les paramètres régionaux du contenu indexé, il doit définir les paramètres régionaux sur les paramètres [**régionaux \_ neutres**](../intl/locale-neutral.md).

Par exemple, si vous implémentez un gestionnaire de filtres (implémentation de l’interface [**IFilter**](https://www.bing.com/search?q=**IFilter**) ), un gestionnaire de propriétés ou un gestionnaire de protocole, vous devez définir les paramètres régionaux pour le contenu indexé sur des [**paramètres régionaux \_ neutres**](../intl/locale-neutral.md) , à moins que vous n’ayez des informations de paramètres régionaux spécifiques et que leur exactitude soit fiable.

> [!TIP]
> Si une requête d’index est basée sur l’entrée d’utilisateur, les paramètres régionaux doivent correspondre à la langue dans laquelle l’utilisateur tape. Vous pouvez déterminer ces paramètres régionaux en appelant la fonction [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) .

 

## <a name="languages-supported-by-wordbreakers"></a>Langues prises en charge par séparateurs

Windows Search comprend séparateurs pour prendre en charge les langues suivantes.



| Clé de Registre             | Langue (sous-langue)                            | LCID   |
|--------------------------|---------------------------------------------------|--------|
| **\_SaudiArabia arabe**  | Arabe (neutre)                                  | 0x0001 |
| **Bengali \_ par défaut**     | Bangla (neutre)                                  | 0x0045 |
| **Bulgare \_ par défaut**   | Bulgare (Bulgarie)                              | 0x0402 |
| **Catalan \_ par défaut**     | Catalan (Catalogne)                                 | 0x0403 |
| **Chinois \_ Hong Kong**    | Chinois (Hong Kong R.A.S., RPC)                      | 0x0C04 |
| **Chinois \_ simplifié**  | Chinois (simplifié)                              | 0x0804 |
| **Chinois \_ traditionnel** | Chinois (traditionnel)                             | 0x0404 |
| **Croate \_ par défaut**    | Croate (Croatie)                                | 0x041A |
| **\_Valeur tchèque par défaut**       | Tchèque (République tchèque)                            | 0x0405 |
| **\_Par défaut danois**      | Danois (Danemark)                                  | 0x0406 |
| **Néerlandais \_ néerlandais**         | Néerlandais (Pays-Bas)                               | 0x0413 |
| **Anglais ( \_ Royaume-Uni)**          | Anglais (Royaume-Uni)                          | 0x0809 |
| **Anglais ( \_ États-Unis)**          | Anglais (États-Unis)                           | 0x0409 |
| **Finnois \_ par défaut**     | Finnois (Finlande)                                 | 0x040B |
| **Français \_ français**       | Français (France)                                   | 0x040C |
| **Allemand \_ allemand**       | Allemand (Allemagne)                                  | 0x0407 |
| **Grec \_ par défaut**       | Grec (Grèce)                                    | 0x0408 |
| **Gujarati \_ par défaut**    | Goudjrati (Inde)                                  | 0x0447 |
| **Hébreu \_ par défaut**      | Hébreu (neutre)                                  | 0x000D |
| **Hindi \_ par défaut**       | Hindi (Inde)                                     | 0x0439 |
| **Hongrois \_ par défaut**   | Hongrois (Hongrie)                               | 0x040E |
| **Islandais \_ par défaut**   | Islandais (Islande)                               | 0x040F |
| **\_Par défaut indonésien**  | Indonésien (Indonésie)                            | 0x0421 |
| **Italien \_ Italien**     | Italien (Italie)                                   | 0x0410 |
| **\_Valeur japonaise par défaut**    | Japonais (Japon)                                  | 0x0411 |
| **\_Valeur par défaut kannada**     | Kannada (Inde)                                   | 0x044B |
| **Coréen \_ par défaut**      | Coréen (Corée)                                    | 0x0412 |
| **\_Valeur par défaut letton**     | Letton (Lettonie)                                  | 0x0426 |
| **\_Valeur par défaut lituanien**  | Lituanien (lituanien)                           | 0x0427 |
| **\_Malaisie Malaisie**      | Malais (Malaisie)                                  | 0x043E |
| **Malayalam \_ par défaut**   | Malayalam (neutre)                               | 0x004C |
| **\_Par défaut mamarathi**     | Marathi (Inde)                                   | 0x044E |
| **\_Bokmål norvégien**    | Norvégien (bokmål, Norvège)                        | 0x0414 |
| **Polonais \_ par défaut**      | Polonais (Pologne)                                   | 0x0415 |
| **Portugais ( \_ Portugal)** | Portugais (Portugal)                             | 0x0816 |
| **Portugais ( \_ Brésil)**   | Portugais (Brésil)                               | 0x0416 |
| **Pendjabi \_ par défaut**     | Pendjabi (Inde)                                   | 0x0446 |
| **Roumain \_ par défaut**    | Roumain (Roumanie)                                | 0x0418 |
| **\_Valeur russe par défaut**     | Russe (neutre)                                 | 0x0019 |
| **Serbe \_ cyrillique**    | Serbe (Serbie et Monténégro, ancien, cyrillique) | 0x0C1A |
| **Serbe \_ latin**       | Serbe (Serbie et Monténégro, ancien, latin)    | 0x081A |
| **\_Valeur par défaut slovaque**      | Slovaque (Slovaquie)                                 | 0x041B |
| **Slovène \_ par défaut**   | Slovène (Slovénie)                              | 0x0424 |
| **Espagnol \_ moderne**      | Espagnol (Espagne, moderne)                      | 0x0C0A |
| **Suédois \_ par défaut**     | Suédois (Suède)                                  | 0x041D |
| **Tamoul \_ par défaut**       | Tamoul (Inde)                                     | 0x0449 |
| **Télougou \_ par défaut**      | Télougou (Inde)                                    | 0x044A |
| **Thaï \_ par défaut**        | Thaï (Thaïlande)                                   | 0x041E |
| **Turc \_ par défaut**     | Turc (Turquie)                                  | 0x041F |
| **\_Valeur par défaut ukrainienne**   | Ukrainien (Ukraine)                               | 0x0422 |
| **Ourdou \_ par défaut**        | Ourdou (Pakistan)                                   | 0x0420 |
| **\_Valeur par défaut vietnamienne**  | Vietnamien (Vietnam)                              | 0x042A |



 

> [!Note]  
> Les LCID de certaines langues de la table sont générés à l’aide de l’identificateur de langue, de l’identificateur de sous-langue et de l’identificateur de tri.

 

Pour plus d’informations sur les langages et les identificateurs associés, consultez [constantes et chaînes](../intl/language-identifier-constants-and-strings.md)de l’identificateur de langue.

> [!Note]  
> Il n’y a aucune garantie que toutes ces clés de registre de langue seront présentes sur un ordinateur donné. Le séparateur de paramètres pour une langue donnée peut ou non être installé sur l’ordinateur en fonction des paramètres utilisateur.

 

À **compter de Windows 8.1**, la meilleure façon d’utiliser séparateurs est d’utiliser la [**classe WORDSSEGMENTER**](/uwp/api/Windows.Data.Text.WordsSegmenter?view=winrt-19041)de l’API WinRT.

## <a name="additional-resources"></a>Ressources supplémentaires

-   Pour plus d’informations sur la façon d’implémenter et d’utiliser des analyseurs lexicaux et des générateurs de formes dérivées personnalisés pour des langues et des paramètres régionaux supplémentaires, consultez [extension des ressources linguistiques dans Windows Search](extending-language-resources-in-windows-search.md).
-   Si vous devez identifier la langue d’un morceau de texte, vous pouvez utiliser la détection automatique de la langue (diagnostic Linux), qui est disponible dans Windows 7 et versions ultérieures. Pour plus d’informations, consultez [services linguistiques étendus](../intl/extended-linguistic-services.md) (ELS).
-   Pour plus d’informations sur la gestion, l’interrogation et l’extension de l’index, consultez le [Guide du développeur Windows Search](-search-developers-guide-entry-page.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble de Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Windows Search en tant que plateforme de développement](-search-3x-wds-development-ovr.md)
</dt> <dt>

[Utilisation de code managé avec Shell Data et Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
