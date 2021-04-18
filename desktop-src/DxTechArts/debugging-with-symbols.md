---
title: Débogage avec des symboles
description: Cet article fournit une vue d’ensemble de l’utilisation optimale des symboles dans votre processus de débogage.
ms.assetid: 7ce0c9c7-485c-8d72-0353-27fd2e369a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff63e2404a07a2f0ab5adcb156d83dc989b42fd4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508017"
---
# <a name="debugging-with-symbols"></a>Débogage avec des symboles

Cet article fournit une vue d’ensemble de l’utilisation optimale des symboles dans votre processus de débogage. Il explique comment utiliser le serveur de symboles Microsoft et comment configurer et utiliser votre propre serveur de symboles privé. Ces meilleures pratiques peuvent vous aider à augmenter votre efficacité et votre capacité à déboguer les problèmes, même dans les cas où tous les symboles et fichiers exécutables liés à un problème ne se trouvent pas sur votre ordinateur.

-   [Symboles](#debugging-with-symbols)
-   [Utilisation de symboles pour le débogage](#using-symbols-for-debugging)
-   [Obtention des symboles dont vous avez besoin](#getting-the-symbols-you-need)
    -   [Vérifier si une DLL ou un fichier. exe donné et PDB dans le même dossier correspondent](#check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match)
    -   [Vérifier si toutes les dll et tous les fichiers exécutables d’un ensemble de dossiers ont des pdb correspondants](#check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs)
    -   [Fonctionnement de Symchk](#how-symchk-works)
-   [Serveurs de symboles](#symbol-servers)
-   [Utilisation du serveur de symboles Microsoft](#using-the-microsoft-symbol-server)
-   [Obtention manuelle des symboles](#getting-symbols-manually)
-   [Configuration d’un serveur de symboles](#setting-up-a-symbol-server)
-   [Ajout de symboles à un serveur de symboles](#adding-symbols-to-a-symbol-server)
-   [Bonnes pratiques](#best-practices)

## <a name="symbols"></a>symboles

Un certain nombre de types différents de symboles sont disponibles pour le débogage. Ils incluent les symboles CodeView, COFF, DBG, SYM, PDB et même les symboles d’exportation générés à partir d’une table d’exportation de fichiers binaires. Ce livre blanc traite uniquement VS.NET et les symboles de format PDB, car il s’agit du format le plus récent et préféré. Ils sont générés par défaut pour les projets qui sont compilés à l’aide de Visual Studio.

La génération de fichiers PDB pour les exécutables de version n’affecte pas les optimisations ou la modification significative de la taille des fichiers générés. En règle générale, la seule différence est le chemin d’accès et le nom de fichier du fichier PDB est incorporé dans l’exécutable. Pour cette raison, vous devez toujours produire des fichiers PDB, même si vous ne souhaitez pas les livrer avec l’exécutable.

Les fichiers PDB sont générés si un projet est généré à l’aide du commutateur de compilateur **/Zi** ou **/Zi** (produire les informations PDB), ainsi que du commutateur de l’éditeur de liens **/Debug** (générer les informations de débogage). Les fichiers PDB générés par le compilateur sont combinés et écrits dans un fichier PDB unique qui est placé dans le même répertoire que l’exécutable.

Par défaut, les fichiers PDB contiennent les informations suivantes :

-   Symboles publics (en général, toutes les fonctions, variables statiques et variables globales)
-   Liste des fichiers objets qui sont responsables des sections de code dans l’exécutable
-   Informations d’optimisation du pointeur de frame (FPO)
-   Informations de nom et de type pour les variables locales et les structures de données
-   Informations sur le fichier source et le numéro de ligne

Si vous craignez que des personnes utilisent les informations de fichier PDB pour les aider à rétroconcevoir votre exécutable, vous pouvez également générer des fichiers PDB supprimés à l’aide de l’option de l’éditeur de liens **/PDBSTRIPPED : filename** . Si vous disposez de fichiers PDB existants à partir desquels vous voulez supprimer des informations privées, vous pouvez utiliser un outil appelé pdbcopy, qui fait partie des outils de débogage pour Windows.

Par défaut, les fichiers PDB supprimés contiennent les informations suivantes :

-   Symboles publics (en général, seules les fonctions non statiques et les variables globales)
-   Liste des fichiers objets qui sont responsables des sections de code dans l’exécutable
-   Informations d’optimisation du pointeur de frame (FPO)

Il s’agit des informations minimales requises pour autoriser le débogage fiable. Les informations minimales rendent également difficile l’obtention d’informations supplémentaires sur votre code source d’origine. Étant donné qu’un fichier PDB supprimé et un fichier PDB standard sont générés, vous pouvez fournir la version supprimée aux utilisateurs qui ont besoin de capacités de débogage limitées, tout en conservant la confidentialité complète des fichiers PDB. Notez que **/PDBSTRIPPED** génère un deuxième fichier PDB plus petit, donc assurez-vous que vous utilisez le fichier PDB correct lorsque vous générez des builds à distribuer de manière générale. Pour un projet standard, un fichier PDB standard peut avoir une taille de quelques mégaoctets, mais une version supprimée du fichier PDB peut être seulement de quelques centaines de kilo-octets.

## <a name="using-symbols-for-debugging"></a>Utilisation de symboles pour le débogage

Quand vous déboguez une application qui s’est bloquée, le débogueur tente de vous montrer les fonctions de la pile qui ont conduit à l’incident. Sans fichier PDB, le débogueur ne peut pas résoudre les noms de fonction, leurs paramètres ou toute variable locale stockée sur la pile. Si vous déboguez des exécutables 32 bits, il existe des situations où vous ne pouvez pas même vous procurer des traces de pile fiables sans symboles. Il est parfois possible d’examiner les valeurs brutes de la pile, et de déterminer les valeurs qui peuvent être des adresses de retour, mais elles peuvent être facilement confondues avec les références de fonction ou les données.

Si les fonctions de la pile active ont été compilées à l’aide de l’optimisation de pointeurs de frames (**/Oy**) et si les symboles ne sont pas présents, le débogueur ne peut pas déterminer de manière fiable la fonction appelée la fonction active. En effet, sans les informations d’optimisation du pointeur de frame (FPO) que PDB contiennent, le débogueur ne peut pas reposer sur le registre de pointeur de frame (EBP) pour pointer vers le pointeur de frame précédent enregistré et à l’adresse de retour de la fonction parente. Au lieu de cela, il devine. Parfois, il est correct. Toutefois, il est souvent erroné, ce qui peut être trompeur. Si vous voyez un avertissement concernant des symboles manquants ou si aucun symbole n’est chargé, comme dans l’exemple suivant, ne faites pas confiance à la pile à partir de ce point.

``` syntax
SWPerfTest.exe!TextFunction(... ...)    Line 59    C++
d3dx9d.dll!008829b5()
[Frames below may be incorrect and/or missing, no symbols loaded for d3dx9d.dll]
SWPerfTest.exe!main(int argc=, const char * * argv=)  Line 328 + 0x12 bytes     C++
SWPerfTest.exe!__mainCRTStartup() Line 716 + 0x17 bytes    C
kernel32.dll!@BaseThreadInitThunk@12() + 0x12 bytes
ntdll.dll!__RtlUserThreadStart@8() + 0x27 bytes
```

Dans de nombreux cas, il est possible de continuer le débogage sans symboles, car le problème se trouve dans un emplacement avec des symboles exacts, et vous n’avez pas besoin d’examiner les fonctions plus loin dans la pile des appels. Même si une bibliothèque qui se trouve dans votre pile des appels n’a pas de PDB disponibles, tant qu’ils ont été compilés avec des pointeurs de frame, le débogueur doit être en mesure de deviner correctement les fonctions parentes. À compter de Windows XP Service Pack 2, tous les fichiers DLL et exécutables Windows sont compilés avec FPO désactivé, car cela rend le débogage plus précis. La désactivation de FPO permet également aux profileurs d’échantillonnage de parcourir la pile pendant l’exécution, avec un impact minime sur les performances. Dans les versions de Windows antérieures à Windows XP SP2, tous les fichiers binaires du système d’exploitation nécessitent des fichiers de symboles correspondants qui contiennent des informations FPO, pour permettre un débogage et un profilage précis.

Si vous déboguez des exécutables natifs 64 bits, vous n’avez pas besoin de fichiers de symboles pour produire des traces de pile valides, car les systèmes d’exploitation et les compilateurs x64 sont conçus pour ne pas les exiger. Toutefois, vous avez toujours besoin de fichiers de symboles pour récupérer les noms de fonction, les paramètres d’appel et les variables locales.

Toutefois, certains cas sont particulièrement difficiles à déboguer sans symboles. Par exemple, si vous déboguez un programme pour lequel vous avez généré un fichier PDB et si vous bloquez un rappel d’une fonction dans une DLL pour laquelle vous n’avez pas de symboles, vous ne pourrez pas voir quelle fonction a provoqué le rappel, car vous ne pourrez pas décoder la pile. Cela se produit fréquemment dans les bibliothèques tierces, si les fichiers PDB ne sont pas fournis ou dans les anciens composants du système d’exploitation, si les fichiers PDB ne sont pas disponibles. Les rappels se produisent souvent pendant le passage de messages, l’énumération, l’allocation de mémoire ou la gestion des exceptions. Le débogage de ces fonctions sans une pile précise peut être frustrant.

Pour déboguer de manière fiable les mini-vidages qui sont générés sur un autre ordinateur ou qui se sont bloqués dans du code dont vous n’êtes pas propriétaire, il est important de pouvoir accéder à tous les symboles et binaires des fichiers exécutables référencés dans le mini-vidage. Si les symboles et les binaires sont disponibles à partir d’un serveur de symboles, ils sont automatiquement obtenus par le débogueur. Pour plus d’informations sur les mini-vidages, consultez le livre blanc [analyse de vidage sur incident](/windows/desktop/DxTechArts/crash-dump-analysis) .

## <a name="getting-the-symbols-you-need"></a>Obtention des symboles dont vous avez besoin

Visual Studio et d’autres débogueurs Microsoft, tels que WinDbg, sont généralement configurés pour fonctionner uniquement si vous générez une application et que vous la déboguez sur votre propre ordinateur. Si vous avez besoin de fournir votre exécutable à une autre personne, si vous avez plusieurs versions d’une DLL ou d’un fichier. exe sur votre ordinateur, ou si vous souhaitez déboguer avec précision une application qui utilise Windows ou d’autres bibliothèques, telles que DirectX, vous devez comprendre comment les débogueurs recherchent et chargent les symboles. Le débogueur utilise soit le chemin de recherche de symboles spécifié par l’utilisateur, qui se trouve dans options de \\ débogage \\ symboles dans Visual Studio, soit la \_ \_ \_ variable d’environnement chemin d’accès aux symboles NT. En règle générale, le débogueur recherche les fichiers PDB correspondants aux emplacements suivants :

-   Emplacement spécifié à l'intérieur de la DLL ou du fichier exécutable.

    Si vous avez créé une DLL ou un fichier exécutable sur votre ordinateur, par défaut, l’éditeur de liens place le chemin d’accès complet et le nom du fichier PDB associé à l’intérieur de la DLL ou du fichier exécutable. Quand vous déboguez, le débogueur vérifie d’abord si le fichier de symboles existe dans l’emplacement spécifié dans la DLL ou le fichier exécutable. Cela est utile, car vous avez toujours des symboles disponibles pour le code que vous avez compilé sur votre ordinateur.

-   Fichiers PDB qui peuvent être présents dans le même dossier que la DLL ou le fichier exécutable.
-   Tout dossier de cache de symboles local.
-   Tous les serveurs de symboles de partage de fichiers de réseau local.
-   Tous les serveurs de symboles Internet, tels que le serveur de symboles Microsoft.

Pour vous assurer que vous disposez de tous les fichiers PDB dont vous avez besoin pour un débogage précis, installez les outils de débogage pour Windows. Les versions 32 et 64 bits se trouvent dans [outils de débogage pour Windows](/windows-hardware/drivers/debugger/).

symchk.exe est un outil utile qui est installé avec ce package. Il peut aider à identifier les symboles manquants ou incorrects. Cet outil comporte un grand nombre d’options de ligne de commande potentielles. Voici deux des plus utiles et les plus couramment utilisés.

### <a name="check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match"></a>Vérifier si une DLL ou un fichier. exe donné et PDB dans le même dossier correspondent

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" testing.dll /s

SYMCHK: FAILED files = 0
SYMCHK: PASSED + IGNORED files = 1
```

L’option **/s** indique à **Symchk** de rechercher les symboles uniquement dans le dossier actif, et de ne pas consulter les serveurs de symboles.

### <a name="check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs"></a>Vérifier si toutes les dll et tous les fichiers exécutables d’un ensemble de dossiers ont des pdb correspondants

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" *.* /r
```

L’option **/r** définit **Symchk** pour parcourir de manière récursive les dossiers, afin de vérifier que tous les fichiers exécutables ont des fichiers PDB correspondants. Sans l’option **/s** , **Symchk** utilise le \_ \_ \_ chemin d’accès aux symboles NT en cours pour rechercher des symboles sur un serveur privé ou local, ou sur les serveurs de symboles Microsoft. L’outil **Symchk** recherche uniquement les symboles pour les fichiers exécutables (. exe,. dll et similaires). Vous ne pouvez pas utiliser des caractères génériques pour rechercher des symboles pour les fichiers non exécutables.

### <a name="how-symchk-works"></a>Fonctionnement de Symchk

Lorsque l’éditeur de liens génère des fichiers. dll, exécutables et PDB, il stocke des GUID identiques dans chaque fichier. Le GUID est utilisé par les outils pour déterminer si un fichier PDB donné correspond à une DLL ou à un fichier exécutable. Si vous modifiez une DLL ou un fichier exécutable (à l’aide d’un éditeur de ressources ou d’un encodage de protection de copie, ou en modifiant ses informations de version), le GUID est mis à jour et le débogueur ne peut pas charger le fichier PDB. Pour cette raison, il est très important de ne pas manipuler la DLL ou le fichier exécutable après sa création par l’éditeur de liens.

Vous pouvez également utiliser l’utilitaire DUMPBIN fourni avec VS.NET pour afficher les chemins d’accès aux symboles recherchés et pour voir si des fichiers de symboles qui correspondent à une DLL ou à un fichier exécutable donné sont trouvés. Par exemple :

``` syntax
DUMPBIN /PDBPATH:VERBOSE filename.exe
```

## <a name="symbol-servers"></a>Serveurs de symboles

Un serveur de symboles est un référentiel pour plusieurs versions des fichiers exécutables et de symboles. Il contient les fichiers de symboles eux-mêmes ou les pointeurs vers les fichiers de symboles associés. Les débogueurs comprennent l’utilisation des serveurs de symboles et peuvent les utiliser pour rechercher des symboles manquants ou inconnus.

La DLL et les fichiers exécutables sont également disponibles à partir du serveur de symboles Microsoft. Cela permet de déboguer les incidents et d’examiner le code pour les fichiers de système d’exploitation qui peuvent ne pas exister sur votre ordinateur. Si un débogueur rencontre un fichier exécutable ou une DLL qui n’existe pas sur le système que vous utilisez pour le débogage, il demande automatiquement les symboles et une copie du fichier binaire à partir des serveurs de symboles Microsoft. Cela est utile si vous déboguez un composant qui comporte de nombreuses versions (par exemple, msvcrt.dll) et que vous devez examiner le code pour une version qui n’existe pas sur votre ordinateur. Cela permet également de déboguer les mini-vidages générés sur un système d’exploitation différent du système que vous utilisez pour le débogage.

Microsoft publie tous les fichiers PDB pour tous les systèmes d’exploitation et autres composants redistribués, tels que le kit de développement logiciel (SDK) DirectX, sur son serveur de symboles accessible en externe. Cela facilite le débogage d’une application qui utilise ces fichiers DLL ou exécutables. Vous pouvez utiliser le serveur de symboles Microsoft pour résoudre les symboles, ainsi que tous les symboles locaux des composants qui ont été créés sur votre ordinateur.

Vous pouvez configurer votre ordinateur pour qu’il utilise le serveur de symboles Microsoft, qui vous permet d’accéder à tous les fichiers de symboles Microsoft. Vous pouvez également configurer un serveur de symboles privé pour votre entreprise, votre équipe ou votre réseau, qui peut être utilisé pour stocker plusieurs versions antérieures d’un projet sur lequel vous travaillez, ou pour fournir un cache local pour les symboles que vous utilisez à partir du serveur de symboles Microsoft.

Pour utiliser un serveur de symboles, spécifiez le chemin de recherche dans une variable d’environnement appelée \_ \_ \_ chemin d’accès aux symboles NT. Les débogueurs et les outils modernes, tels que WinDbg, NTSD ou Visual Studio, utilisent automatiquement ce chemin d’accès pour rechercher des symboles.

Quand un débogueur recherche des symboles, il commence par Rechercher localement. Il recherche ensuite les serveurs de symboles. Lorsqu’il trouve un symbole correspondant, il transfère le fichier de symboles dans votre cache local. La taille des symboles d’une DLL ou d’un fichier exécutable standard est comprise entre 1 et 100 Mo. Par conséquent, si vous déboguez un processus qui comprend de nombreuses dll, il peut être nécessaire de résoudre tous les symboles et de les transférer vers un cache local.

## <a name="using-the-microsoft-symbol-server"></a>Utilisation du serveur de symboles Microsoft

Le serveur de symboles Microsoft vous permet d’obtenir tous les symboles les plus récents, y compris les symboles des fichiers corrigés ou mis à jour. Le serveur de symboles Microsoft est disponible à l’adresse <https://msdl.microsoft.com/download/symbols> .

Vous pouvez accéder au serveur de symboles de l’une des manières suivantes :

-   Entrez l’adresse du serveur directement. Dans Visual Studio, dans le menu **Outils** , choisissez **options**, puis **débogage**, puis **symboles**.
-   Utilisez le \_ \_ chemin d’accès aux symboles NT de la variable \_ d’environnement. Nous recommandons cette méthode.

    Cela est utilisé par tous les outils de débogage. Elle est également utilisée par Visual Studio et est lue et décodée quand Visual Studio s’ouvre. Par conséquent, si vous le modifiez, vous devez redémarrer Visual Studio.

    Cette variable d’environnement vous permet de spécifier plusieurs serveurs de symboles, par exemple un serveur de symboles privé interne. Elle vous permet également de spécifier un répertoire de cache local pour stocker des fichiers PDB pour tous les symboles que vous recherchez à partir de serveurs de symboles, à la fois en interne et sur Internet.

La syntaxe de la \_ \_ variable de \_ chemin d’accès aux symboles NT est la suivante :

``` syntax
srv*[local cache]*[private symbol server]*https://msdl.microsoft.com/download/symbols
```

Remplacez \[ le cache local \] par le nom d’un répertoire sur votre ordinateur où vous souhaitez stocker un cache de tous les symboles utilisés, par exemple,% systemroot% \\ Symbols ou c : \\ Symbols.

Le \[ serveur de symboles privés \] est facultatif. Il peut pointer vers un serveur de symboles situé sur votre réseau, ou il peut pointer vers un serveur de symboles qui est partagé par votre équipe, groupe de produits ou société.

Pour utiliser uniquement le serveur de symboles Microsoft avec un cache local de symboles, pour accélérer l’accès via Internet, utilisez le paramètre suivant pour le \_ \_ chemin d’accès aux symboles NT \_ :

``` syntax
srv*c:\symbols*https://msdl.microsoft.com/download/symbols
```

Vous trouverez d’autres options pour le \_ \_ \_ chemin d’accès aux symboles NT dans le fichier d’aide qui est installé avec le package outils de débogage Microsoft pour Windows.

Les exécutables sans symboles peuvent augmenter le temps nécessaire au lancement d’un débogueur si vous utilisez un serveur de symboles. Cela est dû au fait que le débogueur interroge le serveur de symboles chaque fois qu’il essaie de charger l’exécutable. Pour cette raison, il est préférable de toujours demander des symboles pour tous les composants.

Il se peut qu’il ne soit pas possible de demander des symboles pour chaque composant (par exemple, les pilotes vidéo peuvent avoir des dll dans votre espace de processus et les fichiers PDB requis sont disponibles sur le serveur de symboles Microsoft. Dans ce cas, il y a un petit délai quand vous démarrez une session de débogage.

Pour éviter même ce petit délai, vous pouvez exécuter le débogueur une seule fois, pour mettre en cache tous les symboles localement à partir du serveur de symboles Microsoft. Ensuite, modifiez \_ \_ \_ le chemin d’accès aux symboles NT pour supprimer le serveur de symboles Microsoft. À moins que les fichiers exécutables ne soient modifiés, les recherches de fichiers exécutables qui n’ont pas de symboles ne nécessitent pas de requête sur Internet, car vous avez des copies en cache locales de tous les symboles dont vous avez besoin à partir du serveur de symboles Microsoft.

## <a name="getting-symbols-manually"></a>Obtention manuelle des symboles

Si vous avez correctement configuré votre débogueur, il charge automatiquement tous les symboles nécessaires à partir de votre cache local ou d’un serveur de symboles. Si vous souhaitez obtenir les symboles d’un seul exécutable ou d’un dossier d’exécutables, vous pouvez utiliser **Symchk**. Par exemple, si vous souhaitez télécharger les symboles pour le fichier de \_30.dll d3dx9 dans le dossier système Windows dans le répertoire actif, vous pouvez utiliser la commande suivante :

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" c:\Windows\System32\d3dx9_30.dll /oc \.
```

L’outil **Symchk** a de nombreuses autres utilisations. Pour plus d’informations, consultez **Symchk/ ?**, ou consultez la documentation Microsoft débogage Tools pour Windows.

## <a name="setting-up-a-symbol-server"></a>Configuration d’un serveur de symboles

La configuration d’un serveur de symboles est très simple. Elle est utile pour les raisons suivantes :

-   Pour économiser de la bande passante ou pour accélérer la résolution des symboles pour votre entreprise, votre équipe ou votre produit. Un serveur de symboles interne sur un partage de fichiers local sur votre réseau met en cache toutes les références aux serveurs de symboles externes, tels que le serveur de symboles Microsoft. Un serveur de symboles local ou interne est accessible rapidement par de nombreuses personnes. Par conséquent, elle économise la bande passante et la latence que les demandes de symboles dupliquées peuvent créer.
-   Pour stocker des symboles pour les anciennes builds, versions ou versions externes de votre application. En stockant les symboles de ces builds sur un serveur de symboles auquel vous pouvez accéder facilement, vous pouvez déboguer des incidents et des problèmes dans ces builds sur n’importe quel ordinateur doté d’un débogueur et d’une connexion au serveur de symboles local. Cela s’avère particulièrement utile si vous déboguez des mini-vidages générés par des exécutables que vous n’avez pas créés vous-même, c’est-à-dire des builds qui ont été générées par un autre programmeur ou par un ordinateur de Build. Si les symboles de ces Builds sont stockés sur votre serveur de symboles, vous obtiendrez un débogage fiable et précis.
-   Pour tenir à jour les symboles. Lorsque les composants sont mis à jour, tels que les composants du système d’exploitation qui sont modifiés par Windows Update ou par le kit de développement logiciel (SDK) DirectX, vous pouvez toujours déboguer à l’aide de tous les symboles les plus récents.

La configuration d’un serveur de symboles sur votre propre réseau local est aussi simple que la création d’un partage de fichiers sur un serveur et l’octroi d’autorisations complètes aux utilisateurs pour accéder au partage, afin de créer des fichiers et des dossiers. Ce partage doit être créé sur un système d’exploitation serveur, tel que Windows Server 2003, de sorte que le nombre de personnes qui peuvent accéder simultanément au partage n’est pas limité.

Par exemple, si vous configurez un partage de fichiers sur les \\ \\ \\ symboles mainserver, les membres de votre équipe définissent le \_ \_ \_ chemin d’accès aux symboles NT comme suit :

``` syntax
Srv*c:\symbols*\\mainserver\symbols*https://msdl.microsoft.com/download/symbols
```

À mesure que les symboles sont récupérés, les fichiers et les dossiers apparaissent dans le \\ \\ \\ répertoire partagé de symboles mainserver, ainsi que dans les caches individuels, dans le répertoire c : \\ Symbols.

Il s’agit en général de tout ce qui est impliqué dans la configuration et l’utilisation de votre propre serveur de symboles ou du serveur de symboles Microsoft.

## <a name="adding-symbols-to-a-symbol-server"></a>Ajout de symboles à un serveur de symboles

Pour ajouter, supprimer ou modifier des fichiers sur un partage de serveur de symboles, utilisez l’outil symstore.exe. Cet outil fait partie du package outils de débogage Microsoft pour Windows. La documentation complète sur les serveurs de symboles, l’outil SymStore et les symboles d’indexation est incluse dans le package outils de débogage pour Windows.

Vous pouvez ajouter des symboles directement à votre propre serveur de symboles, dans le cadre d’un processus de génération, ou pour rendre les symboles disponibles pour l’ensemble de votre équipe pour les bibliothèques ou les outils tiers. Le processus d’ajout d’un symbole à un partage de fichiers de serveur de symboles est appelé « symboles d’indexation ». Il existe deux façons courantes d’indexer des symboles. Un fichier de symboles peut être copié sur le serveur de symboles. Ou bien, un pointeur vers l’emplacement du symbole peut être copié sur le serveur de symboles. Si vous disposez d’un dossier d’archive qui contient vos anciennes builds, vous pouvez indexer les pointeurs vers les fichiers PDB qui se trouvent déjà sur le partage, au lieu de dupliquer les symboles. Étant donné que la taille des symboles peut parfois être de dizaines de mégaoctets, il est judicieux de planifier à l’avance l’espace dont vous pouvez avoir besoin pour archiver toutes les builds de votre projet tout au long du développement. Si vous indexez uniquement les pointeurs vers des symboles, vous risquez de rencontrer des problèmes si vous supprimez les anciennes builds ou si vous modifiez le nom d’un partage de fichiers.

Par exemple, pour indexer de manière récursive tous les symboles des symboles c : \\ dxsym \\ extras \\ que vous avez obtenus à partir du kit de développement logiciel (SDK) DirectX d’octobre 2006 sur un partage de fichiers de serveur de symboles appelé \\ \\ mainserver \\ Symbols, vous pouvez utiliser la commande suivante :

``` syntax
"c:\Program Files\Debugging Tools for Windows\symstore" add /f "C:\dxsym\Extras\Symbols\*.pdb"
/s \\mainserver\symbols /t "October 2006 DirectX SDK " /r
```

Le paramètre **/t "Comment"** est utilisé pour ajouter une description à la transaction qui a ajouté les symboles. Cela peut être utile lors de l’exécution de tâches d’administration sur les symboles.

## <a name="best-practices"></a>Bonnes pratiques

-   Configurez votre propre partage de fichiers de serveur de symboles pour votre équipe, société ou produit.
-   Configurez \_ \_ \_ le chemin d’accès des symboles NT pour qu’il pointe vers un cache local, un serveur de symboles privé et le serveur de symboles Microsoft.
-   Si un débogueur ne peut pas charger les symboles d’un composant que vous déboguez, contactez le propriétaire du composant pour demander des symboles, au moins un fichier PDB supprimé.
-   Configurez un système de génération automatisé pour indexer les symboles sur votre serveur de symboles privé pour chaque Build produite. Assurez-vous que les builds que vous distribuez sont les builds générées par ce processus. Cela permet de s’assurer que les symboles sont toujours disponibles pour les problèmes de débogage.
-   Configurez un serveur de symboles pour permettre aux débogueurs d’accéder au code source d’un module spécifique directement à partir d’un système de contrôle de code source Visual Source Safe ou Perforce. Si les informations de fichier source et les symboles d’une version finale d’un jeu sont indexés, les développeurs qui ont accès à votre serveur de symboles peuvent avoir un débogage complet au niveau de la source des problèmes signalés, sans conserver les environnements de génération ou les anciennes versions des fichiers sources sur leurs ordinateurs de développement. Pour configurer votre serveur de symboles afin d’autoriser l’indexation d’informations sur les fichiers sources, consultez la documentation du serveur source.

 

 