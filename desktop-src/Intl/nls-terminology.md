---
description: Cette rubrique définit les termes importants lorsque vous utilisez la fonctionnalité NLS.
ms.assetid: daf929b2-8ff9-4a17-b294-f2c0eaef5848
title: Terminologie NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f83ed44b0ba8be3022721148b688f62379e57f7189ff006a0d9255413e31976
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040799"
---
# <a name="nls-terminology"></a>Terminologie NLS

Cette rubrique définit les termes importants lorsque vous utilisez la fonctionnalité NLS.

## <a name="locale-and-language-terms"></a>Paramètres régionaux et termes de la langue

Le tableau suivant récapitule les paramètres régionaux et les termes de la langue. Voir aussi [paramètres régionaux et langues](locales-and-languages.md).



|                          | Groupe de langues                                                                                                                                                                                                                                                                   | Langue pour les programmes non Unicode                                                                                                                                                                                                                | Normes et formats                                                                                                                                                                                                                   |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Objectif**              | Fournit toutes les dispositions du clavier, les éditeurs de méthode d’entrée (IME), les polices TrueType, les liens de police, les fichiers de package de licence (LPKs), les polices bitmap et les tables de traduction de page de codes nécessaires au système d’exploitation pour un groupe de langues. Affecte donc tous les autres paramètres de cette liste. | Détermine les polices bitmap et les pages de codes OEM, ANSI et Macintosh qui sont des valeurs par défaut pour le système d’exploitation. Cette langue affecte uniquement les applications qui ne sont pas entièrement Unicode. avant Windows XP, cette langue était appelée « paramètres régionaux système ». | Détermine les paramètres qui sont utilisés pour mettre en forme les dates, les heures, les devises et les nombres comme valeur par défaut pour chaque utilisateur. Détermine également l’ordre de tri pour le tri du texte. avant Windows XP, les normes et les Formats étaient appelés « paramètres régionaux de l’utilisateur ». |
| **Premier jeu**            | Installation                                                                                                                                                                                                                                                                     | Installation                                                                                                                                                                                                                                     | Installation                                                                                                                                                                                                                            |
| **Comment les utilisateurs peuvent changer** | Options régionales (élément du panneau de configuration)<br/> **Windows XP :** Options régionales et linguistiques<br/> (administrateurs uniquement)<br/>                                                                                                                                       | Options régionales (élément du panneau de configuration)<br/> **Windows XP :** Options régionales et linguistiques<br/> (administrateurs uniquement)<br/>                                                                                                       | Options régionales (élément du panneau de configuration)<br/> **Windows XP :** Options régionales et linguistiques<br/>                                                                                                                               |
| **Par défaut**              | Europe de l’Ouest et États-Unis et groupe de langues requis pour afficher la langue d’une version localisée.                                                                                                                                                                         | Langue de la version localisée.                                                                                                                                                                                                                   | Langue du système d’exploitation localisé.                                                                                                                                                                                                 |
| **Fonction**             | [**EnumSystemLanguageGroups**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlanguagegroupsa)                                                                                                                                                                                                                     | [**GetSystemDefaultLangID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlangid)                                                                                                                                                                                         | [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid), [ **GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename)                                                                                                                          |



 



|                          | Paramètres régionaux de thread                                                                                                                                                 | Langue d’entrée                                                                                            | Langue de l’interface utilisateur par défaut du système                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Objectif**              | Détermine les paramètres qui sont utilisés pour mettre en forme les dates, les heures, les devises et les nombres importants pour un thread. Détermine également l’ordre de tri pour le tri du texte. | Se compose d’un langage et d’une méthode d’entrée.                                                             | Détermine la langue par défaut des menus et des boîtes de dialogue, des messages, des fichiers d’informations d’installation (INF) et des fichiers d’aide.<br/> **Windows Vista et versions ultérieures :** Appelée langue d’installation. Joue un rôle plus limité, largement remplacé par les langues d’interface utilisateur préférées du système.<br/> Pour plus d’informations, consultez Gestion de la langue de l' [interface utilisateur](user-interface-language-management.md) .<br/> |
| **Premier jeu**            | Normes et formats par défaut                                                                                                                              | Installation                                                                                              | Installation                                                                                                                                                                                                                                                                                                                                                                                   |
| **Comment les utilisateurs peuvent changer** | [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)                                                                                                                    | Options régionales (élément du panneau de configuration)<br/> **Windows XP :** Options régionales et linguistiques<br/> | Non                                                                                                                                                                                                                                                                                                                                                                                             |
| **Par défaut**              | Normes et formats                                                                                                                                         | Langue de la version localisée avec la méthode d’entrée par défaut.                                                  | Langue de la version localisée.                                                                                                                                                                                                                                                                                                                                                                 |
| **Fonction**             | [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale)                                                                                                                    | [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)                                                     | [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)                                                                                                                                                                                                                                                                                                                               |



 



|                          | Langue de l’interface utilisateur système, langues de l’interface utilisateur par défaut du système                                                                                                                                                                  | Langue de l’interface utilisateur de l’utilisateur, langues d’interface utilisateur préférées                                                                                                                                               | Langues de l’interface utilisateur préférée du thread                                                                                                                                                                 |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Objectif**              | Déterminez la langue des menus et des boîtes de dialogue, des messages, des fichiers INF et des fichiers d’aide pour le système d’exploitation. Pour plus d’informations, consultez Gestion de la langue de l' [interface utilisateur](user-interface-language-management.md). | Déterminez la langue des menus, des boîtes de dialogue, des messages et des fichiers d’aide pour l’utilisateur. Pour plus d’informations, consultez Gestion de la langue de l' [interface utilisateur](user-interface-language-management.md). | **Windows Vista et versions ultérieures :** Spécifiez les langues préférées pour les threads d’application. Pour plus d’informations, consultez Gestion de la langue de l' [interface utilisateur](user-interface-language-management.md). |
| **Premier jeu**            | Valeur par défaut NULL                                                                                                                                                                                                    | Valeur par défaut NULL                                                                                                                                                                             | Valeur par défaut NULL                                                                                                                                                                               |
| **Comment les utilisateurs peuvent changer** | Options régionales et linguistiques<br/> (administrateurs uniquement)<br/>                                                                                                                                          | Options régionales (élément du panneau de configuration)<br/> **Windows XP :** Options régionales et linguistiques<br/>                                                                                   | [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)                                                                                                                        |
| **Par défaut**              | **Windows Vista et versions ultérieures :** Langue de la version localisée, suivie de tout secours.                                                                                                                             | **avant Windows Vista :** Langue de la version localisée.<br/> **Windows Vista et versions ultérieures :** Langue de la version localisée, suivie de tout secours.<br/>                     | Liste de valeurs null                                                                                                                                                                                     |
| **Fonction**             | [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)                                                                                                                                             | [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage), [ **GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)                                                            | [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)                                                                                                                        |



 



|                          | Traiter les langues d’interface utilisateur préférées                                                                                                                                                                 |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Objectif**              | **Windows 7 et versions ultérieures :** Déterminer les langues préférées pour un processus d’application. Pour plus d’informations, consultez Gestion de la langue de l' [interface utilisateur](user-interface-language-management.md). |
| **Premier jeu**            | Valeur par défaut NULL                                                                                                                                                                                |
| **Comment les utilisateurs peuvent changer** | Options régionales et linguistiques (uniquement les administrateurs)                                                                                                                                            |
| **Par défaut**              | **Windows 7 et versions ultérieures :** Langue de la version localisée, suivie de tout secours.                                                                                                             |
| **Fonction**             | [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages), [ **SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages)                                             |



 

## <a name="code-page"></a>Page de codes

L’incapacité des pages de codes de point de code 256 pour prendre en charge le mélange de scripts dans un seul texte était l’une des principales raisons de la montée en Unicode. les pages de codes restent importantes pour l’écriture de code de console, pour gérer des applications héritées ou s’exécuter sur des versions antérieures de Windows, et pour l’interfaçage avec certains logiciels non-Microsoft qui ne sont pas compatibles Unicode.

## <a name="input-language"></a>Langue d’entrée

La langue d’entrée est représentée par une variable de données par processus qui décrit une langue (par exemple, le grec) et une méthode d’entrée (par exemple, le clavier). Plusieurs langues d’entrée peuvent être installées et l’utilisateur peut basculer entre elles.

Pour définir et récupérer la valeur de la langue d’entrée, l’application appelle [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) et [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout), respectivement. Les utilisateurs peuvent ajouter et supprimer des langues d’entrée via l’onglet **langues** de la section Options régionales et linguistiques du panneau de configuration.

La langue d’entrée par défaut est la langue localisée du système d’exploitation et il s’agit du paramètre qui est actif au démarrage d’une nouvelle application (ou lorsqu’une nouvelle fenêtre est ouverte pour certaines applications). Le passage à un autre langage d’entrée est effectué pour chaque application. En d’autres termes, deux langues d’entrée différentes peuvent être utilisées dans deux applications différentes. Par exemple, un utilisateur peut taper allemand à l’aide de la disposition du clavier international États-Unis, de l’anglais à l’aide d’une entrée vocale (avec des logiciels non-Microsoft) et de l’espagnol à l’aide d’un IME dans trois applications différentes.

## <a name="language-for-non-unicode-programs"></a>Langue pour les programmes non-Unicode

La langue des programmes non-Unicode (autrefois appelée « paramètres régionaux système ») détermine la page de codes utilisée par défaut sur le système d’exploitation. Le paramètre langue pour les programmes non-Unicode affecte uniquement les applications non-Unicode, autrement dit, les applications ANSI. la définition de la langue indique à Windows d’émuler un système d’exploitation non-Unicode, localisé dans cette langue. La modification de la langue des programmes non-Unicode installe les fichiers de police bitmap nécessaires pour prendre en charge les applications non-Unicode dans la langue spécifiée. Pour permettre à l’utilisateur de sélectionner une langue pour des programmes non-Unicode, le groupe de langues approprié doit être installé. Votre application a besoin de la prise en charge des scripts pour sélectionner une langue pour les programmes non-Unicode. La langue des programmes non-Unicode est un paramètre par système qui nécessite un redémarrage pour être implémenté.

Il n’existe parfois aucune différence notable entre deux langages pour les programmes non-Unicode. Par exemple, c’est le cas avec les paramètres régionaux allemand (neutre) et allemand (Autriche). En général, les paramètres d’un groupe de langues sont très similaires et diffèrent uniquement dans la page de codes OEM ou MAC.

Une application ANSI doit vérifier le paramètre langue pour les programmes non-Unicode au cours de l’installation. Elle utilise [**GetACP**](/windows/desktop/api/Winnls/nf-winnls-getacp) ou [**GetOEMCP**](/windows/desktop/api/Winnls/nf-winnls-getoemcp) pour récupérer la valeur. Aucune fonction n’est prise en charge pour définir la langue des programmes non-Unicode. Toutefois, les utilisateurs peuvent le modifier à l’aide de l’onglet **avancé** de la section Options régionales et linguistiques du panneau de configuration. Voici quelques exemples de langue pour les paramètres de programmes non-Unicode :

1.  un utilisateur allemand qui souhaite exécuter une application japonaise conçue pour le japonais Windows 95 doit sélectionner le japonais comme langue pour les programmes non-Unicode. Après cette sélection, les applications allemandes non-Unicode rencontrent des problèmes. Par exemple, les trémas allemands (̈) ne s’affichent pas correctement.
2.  Un utilisateur allemand qui souhaite taper du texte japonais dans une application allemande non Unicode doit sélectionner le japonais comme langue pour les programmes non-Unicode. Comme dans le premier exemple, cela entraîne des problèmes lors de l’entrée de texte en allemand dans des applications non-Unicode.
3.  Un utilisateur arabe qui souhaite taper l’arabe, le français et l’anglais dans une application arabe non Unicode doit sélectionner l’arabe comme langue pour les programmes non-Unicode, car la page de codes ANSI ANSI contient la plupart des caractères français et tous les caractères anglais.

## <a name="language-group"></a>Groupe de langues

Le groupe de langues contrôle la langue des programmes non-Unicode, les standards et formats, les langues d’entrée et les langues d’interface utilisateur qui peuvent être sélectionnés. Pour chaque version localisée, le groupe de langues spécifié est la valeur par défaut et ne peut pas être supprimé. par exemple, Windows installe par défaut le groupe europe de l’ouest et États-Unis langue. ainsi, si la version anglaise de Windows est installée dans un pays/une région qui n’est pas anglophone, l’utilisateur installe généralement un autre groupe de langues.

lorsque vous ajoutez un groupe de langues, Windows copie (mais n’active pas) les fichiers de clavier nécessaires, les éditeurs de méthode d’entrée (ime), les fichiers de police TrueType, les fichiers de police bitmap et les fichiers de prise en charge linguistique nationale (. nls). L’ajout d’un groupe de langues ajoute également des valeurs de Registre pour la liaison des polices et installe les moteurs de script pour les langages de script complexes (arabe, hébreu, Indo-aryen et thaï).

En plus de l’Europe de l’Ouest et États-Unis groupe de langues, il existe 16 autres groupes de langues :



<table>
<tbody>
<tr class="odd">
<td><dl> Arabe<br />
Arménien<br />
Balte<br />
Europe centrale<br />
Cyrillique<br />
Géorgien<br />
Grec<br />
Hébreu<br />
</dl></td>
<td><dl> Aryenne<br />
Japonais<br />
Coréen<br />
Chinois simplifié<br />
Chinois traditionnel<br />
Thaï<br />
Turc<br />
Vietnamien<br />
</dl></td>
</tr>
</tbody>
</table>



 

Un nombre et une combinaison de groupes de langues peuvent être installés sur n’importe quel système d’exploitation. Par exemple, un utilisateur espagnol peut installer le groupe de langues cyrilliques pour travailler sur des textes russes. Dans ce cas, une application de traitement de texte doit également prendre en charge le groupe de langues cyrilliques.

> [!Note]  
> L’ajout du groupe de langues approprié n’autorise pas automatiquement une application à accepter du texte. Il est recommandé d’effectuer des tests. Par exemple, les applications non-Unicode peuvent nécessiter la modification de la langue des programmes non-Unicode.

 

## <a name="location"></a>Emplacement

**Windows XP :** Un emplacement est un identificateur géographique. Elle est représentée par une variable de données par utilisateur qui définit le pays ou la région où l’utilisateur vit.

Pour définir la valeur, l’application appelle [**SetUserGeoID**](/windows/desktop/api/Winnls/nf-winnls-setusergeoid). Pour récupérer la valeur, l’application appelle [**GetUserGeoID**](/windows/desktop/api/Winnls/nf-winnls-getusergeoid).

## <a name="standards-and-formats"></a>Normes et formats

Normes et formats (anciennement « User locale ») est une variable par utilisateur qui détermine l’ordre de tri par défaut et les paramètres par défaut pour la mise en forme des dates, des heures, des devises et des nombres. La variable est présentée sous la forme d’une langue (parfois associée à un pays ou une région), mais elle n’est pas elle-même une langue. Par exemple, la définition de la variable standards et formats sur Hébreu indique que l’utilisateur souhaite utiliser les conventions de mise en forme de l’hébreu, pas nécessairement la langue de l’hébreu. En outre, la variable standards et formats détermine la chaîne utilisée pour les noms de jours et de mois. Par exemple, si un utilisateur affiche « 25 novembre 1998 », la chaîne « novembre » peut changer en fonction de la variable standards et formats. La modification de la variable ajoute automatiquement des paramètres régionaux d’entrée avec les paramètres par défaut de la langue.

Pour connaître le paramètre de variable standards et formats, l’application appelle [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) ou [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename). Aucune fonction NLS n’est disponible pour définir la variable. Toutefois, les utilisateurs peuvent le modifier par le biais de l’onglet options de la **région** dans la partie Options régionales et linguistiques du panneau de configuration.

Une application doit généralement utiliser les paramètres standards et formats des variables pour afficher les données. Toutefois, une application qui utilise des paramètres régionaux fixes pour afficher les données doit passer un identificateur de paramètres régionaux spécifique au lieu d’utiliser les paramètres régionaux \_ par défaut de l’utilisateur \_ .

## <a name="thread-locale"></a>Paramètres régionaux de thread

Les paramètres régionaux de thread sont représentés par une variable de données de paramètres régionaux par thread qui détermine la mise en forme des dates, des heures, des devises et des nombres importants pour le thread. La valeur par défaut est celle des paramètres régionaux actuellement sélectionnés pour les standards et les formats. Pour définir les paramètres régionaux du thread, l’application appelle [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale). Pour récupérer les paramètres régionaux de thread, l’application appelle [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).

Dans la plupart des cas, les paramètres régionaux de thread ne doivent pas être remplacés. Normalement, il ne doit être utilisé que pour synchroniser les paramètres régionaux de thread d’une application serveur avec la variable standards et formats d’un ordinateur client. par exemple, une application de bourse financière pour le stock de new York Exchange, qui est utilisée dans les banques dans le monde entier, doit afficher les prix de l’heure, de la date et des actions dans États-Unis formats. Cette application utilise [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) pour définir les paramètres régionaux du thread sur l’anglais (États-Unis), puis utilise les fonctions nls pour mettre en forme les dates, les heures et les cours des actions.

La modification des paramètres régionaux du thread n’affecte pas toutes les fonctions de l’API. Par conséquent, il ne s’agit pas toujours d’un moyen fiable de remplacer la variable standards et formats. Au lieu de cela, les applications qui contrôlent les normes et les formats doivent utiliser des paramètres régionaux fixes pour afficher les données, en passant un identificateur de paramètres régionaux spécifique au lieu d’utiliser les paramètres régionaux \_ par défaut de l’utilisateur \_ .

## <a name="nls-example"></a>Exemple NLS

L’exemple suivant montre l’interaction entre les normes et les formats, le langage pour les programmes non-Unicode, l’emplacement et la langue de l’interface utilisateur de l’utilisateur.

un utilisateur qui est un serveur natif du chili mais qui se trouve dans le États-Unis possède un ordinateur exécutant Windows XP en anglais. L’utilisateur définit l’emplacement sur États-Unis pour utiliser un fournisseur de services Internet (ISP) afin d’obtenir la météo pour le États-Unis. Toutefois, la variable standards et formats est définie sur espagnol (Chili) afin que les informations soient mises en forme selon les normes chilienne. En outre, l’utilisateur utilise un traitement de texte coréen, qui est une application ANSI, afin que la langue des programmes non-Unicode soit définie sur coréen (Corée). Pour utiliser l’application, l’utilisateur dispose d’un clavier anglais et installe également un IME coréen pour prendre en charge une deuxième langue d’entrée. Le collègue de l’utilisateur, qui partage l’ordinateur mais ne s’est pas familiarisé avec l’anglais, peut définir la langue de l’interface utilisateur de l’utilisateur sur espagnol (Espagne) lors de l’utilisation de l’ordinateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la prise en charge linguistique nationale](about-national-language-support.md)
</dt> <dt>

[Paramètres régionaux et langues](locales-and-languages.md)
</dt> <dt>

[Interface utilisateur multilingue](multilingual-user-interface.md)
</dt> </dl>

 

 
