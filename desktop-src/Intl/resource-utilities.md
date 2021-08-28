---
description: Cette rubrique décrit deux utilitaires utilisés pour créer des applications MUI.
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: Utilitaires de ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9bb8a8608c97b700beebb53ce95fdf4b85c4d5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481505"
---
# <a name="resource-utilities"></a>Utilitaires de ressource

Cette rubrique décrit deux utilitaires utilisés pour créer des applications MUI. bien que MUIRCT soit un outil spécifique à MUI, mui utilise également l’utilitaire de compilation standard Windows RC. Les instructions relatives à l’utilisation de ces utilitaires sont fournies dans [localisation des ressources et génération de l’application](localizing-resources-and-building-the-application.md).

## <a name="muirct-utility"></a>Utilitaire MUIRCT

MUIRCT (Muirct.exe) est un utilitaire de ligne de commande permettant de fractionner un fichier exécutable standard en fichier LN et de fichiers de ressources spécifiques à une langue (c’est-à-dire localisables). Chacun des fichiers résultants contient des données de configuration de ressource pour l’Association de fichiers. MUIRCT est inclus dans le Microsoft Windows SDK pour Windows Vista.

> [!Note]  
> à compter de Windows Vista, le chargeur de ressources Win32 est mis à jour pour charger des ressources à partir de fichiers spécifiques à une langue et à partir de fichiers LN.

 

### <a name="muirct-usages"></a>Utilisations de MUIRCT

1.  Fractionnez le binaire en fichier binaire principal et en fichier MUI basé sur le \_ fichier de configuration RC.

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  Extrayez la somme de contrôle du fichier de somme de contrôle \_ et insérez-la dans le fichier de sortie \_ .

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  Calculez la somme de contrôle en fonction du fichier de somme de contrôle \_ et insérez-la dans le fichier de sortie \_ .

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  Vider le contenu des données de configuration des ressources à partir du fichier d’entrée \_ .

    `Muirct -d input_file`

### <a name="muirct-syntax"></a>Syntaxe MUIRCT

MUIRCT peut prendre la direction des commutateurs de ligne de commande et/ou d’un fichier de configuration de ressource, spécifié à l’aide du commutateur-q.


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



**Commutateurs et arguments**




| | | -h |- ? | Affiche l’écran d’aide. | | -c | Spécifie le checksum_file d’entrée à partir duquel extraire ou calculer la somme de contrôle de la ressource. Checksum_file doit être un fichier binaire Win32 contenant des ressources localisables. Si checksum_file contient des ressources pour plusieurs langages, le commutateur-b doit être utilisé pour spécifier ceux qui doivent être utilisés, sans quoi MUIRCT échoue. <br /> | | -b | Spécifie la langue à utiliser lorsque la checksum_file spécifiée avec-c contient des ressources dans plusieurs langues. Ce commutateur peut être utilisé uniquement conjointement avec le commutateur-c. L’identificateur de langue peut être au format décimal ou hexadécimal. MUIRCT échoue si le checksum_file contient des ressources dans plusieurs langues et que-b n’est pas spécifié ou si la langue spécifiée par le commutateur-b est introuvable dans le checksum_file. <br /> | | -g | Spécifie l’ID de langue à inclure comme langue de secours ultime dans la section des données de configuration de ressource du fichier LN. Si le chargeur de ressources ne parvient pas à charger un fichier. mui demandé à partir des langues d’interface utilisateur préférées du thread, il utilise le langage de secours ultime comme dernière tentative. La valeur LangID peut être spécifiée au format décimal ou hexadécimal. Par exemple, l’anglais (États-Unis) peut être spécifié par-g 0x40C ou-g 1033. <br /> | | -q | Spécifie que le source_file doit être fractionné dans le output_LN_file et le output_MUI_file en fonction de la disposition de fichier rc_config. Le fichier rc_config est un fichier au format XML qui spécifie les ressources qui seront extraites dans le fichier. mui et qui seront conservées dans le fichier LN. La rc_config peut spécifier la distribution des types de ressources et des éléments nommés individuels entre le output_LN_file et le output_MUI_file. Le source_file doit être un fichier binaire Win32 qui contient des ressources dans une seule langue, sans quoi MUIRCT échoue. MUIRCT ne fractionne pas le fichier s’il est indépendant de la langue, ce qui est indiqué par la présence d’une seule valeur d’ID de langue égale à 0 dans le fichier. Les output_LN_file et output_mui_file sont les noms du fichier. mui et du langage neutre dans lequel l’source_file est fractionné. Ces noms de fichiers sont facultatifs. Si elles ne sont pas spécifiées, MUIRCT ajoute les extensions. ln et. mui pour source_file. En général, vous devez supprimer l’extension « . ln » avant de déployer le fichier. MUIRCT associe le output_LN_file et output_MUI_file en calculant une somme de contrôle en fonction du nom de la source_file et de la version du fichier et en insérant le résultat dans la section de configuration des ressources de chaque fichier de sortie. Lorsqu’il est utilisé conjointement avec le commutateur-c, le commutateur-q est prioritaire. Si le rc_config fichier fourni avec le commutateur-q contient une somme de contrôle MUIRCT ignore le commutateur-c et insère la valeur de somme de contrôle à partir de la valeur, rc_config fichier dans les fichiers LN et. mui. Si aucune valeur de somme de contrôle n’est trouvée dans le rc_config, MUIRCT calcule la somme de contrôle de ressource en fonction du comportement du commutateur-c. <br /> | | -v | Spécifie le niveau de verboseness pour la journalisation. Spécifiez 1 pour imprimer tous les messages d’erreur et les résultats de l’opération de base. Spécifiez 2 pour inclure également les informations de ressource (type, nom, identificateur de langue) incluses dans le fichier. mui et le fichier LN. La valeur par défaut est-v 1 <br /> | | -x | Spécifie l’ID de langue avec lequel MUIRCT marque tous les types de ressources ajoutés à la section de la ressource du fichier. mui. La valeur LangID peut être spécifiée au format décimal ou hexadécimal. Par exemple, l’anglais (États-Unis) peut être spécifié par-x 0x40C ou-x 1033. <br /> | | -e | Extrait la somme de contrôle de la ressource contenue dans le checksum_file fourni avec le commutateur-c et l’insère dans le output_file spécifié. Quand-e est spécifié, MUIRCT ignore tous les commutateurs autres que le commutateur-c. Dans ce cas, le checksum_file doit être un fichier binaire Win32 qui contient une section de données de configuration de ressource avec une valeur de somme de contrôle. Le output_file doit être un fichier LN ou. mui existant. <br /> | | -z | Calcule et insère les données de somme de contrôle de ressource dans le fichier de sortie spécifié. MUIRCT base le calcul de la somme de contrôle sur l’entrée fournie avec le commutateur-c et le commutateur facultatif-b. Si vous spécifiez un fichier de sortie pour le commutateur-z qui n’existe pas, MUIRCT se termine avec un échec.<br /> Exemple : calcule la somme de contrôle en fonction des ressources localisables dans Notepad.exe et insère la somme de contrôle dans le fichier de sortie Notepad2.exe.<br /><code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br /> | | -f | Permet de créer un fichier. mui dont la ressource de version est la seule ressource localisable. Par défaut, MUIRCT ne l’autorise pas.<br /> | | -d | Localise et affiche les données de configuration de ressources incorporées dans le fichier source. Lorsque vous spécifiez ce commutateur, MUIRCT ignore toutes les autres options de ligne de commande.<br /> | | -m | Spécifie le numéro de version à utiliser lors du calcul de la somme de contrôle pour associer les output_LN_file et les output_MUI_file. <br /> | | source_filename | Nom du fichier source binaire localisé ; les caractères génériques ne peuvent pas être utilisés. Ce fichier ne peut contenir que des ressources dans une seule langue. Si le fichier contient des ressources dans plusieurs langues, MUIRCT échoue, sauf si le commutateur-b est utilisé. Si le fichier contient des ressources avec des identificateurs de langue ayant uniquement la valeur 0, MUIRCT ne fractionne pas le fichier, car un identificateur de langue de 0 indique une langue neutre.<br /> Pour le commutateur-d, source_filename est soit un fichier LN, soit un fichier de ressources spécifique à une langue pour lequel MUIRCT doit afficher les données de configuration de ressource. <br /> | | language_neutral_filename | Facultatif. Nom du fichier LN. Si vous ne spécifiez pas le nom de ce fichier, MUIRCT ajoute une deuxième extension « . ln » au nom du fichier source à utiliser comme nom de fichier indépendant de la langue. En général, vous devez supprimer l’extension « . ln » avant de déployer le fichier.<blockquote>[!Note]<br />Le fichier LN ne doit pas contenir de chaînes ou de menus. Vous devez les supprimer manuellement.</blockquote><br /> | | mui_filename | Facultatif. Nom du fichier de ressources spécifique à la langue. Si vous ne spécifiez pas de nom, MUIRCT ajoute une deuxième extension « . mui » au nom du fichier source à utiliser comme nom de fichier. Normalement, MUIRCT crée un fichier de ressources spécifique à une langue. Toutefois, il ne crée pas de fichier de ressources si l’une des conditions suivantes est remplie :<br /><ul><li>Aucune ressource localisable n’est dans le fichier binaire d’origine.</li><li>Le seul langage des ressources trouvé dans le fichier binaire d’origine est le langage neutre.</li><li>Le fichier binaire d’origine contient des ressources pour plusieurs langues, sans compter la langue neutre. Si le fichier binaire contient des ressources pour deux langues et que l’une d’entre elles est la langue neutre, l’utilitaire considère que le fichier est monolingue et crée un fichier de ressources spécifique à la langue s’il existe des ressources localisables.</li></ul> | 




 

### <a name="muirct-language-output"></a>Sortie du langage MUIRCT

MUIRCT choisit la valeur de l’attribut « UltimateFallbackLanguage » à insérer dans les données de configuration de ressource du fichier LN en fonction de l’ordre suivant, de la priorité la plus élevée à la plus faible :

1.  Attribut « UltimateFallbackLanguage » dans le fichier de configuration de ressource source, s’il est passé en tant qu’entrée.
2.  Langue spécifiée avec le commutateur-g.
3.  Langue du fichier d’entrée.

MUIRCT choisit la valeur de l’attribut « Language » à insérer dans les données de configuration de ressource de fichier. mui selon l’ordre suivant :

1.  attribut « Language » dans le fichier de configuration de ressource source, s’il est passé en tant qu’entrée.
2.  Langue spécifiée par le commutateur-x (forcer la langue).
3.  Langue du fichier d’entrée.

### <a name="muirct-checksum-handling"></a>Gestion de la somme de contrôle MUIRCT

Le système d’exploitation calcule normalement la somme de contrôle sur les ressources spécifiques à une langue dans un fichier, sauf si vous spécifiez la somme de contrôle via un fichier de configuration de ressource. Tant que la somme de contrôle est la même pour le fichier LN et tous les fichiers de ressources spécifiques à la langue associés, et que l’attribut Language dans la configuration de ressource dans le LN et le Language dépendent, le chargeur de ressources peut charger des ressources avec succès.

MUIRCT prend en charge plusieurs méthodes pour placer les sommes de contrôle appropriées dans les données de configuration de ressource :

1.  Générez un exécutable pour chaque langage, contenant à la fois le code et les ressources. Après cela, utilisez MUIRCT pour fractionner chacun de ces fichiers en un fichier LN et un fichier de ressources spécifique à une langue. MUIRCT s’exécute plusieurs fois, une fois pour générer un fichier de ressources pour chaque langue. Vous pouvez effectuer la génération des manières suivantes :
    1.  Utilisez le commutateur-q pour spécifier une valeur de somme de contrôle dans le fichier de configuration de ressource. MUIRCT place cette valeur dans tous les fichiers LN et les fichiers de ressources spécifiques à la langue produits. Vous devez adopter une stratégie pour choisir cette valeur, comme décrit plus loin dans cette rubrique.
    2.  Utilisez le commutateur-c (et, éventuellement, le commutateur-b) pour choisir une seule langue dont les ressources dont MUIRCT extrait la somme de contrôle.
    3.  Utilisez le commutateur-z pour choisir une seule langue dont les ressources sont à partir desquelles MUIRCT extrait toujours la somme de contrôle. Appliquez cette somme de contrôle une fois que les fichiers ont été générés à l’aide d’autres méthodes.
2.  Créez un exécutable contenant à la fois le code et les ressources pour une seule langue. Ensuite, utilisez MUIRCT pour fractionner les ressources entre le fichier LN et le fichier de ressources spécifique à la langue. Enfin, utilisez un outil de localisation binaire pour modifier le fichier de ressources résultant pour chaque langue.

La Convention la plus courante pour gérer les sommes de contrôle consiste à baser la somme de contrôle sur les ressources anglaises (États-Unis). Vous êtes libre d’adopter une convention différente, à condition qu’elle soit cohérente pour chaque fichier LN. Par exemple, il est parfaitement acceptable pour une entreprise de développement de logiciels de baser ses sommes de contrôle dans le logiciel qu’elle construit sur des ressources françaises (France) à la place des ressources anglais (États-Unis), à condition que toutes les applications aient des ressources françaises (France) sur lesquelles baser les sommes de contrôle. Il est également possible d’utiliser le fichier de configuration de ressources pour assigner une valeur hexadécimale arbitraire pouvant atteindre 16 chiffres hexadécimaux en tant que somme de contrôle. Cette dernière stratégie exclut l’utilisation effective des commutateurs-z,-c et-b de MUIRCT. Elle nécessite l’adoption d’une méthode à l’aide de [**Guidgen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) ou d’un autre outil pour générer des valeurs de somme de contrôle. Cette stratégie vous oblige également à configurer une stratégie pour déterminer quand modifier la valeur lors de l’ajout de nouvelles ressources localisables.

Pour appliquer la somme de contrôle anglais (États-Unis) à tous les fichiers, vous pouvez utiliser l’une des méthodes de gestion de la somme de contrôle décrites ci-dessus. Par exemple, vous pouvez générer le fichier de LN et le fichier de ressources spécifique à la langue pour l’anglais (États-Unis), puis utiliser le commutateur MUIRCT-d pour obtenir la somme de contrôle résultante. Vous pouvez copier cette somme de contrôle dans votre fichier de configuration de ressources et utiliser le commutateur-q avec MUIRCT pour appliquer la somme de contrôle à tous les autres fichiers.

### <a name="use-of-a-resource-configuration-file-with-muirct"></a>Utilisation d’un fichier de configuration de ressource avec MUIRCT

Vous pouvez spécifier des données de configuration de ressources lors de l’utilisation de MUIRCT. Que vous fournissiez ou non explicitement un fichier de configuration de ressource, chaque fichier de ressources spécifique à une langue contient des données de configuration de ressource, comme tout fichier LN avec un fichier de ressources associé. Par exemple :

-   Si vous utilisez le commutateur-q pour spécifier un fichier de configuration de ressource, mais qu’il n’existe pas de ressources localisables dans votre fichier source d’entrée, aucun fichier de ressources spécifique à la langue n’est généré et le fichier LN résultant ne contient pas de données de configuration de ressource. En outre, si le fichier source d’entrée contient des ressources multilingues, MUIRCT ne fractionne pas le fichier.

> [!Note]  
> Actuellement, le comportement de MUIRCT est incohérent lorsque l’élément neutralResources du fichier de configuration de ressource ne contient pas d’éléments resourceType et que l’élément localizedResources contient des chaînes et des menus, par exemple. Dans ce cas, MUIRCT fractionne les ressources comme suit :
>
> -   Toutes les ressources du fichier binaire d’origine (y compris les chaînes et les menus), ainsi que les ressources MUI, sont placées dans le fichier LN.
> -   Les chaînes, les menus et les ressources MUI sont placés dans le fichier de ressources propre à la langue approprié.

 

### <a name="examples-for-using-muirct"></a>Exemples d’utilisation de MUIRCT

**Exemples d’utilisation standard**


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



**Exemple de sortie de fichier LN en utilisant le commutateur-d**

Voici un exemple de la sortie de données de configuration de ressource d’un fichier LN, Shell32.dll, à l’aide du commutateur-d avec MUIRCT :


```C++
Signature          -    fecdfecd
Length             -    148
RC Config Version  -    10000
FileType           -    11
SystemAttributes   -    100
UltimateFallback location    -  external
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    AVI FTR ORDERSTREAM TYPELIB UIFILE XML MUI
MainIDTypes        -    1 2 3 12 14 16 24
MuiNameTypes       -    MUI
MuiIDTypes         -    2 3 4 5 6 9 14 16
UltimateFallbackLanguage   -   en-US
```



**Exemple de Language-Specific sortie de fichier de ressources à l’aide du commutateur-d**

Voici un exemple de la sortie de données de configuration de ressources à partir d’un fichier. mui, Shell32.dll. mui, à l’aide du commutateur-d pour MUIRCT :


```C++
Signature          -    fecdfecd
Length             -     c8
RC Config Version  -    10000
FileType           -    12
SystemAttributes   -    100
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    MUI
MainIDTypes        -    2 3 4 5 6 9 14 16
Language           -    en-US
```



## <a name="rc-compiler-utility"></a>Utilitaire de compilation RC

Le compilateur RC (Rc.exe) est un utilitaire de ligne de commande permettant de compiler un fichier de script de définition de ressource (extension. RC) dans des fichiers de ressources (extension. res). le compilateur RC est inclus dans le SDK Windows. Ce document explique uniquement comment utiliser le compilateur RC avec les fonctionnalités MUI du chargeur de ressources. Pour obtenir des informations complètes sur le compilateur, consultez [à propos des fichiers de ressources](../menurc/about-resource-files.md).

Le compilateur RC vous permet de générer, à partir d’un seul ensemble de sources, un fichier LN et un fichier de ressources propre au langage. Comme pour MUIRCT, les fichiers sont associés à des données de configuration de ressource.

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a>Syntaxe du compilateur RC utilisée pour les ressources MUI

Les commutateurs du compilateur RC sont définis en détail dans [utilisation de RC](../menurc/using-rc-the-rc-command-line-.md). Cette section définit uniquement les commutateurs utilisés pour créer des ressources MUI. N’oubliez pas que chaque commutateur ne respecte pas la casse. Les types de ressources sont supposés être indépendants du langage, sauf indication contraire.


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



**Commutateurs et arguments**




| | | -h |- ? | Affiche l’écran d’aide. | | -FM | Utilise le fichier de ressources spécifié pour les ressources spécifiques à une langue. Normalement, le compilateur de ressources crée un fichier de ressources spécifique à une langue. Toutefois, il ne crée pas le fichier si l’une des conditions suivantes est remplie :<br /><ul><li>Il n’existe pas de ressources localisables dans le fichier. rc.</li><li>Le seul langage des ressources trouvé dans le fichier. RC est le langage neutre.</li><li>Le fichier. rc contient des ressources pour plusieurs langues, sans compter la langue neutre. Si le fichier. rc contient des ressources pour deux langues et que l’une d’entre elles est la langue neutre, le compilateur considère que le fichier est monolingue. S’il existe des ressources localisables, le compilateur crée un fichier de ressources spécifique à la langue.</li></ul> | | -q | Utilise le fichier de configuration de ressource spécifié pour obtenir les types de ressources à placer dans le fichier de ressources spécifique à la langue et dans le fichier LN. Pour plus d’informations, consultez <a href="preparing-a-resource-configuration-file.md">préparation d’un fichier de configuration de ressource</a>. Comme alternative à ce commutateur, vous pouvez utiliser les commutateurs-j et-k, mais il est préférable d’utiliser un fichier de configuration de ressource. <br /> En utilisant le commutateur-q avec un fichier de configuration de ressource, vous pouvez implémenter un fractionnement basé sur les éléments et fournir des attributs qui finissent par la configuration des ressources binaires dans le fichier de ressources en LN et spécifiques à une langue. Ce fractionnement n’est pas possible à l’aide des commutateurs-j et-k.<blockquote>[!Note]<br />Le processus de fractionnement du compilateur RC ne fonctionne pas correctement si vous stockez des ressources et des informations de version dans des fichiers de configuration de ressources différents. Dans ce cas, le compilateur RC ne fractionne pas les informations de version. Par conséquent, une erreur de l’éditeur de liens se produit lors de la liaison du fichier de ressources spécifique à la langue, car le fichier n’a pas de ressources de version.</blockquote><br /><br /> | | -g | Spécifie l’identificateur de <a href="language-identifiers.md">langue de secours</a> ultime en notation hexadécimale.<br /> | | -G1 | Crée un fichier MUI. res même si la ressource de VERSION est le seul contenu localisable. Par défaut, le compilateur RC ne produit pas de fichier. res si la VERSION est la seule ressource localisable.<br /> | | -G2 | Spécifie le numéro de version personnalisé à utiliser lors du calcul de la somme de contrôle.<br /> | | mui_res_name | Fichier de ressources pour les ressources spécifiques à une langue.<br /> | | rc_config_file_name | Fichier de configuration de ressource.<br /> | | langid | Identificateur de langue.<br /> | | version | Numéro de version personnalisé, dans un format tel que « 6.2.0.0 ».<br /> | 




 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a>Exemple d’utilisation du compilateur RC pour générer des ressources MUI

Pour illustrer l’opération du compilateur RC avec les ressources MUI, examinons la ligne de commande suivante pour le fichier de ressources MyFile. RC :


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



Cette ligne de commande force le compilateur RC à effectuer les opérations suivantes :

-   Créez le fichier de ressources propre à la langue MyFile \_ res. res et un fichier de ressources indépendant de la langue dont la valeur par défaut est MyFile. res, en fonction du nom du fichier. rc.
-   Ajoutez le 2 (élément 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 \_ types de ressources de type dans le fichier. res spécifique à la langue, s’ils se trouvent dans le fichier. rc.
-   Ajoutez le type de ressource 16, ainsi que tous les autres types de ressources décrits dans le fichier de ressources au fichier. res indépendant de la langue et au fichier. res propre à la langue. Notez que, dans cet exemple, le type de ressource 16 est ajouté à deux emplacements.
-   Choisissez la valeur de l’attribut « UltimateFallbackLanguage » pour insérer les données de configuration de ressource du fichier LN en fonction des critères suivants, classés de la plus haute à la plus faible :
    -   Attribut « UltimateFallbackLanguage » dans le fichier de configuration de ressource, s’il est passé en tant qu’entrée.
    -   Valeur de l’attribut de langage à insérer dans les données de configuration de ressource en fonction de l’ordre de la langue du compilateur RC (langue indépendante de la langue et langue du fichier de ressources propre à la langue). Les considérations incluent le langage dans le fichier. RC, la valeur de langue du commutateur-GL et l’identificateur 0x0409 pour l’anglais (États-Unis).

## <a name="remarks"></a>Remarques

Si vous incluez des types de ressources icône (3), boîte de dialogue (5), chaîne (6) ou VERSION (16) dans l’élément neutralResources, vous devez dupliquer cette entrée dans l’élément localizedResources dans le fichier de configuration de ressource.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[interface utilisateur multilingue Faire](multilingual-user-interface-reference.md)
</dt> <dt>

[Gestion des ressources MUI](mui-resource-management.md)
</dt> <dt>

[Localisation des ressources et génération de l’application](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
