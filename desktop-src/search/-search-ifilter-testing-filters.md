---
description: La suite de tests IFilter valide vos gestionnaires de filtres.
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: Test des gestionnaires de filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2a2b0b6a6728051ab22590a481ad23a7197692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112447"
---
# <a name="testing-filter-handlers"></a><span data-ttu-id="3ce68-103">Test des gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="3ce68-103">Testing Filter Handlers</span></span>

<span data-ttu-id="3ce68-104">La suite de tests [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) valide vos gestionnaires de filtres.</span><span class="sxs-lookup"><span data-stu-id="3ce68-104">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite validates your filter handlers.</span></span> <span data-ttu-id="3ce68-105">La suite de tests effectue cette vérification en appelant des méthodes [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) et en vérifiant les valeurs retournées pour la conformité avec la spécification de l’interface **IFilter** . et le fait de vérifier que les identificateurs de bloc sont uniques et s’améliorent, que l’interface **IFilter** se comporte de manière cohérente après la réinitialisation, et que toute méthode **IFilter** qui appelle avec des paramètres non valides retourne les codes d’erreur attendus.</span><span class="sxs-lookup"><span data-stu-id="3ce68-105">The test suite does so by: calling [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) methods and checking the returned values for compliance with the **IFilter** interface specification; and checking that chunk identifiers are unique and increasing, that the **IFilter** interface behaves consistently after re-initialization, and that any **IFilter** method calls with invalid parameters return expected error codes.</span></span> <span data-ttu-id="3ce68-106">Les programmes de suite de tests enregistrent également la sortie d’un fichier filtré par un gestionnaire de filtres et vérifient les informations d’inscription **IFilter** dans le registre.</span><span class="sxs-lookup"><span data-stu-id="3ce68-106">The test suite programs also dump the output of a file filtered by a filter handler, and check the **IFilter** registration information in the registry.</span></span>

<span data-ttu-id="3ce68-107">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="3ce68-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="3ce68-108">Appel de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="3ce68-108">Command-Line Invocation</span></span>](#command-line-invocation)
  - [<span data-ttu-id="3ce68-109">ifilttst.exe</span><span class="sxs-lookup"><span data-stu-id="3ce68-109">ifilttst.exe</span></span>](#ifilttstexe)
  - [<span data-ttu-id="3ce68-110">filtdump.exe</span><span class="sxs-lookup"><span data-stu-id="3ce68-110">filtdump.exe</span></span>](#filtdumpexe)
  - [<span data-ttu-id="3ce68-111">filtreg.exe</span><span class="sxs-lookup"><span data-stu-id="3ce68-111">filtreg.exe</span></span>](#filtregexe)
  - [<span data-ttu-id="3ce68-112">ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="3ce68-112">ifilttst.ini</span></span>](#ifilttstini)
- [<span data-ttu-id="3ce68-113">Procédure de test IFilter</span><span class="sxs-lookup"><span data-stu-id="3ce68-113">IFilter Test Procedure</span></span>](#ifilter-test-procedure)
  - [<span data-ttu-id="3ce68-114">Test de validation</span><span class="sxs-lookup"><span data-stu-id="3ce68-114">Validation Test</span></span>](#validation-test)
  - [<span data-ttu-id="3ce68-115">Test de cohérence</span><span class="sxs-lookup"><span data-stu-id="3ce68-115">Consistency Test</span></span>](#consistency-test)
  - [<span data-ttu-id="3ce68-116">Test d’entrée non valide</span><span class="sxs-lookup"><span data-stu-id="3ce68-116">Invalid Input Test</span></span>](#invalid-input-test)
  - [<span data-ttu-id="3ce68-117">Test de différentes configurations IFilter</span><span class="sxs-lookup"><span data-stu-id="3ce68-117">Testing Different IFilter Configurations</span></span>](#testing-different-ifilter-configurations)
- [<span data-ttu-id="3ce68-118">Vérification de l’indexation des éléments inscrits</span><span class="sxs-lookup"><span data-stu-id="3ce68-118">Ensuring Registered Items Get Indexed</span></span>](#ensuring-registered-items-get-indexed)
  - [<span data-ttu-id="3ce68-119">Exemple de fichier journal</span><span class="sxs-lookup"><span data-stu-id="3ce68-119">Sample Log File</span></span>](#sample-log-file)
  - [<span data-ttu-id="3ce68-120">Exemple de fichier dump</span><span class="sxs-lookup"><span data-stu-id="3ce68-120">Sample Dump File</span></span>](#sample-dump-file)
- [<span data-ttu-id="3ce68-121">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3ce68-121">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="3ce68-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ce68-122">Related topics</span></span>](#related-topics)

> [!NOTE]  
> <span data-ttu-id="3ce68-123">Si un nouveau gestionnaire de filtres pour un type de fichier est en cours d’installation en remplacement d’une inscription de filtre existante, le programme d’installation doit enregistrer l’inscription actuelle et la restaurer si le nouveau gestionnaire de filtres est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="3ce68-123">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="3ce68-124">Il n’existe aucun mécanisme pour la chaîne de filtres.</span><span class="sxs-lookup"><span data-stu-id="3ce68-124">There is no mechanism to chain filters.</span></span> <span data-ttu-id="3ce68-125">Par conséquent, le nouveau gestionnaire de filtres est chargé de répliquer toutes les fonctionnalités nécessaires de l’ancien filtre.</span><span class="sxs-lookup"><span data-stu-id="3ce68-125">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>

## <a name="command-line-invocation"></a><span data-ttu-id="3ce68-126">Appel de Command-Line</span><span class="sxs-lookup"><span data-stu-id="3ce68-126">Command-Line Invocation</span></span>

<span data-ttu-id="3ce68-127">La suite de tests [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) se compose de trois applications en ligne de commande : [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe)et [filtreg.exe](#filtregexe) et un fichier d’initialisation, [ifilttst.ini](#ifilttstini).</span><span class="sxs-lookup"><span data-stu-id="3ce68-127">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite consists of three command-line applications - [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe), and [filtreg.exe](#filtregexe) and an initialization file, [ifilttst.ini](#ifilttstini).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3ce68-128">Dans Windows 7 et versions ultérieures, les filtres écrits en code managé sont bloqués explicitement.</span><span class="sxs-lookup"><span data-stu-id="3ce68-128">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="3ce68-129">Les filtres doivent être écrits en code natif en raison de problèmes potentiels de contrôle de version du common language runtime (CLR) avec le processus dans lequel plusieurs compléments s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="3ce68-129">Filters MUST be written in native code due to potential common language runtime (CLR) versioning issues with the process that multiple add-ins run in.</span></span>

### <a name="ifilttstexe"></a><span data-ttu-id="3ce68-130">ifilttst.exe</span><span class="sxs-lookup"><span data-stu-id="3ce68-130">ifilttst.exe</span></span>

<span data-ttu-id="3ce68-131">Le programme ifilttst.exe exécute plusieurs tests pour valider un gestionnaire de filtres.</span><span class="sxs-lookup"><span data-stu-id="3ce68-131">The ifilttst.exe program runs several tests to validate a filter handler.</span></span> <span data-ttu-id="3ce68-132">L’exemple suivant illustre l’appel du programme ifilttst.exe à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="3ce68-132">The following example illustrates how to invoke the ifilttst.exe program from the command line:</span></span>


```
ifilttst /i test.htm /l /d /v 1
```

<span data-ttu-id="3ce68-133">L’exemple effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ce68-133">The example performs the following tasks:</span></span>

- <span data-ttu-id="3ce68-134">Indique au programme de filtrer le fichier test.htm</span><span class="sxs-lookup"><span data-stu-id="3ce68-134">Directs the program to filter the file test.htm</span></span>
- <span data-ttu-id="3ce68-135">Redirige les messages du journal vers test.htm. log</span><span class="sxs-lookup"><span data-stu-id="3ce68-135">Redirects the log messages to test.htm.log</span></span>
- <span data-ttu-id="3ce68-136">Redirige les messages de vidage vers test.htm. dmp</span><span class="sxs-lookup"><span data-stu-id="3ce68-136">Redirects the dump messages to test.htm.dmp</span></span>
- <span data-ttu-id="3ce68-137">Définit le niveau de détail sur 1</span><span class="sxs-lookup"><span data-stu-id="3ce68-137">Sets the verbosity to 1</span></span>

<span data-ttu-id="3ce68-138">Pour que la commande précédente fonctionne, trois fichiers doivent se trouver dans le répertoire de travail actuel : `test.htm` , [ifilttst.exe](#ifilttstexe)et [ifilttst.ini](#ifilttstini).</span><span class="sxs-lookup"><span data-stu-id="3ce68-138">For the preceding command to work, three files must be located in the current working directory: `test.htm`, [ifilttst.exe](#ifilttstexe), and [ifilttst.ini](#ifilttstini).</span></span> <span data-ttu-id="3ce68-139">Les commutateurs de ligne de commande sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3ce68-139">Command-line switches are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ce68-140">Commutateur et variables possibles</span><span class="sxs-lookup"><span data-stu-id="3ce68-140">Switch and possible variables</span></span></th>
<th><span data-ttu-id="3ce68-141">Description</span><span class="sxs-lookup"><span data-stu-id="3ce68-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ce68-142"><strong>/i nom du fichier</strong></span><span class="sxs-lookup"><span data-stu-id="3ce68-142"><strong>/i file name</strong></span></span></td>
<td><span data-ttu-id="3ce68-143">Fichier d’entrée ou répertoire à filtrer.</span><span class="sxs-lookup"><span data-stu-id="3ce68-143">The input file or directory to be filtered.</span></span> <span data-ttu-id="3ce68-144">Le nom de fichier peut contenir les caractères génériques <code>\*</code> et <code>?</code> .</span><span class="sxs-lookup"><span data-stu-id="3ce68-144">The file name can contain the wildcard characters <code>\*</code> and <code>?</code>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ce68-145"><strong>/l</strong></span><span class="sxs-lookup"><span data-stu-id="3ce68-145"><strong>/l</strong></span></span></td>
<td><span data-ttu-id="3ce68-146">Les messages de journal sont dirigés vers un fichier au lieu de l’écran.</span><span class="sxs-lookup"><span data-stu-id="3ce68-146">Log messages are directed to a file instead of the screen.</span></span> <span data-ttu-id="3ce68-147">Les messages de journal décrivent les tests individuels effectués et les résultats de réussite/échec des tests.</span><span class="sxs-lookup"><span data-stu-id="3ce68-147">Log messages describe the individual tests performed and the pass/fail results of the tests.</span></span> <span data-ttu-id="3ce68-148">Le nom du fichier journal est le même que le nom du fichier d’entrée, mais avec une extension. log.</span><span class="sxs-lookup"><span data-stu-id="3ce68-148">The log file name is the same as the input file name but with a .log extension.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ce68-149"><strong>/d</strong></span><span class="sxs-lookup"><span data-stu-id="3ce68-149"><strong>/d</strong></span></span></td>
<td><span data-ttu-id="3ce68-150">Les messages de vidage sont dirigés vers un fichier au lieu de l’écran.</span><span class="sxs-lookup"><span data-stu-id="3ce68-150">Dump messages are directed to a file instead of the screen.</span></span> <span data-ttu-id="3ce68-151">Les messages de vidage décrivent le contenu des segments.</span><span class="sxs-lookup"><span data-stu-id="3ce68-151">Dump messages describe the contents of the chunks.</span></span> <span data-ttu-id="3ce68-152">La structure du bloc est vidée lorsque le niveau de détail est 3.</span><span class="sxs-lookup"><span data-stu-id="3ce68-152">The chunk structure is dumped when the verbosity level is 3.</span></span> <span data-ttu-id="3ce68-153">Le nom du fichier dump est le même que le nom du fichier d’entrée, mais avec une extension. dmp.</span><span class="sxs-lookup"><span data-stu-id="3ce68-153">The dump file name is the same as the input file name but with a .dmp extension.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ce68-154"><strong>/-l</strong></span><span class="sxs-lookup"><span data-stu-id="3ce68-154"><strong>/-l</strong></span></span></td>
<td><span data-ttu-id="3ce68-155">Désactivez la journalisation.</span><span class="sxs-lookup"><span data-stu-id="3ce68-155">Disable logging.</span></span> <span data-ttu-id="3ce68-156">Cet indicateur remplace le <code>/l</code> commutateur.</span><span class="sxs-lookup"><span data-stu-id="3ce68-156">This flag overrides the <code>/l</code> switch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ce68-157"><strong>/-d</strong></span><span class="sxs-lookup"><span data-stu-id="3ce68-157"><strong>/-d</strong></span></span></td>
<td><span data-ttu-id="3ce68-158">Désactiver le vidage.</span><span class="sxs-lookup"><span data-stu-id="3ce68-158">Disable dumping.</span></span> <span data-ttu-id="3ce68-159">Cet indicateur remplace le <code>/d</code> commutateur.</span><span class="sxs-lookup"><span data-stu-id="3ce68-159">This flag overrides the <code>/d</code> switch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ce68-160"><strong>entier/v</strong></span><span class="sxs-lookup"><span data-stu-id="3ce68-160"><strong>/v integer</strong></span></span></td>
<td><span data-ttu-id="3ce68-161">Niveau de commentaires.</span><span class="sxs-lookup"><span data-stu-id="3ce68-161">The verbosity level.</span></span> <span data-ttu-id="3ce68-162">La valeur par défaut est 3.</span><span class="sxs-lookup"><span data-stu-id="3ce68-162">The default is 3.</span></span>
<ul>
<li><span data-ttu-id="3ce68-163">0-le test enregistre uniquement les messages relatifs à des échecs spécifiques de l’interface <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3ce68-163">0 - The test logs only messages concerning specific <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> interface failures.</span></span> <span data-ttu-id="3ce68-164">Le test vide le contenu du bloc.</span><span class="sxs-lookup"><span data-stu-id="3ce68-164">The test dumps the chunk contents.</span></span></li>
<li><span data-ttu-id="3ce68-165">1-le test journalise les messages d’avertissement, ainsi que ceux pour le niveau 0.</span><span class="sxs-lookup"><span data-stu-id="3ce68-165">1 - The test logs warning messages as well as those for level 0.</span></span></li>
<li><span data-ttu-id="3ce68-166">2-le test journalise les messages relatifs aux tests qui ont réussi, ainsi qu’à ceux du niveau 1.</span><span class="sxs-lookup"><span data-stu-id="3ce68-166">2 - The test logs messages concerning tests that passed as well as those for level 1.</span></span></li>
<li><span data-ttu-id="3ce68-167">3-le test journalise les messages d’information, ainsi que ceux pour le niveau 2.</span><span class="sxs-lookup"><span data-stu-id="3ce68-167">3 - The test logs informational messages as well as those for level 2.</span></span> <span data-ttu-id="3ce68-168">En outre, le test vide la structure du bloc.</span><span class="sxs-lookup"><span data-stu-id="3ce68-168">In addition, the test dumps the structure of the chunk.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ce68-169"><strong>/t entier</strong></span><span class="sxs-lookup"><span data-stu-id="3ce68-169"><strong>/t integer</strong></span></span></td>
<td><span data-ttu-id="3ce68-170">Nombre de threads à lancer.</span><span class="sxs-lookup"><span data-stu-id="3ce68-170">The number of threads to launch.</span></span> <span data-ttu-id="3ce68-171">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="3ce68-171">The default is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ce68-172"><strong>/r entier</strong>]</span><span class="sxs-lookup"><span data-stu-id="3ce68-172"><strong>/r integer</strong>]</span></span></td>
<td><span data-ttu-id="3ce68-173">Filtre de manière récursive les sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="3ce68-173">Recursively filters subdirectories.</span></span> <span data-ttu-id="3ce68-174">Le paramètre Integer facultatif spécifie la profondeur d’exercice de la récursivité.</span><span class="sxs-lookup"><span data-stu-id="3ce68-174">The optional integer parameter specifies the depth to which to exercise recursion.</span></span> <span data-ttu-id="3ce68-175">Si aucun entier n’est spécifié, ou si l’entier est égal à 0, la récursivité complète est supposée.</span><span class="sxs-lookup"><span data-stu-id="3ce68-175">If no integer is specified, or if the integer is 0, full recursion is assumed.</span></span> <span data-ttu-id="3ce68-176">Par défaut, la profondeur de récurrence est 1.</span><span class="sxs-lookup"><span data-stu-id="3ce68-176">By default, the recursion depth is 1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ce68-177"><strong>entier/c</strong></span><span class="sxs-lookup"><span data-stu-id="3ce68-177"><strong>/c integer</strong></span></span></td>
<td><span data-ttu-id="3ce68-178">Nombre de boucles.</span><span class="sxs-lookup"><span data-stu-id="3ce68-178">The number of times to loop.</span></span> <span data-ttu-id="3ce68-179">Si l’entier est 0, le test effectue une boucle infinie.</span><span class="sxs-lookup"><span data-stu-id="3ce68-179">If the integer is 0, the test loops infinitely.</span></span> <span data-ttu-id="3ce68-180">Par défaut, le test ne boucle qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="3ce68-180">By default, the test loops only once.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]  
> <span data-ttu-id="3ce68-181">Vous devez inclure un espace entre le commutateur de ligne de commande et la valeur.</span><span class="sxs-lookup"><span data-stu-id="3ce68-181">You must include a space between the command line switch and the value.</span></span>

### <a name="filtdumpexe"></a><span data-ttu-id="3ce68-182">filtdump.exe</span><span class="sxs-lookup"><span data-stu-id="3ce68-182">filtdump.exe</span></span>

<span data-ttu-id="3ce68-183">Le programme filtdump.exe charge un gestionnaire de filtres pour un document spécifié et imprime la sortie produite par la dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="3ce68-183">The filtdump.exe program loads a filter handler for a specified document and prints the output produced by the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL.</span></span> <span data-ttu-id="3ce68-184">L’exemple suivant illustre l’appel du programme filtdump.exe.</span><span class="sxs-lookup"><span data-stu-id="3ce68-184">The following example illustrates how to invoke the filtdump.exe program.</span></span>

```
filtdump filename.ext
```
<span data-ttu-id="3ce68-185">Filtdump.exe utilise la méthode [ILoadFilter :: LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) pour charger la dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) appropriée pour l’extension de nom de fichier spécifiée et imprime les résultats.</span><span class="sxs-lookup"><span data-stu-id="3ce68-185">Filtdump.exe uses the [ILoadFilter::LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) method to load the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL appropriate for the specified file name extension and prints the results.</span></span> <span data-ttu-id="3ce68-186">Par exemple, la commande suivante indique à filtdump.exe de charger le gestionnaire de filtre smpfilt.dll pour l’extension. SMP, d’extraire l’ensemble du texte et des propriétés du fichier MyFile. SMP et d’imprimer les résultats.</span><span class="sxs-lookup"><span data-stu-id="3ce68-186">For example, the following command instructs filtdump.exe to load the smpfilt.dll filter handler for the extension .smp, extract all text and properties from the file myfile.smp, and print the results.</span></span>

```
filtdump myfile.smp
```

### <a name="filtregexe"></a><span data-ttu-id="3ce68-187">filtreg.exe</span><span class="sxs-lookup"><span data-stu-id="3ce68-187">filtreg.exe</span></span>

<span data-ttu-id="3ce68-188">Le programme filtreg.exe inspecte les informations d’installation [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) dans le registre.</span><span class="sxs-lookup"><span data-stu-id="3ce68-188">The filtreg.exe program inspects [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) installation information in the registry.</span></span> <span data-ttu-id="3ce68-189">Vous appelez le programme filtreg.exe à partir de la ligne de commande en tapant son nom, comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="3ce68-189">You invoke the filtreg.exe program from the command line by typing its name, as in the following example.</span></span>

```
filtreg
```

<span data-ttu-id="3ce68-190">Filtreg.exe énumère toutes les extensions de nom de fichier associées à des gestionnaires de filtre en imprimant l’extension de nom de fichier et le nom de la dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) pour l’extension.</span><span class="sxs-lookup"><span data-stu-id="3ce68-190">Filtreg.exe enumerates all file name extensions that have filter handlers associated with them by printing the file name extension and the name of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL for the extension.</span></span> <span data-ttu-id="3ce68-191">Il s’agit d’un moyen simple de vérifier l’installation correcte d’un **IFilter**.</span><span class="sxs-lookup"><span data-stu-id="3ce68-191">This is a simple way to verify the correct installation of an **IFilter**.</span></span>

### <a name="ifilttstini"></a><span data-ttu-id="3ce68-192">ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="3ce68-192">ifilttst.ini</span></span>

<span data-ttu-id="3ce68-193">Une interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) est initialisée par l’appel de la méthode [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="3ce68-193">An [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface is initialized by calling the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span> <span data-ttu-id="3ce68-194">La méthode **IFilter :: init** prend les quatre paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="3ce68-194">The **IFilter::Init** method takes the following four parameters:</span></span>

1. <span data-ttu-id="3ce68-195">*grfFlags*</span><span class="sxs-lookup"><span data-stu-id="3ce68-195">*grfFlags*</span></span>
2. <span data-ttu-id="3ce68-196">*cAttributes*</span><span class="sxs-lookup"><span data-stu-id="3ce68-196">*cAttributes*</span></span>
3. <span data-ttu-id="3ce68-197">*aAttributes*</span><span class="sxs-lookup"><span data-stu-id="3ce68-197">*aAttributes*</span></span>
4. <span data-ttu-id="3ce68-198">*pdwFlags*</span><span class="sxs-lookup"><span data-stu-id="3ce68-198">*pdwFlags*</span></span>

<span data-ttu-id="3ce68-199">L’utilisateur du programme ifilttst.exe de la suite de tests [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) peut spécifier les valeurs de ces paramètres dans un fichier appelé ifilttst.ini.</span><span class="sxs-lookup"><span data-stu-id="3ce68-199">The user of the ifilttst.exe program of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite can specify the values for these parameters in a file called ifilttst.ini.</span></span> <span data-ttu-id="3ce68-200">Le tableau suivant décrit les entrées dans le fichier ifilttst.ini qui spécifient les trois premiers paramètres (les paramètres d’entrée).</span><span class="sxs-lookup"><span data-stu-id="3ce68-200">The following table describes the entries in the ifilttst.ini file that specify the first three parameters(the input parameters).</span></span> <span data-ttu-id="3ce68-201">Pour obtenir un exemple de fichier, consultez [exemple de fichier de ifilttst.ini](#sample-ifilttstini-file).</span><span class="sxs-lookup"><span data-stu-id="3ce68-201">For a sample file, see [Sample ifilttst.ini File](#sample-ifilttstini-file).</span></span>

> [!NOTE]  
> <span data-ttu-id="3ce68-202">Il n’existe aucune entrée de table pour le paramètre *pdwFlags* , car il s’agit d’un paramètre de sortie ; Il n’est pas nécessaire d’avoir une valeur spéciale avant l’appel à la méthode [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="3ce68-202">There is no table entry for the *pdwFlags* parameter because it is an output parameter; it does not need to have any special value prior to the call to the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span>

 | <span data-ttu-id="3ce68-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="3ce68-203">Entry</span></span>         | <span data-ttu-id="3ce68-204">Description</span><span class="sxs-lookup"><span data-stu-id="3ce68-204">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce68-205">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="3ce68-205">Flags</span></span>         | <span data-ttu-id="3ce68-206">Noms des indicateurs d' [**\_ initialisation IFilter**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) qui doivent être joints par l’opérateur or pour former le paramètre *GrfFlags* de la méthode [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="3ce68-206">The names of the [**IFILTER\_INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) flags that are to be joined by the OR operator to form the *grfFlags* parameter of the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span> <span data-ttu-id="3ce68-207">Les noms des indicateurs doivent tous être en majuscules et sur la même ligne.</span><span class="sxs-lookup"><span data-stu-id="3ce68-207">The flag names must all be uppercase, and on the same line.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3ce68-208">*cAttributes*</span><span class="sxs-lookup"><span data-stu-id="3ce68-208">*cAttributes*</span></span> | <span data-ttu-id="3ce68-209">Entier décimal représentant la valeur du paramètre *cAttributes* .</span><span class="sxs-lookup"><span data-stu-id="3ce68-209">A decimal integer representing the value of the *cAttributes* parameter.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3ce68-210">*aAttributes*</span><span class="sxs-lookup"><span data-stu-id="3ce68-210">*aAttributes*</span></span> | <span data-ttu-id="3ce68-211">Cette entrée doit commencer par *aAttributes* et doit être différente des autres entrées *aAttributes* dans la section.</span><span class="sxs-lookup"><span data-stu-id="3ce68-211">This entry must start with *aAttributes* and must be different from the other *aAttributes* entries within the section.</span></span> <span data-ttu-id="3ce68-212">Les noms légaux de l’entrée *aAttributes* sont : *aAttributes*, *aAttributes1*, *aAttributes2*, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="3ce68-212">Legal names for the *aAttributes* entry are: *aAttributes*, *aAttributes1*, *aAttributes2*, and so forth.</span></span> <span data-ttu-id="3ce68-213">Le premier jeton doit être un GUID.</span><span class="sxs-lookup"><span data-stu-id="3ce68-213">The first token must be a GUID.</span></span> <span data-ttu-id="3ce68-214">Le GUID doit être mis en forme exactement comme illustré dans la `[Test3]` section de l' [exemple de fichier ifilttst.ini](#sample-ifilttstini-file).</span><span class="sxs-lookup"><span data-stu-id="3ce68-214">The GUID must be formatted exactly as illustrated in the `[Test3]` section of the [Sample ifilttst.ini File](#sample-ifilttstini-file).</span></span> <span data-ttu-id="3ce68-215">Le deuxième jeton peut être soit un identificateur de propriété (PID) composé d’un nombre en notation hexadécimale, soit un pointeur vers une chaîne de caractères larges (LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="3ce68-215">The second token can be either a property identifier (PID) consisting of a number in hexadecimal notation, or a pointer to a wide character string (lpwstr).</span></span> <span data-ttu-id="3ce68-216">Vous pouvez spécifier un LPWStr en plaçant la chaîne entre guillemets doubles, comme illustré dans la `[Test6]` section de l’exemple de fichier de ifilttst.ini.</span><span class="sxs-lookup"><span data-stu-id="3ce68-216">A lpwstr can be specified by enclosing the string in double quotes, as illustrated in the `[Test6]` section of the Sample ifilttst.ini File.</span></span> |

<span data-ttu-id="3ce68-217">Si les entrées Flags et *cAttributes* ne sont pas spécifiées, la valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="3ce68-217">If the Flags and *cAttributes* entries are not specified, they default to 0.</span></span> <span data-ttu-id="3ce68-218">Si vous affectez à *cAttributes* la valeur 2, vous devez spécifier deux noms *aAttributes* .</span><span class="sxs-lookup"><span data-stu-id="3ce68-218">If you set *cAttributes* equal to 2, you should specify two *aAttributes* names.</span></span> <span data-ttu-id="3ce68-219">Dans la `[Test5]` section de l’exemple, *cAttributes* est 1, mais aucun *aAttributes* n’a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="3ce68-219">In the `[Test5]` section of the sample, *cAttributes* is 1, but no *aAttributes* have been specified.</span></span> <span data-ttu-id="3ce68-220">Le test appelle ensuite la méthode [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init) avec *cAttributes* égal à 1 et *aAttributes* égal à **null**.</span><span class="sxs-lookup"><span data-stu-id="3ce68-220">The test then calls the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method with *cAttributes* equal to 1 and *aAttributes* equal to **NULL**.</span></span> <span data-ttu-id="3ce68-221">Il s’agit d’un cas de test utile, car il est susceptible de provoquer une violation d’accès dans la méthode **IFilter :: init** .</span><span class="sxs-lookup"><span data-stu-id="3ce68-221">This is a useful test case because it is likely to cause an access violation in the **IFilter::Init** method.</span></span>

<span data-ttu-id="3ce68-222">Si ifilttst.exe ne parvient pas à trouver un fichier nommé ifilttst.ini dans le répertoire de travail, une configuration par défaut est utilisée pour initialiser l’objet [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="3ce68-222">If ifilttst.exe cannot find a file named ifilttst.ini in the working directory, a default configuration is used to initialize the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) object.</span></span> <span data-ttu-id="3ce68-223">L’exemple suivant illustre la configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="3ce68-223">The following example illustrates the default configuration.</span></span>

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a><span data-ttu-id="3ce68-224">Exemple de fichier de ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="3ce68-224">Sample ifilttst.ini File</span></span>

<span data-ttu-id="3ce68-225">Le fichier ifilttst.ini est organisé en sections, avec le nom de la section entre crochets.</span><span class="sxs-lookup"><span data-stu-id="3ce68-225">The ifilttst.ini file is organized in sections, with the section name enclosed in square brackets.</span></span> <span data-ttu-id="3ce68-226">Dans l’exemple, les sections sont nommées `[Test1]` , `[Test2]` , et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="3ce68-226">In the example, the sections are named `[Test1]`, `[Test2]`, and so forth.</span></span> <span data-ttu-id="3ce68-227">Tous les noms de section doivent être uniques.</span><span class="sxs-lookup"><span data-stu-id="3ce68-227">All section names must be unique.</span></span> <span data-ttu-id="3ce68-228">Le test lit les valeurs de la première section et initialise le [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) avec ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="3ce68-228">The test reads the values from the first section and initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) with those values.</span></span> <span data-ttu-id="3ce68-229">Ensuite, tous les tests sont exécutés à l’aide de cette configuration **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="3ce68-229">Then all the tests are run using this **IFilter** configuration.</span></span> <span data-ttu-id="3ce68-230">Le **IFilter** est ensuite libéré et réinitialisé à l’aide des paramètres répertoriés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="3ce68-230">Then the **IFilter** is released and reinitialized, using parameters that are listed above.</span></span> <span data-ttu-id="3ce68-231">Le processus se répète jusqu’à ce que toutes les configurations soient testées.</span><span class="sxs-lookup"><span data-stu-id="3ce68-231">The process is repeated until all configurations are tested.</span></span>

```
; Only extract text from the object
            [Test1]
            Flags =
            cAttributes = 0

            // Get all attributes (text-type and internal value-type properties.
            [Test2]
            Flags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

            // This also extracts just text from the object (the GUID is PSGUID_STORAGE, and the propid is
            // PID_STG_CONTENTS).
            [Test3]
            Flags = IFILTER_INIT_CANON_PARAGRAPHS IFILTER_INIT_HARD_LINE_BREAKS
            cAttributes = 1
            aAttributes1 = b725f130-47ef-101a-a5f1-02608c9eebac 13

            // Only extract requested attribute from the html object (the GUID corresponds to the HTML IFilter.
            [Test4]
            Flags = IFILTER_INIT_CANON_HYPHENS IFILTER_INIT_CANON_SPACES
            cAttributes = 1
            aAttributes1 = 70eb7a10-55d9-11cf-b75b-00aa0051fe20 2

            // Question: what happens if cAttributes is nonzero, but aAttributes is empty?
            [Test5]
            Flags = IFILTER_INIT_CANON_SPACES IFILTER_INIT_APPLY_INDEX_ATTRIBUTES IFILTER_INIT_APPLY_OTHER_ATTRIBUTES
            cAttributes = 1

            // Here is an attribute with a lpwstr instead of a propid (the lpwstr is enclosed in quotes).
            // The GUID corresponds to the meta tag clsid for the HTML IFilter.
            [Test6]
            Flags =
            cAttributes = 1
            aAttributes1 = D1B5D3F0-C0B3-11CF-9A92-00A0C908DBF1 "GENERATOR"
```

## <a name="ifilter-test-procedure"></a><span data-ttu-id="3ce68-232">Procédure de test IFilter</span><span class="sxs-lookup"><span data-stu-id="3ce68-232">IFilter Test Procedure</span></span>

<span data-ttu-id="3ce68-233">Une fois que le [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) a été initialisé, le programme ifilttst.exe effectue une série de tests sur le **IFilter**.</span><span class="sxs-lookup"><span data-stu-id="3ce68-233">After the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) has been initialized, the ifilttst.exe program conducts a series of tests on the **IFilter**.</span></span> <span data-ttu-id="3ce68-234">En plus de suivre les procédures de test **IFilter** , assurez-vous que votre implémentation **IFilter** utilise des pratiques de code sécurisé.</span><span class="sxs-lookup"><span data-stu-id="3ce68-234">In addition to following the **IFilter** test procedures, ensure that your **IFilter** implementation employs secure code practices.</span></span> <span data-ttu-id="3ce68-235">Consultez « pratiques de code sécurisé pour Windows Search » dans [implémentation de gestionnaires de filtres dans Windows Search](-search-ifilter-constructing-filters.md).</span><span class="sxs-lookup"><span data-stu-id="3ce68-235">See "Secure Code Practices for Windows Search" in [Implementing Filter Handlers in Windows Search](-search-ifilter-constructing-filters.md).</span></span>

### <a name="validation-test"></a><span data-ttu-id="3ce68-236">Test de validation</span><span class="sxs-lookup"><span data-stu-id="3ce68-236">Validation Test</span></span>

<span data-ttu-id="3ce68-237">Les étapes de test de validation passent par un segment à la fois dans l’objet, en vérifiant chaque bloc individuel et tous les codes de retour.</span><span class="sxs-lookup"><span data-stu-id="3ce68-237">The validation test steps through the object one chunk at a time, verifying each individual chunk and all return codes.</span></span> <span data-ttu-id="3ce68-238">Le test de validation enregistre toutes les structures de [**\_ blocs stats**](/windows/win32/api/filter/ns-filter-stat_chunk) retournées dans une liste.</span><span class="sxs-lookup"><span data-stu-id="3ce68-238">The validation test saves all returned [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) structures in a list.</span></span>

<span data-ttu-id="3ce68-239">Le test de validation vérifie les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ce68-239">The validation test verifies the following conditions:</span></span>

- <span data-ttu-id="3ce68-240">[**\_ Bloc stat**](/windows/win32/api/filter/ns-filter-stat_chunk).\*\* les ID de bloc idChunk doivent être uniques et en constante évolution.</span><span class="sxs-lookup"><span data-stu-id="3ce68-240">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunk* chunk IDs must be unique and increasing.</span></span>
- <span data-ttu-id="3ce68-241">[**\_ Bloc stat**](/windows/win32/api/filter/ns-filter-stat_chunk).*le paramètre flags* est un état de bloc reconnu, tel que [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate), le texte de bloc \_ ou les \_ constantes de valeur CenabledHUNK.</span><span class="sxs-lookup"><span data-stu-id="3ce68-241">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*flags* parameter is a recognized chunk state, such as [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate), CHUNK\_TEXT, or CenabledHUNK\_VALUE constants.</span></span>
- <span data-ttu-id="3ce68-242">[**\_ Bloc stat**](/windows/win32/api/filter/ns-filter-stat_chunk).\*\* le paramètre breakType est un type d’arrêt reconnu (0, 1, 2, 3, 4).</span><span class="sxs-lookup"><span data-stu-id="3ce68-242">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*breakType* parameter is a recognized break type (0, 1, 2, 3, 4).</span></span>
- <span data-ttu-id="3ce68-243">Si les attributs d’initialisation [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) spécifient que le **IFilter** doit retourner uniquement des blocs contenant des propriétés de type valeur interne, *idChunkSource* doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="3ce68-243">If the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) initialization attributes specify that the **IFilter** should return only chunks containing internal value-type properties, then *idChunkSource* must equal 0.</span></span>
- <span data-ttu-id="3ce68-244">Si le segment n’est pas dérivé, s’il ne s’agit pas d’une propriété de type valeur interne, le [**\_ bloc stat**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* doit être égal au **\_ bloc stat**.*idChunk*.</span><span class="sxs-lookup"><span data-stu-id="3ce68-244">If the chunk is not derived that is, if it is not an internal value-type property, then [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* must equal **STAT\_CHUNK**.*idChunk*.</span></span>
- <span data-ttu-id="3ce68-245">[**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retourne le \_ ou les autres valeurs de retour acceptables, comme le filtre \_ e \_ End \_ des \_ segments, le filtre \_ e \_ Link \_ non disponible, etc.</span><span class="sxs-lookup"><span data-stu-id="3ce68-245">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns S\_OK or other acceptable return value, such as FILTER\_E\_END\_OF\_CHUNKS, FILTER\_E\_LINK\_UNAVAILABLE, and so forth.</span></span>
- <span data-ttu-id="3ce68-246">Si le segment contient du texte, [**IFilter :: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retourne s \_ OK, filtre \_ S \_ dernier \_ texte ou filtre \_ E \_ plus de \_ \_ texte.</span><span class="sxs-lookup"><span data-stu-id="3ce68-246">If the chunk contains text, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns S\_OK, FILTER\_S\_LAST\_TEXT, or FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="3ce68-247">Si [**IFilter :: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retourne \_ \_ \_ le dernier texte du filtre, l’appel suivant à **IFilter :: gettext** retourne le filtre \_ E (plus de texte) \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3ce68-247">If [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns FILTER\_S\_LAST\_TEXT, the next call to **IFilter::GetText** returns FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="3ce68-248">Si le segment contient une valeur, [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retourne S \_ OK ou filtre \_ E \_ n’a \_ plus aucune \_ valeur.</span><span class="sxs-lookup"><span data-stu-id="3ce68-248">If the chunk contains a value, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns S\_OK or FILTER\_E\_NO\_MORE\_VALUES.</span></span>

### <a name="consistency-test"></a><span data-ttu-id="3ce68-249">Test de cohérence</span><span class="sxs-lookup"><span data-stu-id="3ce68-249">Consistency Test</span></span>

<span data-ttu-id="3ce68-250">Le programme de ifilttxt.exe réinitialise l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) avec les mêmes paramètres que dans le test de validation et effectue un test de cohérence.</span><span class="sxs-lookup"><span data-stu-id="3ce68-250">The ifilttxt.exe program re-initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface with the same parameters as in the validation test and performs a consistency test.</span></span> <span data-ttu-id="3ce68-251">Si l’implémentation **IFilter** a été initialisée avec l’indicateur [**IFilter \_ init**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFilter \_ init \_ Indexing \_ uniquement, le test libère l’interface **IFilter** et la lie de nouveau avant d’effectuer un autre appel à la méthode [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="3ce68-251">If the **IFilter** implementation has been initialized with the [**IFILTER\_INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFILTER\_INIT\_INDEXING\_ONLY flag, the test releases the **IFilter** interface and re-binds it before making another call to the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span>

<span data-ttu-id="3ce68-252">Le test de cohérence vérifie les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ce68-252">The consistency test verifies the following conditions:</span></span>

- <span data-ttu-id="3ce68-253">Chaque structure de [**\_ bloc stat**](/windows/win32/api/filter/ns-filter-stat_chunk) retournée par la méthode [**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) est identique au **\_ segment stat** correspondant retourné dans le test de validation.</span><span class="sxs-lookup"><span data-stu-id="3ce68-253">Each [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) structure returned by the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) method is identical to the corresponding **STAT\_CHUNK** returned in the validation test.</span></span>
- <span data-ttu-id="3ce68-254">[**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retourne le \_ ou les autres valeurs de retour acceptables, comme le filtre \_ e \_ End \_ des \_ segments, le filtre \_ e \_ Link \_ non disponible, etc.</span><span class="sxs-lookup"><span data-stu-id="3ce68-254">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns S\_OK or other acceptable return value, such as FILTER\_E\_END\_OF\_CHUNKS, FILTER\_E\_LINK\_UNAVAILABLE, and so forth.</span></span>

### <a name="invalid-input-test"></a><span data-ttu-id="3ce68-255">Test d’entrée non valide</span><span class="sxs-lookup"><span data-stu-id="3ce68-255">Invalid Input Test</span></span>

<span data-ttu-id="3ce68-256">Le programme de ifilttst.exe réinitialise l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) avec les mêmes paramètres et effectue un test d’entrée non valide.</span><span class="sxs-lookup"><span data-stu-id="3ce68-256">The ifilttst.exe program re-initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface with the same parameters,and performs an invalid input test.</span></span> <span data-ttu-id="3ce68-257">Ce test parcourt le document un segment à la fois, ce qui rend les appels de fonction incorrects, tels que l’appel de la méthode [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) lorsque le mandrin actuel contient du texte.</span><span class="sxs-lookup"><span data-stu-id="3ce68-257">This test steps through the document one chunk at a time making function calls incorrectly, such as calling the [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) method when the current chuck contains text.</span></span> <span data-ttu-id="3ce68-258">Le test vérifie que tous les codes de retour sont conformes à la spécification **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="3ce68-258">The test checks all return codes for compliance with the **IFilter** specification.</span></span>

<span data-ttu-id="3ce68-259">Le test d’entrée non valide vérifie les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ce68-259">The invalid input test verifies the following conditions:</span></span>

- <span data-ttu-id="3ce68-260">Si le bloc actuel contient du texte, [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retourne \_ le filtre E \_ no \_ values et un appel à [**IFilter :: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) se déroule correctement.</span><span class="sxs-lookup"><span data-stu-id="3ce68-260">If the current chunk contains text, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns FILTER\_E\_NO\_VALUES, and a call to [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) succeeds.</span></span>
- <span data-ttu-id="3ce68-261">Si le bloc actuel contient une valeur, [**IFilter :: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retourne le filtre \_ E \_ no \_ Text et un appel à [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) se déroule correctement.</span><span class="sxs-lookup"><span data-stu-id="3ce68-261">If the current chunk contains a value, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns FILTER\_E\_NO\_TEXT, and a call to [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) succeeds.</span></span>
- <span data-ttu-id="3ce68-262">Si l’appel précédent à [**IFilter :: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) a retourné le filtre \_ e \_ plus de \_ \_ texte, les appels successifs à **IFilter :: gettext** retournent le filtre e plus de \_ \_ \_ \_ texte.</span><span class="sxs-lookup"><span data-stu-id="3ce68-262">If the previous call to [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returned FILTER\_E\_NO\_MORE\_TEXT, successive calls to **IFilter::GetText** return FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="3ce68-263">Si l’appel précédent à [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) a retourné le filtre \_ e \_ plus de \_ \_ valeurs, les appels successifs à **IFilter :: GetValue** retournent le filtre e, plus \_ \_ aucune \_ \_ valeur.</span><span class="sxs-lookup"><span data-stu-id="3ce68-263">If the previous call to [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returned FILTER\_E\_NO\_MORE\_VALUES, successive calls to **IFilter::GetValue** return FILTER\_E\_NO\_MORE\_VALUES.</span></span>
- <span data-ttu-id="3ce68-264">Si l’appel précédent à [**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) a retourné le filtre \_ e \_ End \_ de \_ segments, les appels successifs à **IFilter :: GetChunk** retournent le filtre \_ e \_ End \_ des \_ segments.</span><span class="sxs-lookup"><span data-stu-id="3ce68-264">If the previous call to [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returned FILTER\_E\_END\_OF\_CHUNKS, successive calls to **IFilter::GetChunk** return FILTER\_E\_END\_OF\_CHUNKS.</span></span>

> [!NOTE]  
> <span data-ttu-id="3ce68-265">Le test d’entrée non valide compare les structures de blocs actuelles à celles retournées dans le test de validation pour s’assurer qu’elles sont identiques.</span><span class="sxs-lookup"><span data-stu-id="3ce68-265">The invalid input test compares the current chunk structures to those returned in the validation test to make sure they are identical.</span></span>

### <a name="testing-different-ifilter-configurations"></a><span data-ttu-id="3ce68-266">Test de différentes configurations IFilter</span><span class="sxs-lookup"><span data-stu-id="3ce68-266">Testing Different IFilter Configurations</span></span>

<span data-ttu-id="3ce68-267">Le programme ifilttst.exe libère l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) et se reconnecte, ce qui l’initialise avec le jeu de paramètres suivant.</span><span class="sxs-lookup"><span data-stu-id="3ce68-267">The ifilttst.exe program releases the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface and rebinds, this time initializing it with the next set of parameters.</span></span> <span data-ttu-id="3ce68-268">Le test répète le cycle : test de validation, test de cohérence et test d’entrée non valide, jusqu’à ce que toutes les configurations **IFilter** souhaitées spécifiées dans [ifilttst.ini](#ifilttstini) fichier aient été testées.</span><span class="sxs-lookup"><span data-stu-id="3ce68-268">The test repeats the cycle: validation test, consistency test, and invalid input test, until all the desired **IFilter** configurations specified in [ifilttst.ini](#ifilttstini) file have been tested.</span></span>

## <a name="ensuring-registered-items-get-indexed"></a><span data-ttu-id="3ce68-269">Vérification de l’indexation des éléments inscrits</span><span class="sxs-lookup"><span data-stu-id="3ce68-269">Ensuring Registered Items Get Indexed</span></span>

<span data-ttu-id="3ce68-270">Le test final de votre [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) garantit que votre **IFilter** est correctement inscrit et qu’il est appelé pour indexer les éléments que vous avez enregistrés pour l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="3ce68-270">The final test of your [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ensures that your **IFilter** is properly registered and that it is invoked to index the items that you registered to use it.</span></span> <span data-ttu-id="3ce68-271">Vous pouvez utiliser le gestionnaire de catalogues pour initier la réindexation, ou utiliser le gestionnaire de portée d’analyse (CSM) pour configurer des règles par défaut indiquant les URL que vous souhaitez que l’indexeur analyse.</span><span class="sxs-lookup"><span data-stu-id="3ce68-271">You can use the Catalog Manager to initiate re-indexing, or use the Crawl Scope Manager (CSM) to set up default rules indicating the URLs that you want the indexer to crawl.</span></span> <span data-ttu-id="3ce68-272">Une fois l’indexation terminée, utilisez l’interface utilisateur de recherche Windows pour rechercher une chaîne dans le contenu ou les propriétés des éléments.</span><span class="sxs-lookup"><span data-stu-id="3ce68-272">After indexing is complete, use the Windows Search UI to search for a string in the content or properties of items.</span></span> <span data-ttu-id="3ce68-273">Si les éléments ont été indexés, ils s’affichent dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="3ce68-273">If the items were indexed, they will appear in the search results.</span></span>

<span data-ttu-id="3ce68-274">Pour plus d’informations sur la réindexation, consultez [utilisation du gestionnaire de catalogues](-search-3x-wds-mngidx-catalog-manager.md) et [utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="3ce68-274">For more information about re-indexing, see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span> <span data-ttu-id="3ce68-275">L’exemple de code ReindexMatchingUrls montre comment spécifier les fichiers à réindexer et comment.</span><span class="sxs-lookup"><span data-stu-id="3ce68-275">The ReindexMatchingUrls code sample demonstrates ways to specify which files to re-index and how.</span></span> <span data-ttu-id="3ce68-276">L’exemple de code CrawlScopeCommandLine montre comment définir des options de ligne de commande pour les opérations d’indexation du gestionnaire de portée d’analyse (CSM).</span><span class="sxs-lookup"><span data-stu-id="3ce68-276">The CrawlScopeCommandLine code sample demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.</span></span> <span data-ttu-id="3ce68-277">Les deux exemples de code sont disponibles sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span><span class="sxs-lookup"><span data-stu-id="3ce68-277">Both code samples are available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span></span>

### <a name="sample-log-file"></a><span data-ttu-id="3ce68-278">Exemple de fichier journal</span><span class="sxs-lookup"><span data-stu-id="3ce68-278">Sample Log File</span></span>

<span data-ttu-id="3ce68-279">À la demande, le programme Ifilttst.exe peut générer un journal contenant une description des étapes qu’il effectue pendant l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3ce68-279">Upon request, the Ifilttst.exe program can produce a log containing a description of the steps it takes during execution.</span></span> <span data-ttu-id="3ce68-280">Les exemples suivants sont des extraits d’un fichier journal, avec le niveau de détail défini sur la valeur la plus élevée possible 3.</span><span class="sxs-lookup"><span data-stu-id="3ce68-280">The following examples are excerpts from a log file, with the verbosity set to the highest possible value 3.</span></span>

```
            1. INFO----**** New configuration ****
            2.
            3. Section name : Test2
            4. grfFlags     : 63
            5. cAttributes  : 0
            6. aAttributes  : NONE
            7. pdwFlags     : 0
            8.
            9. INFO----Successfully bound filter.
            10.
            11. PASS----Init() returned a valid value for pdwFlags.
            12.
            13. INFO----Successfully initialized filter.
            14.
            15. INFO----Performing validation test. In this part of the test, the chunks structures
            16.         returned by the IFilter are checked for correctness, and the return values
            17.         of the IFilter calls are checked.
            18.
            19. PASS----GetChunk() succeeded.
            20.
            21. PASS----The current chunk has a legal value for the flags field.

```

<span data-ttu-id="3ce68-281">La première ligne est un message d’information indiquant qu’une nouvelle configuration a été chargée à partir du fichier ifilttst.ini.</span><span class="sxs-lookup"><span data-stu-id="3ce68-281">The first line is an informational message, indicating that a new configuration has been loaded from the ifilttst.ini file.</span></span> <span data-ttu-id="3ce68-282">Line (3) indique le nom de la section dans le fichier ifilttst.ini à partir duquel la configuration actuelle a été lue.</span><span class="sxs-lookup"><span data-stu-id="3ce68-282">Line (3) indicates the section name in the ifilttst.ini file from which the current configuration has been read.</span></span> <span data-ttu-id="3ce68-283">Les lignes (4) à (7) répertorient les paramètres de [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init).</span><span class="sxs-lookup"><span data-stu-id="3ce68-283">Lines (4) through (7) list the parameters to [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init).</span></span> <span data-ttu-id="3ce68-284">Les lignes commençant par `INFO` sont des messages d’information sur la liaison du [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) et le début du test de validation.</span><span class="sxs-lookup"><span data-stu-id="3ce68-284">The lines starting with `INFO` are informational messages about the binding of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) and the start of the validation test.</span></span> <span data-ttu-id="3ce68-285">Les lignes commençant par `PASS` sont des messages relatifs à des tests spécifiques qui ont réussi.</span><span class="sxs-lookup"><span data-stu-id="3ce68-285">Lines starting with `PASS` are messages regarding specific tests that have passed.</span></span>

<span data-ttu-id="3ce68-286">La ligne de l’exemple de journal suivant est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="3ce68-286">The line in the following log example is a warning.</span></span> <span data-ttu-id="3ce68-287">Les avertissements attirent l’attention sur le comportement [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) qui pose problème, bien que légal.</span><span class="sxs-lookup"><span data-stu-id="3ce68-287">Warnings call attention to [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) behavior that is problematic, although legal.</span></span> <span data-ttu-id="3ce68-288">Cet avertissement indique que la méthode [**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) a retourné un segment de texte qui ne contient pas de texte.</span><span class="sxs-lookup"><span data-stu-id="3ce68-288">This warning indicates that the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) method has returned a text chunk that contains no text.</span></span>

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

<span data-ttu-id="3ce68-289">L’exemple de message d’erreur suivant indique que le [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) a émis un segment qui n’a pas été demandé.</span><span class="sxs-lookup"><span data-stu-id="3ce68-289">The following example error message indicates that the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitted a chunk that was not requested.</span></span>

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

<span data-ttu-id="3ce68-290">Dans le cas de cet exemple de message d’erreur, le [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) a émis un segment avec un PID de `0x5` .</span><span class="sxs-lookup"><span data-stu-id="3ce68-290">In the case of this example error message, the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitted a chunk with a PID of `0x5`.</span></span> <span data-ttu-id="3ce68-291">L’inspection de `[Test1]` la section dans ifilttst.ini indique que le **IFilter** a été configuré pour ne pas émettre de segments avec ce PID.</span><span class="sxs-lookup"><span data-stu-id="3ce68-291">Inspection of section `[Test1]` in ifilttst.ini would show that the **IFilter** was configured to not emit chunks with this PID.</span></span> <span data-ttu-id="3ce68-292">Par exemple, si vous n' \_ appliquez pas d’attributs d’initialisation IFilter ou d' \_ \_ \_ initialisation IFilter, \_ \_ \_ \_ les autres attributs n’ont pas été spécifiés dans l’entrée Flags et si les *cAttributes* étaient 0, **IFilter** émettra uniquement des segments avec un PID de `0x13` et correspondant au \_ contenu PID STG \_ .</span><span class="sxs-lookup"><span data-stu-id="3ce68-292">For example, if neither IFILTER\_INIT\_APPLY\_INDEX\_ATTRIBUTES nor IFILTER\_INIT\_APPLY\_OTHER\_ATTRIBUTES were specified in the Flags entry and if *cAttributes* were 0, then **IFilter** would emit only chunks with a PID of `0x13` and corresponding to PID\_STG\_CONTENTS.</span></span>

### <a name="sample-dump-file"></a><span data-ttu-id="3ce68-293">Exemple de fichier dump</span><span class="sxs-lookup"><span data-stu-id="3ce68-293">Sample Dump File</span></span>

<span data-ttu-id="3ce68-294">À la demande, le programme Ifilttst.exe peut produire un vidage contenant les segments qu’il trouve et leur contenu.</span><span class="sxs-lookup"><span data-stu-id="3ce68-294">Upon request, the Ifilttst.exe program can produce a dump containing the chunks it finds and their content.</span></span> <span data-ttu-id="3ce68-295">L’exemple suivant est un extrait de ce type de fichier de vidage.</span><span class="sxs-lookup"><span data-stu-id="3ce68-295">The following example is an excerpt from such a dump file.</span></span>

```
                1. Chunk ID: ........... 2
                2. Chunk Break Type: ... END OF SENTENCE
                3. Chunk State: ........ TEXT
                4. Chunk Locale: ....... 0x411
                5. Chunk Source ID: .... 2
                6. Chunk Start Source .. 0x0
                7. Chunk Length Source . 0x0
                8. GUID ................ b725f130-47ef-101a-a5f1-02608c9eebac
                9. Property ID ......... 0x13

                10. This is a HTML IFilter test page

                11. Chunk ID: ........... 3
                12. Chunk Break Type: ... END OF SENTENCE
                13. Chunk State: ........ TEXT
                14. Chunk Locale: ....... 0x411
                15. Chunk Source ID: .... 2
                16. Chunk Start Source .. 0x0
                17. Chunk Length Source . 0x0
                18. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                19. Property ID ......... 0x2

                20. This is a HTML IFilter test page

                21. Chunk ID: ........... 4
                22. Chunk Break Type: ... END OF SENTENCE
                23. Chunk State: ........ VALUE
                24. Chunk Locale: ....... 0x411
                25. Chunk Source ID: .... 2
                26. Chunk Start Source .. 0x0
                27. Chunk Length Source . 0x0
                28. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                29. Property ID ......... 0x2

                30. This is an HTML IFilter test page
```

<span data-ttu-id="3ce68-296">Les neuf premières lignes décrivent la structure de blocs actuelle.</span><span class="sxs-lookup"><span data-stu-id="3ce68-296">The first nine lines describe the current chunk structure.</span></span> <span data-ttu-id="3ce68-297">Le GUID et le PID correspondent au \_ contenu de stockage/PID PSGUID \_ STG \_ .</span><span class="sxs-lookup"><span data-stu-id="3ce68-297">The GUID and the PID correspond to PSGUID\_STORAGE / PID\_STG\_CONTENTS.</span></span> <span data-ttu-id="3ce68-298">Il s’agit d’un bloc contenant du texte brut.</span><span class="sxs-lookup"><span data-stu-id="3ce68-298">This is a chunk containing plain text.</span></span> <span data-ttu-id="3ce68-299">Le texte se trouve dans la structure de blocs suivante :</span><span class="sxs-lookup"><span data-stu-id="3ce68-299">The text is in the following chunk structure:</span></span>

```
10. This is an HTML IFilter test page
```

<span data-ttu-id="3ce68-300">Le bloc suivant, à partir de la ligne 11, a un GUID différent, correspondant à `HTML IFilter` et un PID différent, correspondant à une href html.</span><span class="sxs-lookup"><span data-stu-id="3ce68-300">The next chunk, starting at line 11, has a different GUID, corresponding to the `HTML IFilter`, and a different PID, corresponding to an HTML HREF.</span></span> <span data-ttu-id="3ce68-301">Il s’agit d’une propriété de type valeur interne, exportée par `HTML IFilter` .</span><span class="sxs-lookup"><span data-stu-id="3ce68-301">This is an internal value-type property, exported by the `HTML IFilter`.</span></span>

<span data-ttu-id="3ce68-302">Le bloc suivant, à partir de la ligne 21, a le même GUID et PID, mais son état `VALUE` de bloc est au lieu de `TEXT` .</span><span class="sxs-lookup"><span data-stu-id="3ce68-302">The next chunk, starting at line 21, has the same GUID and PID, but its chunk state is `VALUE` instead of `TEXT`.</span></span> <span data-ttu-id="3ce68-303">Notez que le texte de ces deux derniers segments est le même que pour le premier segment.</span><span class="sxs-lookup"><span data-stu-id="3ce68-303">Note that the text in these last two chunks is the same as for the first chunk.</span></span> <span data-ttu-id="3ce68-304">Toutefois, étant donné que le [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) est conçu pour appliquer trois attributs (texte brut, texte de description html et href html comme valeur) à appliquer à cette expression, les résultats sont émis dans trois segments distincts.</span><span class="sxs-lookup"><span data-stu-id="3ce68-304">But because the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is designed for three attributes (plain text, HTML HREF as text, and HTML HREF as a value) to be applied to this phrase, the results are emitted in three separate chunks.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ce68-305">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3ce68-305">Additional Resources</span></span>

- <span data-ttu-id="3ce68-306">L’exemple de code [IFilterSample](-search-sample-ifiltersample.md) , disponible sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), montre comment créer une classe de base IFilter pour l’implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="3ce68-306">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="3ce68-307">Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3ce68-307">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="3ce68-308">Pour obtenir une vue d’ensemble des types de fichiers, consultez [types de fichiers](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="3ce68-308">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="3ce68-309">Pour interroger des attributs d’association de fichiers pour un type de fichier, consultez [PerceivedTypes, SystemFileAssociations et inscription d’application](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ce68-309">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ce68-310">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ce68-310">Related topics</span></span>

[<span data-ttu-id="3ce68-311">Développement de gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="3ce68-311">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="3ce68-312">À propos des gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="3ce68-312">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="3ce68-313">Meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="3ce68-313">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="3ce68-314">Retour des propriétés d’un gestionnaire de filtres</span><span class="sxs-lookup"><span data-stu-id="3ce68-314">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="3ce68-315">Gestionnaires de filtres fournis avec Windows</span><span class="sxs-lookup"><span data-stu-id="3ce68-315">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="3ce68-316">Implémentation de gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="3ce68-316">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="3ce68-317">Inscription des gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="3ce68-317">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
