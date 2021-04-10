---
description: La bibliothèque DbgHelp utilise le chemin de recherche des symboles pour localiser les symboles de débogage (fichiers. pdb et. dbg). Le chemin de recherche peut être constitué d’un ou plusieurs éléments de chemin d’accès séparés par des points-virgules.
ms.assetid: 3527f589-285b-4cdf-b024-17920971a904
title: Chemins d'accès aux symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 977772e45c345e1e990dc038fccd852d17d279dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950542"
---
# <a name="symbol-paths"></a>Chemins d'accès aux symboles

La bibliothèque DbgHelp utilise le chemin de recherche des symboles pour localiser les symboles de débogage (fichiers. pdb et. dbg). Le chemin de recherche peut être constitué d’un ou plusieurs éléments de chemin d’accès séparés par des points-virgules.

## <a name="specifying-search-paths"></a>Spécification des chemins de recherche

Pour spécifier l’emplacement où le gestionnaire de symboles va rechercher les fichiers de symboles dans les répertoires de disque, appelez la fonction [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) . Vous pouvez également spécifier un chemin de recherche de symboles dans le paramètre *UserSearchPath* de la fonction [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .

Le paramètre *UserSearchPath* dans [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) et le paramètre *SearchPath* dans [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) prennent un pointeur vers une chaîne se terminant par un caractère null qui spécifie un chemin d’accès ou une série de chemins d’accès séparés par un point-virgule. Le gestionnaire de symboles utilise ces chemins d’accès pour rechercher des fichiers de symboles. Si ce paramètre a la **valeur null**, le gestionnaire de symboles recherche dans le répertoire qui contient le module pour lequel des recherches de symboles sont effectuées. Dans le cas contraire, si ce paramètre est spécifié en tant que valeur non **null** , le gestionnaire de symboles recherche d’abord les chemins d’accès définis par l’application avant de rechercher dans le répertoire du module. Si vous définissez le \_ \_ \_ chemin d’accès aux symboles NT ou la \_ \_ \_ \_ variable d’environnement du chemin d’accès aux symboles de Alt NT, le gestionnaire de symboles recherche les fichiers de symboles dans l’ordre suivant :

1. \_ \_ \_ Variable d’environnement du chemin d’accès aux symboles NT.
2. \_ \_ \_ \_ Variable d’environnement du chemin d’accès de symbole Alt de NT.
3. Répertoire qui contient le module correspondant.

Pour récupérer les chemins de recherche, appelez la fonction [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) .

Le chemin de recherche des fichiers de base de données du programme (. pdb) est différent du chemin d’accès des fichiers de débogage (. dbg). L’algorithme est déterminé par les fonctionnalités de la bibliothèque de symboles. Par défaut, Microsoft Visual C/C++ crée des symboles de format Microsoft, les supprime de l’image et les place dans un fichier. pdb distinct. En général, le fichier. pdb se trouve dans le répertoire qui contient l’image exécutable. Visual C/C++ incorpore le chemin d’accès absolu au fichier. pdb dans l’image exécutable. Si le gestionnaire de symboles ne peut pas trouver le fichier. pdb à cet emplacement ou si le fichier. pdb a été déplacé vers un autre répertoire, le gestionnaire de symboles trouvera le fichier. pdb à l’aide du chemin de recherche décrit pour les fichiers. dbg.

## <a name="path-element-types"></a>Types d’éléments Path

Il existe trois types d’éléments Path.

### <a name="standard-path-element"></a>Élément de chemin d’accès standard

Une recherche est effectuée dans un élément de chemin d’accès standard en examinant la racine du répertoire spécifié par l’élément Path. Le gestionnaire de symboles recherche également dans un sous-répertoire « Symbols » qui correspond à l’extension de fichier du module dans lequel les symboles sont recherchés. Il s’agit généralement de « dll », « exe » ou « sys ». Enfin, il recherche dans un sous-répertoire appelé « Symbols » un répertoire portant le même nom que l’extension. Par exemple, si l’élément de chemin d’accès aux symboles est « c : \\ mySymbols » et que le fichier dans lequel les symboles sont recherchés est « boo.dll », les répertoires suivants sont recherchés.

- c : \\ mySymbols  
- c : \\ mySymbols \\ dll  
- c : \\ mySymbols de \\ symboles \\ dll  

Le gestionnaire de symboles utilise cette logique pour rechercher dans tout élément de chemin d’accès qui ne répond pas aux critères d’être un *serveur de symboles* ou un *cache* (décrit ci-dessous).

### <a name="symbol-server-path-element"></a>Élément de chemin d’accès du serveur de symboles

Un élément de chemin d’accès du *serveur de symboles* utilise une technologie spéciale qui peut localiser un symbole qui correspond exactement au module en question. Pour plus d’informations, consultez [utilisation de symsrv](using-symsrv.md) .

Le gestionnaire de symboles traite un élément de chemin d’accès comme un serveur de symboles s’il commence par le texte « SRV \* ».

> [!Note]  
> Si le texte « SRV \* » n’est pas spécifié mais que l’élément de chemin d’accès réel est un magasin de serveurs de symboles, le gestionnaire de symboles agit comme si « SRV \* » avait été spécifié. Le gestionnaire de symboles effectue cette détermination en recherchant l’existence d’un fichier appelé « pingme.txt » dans le répertoire racine du chemin d’accès spécifié.

 

### <a name="cache-path-element"></a>Élément du chemin d’accès du cache

Un élément de chemin d’accès *du cache* est une variation sur un élément de chemin d’accès du serveur de symboles.

Ce répertoire est recherché comme n’importe quel autre serveur de symboles. Toutefois, si le symbole est introuvable ici et qu’il se trouve dans un élément Path plus loin dans la chaîne du chemin d’accès aux symboles, le symbole sera copié et stocké dans le serveur de symboles spécifié dans cet élément.

Le gestionnaire de symboles traite un élément de chemin d’accès comme un élément de cache s’il commence par le texte « cache \* ». Pour spécifier un cache dans « c : \\ myCache », utilisez un élément de chemin d’accès aux symboles « cache \* c : \\ myCache ».

## <a name="example-search-path"></a>Exemple de chemin de recherche

Pour voir comment cela fonctionne, définissez ce chemin de recherche.

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

Voici une liste de la sortie détaillée du gestionnaire de symboles lors de la recherche de ntdll. pdb, à l’aide du chemin de recherche répertorié ci-dessus.

```
DBGHELP: .\ntdll.pdb - file not found
DBGHELP: .\dll\ntdll.pdb - file not found
DBGHELP: .\symbols\dll\ntdll.pdb - file not found
SYMSRV: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb not found
SYMSRV: ntdll.pdb from \\symbols\symbols: 10497024 bytes - copied
DBGHELP: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb already cached
DBGHELP: ntdll - private symbols & lines
c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb
```

Les trois premières lignes de sortie affichent le gestionnaire de symboles qui traite le premier élément de chemin d’accès de `.` . Il s’agit d’un élément de chemin d’accès standard.

La quatrième ligne montre le gestionnaire de symboles à l’aide du serveur de symboles pour rechercher le fichier dans le deuxième élément de chemin d’accès `cache*c:\myCache` qui est un élément de chemin d’accès du cache.

La cinquième ligne indique que le fichier se trouve dans le troisième élément de chemin d’accès de `srv*\\symbols\symbols` , qui est un élément de chemin d’accès du serveur de symboles.

La sixième ligne indique que le fichier est copié dans le cache.

Les deux dernières lignes sur lesquelles le fichier est ouvert à partir du cache.
