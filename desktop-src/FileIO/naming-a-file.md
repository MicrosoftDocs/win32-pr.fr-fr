---
description: tous les systèmes de fichiers pris en charge par Windows utilisent le concept de fichiers et de répertoires pour accéder aux données stockées sur un disque ou un périphérique.
ms.assetid: 121cd5b2-e6fd-4eb4-99b4-b652d27b53e8
title: Nommage des fichiers, chemins d’accès et espaces de noms
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: 59f626c931a61255cef8be9ede594cb97924cfb0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009901"
---
# <a name="naming-files-paths-and-namespaces"></a>Nommage des fichiers, chemins d’accès et espaces de noms

tous les systèmes de fichiers pris en charge par Windows utilisent le concept de fichiers et de répertoires pour accéder aux données stockées sur un disque ou un périphérique. Windows les développeurs qui travaillent avec les api Windows pour les e/s de fichiers et de périphériques doivent comprendre les différentes règles, conventions et limitations des noms de fichiers et de répertoires.

Les données sont accessibles à partir de disques, d’appareils et de partages réseau à l’aide des API d’e/s de fichier. Les fichiers et les répertoires, ainsi que les espaces de noms, font partie du concept de chemin d’accès, qui est une représentation sous forme de chaîne de l’emplacement des données, quel que soit l’emplacement d’un disque ou d’un périphérique ou d’une connexion réseau pour une opération spécifique.

Certains systèmes de fichiers, tels que NTFS, prennent en charge les fichiers et les répertoires liés, qui suivent également les conventions d’affectation de noms de fichiers et les règles comme un fichier ou un répertoire normal. Pour plus d’informations, consultez [liens physiques et jonctions](hard-links-and-junctions.md) , [points d’analyse et opérations de fichier](reparse-points-and-file-operations.md).

Pour plus d’informations, consultez les sous-sections suivantes :

-   [Noms de fichiers et de répertoires](#file-and-directory-names)
    -   [Conventions d’affectation des noms](#naming-conventions)
    -   [Noms courts et noms longs](#short-vs-long-names)
-   [Chemins d’accès](#fully-qualified-vs-relative-paths)
    -   [Chemins d’accès complets et chemins relatifs](#fully-qualified-vs-relative-paths)
    -   [Limitation de longueur maximale du chemin](#maximum-path-length-limitation)
-   [Espaces de noms](#win32-file-namespaces)
    -   [Espaces de noms de fichier Win32](#win32-file-namespaces)
    -   [Espaces de noms d’appareils Win32](#win32-device-namespaces)
    -   [Espaces de noms NT](#nt-namespaces)
-   [Rubriques connexes](#related-topics)


pour en savoir plus sur la configuration de Windows 10 pour prendre en charge les chemins d’accès de fichiers longs, consultez [Limitation de longueur maximale du chemin d’accès](./maximum-file-path-limitation.md).


## <a name="file-and-directory-names"></a>Noms de fichiers et de répertoires

Tous les systèmes de fichiers suivent les mêmes conventions d’affectation de noms générales pour un fichier individuel : un nom de fichier de base et une extension facultative, séparés par un point. Toutefois, chaque système de fichiers, tel que NTFS, CDFS, exFAT, UDF, FAT et FAT32, peut avoir des règles spécifiques et différentes sur la formation des composants individuels dans le chemin d’accès à un répertoire ou à un fichier. Notez qu’un *répertoire* est simplement un fichier avec un attribut spécial qui le désignant comme répertoire, mais qui, dans le cas contraire, doit suivre les mêmes règles d’affectation de noms qu’un fichier normal. Étant donné que le terme *répertoire* fait simplement référence à un type spécial de fichier en ce qui concerne le système de fichiers, certains documents de référence utilisent le *fichier* terme général pour englober les deux concepts des répertoires et des fichiers de données. Pour cette raison, sauf indication contraire, les règles d’affectation de noms ou d’utilisation ou des exemples pour un fichier doivent également s’appliquer à un répertoire. Le terme *chemin d’accès* fait référence à un ou plusieurs répertoires, barres obliques inverses et éventuellement un nom de volume. Pour plus d’informations, consultez la section [chemins d’accès](#fully-qualified-vs-relative-paths) .

Les limites du nombre de caractères peuvent également être différentes et peuvent varier en fonction du format de préfixe du système de fichiers et du chemin d’accès utilisé. Cela est encore plus compliqué par la prise en charge des mécanismes de compatibilité descendante. Par exemple, l’ancien système de fichiers FAT MS-DOS prend en charge un maximum de 8 caractères pour le nom de fichier de base et 3 caractères pour l’extension, pour un total de 12 caractères, y compris le séparateur de points. Ce *nom de fichier* est communément appelé 8,3. les systèmes de fichiers Windows FAT et NTFS ne sont pas limités aux noms de fichiers 8,3, car ils *prennent en charge le nom* de fichier long, mais ils prennent toujours en charge la version 8,3 des noms de fichiers longs.

### <a name="naming-conventions"></a>Conventions d'affectation de noms

Les règles fondamentales suivantes permettent aux applications de créer et de traiter des noms valides pour les fichiers et les répertoires, quel que soit le système de fichiers :

-   Utilisez un point pour séparer le nom de fichier de base de l’extension dans le nom d’un répertoire ou d’un fichier.
-   Utilisez une barre oblique inverse ( \\ ) pour séparer les *composants* d’un *chemin d’accès*. La barre oblique inverse sépare le nom de fichier du chemin d’accès et un nom de répertoire d’un autre nom de répertoire dans un chemin d’accès. Vous ne pouvez pas utiliser une barre oblique inverse dans le nom du fichier ou du répertoire réel, car il s’agit d’un caractère réservé qui sépare les noms en composants.
-   Utilisez une barre oblique inverse si nécessaire dans le cadre des [noms de volume](naming-a-volume.md), par exemple, « c : \\ » dans « c : \\ path \\ file » ou « \\ \\ Server \\ share » dans « \\ \\ Server \\ share \\ path \\ file » pour les noms UNC (Universal Naming Convention). Pour plus d’informations sur les noms UNC, consultez la section limitation de la [longueur maximale du chemin d’accès](#maximum-path-length-limitation) .
-   Ne supposez pas le respect de la casse. Par exemple, considérez les noms OSCAR, Oscar et Oscar comme identiques, même si certains systèmes de fichiers (tels qu’un système de fichiers compatible POSIX) peuvent être considérés comme différents. Notez que NTFS prend en charge la sémantique POSIX pour le respect de la casse, mais ce n’est pas le comportement par défaut. Pour plus d’informations, consultez [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).
-   Les indicateurs de volume (lettres de lecteur) ne respectent pas la casse. Par exemple, « D : \\ » et « d : » \\ font référence au même volume.
-   Utilisez n’importe quel caractère de la page de codes actuelle pour un nom, y compris les caractères Unicode et les caractères dans le jeu de caractères étendus (128 – 255), à l’exception des éléments suivants :

    -   Les caractères réservés suivants :

        -   < (inférieur à)
        -   \> (supérieur à)
        -   : (deux-points)
        -   " (guillemet double)
        -   / (barre oblique)
        -   \\ vers
        -   \| (barre verticale ou canal)
        -   ? (point d’interrogation)
        -   \* sert

    -   Valeur entière zéro, parfois appelée « caractère *nul* ASCII ».
    -   Les caractères dont les représentations entières sont comprises dans la plage comprise entre 1 et 31, à l’exception des flux de données alternatifs où ces caractères sont autorisés. Pour plus d’informations sur les flux de fichiers, consultez [flux de fichiers](file-streams.md).
    -   Tout autre caractère qui n’est pas autorisé par le système de fichiers cible.

-   Utilisez un point comme *composant* de répertoire dans un chemin d’accès pour représenter le répertoire actif, par exemple «. \\temp.txt». Pour plus d’informations, consultez [chemins d’accès](#fully-qualified-vs-relative-paths).
-   Utilisez deux points consécutifs (..) comme *composant* de répertoire dans un chemin d’accès pour représenter le parent du répertoire actif, par exemple «.. \\temp.txt». Pour plus d’informations, consultez [chemins d’accès](#fully-qualified-vs-relative-paths).
-   N’utilisez pas les noms réservés suivants pour le nom d’un fichier :

    CON, PRN, aux, NUL, COM1, COM2, COM3, COM4, COM5, COM6, COM7, COM8, COM9, LPT1, LPT2, LPT3, LPT4, LPT5, LPT6, LPT7, LPT8 et LPT9. Évitez également que ces noms soient immédiatement suivis par une extension ; par exemple, NUL.txt n’est pas recommandé. Pour plus d’informations, consultez l’article [Espaces de noms](#win32-file-namespaces).

-   Ne terminez pas un nom de fichier ou de répertoire par un espace ou un point. même si le système de fichiers sous-jacent peut prendre en charge ces noms, le shell Windows et l’interface utilisateur ne le sont pas. Toutefois, il est acceptable de spécifier un point comme premier caractère d’un nom. Par exemple, « . Temp ».

### <a name="short-vs-long-names"></a>Noms courts et noms longs

Un nom de fichier long est considéré comme n’importe quel nom de fichier qui dépasse la petite Convention de nommage de style MS-DOS (également appelée *8,3*). lorsque vous créez un nom de fichier long, Windows peut également créer une forme abrégée 8,3 du nom, appelée *alias 8,3* ou nom abrégé, et le stocker sur le disque également. Cette 8,3 d’alias peut être désactivée pour des raisons de performances à l’échelle du système ou pour un volume spécifique, selon le système de fichiers.

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** 8,3 les alias ne peuvent pas être désactivés pour les volumes spécifiés tant que Windows 7 et Windows Server 2008 R2.

Dans de nombreux systèmes de fichiers, un nom de fichier contient un tilde (~) à l’intérieur de chaque composant du nom qui est trop long pour être conforme aux règles d’affectation de noms 8,3.

> [!Note]  
> Tous les systèmes de fichiers ne suivent pas la Convention de substitution tilde, et les systèmes peuvent être configurés pour désactiver la génération d’alias 8,3 même s’ils le prennent normalement en charge. Par conséquent, ne supposez pas que l’alias 8,3 existe déjà sur le disque.

 

Pour demander des noms de fichiers 8,3, des noms de fichiers longs ou le chemin d’accès complet d’un fichier du système, envisagez les options suivantes :

-   Pour obtenir la forme 8,3 d’un nom de fichier long, utilisez la fonction [**GetShortPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getshortpathnamew) .
-   Pour obtenir la version de nom de fichier long d’un nom abrégé, utilisez la fonction [**GetLongPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getlongpathnamea) .
-   Pour obtenir le chemin d’accès complet à un fichier, utilisez la fonction [**GetFullPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) .

sur les systèmes de fichiers plus récents, tels que NTFS, exFAT, udf et FAT32, Windows stocke les noms de fichiers longs sur le disque en Unicode, ce qui signifie que le nom de fichier long d’origine est toujours préservé. Cela est vrai même si un nom de fichier long contient des caractères étendus, quelle que soit la page de codes active au cours d’une opération de lecture ou d’écriture sur le disque.

les fichiers utilisant des noms de fichiers longs peuvent être copiés entre les partitions du système de fichiers NTFS et les partitions du système de fichiers FAT Windows sans perdre les informations de nom de fichier. Cela peut ne pas être le cas pour l’ancien FAT MS-DOS et certains types de systèmes de fichiers CDFS (CD-ROM), en fonction du nom de fichier réel. Dans ce cas, le nom de fichier bref est remplacé si possible.

## <a name="paths"></a>Chemins

Le *chemin d’accès* à un fichier spécifié se compose d’un ou de plusieurs *composants*, séparés par un caractère spécial (une barre oblique inverse), chaque composant étant généralement un nom de répertoire ou un nom de fichier, mais avec des exceptions notables présentées ci-dessous. Il est souvent essentiel que l’interprétation du système corresponde à l’aspect du début ou du *préfixe* du chemin d’accès. Ce préfixe détermine l' *espace de noms* utilisé par le chemin d’accès, ainsi que les caractères spéciaux qui sont utilisés dans la position dans le tracé, y compris le dernier caractère.

Si un composant d’un chemin d’accès est un nom de fichier, il doit s’agir du dernier composant.

Chaque composant d’un chemin d’accès est également limité par la longueur maximale spécifiée pour un système de fichiers particulier. En général, ces règles se répartissent en deux catégories : *short* et *long*. Notez que les noms de répertoires sont stockés par le système de fichiers en tant que type spécial de fichier, mais que les règles d’affectation de noms pour les fichiers s’appliquent également aux noms de répertoire. Pour résumer, un chemin d’accès est simplement la représentation sous forme de chaîne de la hiérarchie entre tous les répertoires qui existent pour un nom de fichier ou de répertoire particulier.

### <a name="fully-qualified-vs-relative-paths"></a>Chemins d’accès complets et chemins relatifs

pour les Windows fonctions d’API qui manipulent des fichiers, les noms de fichiers peuvent souvent être relatifs au répertoire actif, tandis que certaines api requièrent un chemin d’accès complet. Un nom de fichier est relatif au répertoire actif s’il ne commence pas par l’un des éléments suivants :

-   Nom UNC de n’importe quel format, qui commence toujours par deux barres obliques inverses (« \\ \\ »). Pour plus d'informations, consultez la section suivante.
-   Un indicateur de disque avec une barre oblique inverse, par exemple « C : \\ » ou « d : \\ ».
-   Une seule barre oblique inverse, par exemple « \\ Directory » ou « \\file.txt ». On parle également de *chemin absolu*.

Si un nom de fichier commence par un seul indicateur de disque mais pas par la barre oblique inverse après le signe deux-points, il est interprété comme un chemin d’accès relatif au répertoire actif sur le lecteur avec la lettre spécifiée. Notez que le répertoire actif peut ou non être le répertoire racine en fonction de ce qui a été défini lors de la dernière opération de modification de l’annuaire sur ce disque. Voici quelques exemples de ce format :

-   « C:tmp.txt » fait référence à un fichier nommé « tmp.txt » dans le répertoire actif sur le lecteur C.
-   « C :TEMPDIR \\tmp.txt » fait référence à un fichier dans un sous-répertoire du répertoire actif sur le lecteur C.

Un chemin d’accès est également dit relatif s’il contient des « doubles points »; autrement dit, deux points dans un composant du chemin d’accès. Ce spécificateur spécial est utilisé pour désigner le répertoire au-dessus du répertoire actif, également appelé « répertoire parent ». Voici quelques exemples de ce format :

-   "..\\tmp.txt» spécifie un fichier nommé tmp.txt situé dans le parent du répertoire actif.
-   "..\\..\\tmp.txt» spécifie un fichier qui se trouve deux répertoires au-dessus du répertoire actif.
-   "..\\ TEMPDIR \\tmp.txt» spécifie un fichier nommé tmp.txt situé dans un répertoire nommé TEMPDIR qui est un répertoire homologue du répertoire actif.

Les chemins d’accès relatifs peuvent combiner les deux exemples de types, par exemple «C :.. \\tmp.txt». Cela est utile car, même si le système effectue le suivi du lecteur actuel avec le répertoire actuel de ce lecteur, il garde également une trace des répertoires actuels dans chacune des différentes lettres de lecteur (si votre système en a plusieurs), quel que soit l’indicateur de lecteur défini en tant que lecteur actif.

### <a name="maximum-path-length-limitation"></a>Limitation de longueur maximale du chemin


dans les éditions de Windows antérieures à Windows 10 version 1607, la longueur maximale d’un chemin d’accès est un **\_ chemin d'** accès maximal, qui est défini sous la forme de 260 caractères. dans les versions ultérieures de Windows, il est nécessaire de modifier une clé de registre ou d’utiliser l’outil stratégie de groupe pour supprimer cette limite. Pour plus d’informations, consultez limitation de la [longueur maximale du chemin d’accès](./maximum-file-path-limitation.md) .


## <a name="namespaces"></a>Espaces de noms

il existe deux catégories principales de conventions d’espaces de noms utilisées dans les api Windows, communément appelées espaces de noms *NT* et *espaces de noms Win32*. L’espace de noms NT a été conçu pour être l’espace de noms de niveau le plus bas sur lequel d’autres sous-systèmes et espaces de noms pouvaient exister, y compris le sous-système Win32 et, par extension, les espaces de noms Win32. POSIX est un autre exemple de sous-système dans Windows qui repose sur l’espace de noms NT. les premières versions de Windows également défini plusieurs noms prédéfinis, ou réservés, pour certains périphériques spéciaux, tels que les ports de communication (série et parallèle) et la console d’affichage par défaut dans le cadre de ce qui est maintenant appelé espace de noms d’appareil NT, et sont toujours pris en charge dans les versions actuelles de Windows à des fins de compatibilité descendante.

### <a name="win32-file-namespaces"></a>Espaces de noms de fichier Win32

Les conventions et préfixes d’espaces de noms Win32 sont résumées dans cette section et dans la section suivante, avec les descriptions de leur utilisation. notez que ces exemples sont destinés à être utilisés avec les fonctions d’API Windows et ne fonctionnent pas tous nécessairement avec les applications de shell Windows telles que Windows Explorer. pour cette raison, il existe un éventail plus large de chemins possibles que ce qui est généralement disponible à partir des applications de l’interpréteur de commandes Windows, et Windows applications qui en tirent parti peuvent être développées à l’aide de ces conventions d’espace de noms.

pour les e/s de fichier, le \\ \\ \\ préfixe «  ? » d’une chaîne de chemin d’accès indique aux api Windows de désactiver toutes les analyses de chaîne et d’envoyer la chaîne qui la suit directement au système de fichiers. par exemple, si le système de fichiers prend en charge des chemins d’accès et des noms de fichiers volumineux, vous pouvez dépasser les limites **maximales de \_ chemin d’accès** qui sont autrement appliquées par les api Windows. Pour plus d’informations sur la limitation maximale normale du chemin d’accès, consultez la section précédente limitation de la [longueur maximale du chemin d’accès](#maximum-path-length-limitation).

Comme il désactive l’expansion automatique de la chaîne de chemin d’accès, le \\ \\ \\ préfixe «  ? » autorise également l’utilisation de « .. » et « . » dans les noms de chemins d’accès, ce qui peut être utile si vous tentez d’effectuer des opérations sur un fichier avec ces spécificateurs de chemin d’accès relatif réservés dans le cadre du chemin d’accès complet.

Bien que toutes les API d’e/s de fichier ne prennent pas en charge « \\ \\ ? \\ », vous devez consulter la rubrique de référence pour chaque API pour être sûr. 

Notez que les API Unicode doivent être utilisées pour s’assurer que le \\ \\ \\ préfixe «  ? » vous permet de dépasser le **\_ chemin d’accès maximal** 

### <a name="win32-device-namespaces"></a>Espaces de noms d’appareils Win32

Le \\ \\ \\ préfixe « . » accédera à l’espace de noms de l’appareil Win32 au lieu de l’espace de noms du fichier Win32. C’est ainsi que l’accès aux disques physiques et aux volumes est réalisé directement, sans passer par le système de fichiers, si l’API prend en charge ce type d’accès. Vous pouvez accéder à de nombreux appareils autres que les disques de cette manière (à l’aide des fonctions [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) et [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) , par exemple).

Par exemple, si vous souhaitez ouvrir le port de communication série 1 du système, vous pouvez utiliser « COM1 » dans l’appel à la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Cela fonctionne, car COM1 – COM9 fait partie des noms réservés dans l’espace de noms NT, bien que l’utilisation du \\ \\ \\ préfixe « . » fonctionne également avec ces noms d’appareils. Par comparaison, si vous avez installé une carte d’extension de port série 100 et que vous souhaitez ouvrir COM56, vous ne pouvez pas l’ouvrir à l’aide de « COM56 », car il n’existe pas d’espace de noms NT prédéfini pour COM56. Vous devrez l’ouvrir à l’aide de « \\ \\ . \\ COM56 ", car" \\ \\ . \\ "accède directement à l’espace de noms de l’appareil sans tenter de localiser un alias prédéfini.

Un autre exemple d’utilisation de l’espace de noms d’appareil Win32 utilise la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) avec « \\ \\ . \\ PhysicalDisk *x*"(où *x* est une valeur entière valide) ou" \\ \\ . \\ CdRom *X*». Cela vous permet d’accéder directement à ces appareils, en ignorant le système de fichiers. Cela fonctionne parce que ces noms d’appareils sont créés par le système, car ces périphériques sont énumérés, et certains pilotes créent également d’autres alias dans le système. Par exemple, le pilote de périphérique qui implémente le nom « C : \\ » a son propre espace de noms qui est également le système de fichiers.

Les API qui passent par la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) fonctionnent généralement avec le \\ \\ \\ préfixe « . », car **CreateFile** est la fonction utilisée pour ouvrir des fichiers et des périphériques, selon les paramètres que vous utilisez.

si vous utilisez Windows fonctions d’API, vous devez utiliser le \\ \\ \\ préfixe « . » pour accéder aux appareils uniquement et non aux fichiers.

La plupart des API ne prennent pas en charge « \\ \\ . \\ »; seules celles qui sont conçues pour fonctionner avec l’espace de noms d’appareil la reconnaissent. Vérifiez toujours la rubrique de référence pour chaque API pour vous en assurer.

### <a name="nt-namespaces"></a>Espaces de noms NT

il existe également des api qui autorisent l’utilisation de la convention d’espace de noms NT, mais le gestionnaire d’objets Windows fait cela inutile dans la plupart des cas. pour illustrer cela, il est utile de parcourir les espaces de noms Windows dans l’explorateur d’objets système à l’aide de l’outil Windows Sysinternals [WinObj](/sysinternals/downloads/winobj) . Quand vous exécutez cet outil, ce que vous voyez est l’espace de noms NT qui commence à la racine, ou « \\ ». Le sous-dossier appelé « Global ?? » est l’emplacement où l’espace de noms Win32 réside. Les objets d’appareil nommés résident dans l’espace de noms NT dans le sous-répertoire « Device ». Vous pouvez également trouver Serial0 et serial1, les objets d’appareil représentant les deux premiers ports COM s’ils sont présents sur votre système. Un objet appareil représentant un volume est semblable à « HarddiskVolume1 », bien que le suffixe numérique puisse varier. Le nom « DR0 » dans le sous-répertoire « Harddisk0 » est un exemple de l’objet appareil représentant un disque, et ainsi de suite.

pour rendre ces objets périphériques accessibles par Windows applications, les pilotes de périphérique créent un lien symbolique (symlink) dans l’espace de noms Win32, « Global ?? », vers leurs objets périphériques respectifs. Par exemple, COM0 et COM1 sous « global ?? » le sous-répertoire est simplement liens symboliques à Serial0 et serial1, "C :" est un lien symbolique vers HarddiskVolume1, "Physicaldrive0" est un lien symbolique vers DR0, et ainsi de suite. sans symlink, un appareil spécifié « Xxx » ne sera disponible pour aucune application Windows utilisant les conventions d’espace de noms Win32 comme décrit précédemment. Toutefois, un descripteur peut être ouvert sur cet appareil à l’aide d’API qui prennent en charge le chemin d’accès absolu de l’espace de noms NT au format « \\ Device \\ xxx ».

Avec l’ajout de la prise en charge de plusieurs utilisateurs via les services Terminal Server et les machines virtuelles, il est plus nécessaire de virtualiser l’appareil racine à l’ensemble du système dans l’espace de noms Win32. Pour ce faire, vous devez ajouter le lien symbolique nommé « GLOBALROOT » à l’espace de noms Win32, que vous pouvez voir dans le « Global ?? » sous-répertoire de l’outil de navigateur WinObj abordé précédemment et pouvant accéder via le chemin d’accès « \\ \\ ? \\ GLOBALROOT". Ce préfixe garantit que le chemin d’accès qui le suit se trouve dans le chemin d’accès racine réel du gestionnaire d’objets système et non dans un chemin d’accès dépendant de la session.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comparaison des fonctionnalités du système de fichiers](filesystem-functionality-comparison.md)
</dt> </dl>

 

 