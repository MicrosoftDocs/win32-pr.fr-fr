---
description: Cette section explique comment créer un dictionnaire personnalisé pour la reconnaissance de l’écriture manuscrite.
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: création de dictionnaires personnalisés pour la reconnaissance de l’écriture manuscrite dans Windows 7 et Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe391125b21bfe35a9e1a69be6258e1643b424e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412298"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a>création de dictionnaires personnalisés pour la reconnaissance de l’écriture manuscrite dans Windows 7 et Windows Server 2008 R2

Cette section explique comment créer un dictionnaire personnalisé pour la reconnaissance de l’écriture manuscrite.

dans le système d’exploitation Windows 7 et le système d’exploitation Windows Server 2008 R2, la précision de la reconnaissance de l’écriture manuscrite peut être considérablement améliorée grâce à l’utilisation de dictionnaires personnalisés. Ces dictionnaires complètent ou remplacent les dictionnaires système utilisés pour l’écriture manuscrite. La prise en charge de la reconnaissance de l’écriture manuscrite est fournie par la fonctionnalité Services de prise en charge de l’écriture manuscrite qui doit être activée via Gestionnaire de serveur.

> [!Note]  
> Les dictionnaires personnalisés peuvent être installés pour une langue uniquement si le module de reconnaissance de l’écriture manuscrite pour cette langue est installé.

 

Il existe deux étapes de base pour configurer un dictionnaire personnalisé pour l’écriture manuscrite :

-   Compiler une liste de mots. La compilation crée un fichier de dictionnaire personnalisé (. hwrdict) compilé.
-   Installez le dictionnaire personnalisé compilé.

## <a name="compiling-a-word-list"></a>Compilation d’une liste de mots

La liste de mots à compiler doit être au format texte brut et doit être enregistrée à l’aide d’un encodage Unicode. Les autres encodages ne fonctionneront pas. Chaque ligne du fichier texte est considérée comme une seule entrée dans le dictionnaire. Les entrées d’unités multimots contenant un ou plusieurs espaces sont autorisées. Les espaces au début ou à la fin d’une ligne sont ignorés.

Un dictionnaire personnalisé est compilé à partir d’une ligne de commande. Pour compiler un dictionnaire, ouvrez une fenêtre de commande, accédez au dossier contenant la liste de mots, puis exécutez HwrComp.exe avec les options de ligne de commande que vous souhaitez utiliser.

L’exemple suivant illustre la syntaxe d’utilisation pour les options de ligne de commande.

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a>Explication des options



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Paramètre</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-lang &lt; localename&gt;</td>
<td>Nom des paramètres régionaux spécifiés attribués au fichier de dictionnaire personnalisé compilé. L’argument &lt; localename &gt; se présente sous la forme langue-région. Par exemple, est en-US, ce qui signifie la langue anglaise dans la région États-Unis. Pour obtenir des exemples de ce formulaire, consultez [constantes et chaînes](/windows/desktop/Intl/language-identifier-constants-and-strings)de l’identificateur de langage. les langues suivantes sont prises en charge pour Windows 7 et Windows Server 2008 R2 par cette fonctionnalité : en-US, en-GB, en-CA, en-au, de-de, de-CH, fr-fr, es-es, es-MX, es-AR, it-it, nl-nl, nl-is, pt-BR, pt-pt, da-DK, sv-SE, nb-no, nn-no, fi-fi, pl-pl, cs-CZ, ru-ru, ro-ro, sr-Latn-cs, sr-Cyrl-cs, CA-es et hr-hr.<br/></td>
</tr>
<tr class="even">
<td>type-type &lt;&gt;</td>
<td>Le type d’argument option &lt; &gt; est une concaténation à chaîne unique de l’utilisation de la ressource en tant que liste de mots principale (principale) ou en complément de la liste de mots principale (secondaire), suivie du nom de la liste de mots réelle à laquelle la ressource est appliquée (par exemple, dictionary ou Surname). Les valeurs possibles sont les suivantes :
<ul>
<li>PRIMARY-NOM_VILLE-LIST</li>
<li>PRIMARY-COUNTRYNAME-LIST</li>
<li>PRIMARY-COUNTRYSHORTNAME-LIST</li>
<li>DICTIONNAIRE PRINCIPAL</li>
<li>PRIMARY-GIVENNAME-LIST</li>
<li>PRIMARY-STATEORPROVINCE-LIST</li>
<li>PRIMARY-STREETNAME-LIST</li>
<li>PRIMARY-SURNAME-LIST</li>
<li>SECONDARY-NOM_VILLE-LIST</li>
<li>COUNTRYNAME SECONDAIRE-LISTE</li>
<li>COUNTRYSHORTNAME SECONDAIRE-LISTE</li>
<li>DICTIONNAIRE SECONDAIRE</li>
<li>EMAILSMTP SECONDAIRE-LISTE</li>
<li>EMAILUSERNAME SECONDAIRE-LISTE</li>
<li>SECONDAIRE-GIVENNAME-LIST</li>
<li>STATEORPROVINCE SECONDAIRE-LISTE</li>
<li>STREETNAME SECONDAIRE-LISTE</li>
<li>SECONDAIRE-SURNAME-LIST</li>
<li>LISTE D’URL SECONDAIRE</li>
</ul>
Si une valeur de type commence par le préfixe PRIMARY, le dictionnaire compilé, après son installation, remplace le dictionnaire système pour cette langue. La valeur principal-DICTIONARY représente le dictionnaire principal du système pour une langue.
<blockquote>
[!Note]<br />
Le remplacement d’un dictionnaire système n’a aucun effet sur le contenu du dictionnaire système d’origine, car le remplacement est effectif uniquement jusqu’à ce que le dictionnaire personnalisé ait été supprimé.
</blockquote>
<br/> Si une valeur de type commence par le préfixe SECONDARY, le dictionnaire compilé complète le dictionnaire système sans le remplacer.</td>
</tr>
<tr class="odd">
<td>-Comment <comment></td>
<td>Le commentaire spécifié est compilé dans le fichier de dictionnaire. Le commentaire doit être une chaîne unique et ne pas dépasser 64 caractères.</td>
</tr>
<tr class="even">
<td>-o <dictfile.hwrdict></td>
<td>La sortie est écrite dans le nom de fichier spécifié par <dictfile.hwrdict> .<br/> Si cette option est manquante, le nom du fichier de sortie est dérivé du nom du fichier d’entrée d’origine, avec l’extension de fichier d’entrée remplacée par. hwrdict.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a>Valeurs par défaut

Si aucun paramètre n’est spécifié, les valeurs d’option par défaut sont

-lang <current input language> -type secondaire-dictionnaire

### <a name="examples"></a>Exemples

L’exemple suivant compile le fichier d’entrée mylist1.txt, applique les valeurs d’option par défaut et crée le fichier de sortie mylist1. hwrdict.

``` syntax
hwrcomp mylist1.txt
```

En revanche, le code suivant compile mylist1.txt dans myrsrc1. hwrdict, mais affecte « English (US) » (en-US) comme langage et le dictionnaire secondaire comme type.

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a>Installation d’un dictionnaire personnalisé compilé

HwrComp.exe crée un fichier. hwrdict, qui est dans un format binaire utilisable par un module de reconnaissance de l’écriture manuscrite. ce fichier peut être installé sur n’importe quel ordinateur exécutant Windows 7 ou Windows Server 2008 R2 qui prend en charge la reconnaissance de l’écriture manuscrite. Un dictionnaire est installé uniquement pour l’utilisateur actuel ou pour tous les utilisateurs sur un ordinateur.

Un fichier de dictionnaire personnalisé compilé peut être installé à partir de la ligne de commande à l’aide de l’outil HwrReg.exe. Cet outil est utile si vous souhaitez remplacer certaines des valeurs de configuration qui sont compilées dans le fichier ou qui sont les valeurs par défaut. Il existe deux façons d’exécuter HwrReg.exe : en mode vérification/installation et en mode liste/suppression.

### <a name="running-hwrregexe-in-checkinstall-mode"></a>Exécution de HwrReg.exe en mode de vérification/installation

Ce mode est destiné aux fichiers de dictionnaires personnalisés qui n’ont pas encore été installés. L’exemple suivant illustre la syntaxe d’utilisation des options de ligne de commande.

``` syntax
Usage: hwrreg        [-check]
    [-lang <localename>] 
    [-scope {all|me}]
    [-noprompt] 
    <dictfile.hwrdict>
```

### <a name="explanation-of-options"></a>Explication des options



| Paramètre                | Description                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -vérifier                   | Le fichier du dictionnaire est vérifié sans être installé. L’option vérifier affiche le commentaire du fichier, ainsi que les informations d’enregistrement qui seraient utilisées pour installer le fichier. Cette option est utile pour vérifier les informations d’inscription avant l’exécution de l’installation. <br/> Si cette option est manquante, HwrReg.exe installe le dictionnaire personnalisé.<br/>  |
|  &lt;localename lang&gt; | Le fichier du dictionnaire est vérifié sans être installé. L’option vérifier affiche le commentaire du fichier, ainsi que les informations d’enregistrement qui seraient utilisées pour installer le fichier. Cette option est utile pour vérifier les informations d’inscription avant l’exécution de l’installation. <br/> Si cette option est manquante, HwrReg.exe installe le dictionnaire personnalisé. <br/> |
|  étendue {All \| me}         | Le dictionnaire personnalisé est installé pour tous les utilisateurs (étendue tous) ou uniquement pour l’utilisateur actuel (étendue me). L’installation de avec l’étendue All requiert que la commande soit exécutée dans une invite de commandes avec élévation de privilèges ; dans le cas contraire, un code d’erreur est retourné. <br/> Si cette option est manquante, l’installation est limitée à l’utilisateur actuel.<br/>                          |
|  commutateur noprompt                | HwrReg.exe ne demande pas de confirmation. Cela peut être utile lors de l’exécution de hwrReg.exe à partir d’un script. <br/>                                                                                                                                                                                                                                                                 |



 

L’exemple suivant installe le dictionnaire personnalisé myrsrc1. hwrdict pour le langage « danois (Denmark) » (da DK), avec uniquement l’étendue par défaut de l’utilisateur actuel.

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a>Exécution de HwrReg.exe en mode liste/suppression

Ce mode permet de répertorier ou de supprimer les dictionnaires personnalisés installés. L’exemple suivant illustre la syntaxe d’utilisation des options de ligne de commande.

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a>Explication des options



| Paramètre                | Description                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  &lt;localename lang&gt; | Les dictionnaires inscrits pour uniquement ce nom de paramètres régionaux sont répertoriés ou supprimés. L’argument &lt; localename &gt; a la région de langue du formulaire. Pour obtenir des exemples de ce formulaire, consultez [constantes et chaînes](/windows/desktop/Intl/language-identifier-constants-and-strings)de l’identificateur de langage. <br/> Si cette option est manquante, les dictionnaires pour toutes les langues sont répertoriés ou supprimés.<br/> |
|  étendue {All \| me}         | Le dictionnaire personnalisé est installé pour tous les utilisateurs (étendue tous) ou uniquement pour l’utilisateur actuel (étendue me). L’installation de avec l’étendue All requiert que la commande soit exécutée dans une invite de commandes avec élévation de privilèges ; dans le cas contraire, un code d’erreur est retourné. <br/> Si cette option est manquante, l’installation est limitée à l’utilisateur actuel.<br/>                      |
|  type &lt; de type&gt;       | Répertorie ou supprime uniquement les dictionnaires inscrits avec le type spécifié.<br/> Si cette option est manquante, tous les types de dictionnaires sont répertoriés ou supprimés. L’installation ou la suppression d’un dictionnaire personnalisé d’un autre type (par exemple, PRIMARY-COUNTRYNAME-LIST) peut affecter la reconnaissance de l’écriture manuscrite dans d’autres contextes. <br/>                                              |
|  list                    | Répertorie tous les dictionnaires installés qui correspondent aux autres options.<br/> Si cette option est manquante, l’option supprimer doit être spécifiée.<br/>                                                                                                                                                                                                                          |
|  remove                  | Demande la suppression d’un dictionnaire qui correspond aux autres options.<br/> Si cette option est manquante, la liste d’options doit être spécifiée.<br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Exemples

Les listes suivantes répertorient les dictionnaires dont la langue est l’anglais (États-Unis) et le dictionnaire principal de type et qui sont installés uniquement pour l’utilisateur actuel.

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

De même, le code suivant supprime les dictionnaires qui correspondent aux mêmes critères.

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a>Remarques générales sur les dictionnaires personnalisés

-   Si vous installez deux dictionnaires personnalisés qui ont le même type, la même langue et la même étendue, la deuxième installation remplacera la première.
-   Si vous installez deux dictionnaires personnalisés avec le même type et la même langue, mais avec des étendues différentes (une pour tous les utilisateurs et une pour l’utilisateur actuel), le dictionnaire installé pour l’utilisateur actuel est prioritaire et le dictionnaire installé pour tous les utilisateurs est ignoré.

 

