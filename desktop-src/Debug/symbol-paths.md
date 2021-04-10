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
# <a name="symbol-paths"></a><span data-ttu-id="00e74-104">Chemins d'accès aux symboles</span><span class="sxs-lookup"><span data-stu-id="00e74-104">Symbol Paths</span></span>

<span data-ttu-id="00e74-105">La bibliothèque DbgHelp utilise le chemin de recherche des symboles pour localiser les symboles de débogage (fichiers. pdb et. dbg).</span><span class="sxs-lookup"><span data-stu-id="00e74-105">The DbgHelp library uses the symbol search path to locate debug symbols (.pdb and .dbg files).</span></span> <span data-ttu-id="00e74-106">Le chemin de recherche peut être constitué d’un ou plusieurs éléments de chemin d’accès séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="00e74-106">The search path can be made up of one or more path elements separated by semicolons.</span></span>

## <a name="specifying-search-paths"></a><span data-ttu-id="00e74-107">Spécification des chemins de recherche</span><span class="sxs-lookup"><span data-stu-id="00e74-107">Specifying Search Paths</span></span>

<span data-ttu-id="00e74-108">Pour spécifier l’emplacement où le gestionnaire de symboles va rechercher les fichiers de symboles dans les répertoires de disque, appelez la fonction [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) .</span><span class="sxs-lookup"><span data-stu-id="00e74-108">To specify where the symbol handler will search disk directories for symbol files, call the [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) function.</span></span> <span data-ttu-id="00e74-109">Vous pouvez également spécifier un chemin de recherche de symboles dans le paramètre *UserSearchPath* de la fonction [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="00e74-109">Alternatively, you can specify a symbol search path in the *UserSearchPath* parameter of the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span>

<span data-ttu-id="00e74-110">Le paramètre *UserSearchPath* dans [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) et le paramètre *SearchPath* dans [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) prennent un pointeur vers une chaîne se terminant par un caractère null qui spécifie un chemin d’accès ou une série de chemins d’accès séparés par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="00e74-110">The *UserSearchPath* parameter in [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) and the *SearchPath* parameter in [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) take a pointer to a null-terminated string that specifies a path, or series of paths separated by a semicolon.</span></span> <span data-ttu-id="00e74-111">Le gestionnaire de symboles utilise ces chemins d’accès pour rechercher des fichiers de symboles.</span><span class="sxs-lookup"><span data-stu-id="00e74-111">The symbol handler uses these paths to search for symbol files.</span></span> <span data-ttu-id="00e74-112">Si ce paramètre a la **valeur null**, le gestionnaire de symboles recherche dans le répertoire qui contient le module pour lequel des recherches de symboles sont effectuées.</span><span class="sxs-lookup"><span data-stu-id="00e74-112">If this parameter is **NULL**, the symbol handler searches the directory that contains the module for which symbols are being searched.</span></span> <span data-ttu-id="00e74-113">Dans le cas contraire, si ce paramètre est spécifié en tant que valeur non **null** , le gestionnaire de symboles recherche d’abord les chemins d’accès définis par l’application avant de rechercher dans le répertoire du module.</span><span class="sxs-lookup"><span data-stu-id="00e74-113">Otherwise, if this parameter is specified as a non-**NULL** value, the symbol handler first searches the paths set by the application before searching the module directory.</span></span> <span data-ttu-id="00e74-114">Si vous définissez le \_ \_ \_ chemin d’accès aux symboles NT ou la \_ \_ \_ \_ variable d’environnement du chemin d’accès aux symboles de Alt NT, le gestionnaire de symboles recherche les fichiers de symboles dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="00e74-114">If you set the \_NT\_SYMBOL\_PATH or \_NT\_ALT\_SYMBOL\_PATH environment variable, the symbol handler searches for symbol files in the following order:</span></span>

1. <span data-ttu-id="00e74-115">\_ \_ \_ Variable d’environnement du chemin d’accès aux symboles NT.</span><span class="sxs-lookup"><span data-stu-id="00e74-115">The \_NT\_SYMBOL\_PATH environment variable.</span></span>
2. <span data-ttu-id="00e74-116">\_ \_ \_ \_ Variable d’environnement du chemin d’accès de symbole Alt de NT.</span><span class="sxs-lookup"><span data-stu-id="00e74-116">The \_NT\_ALT\_SYMBOL\_PATH environment variable.</span></span>
3. <span data-ttu-id="00e74-117">Répertoire qui contient le module correspondant.</span><span class="sxs-lookup"><span data-stu-id="00e74-117">The directory that contains the corresponding module.</span></span>

<span data-ttu-id="00e74-118">Pour récupérer les chemins de recherche, appelez la fonction [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) .</span><span class="sxs-lookup"><span data-stu-id="00e74-118">To retrieve the search paths, call the [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) function.</span></span>

<span data-ttu-id="00e74-119">Le chemin de recherche des fichiers de base de données du programme (. pdb) est différent du chemin d’accès des fichiers de débogage (. dbg).</span><span class="sxs-lookup"><span data-stu-id="00e74-119">The search path for program database (.pdb) files is different than the path for debug (.dbg) files.</span></span> <span data-ttu-id="00e74-120">L’algorithme est déterminé par les fonctionnalités de la bibliothèque de symboles.</span><span class="sxs-lookup"><span data-stu-id="00e74-120">The algorithm is determined by the functionality of the symbol library.</span></span> <span data-ttu-id="00e74-121">Par défaut, Microsoft Visual C/C++ crée des symboles de format Microsoft, les supprime de l’image et les place dans un fichier. pdb distinct.</span><span class="sxs-lookup"><span data-stu-id="00e74-121">By default, Microsoft Visual C/C++ creates Microsoft format symbols, strips them from the image, and places them in a separate .pdb file.</span></span> <span data-ttu-id="00e74-122">En général, le fichier. pdb se trouve dans le répertoire qui contient l’image exécutable.</span><span class="sxs-lookup"><span data-stu-id="00e74-122">Typically, the .pdb file will be located in the directory that contains the executable image.</span></span> <span data-ttu-id="00e74-123">Visual C/C++ incorpore le chemin d’accès absolu au fichier. pdb dans l’image exécutable.</span><span class="sxs-lookup"><span data-stu-id="00e74-123">Visual C/C++ embeds the absolute path to the .pdb file in the executable image.</span></span> <span data-ttu-id="00e74-124">Si le gestionnaire de symboles ne peut pas trouver le fichier. pdb à cet emplacement ou si le fichier. pdb a été déplacé vers un autre répertoire, le gestionnaire de symboles trouvera le fichier. pdb à l’aide du chemin de recherche décrit pour les fichiers. dbg.</span><span class="sxs-lookup"><span data-stu-id="00e74-124">If the symbol handler cannot find the .pdb file in that location or if the .pdb file was moved to another directory, the symbol handler will locate the .pdb file using the search path described for .dbg files.</span></span>

## <a name="path-element-types"></a><span data-ttu-id="00e74-125">Types d’éléments Path</span><span class="sxs-lookup"><span data-stu-id="00e74-125">Path Element Types</span></span>

<span data-ttu-id="00e74-126">Il existe trois types d’éléments Path.</span><span class="sxs-lookup"><span data-stu-id="00e74-126">There are three types of path elements.</span></span>

### <a name="standard-path-element"></a><span data-ttu-id="00e74-127">Élément de chemin d’accès standard</span><span class="sxs-lookup"><span data-stu-id="00e74-127">Standard Path Element</span></span>

<span data-ttu-id="00e74-128">Une recherche est effectuée dans un élément de chemin d’accès standard en examinant la racine du répertoire spécifié par l’élément Path.</span><span class="sxs-lookup"><span data-stu-id="00e74-128">A standard path element is searched by looking in the root of the directory specified by the path element.</span></span> <span data-ttu-id="00e74-129">Le gestionnaire de symboles recherche également dans un sous-répertoire « Symbols » qui correspond à l’extension de fichier du module dans lequel les symboles sont recherchés.</span><span class="sxs-lookup"><span data-stu-id="00e74-129">The symbol handler also looks in a subdirectory of "symbols" that matches the file extension of the module that symbols are being looked for.</span></span> <span data-ttu-id="00e74-130">Il s’agit généralement de « dll », « exe » ou « sys ».</span><span class="sxs-lookup"><span data-stu-id="00e74-130">This is typically "dll", "exe", or "sys".</span></span> <span data-ttu-id="00e74-131">Enfin, il recherche dans un sous-répertoire appelé « Symbols » un répertoire portant le même nom que l’extension.</span><span class="sxs-lookup"><span data-stu-id="00e74-131">Lastly, it looks in a subdirectory called "symbols" with a directory of the same name as the extension.</span></span> <span data-ttu-id="00e74-132">Par exemple, si l’élément de chemin d’accès aux symboles est « c : \\ mySymbols » et que le fichier dans lequel les symboles sont recherchés est « boo.dll », les répertoires suivants sont recherchés.</span><span class="sxs-lookup"><span data-stu-id="00e74-132">For example, if the symbol path element is "c:\\mySymbols" and the file that symbols are being searched for is "boo.dll", then the following directories would be searched.</span></span>

- <span data-ttu-id="00e74-133">c : \\ mySymbols</span><span class="sxs-lookup"><span data-stu-id="00e74-133">c:\\mySymbols</span></span>  
- <span data-ttu-id="00e74-134">c : \\ mySymbols \\ dll</span><span class="sxs-lookup"><span data-stu-id="00e74-134">c:\\mySymbols\\dll</span></span>  
- <span data-ttu-id="00e74-135">c : \\ mySymbols de \\ symboles \\ dll</span><span class="sxs-lookup"><span data-stu-id="00e74-135">c:\\mySymbols\\symbols\\dll</span></span>  

<span data-ttu-id="00e74-136">Le gestionnaire de symboles utilise cette logique pour rechercher dans tout élément de chemin d’accès qui ne répond pas aux critères d’être un *serveur de symboles* ou un *cache* (décrit ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="00e74-136">The symbol handler uses this logic to search any path element that does not meet the criteria to be a *symbol server* or *cache* (described below).</span></span>

### <a name="symbol-server-path-element"></a><span data-ttu-id="00e74-137">Élément de chemin d’accès du serveur de symboles</span><span class="sxs-lookup"><span data-stu-id="00e74-137">Symbol Server Path Element</span></span>

<span data-ttu-id="00e74-138">Un élément de chemin d’accès du *serveur de symboles* utilise une technologie spéciale qui peut localiser un symbole qui correspond exactement au module en question.</span><span class="sxs-lookup"><span data-stu-id="00e74-138">A *symbol server* path element uses special technology that can locate a symbol that is an exact match for the module in question.</span></span> <span data-ttu-id="00e74-139">Pour plus d’informations, consultez [utilisation de symsrv](using-symsrv.md) .</span><span class="sxs-lookup"><span data-stu-id="00e74-139">See [Using SymSrv](using-symsrv.md) for more details.</span></span>

<span data-ttu-id="00e74-140">Le gestionnaire de symboles traite un élément de chemin d’accès comme un serveur de symboles s’il commence par le texte « SRV \* ».</span><span class="sxs-lookup"><span data-stu-id="00e74-140">The symbol handler treats a path element as a symbol server if it begins with the text, "srv\*".</span></span>

> [!Note]  
> <span data-ttu-id="00e74-141">Si le texte « SRV \* » n’est pas spécifié mais que l’élément de chemin d’accès réel est un magasin de serveurs de symboles, le gestionnaire de symboles agit comme si « SRV \* » avait été spécifié.</span><span class="sxs-lookup"><span data-stu-id="00e74-141">If the "srv\*" text is not specified but the actual path element is a symbol server store, then the symbol handler will act as if "srv\*" were specified.</span></span> <span data-ttu-id="00e74-142">Le gestionnaire de symboles effectue cette détermination en recherchant l’existence d’un fichier appelé « pingme.txt » dans le répertoire racine du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="00e74-142">The symbol handler makes this determination by searching for the existence of a file called "pingme.txt" in the root directory of the specified path.</span></span>

 

### <a name="cache-path-element"></a><span data-ttu-id="00e74-143">Élément du chemin d’accès du cache</span><span class="sxs-lookup"><span data-stu-id="00e74-143">Cache Path Element</span></span>

<span data-ttu-id="00e74-144">Un élément de chemin d’accès *du cache* est une variation sur un élément de chemin d’accès du serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="00e74-144">A *cache* path element is a variation on a symbol server path element.</span></span>

<span data-ttu-id="00e74-145">Ce répertoire est recherché comme n’importe quel autre serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="00e74-145">This directory is searched like any other symbol server.</span></span> <span data-ttu-id="00e74-146">Toutefois, si le symbole est introuvable ici et qu’il se trouve dans un élément Path plus loin dans la chaîne du chemin d’accès aux symboles, le symbole sera copié et stocké dans le serveur de symboles spécifié dans cet élément.</span><span class="sxs-lookup"><span data-stu-id="00e74-146">However, if the symbol is not found here and it is found in a path element farther down the chain of the symbol path, then the symbol will be copied and stored in the symbol server specified in this element.</span></span>

<span data-ttu-id="00e74-147">Le gestionnaire de symboles traite un élément de chemin d’accès comme un élément de cache s’il commence par le texte « cache \* ».</span><span class="sxs-lookup"><span data-stu-id="00e74-147">The symbol handler treats a path element as a cache element if it begins with the text, "cache\*".</span></span> <span data-ttu-id="00e74-148">Pour spécifier un cache dans « c : \\ myCache », utilisez un élément de chemin d’accès aux symboles « cache \* c : \\ myCache ».</span><span class="sxs-lookup"><span data-stu-id="00e74-148">To specify a cache in "c:\\myCache", use a symbol path element of "cache\*c:\\myCache".</span></span>

## <a name="example-search-path"></a><span data-ttu-id="00e74-149">Exemple de chemin de recherche</span><span class="sxs-lookup"><span data-stu-id="00e74-149">Example Search Path</span></span>

<span data-ttu-id="00e74-150">Pour voir comment cela fonctionne, définissez ce chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="00e74-150">To see how this works, set this search path.</span></span>

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

<span data-ttu-id="00e74-151">Voici une liste de la sortie détaillée du gestionnaire de symboles lors de la recherche de ntdll. pdb, à l’aide du chemin de recherche répertorié ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="00e74-151">The following is a listing of the symbol handler's verbose output while searching for ntdll.pdb, using the above listed search path.</span></span>

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

<span data-ttu-id="00e74-152">Les trois premières lignes de sortie affichent le gestionnaire de symboles qui traite le premier élément de chemin d’accès de `.` .</span><span class="sxs-lookup"><span data-stu-id="00e74-152">The first three lines of output show the symbol handler processing the first path element of `.`.</span></span> <span data-ttu-id="00e74-153">Il s’agit d’un élément de chemin d’accès standard.</span><span class="sxs-lookup"><span data-stu-id="00e74-153">This is a standard path element.</span></span>

<span data-ttu-id="00e74-154">La quatrième ligne montre le gestionnaire de symboles à l’aide du serveur de symboles pour rechercher le fichier dans le deuxième élément de chemin d’accès `cache*c:\myCache` qui est un élément de chemin d’accès du cache.</span><span class="sxs-lookup"><span data-stu-id="00e74-154">The fourth line shows the symbol handler using the symbol server to look for the file in the second path element of `cache*c:\myCache` which is a cache path element.</span></span>

<span data-ttu-id="00e74-155">La cinquième ligne indique que le fichier se trouve dans le troisième élément de chemin d’accès de `srv*\\symbols\symbols` , qui est un élément de chemin d’accès du serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="00e74-155">The fifth line shows the file is found in the third path element of `srv*\\symbols\symbols`, which is a symbol server path element.</span></span>

<span data-ttu-id="00e74-156">La sixième ligne indique que le fichier est copié dans le cache.</span><span class="sxs-lookup"><span data-stu-id="00e74-156">The sixth line shows that the file is copied to the cache.</span></span>

<span data-ttu-id="00e74-157">Les deux dernières lignes sur lesquelles le fichier est ouvert à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="00e74-157">The last two lines that the file is opened from the cache.</span></span>
