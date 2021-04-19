---
title: Syntaxe
description: Voici la syntaxe d’appel de FXC.exe, l’outil Effect-compiler. Pour obtenir un exemple, consultez Compilation hors connexion.
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- fxc, syntaxe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241a728b4835b11d10ea6e39d67fd73a8576cd7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "106511104"
---
# <a name="syntax"></a><span data-ttu-id="427c1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="427c1-105">Syntax</span></span>

<span data-ttu-id="427c1-106">Voici la syntaxe d’appel de FXC.exe, l’outil Effect-compiler.</span><span class="sxs-lookup"><span data-stu-id="427c1-106">Here is the syntax for calling FXC.exe, the effect-compiler tool.</span></span> <span data-ttu-id="427c1-107">Pour obtenir un exemple, consultez [compilation hors connexion](dx-graphics-tools-fxc-using.md).</span><span class="sxs-lookup"><span data-stu-id="427c1-107">For an example, see [Offline Compiling](dx-graphics-tools-fxc-using.md).</span></span>

-   [<span data-ttu-id="427c1-108">Utilisation</span><span class="sxs-lookup"><span data-stu-id="427c1-108">Usage</span></span>](#usage)
-   [<span data-ttu-id="427c1-109">Arguments</span><span class="sxs-lookup"><span data-stu-id="427c1-109">Arguments</span></span>](#arguments)
-   [<span data-ttu-id="427c1-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="427c1-110">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="427c1-111">Profils</span><span class="sxs-lookup"><span data-stu-id="427c1-111">Profiles</span></span>](#profiles)
-   [<span data-ttu-id="427c1-112">Notes de version</span><span class="sxs-lookup"><span data-stu-id="427c1-112">Version notes</span></span>](#version-notes)
-   [<span data-ttu-id="427c1-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="427c1-113">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="427c1-114">Utilisation</span><span class="sxs-lookup"><span data-stu-id="427c1-114">Usage</span></span>

<span data-ttu-id="427c1-115">**fxc** *SwitchOptions* *nom de fichier*</span><span class="sxs-lookup"><span data-stu-id="427c1-115">**fxc** *SwitchOptions* *Filenames*</span></span>

## <a name="arguments"></a><span data-ttu-id="427c1-116">Arguments</span><span class="sxs-lookup"><span data-stu-id="427c1-116">Arguments</span></span>
<span data-ttu-id="427c1-117">Séparez chaque option de commutateur par un espace ou un signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="427c1-117">Separate each switch option with a space or a colon.</span></span>

### <a name="switchoptions"></a><span data-ttu-id="427c1-118">*SwitchOptions*</span><span class="sxs-lookup"><span data-stu-id="427c1-118">*SwitchOptions*</span></span>
<span data-ttu-id="427c1-119">\[dans les \] options de compilation.</span><span class="sxs-lookup"><span data-stu-id="427c1-119">\[in\] Compile options.</span></span> <span data-ttu-id="427c1-120">Il n’existe qu’une seule option obligatoire, et bien d’autres sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="427c1-120">There is just one required option, and many more that are optional.</span></span> <span data-ttu-id="427c1-121">Séparez-les par un espace ou un signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="427c1-121">Separate each with a space or colon.</span></span>

#### <a name="required-option"></a><span data-ttu-id="427c1-122">Option obligatoire</span><span class="sxs-lookup"><span data-stu-id="427c1-122">Required option</span></span>
##### <a name="t-profile"></a><span data-ttu-id="427c1-123">/T <*Profil*></span><span class="sxs-lookup"><span data-stu-id="427c1-123">/T <*profile*></span></span>
<span data-ttu-id="427c1-124">Modèle de nuanceur (voir [profils](#profiles)).</span><span class="sxs-lookup"><span data-stu-id="427c1-124">Shader model (see [Profiles](#profiles)).</span></span>

#### <a name="optional-options"></a><span data-ttu-id="427c1-125">Options facultatives</span><span class="sxs-lookup"><span data-stu-id="427c1-125">Optional options</span></span>
##### <a name="-help"></a><span data-ttu-id="427c1-126">/?, /help</span><span class="sxs-lookup"><span data-stu-id="427c1-126">/?, /help</span></span>
<span data-ttu-id="427c1-127">Imprimer l’aide pour `FXC.exe` .</span><span class="sxs-lookup"><span data-stu-id="427c1-127">Print help for `FXC.exe`.</span></span>

##### <a name="commandoptionfile"></a><span data-ttu-id="427c1-128">@<*commande. option. file*></span><span class="sxs-lookup"><span data-stu-id="427c1-128">@<*command.option.file*></span></span>
<span data-ttu-id="427c1-129">Fichier qui contient des options de compilation supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="427c1-129">File that contains additional compile options.</span></span> <span data-ttu-id="427c1-130">Cette option peut être mélangée à d’autres options de compilation de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="427c1-130">This option can be mixed with other command line compile options.</span></span> <span data-ttu-id="427c1-131">La *commande. option. file* ne doit contenir qu’une seule option par ligne.</span><span class="sxs-lookup"><span data-stu-id="427c1-131">The *command.option.file* must contain only one option per line.</span></span> <span data-ttu-id="427c1-132">La *commande. option. file* ne peut pas contenir de lignes vides.</span><span class="sxs-lookup"><span data-stu-id="427c1-132">The *command.option.file* cannot contain any blank lines.</span></span> <span data-ttu-id="427c1-133">Les options spécifiées dans le fichier ne doivent pas contenir d’espaces de début ou de fin.</span><span class="sxs-lookup"><span data-stu-id="427c1-133">Options specified in the file must not contain any leading or trailing spaces.</span></span>

##### <a name="all_resources_bound"></a><span data-ttu-id="427c1-134">/all_resources_bound</span><span class="sxs-lookup"><span data-stu-id="427c1-134">/all_resources_bound</span></span>
<span data-ttu-id="427c1-135">Activez la mise à plat agressive dans SM 5.1 +.</span><span class="sxs-lookup"><span data-stu-id="427c1-135">Enable aggressive flattening in SM5.1+.</span></span> <span data-ttu-id="427c1-136">Nouveauté de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="427c1-136">New for Direct3D 12.</span></span>

##### <a name="cc"></a><span data-ttu-id="427c1-137">/CC</span><span class="sxs-lookup"><span data-stu-id="427c1-137">/Cc</span></span>
<span data-ttu-id="427c1-138">Assembly avec code de couleur de sortie.</span><span class="sxs-lookup"><span data-stu-id="427c1-138">Output color-coded assembly.</span></span>

##### <a name="compress"></a><span data-ttu-id="427c1-139">/compress</span><span class="sxs-lookup"><span data-stu-id="427c1-139">/compress</span></span>
<span data-ttu-id="427c1-140">Compresser le bytecode de nuanceur facilement à partir de fichiers.</span><span class="sxs-lookup"><span data-stu-id="427c1-140">Compress DX10 shader bytecode from files.</span></span>

##### <a name="d-idtext"></a><span data-ttu-id="427c1-141">/D <d' *ID* >=< *texte*></span><span class="sxs-lookup"><span data-stu-id="427c1-141">/D <*id*>=<*text*></span></span>
<span data-ttu-id="427c1-142">Définissez la macro.</span><span class="sxs-lookup"><span data-stu-id="427c1-142">Define macro.</span></span>

##### <a name="decompress"></a><span data-ttu-id="427c1-143">/decompress</span><span class="sxs-lookup"><span data-stu-id="427c1-143">/decompress</span></span>
<span data-ttu-id="427c1-144">Décompressez le bytecode de nuanceur facilement à partir du premier fichier.</span><span class="sxs-lookup"><span data-stu-id="427c1-144">Decompress DX10 shader bytecode from first file.</span></span> <span data-ttu-id="427c1-145">Les fichiers de sortie doivent être listés dans l’ordre dans lequel ils se trouvaient lors de la compression.</span><span class="sxs-lookup"><span data-stu-id="427c1-145">Output files should be listed in the order they were in during compression.</span></span>

##### <a name="dumpbin"></a><span data-ttu-id="427c1-146">/dumpbin</span><span class="sxs-lookup"><span data-stu-id="427c1-146">/dumpbin</span></span>
<span data-ttu-id="427c1-147">Charge un fichier binaire au lieu de compiler un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="427c1-147">Loads a binary file rather than compiling a shader.</span></span>

##### <a name="e-name"></a><span data-ttu-id="427c1-148">/E <name></span><span class="sxs-lookup"><span data-stu-id="427c1-148">/E <name></span></span>
<span data-ttu-id="427c1-149">Point d’entrée du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="427c1-149">Shader entry point.</span></span> <span data-ttu-id="427c1-150">Si aucun point d’entrée n’est spécifié, **main** est considéré comme le nom de l’entrée du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="427c1-150">If no entry point is given, **main** is considered to be the shader entry name.</span></span>

##### <a name="enable_unbounded_descriptor_tables"></a><span data-ttu-id="427c1-151">/enable_unbounded_descriptor_tables</span><span class="sxs-lookup"><span data-stu-id="427c1-151">/enable_unbounded_descriptor_tables</span></span>
<span data-ttu-id="427c1-152">Active les tables de descripteurs non liées.</span><span class="sxs-lookup"><span data-stu-id="427c1-152">Enables unbounded descriptor tables.</span></span> <span data-ttu-id="427c1-153">Nouveauté de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="427c1-153">New for Direct3D 12.</span></span>

##### <a name="extractrootsignature-file"></a><span data-ttu-id="427c1-154">*fichier* de </extractrootsignature></span><span class="sxs-lookup"><span data-stu-id="427c1-154">/extractrootsignature <*file*></span></span>
<span data-ttu-id="427c1-155">Extrayez la signature racine à partir du bytecode du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="427c1-155">Extract root signature from shader bytecode.</span></span> <span data-ttu-id="427c1-156">Nouveauté de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="427c1-156">New for Direct3D 12.</span></span>

##### <a name="fc-file"></a><span data-ttu-id="427c1-157">/FC <*fichier*></span><span class="sxs-lookup"><span data-stu-id="427c1-157">/Fc <*file*></span></span>
<span data-ttu-id="427c1-158">Fichier de liste de code d’assembly de sortie.</span><span class="sxs-lookup"><span data-stu-id="427c1-158">Output assembly code listing file.</span></span>

##### <a name="fd-file"></a><span data-ttu-id="427c1-159">*Fichier* </FD></span><span class="sxs-lookup"><span data-stu-id="427c1-159">/Fd <*file*></span></span>
<span data-ttu-id="427c1-160">Extrayez les informations de la base de données du programme Shader (PDB) et écrivez dans le fichier donné. Quand vous compilez le nuanceur, utilisez/FD pour générer un fichier PDB avec les informations de débogage du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="427c1-160">Extract shader program database (PDB) info and write to the given file.When you compile the shader, use /Fd to generate a PDB file with shader debugging info.</span></span>

##### <a name="fe-file"></a><span data-ttu-id="427c1-161">/Fe <*fichier*></span><span class="sxs-lookup"><span data-stu-id="427c1-161">/Fe <*file*></span></span>
<span data-ttu-id="427c1-162">Affiche les avertissements et les erreurs dans le fichier donné.</span><span class="sxs-lookup"><span data-stu-id="427c1-162">Output warnings and errors to the given file.</span></span>

##### <a name="fh-file"></a><span data-ttu-id="427c1-163">*Fichier* de </FH></span><span class="sxs-lookup"><span data-stu-id="427c1-163">/Fh <*file*></span></span>
<span data-ttu-id="427c1-164">Fichier d’en-tête de sortie contenant le code objet.</span><span class="sxs-lookup"><span data-stu-id="427c1-164">Output header file containing object code.</span></span>

##### <a name="fl-file"></a><span data-ttu-id="427c1-165">*Fichier* de </FL</span><span class="sxs-lookup"><span data-stu-id="427c1-165">/Fl <*file*</span></span>
<span data-ttu-id="427c1-166">Sortie d’une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="427c1-166">Output a library.</span></span> <span data-ttu-id="427c1-167">Requiert le \_47.dll D3dcompiler ou une version ultérieure de la dll.</span><span class="sxs-lookup"><span data-stu-id="427c1-167">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="fo-file"></a><span data-ttu-id="427c1-168">/FO <*fichier*></span><span class="sxs-lookup"><span data-stu-id="427c1-168">/Fo <*file*></span></span>
<span data-ttu-id="427c1-169">Fichier objet de sortie.</span><span class="sxs-lookup"><span data-stu-id="427c1-169">Output object file.</span></span> <span data-ttu-id="427c1-170">Souvent avec l’extension &quot; . fxc &quot; , bien que d’autres extensions soient utilisées, telles que &quot; . o &quot; , &quot; . obj &quot; ou &quot; . dxbc &quot; .</span><span class="sxs-lookup"><span data-stu-id="427c1-170">Often given the extension &quot;.fxc&quot;, though other extensions are used, such as &quot;.o&quot;, &quot;.obj&quot; or &quot;.dxbc&quot;.</span></span>

##### <a name="fx-file"></a><span data-ttu-id="427c1-171">/FX <*fichier*></span><span class="sxs-lookup"><span data-stu-id="427c1-171">/Fx <*file*></span></span>
<span data-ttu-id="427c1-172">Code assembleur de sortie et fichier de liste hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="427c1-172">Output assembly code and hex listing file.</span></span>

##### <a name="gch"></a><span data-ttu-id="427c1-173">/Gch</span><span class="sxs-lookup"><span data-stu-id="427c1-173">/Gch</span></span>
<span data-ttu-id="427c1-174">Compilez comme un effet enfant pour les profils de fx_4_x.</span><span class="sxs-lookup"><span data-stu-id="427c1-174">Compile as a child effect for fx_4_x profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="427c1-175">La prise en charge des profils d’effets hérités est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="427c1-175">Support for legacy Effects profiles is deprecated.</span></span>

##### <a name="gdp"></a><span data-ttu-id="427c1-176">/Gdp</span><span class="sxs-lookup"><span data-stu-id="427c1-176">/Gdp</span></span>
<span data-ttu-id="427c1-177">Désactivez le mode performance Effect.</span><span class="sxs-lookup"><span data-stu-id="427c1-177">Disable effect performance mode.</span></span>

##### <a name="gec"></a><span data-ttu-id="427c1-178">/Gec</span><span class="sxs-lookup"><span data-stu-id="427c1-178">/Gec</span></span>
<span data-ttu-id="427c1-179">Activez le mode de compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="427c1-179">Enable backward compatibility mode.</span></span>

##### <a name="ges"></a><span data-ttu-id="427c1-180">/Ges</span><span class="sxs-lookup"><span data-stu-id="427c1-180">/Ges</span></span>
<span data-ttu-id="427c1-181">Activez le mode strict.</span><span class="sxs-lookup"><span data-stu-id="427c1-181">Enable strict mode.</span></span>

##### <a name="getprivate-file"></a><span data-ttu-id="427c1-182">*fichier* de </getPrivate></span><span class="sxs-lookup"><span data-stu-id="427c1-182">/getprivate <*file*></span></span>
<span data-ttu-id="427c1-183">Enregistrer les données privées à partir de l’objet blob de nuanceur (binaire compilé) dans le fichier donné.</span><span class="sxs-lookup"><span data-stu-id="427c1-183">Save private data from the shader blob (compiled shader binary) to the given file.</span></span> <span data-ttu-id="427c1-184">Extrait les données privées précédemment incorporées par/SetPrivate à partir de l’objet blob de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="427c1-184">Extracts private data, previously embedded by /setprivate, from the shader blob.</span></span>

<span data-ttu-id="427c1-185">Vous devez spécifier l’option/DUMPBIN avec/getPrivate.</span><span class="sxs-lookup"><span data-stu-id="427c1-185">You must specify the /dumpbin option with /getprivate.</span></span> <span data-ttu-id="427c1-186">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="427c1-186">For example:</span></span>

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a><span data-ttu-id="427c1-187">/Gfa</span><span class="sxs-lookup"><span data-stu-id="427c1-187">/Gfa</span></span>
<span data-ttu-id="427c1-188">Évitez les constructions de contrôle de Flow.</span><span class="sxs-lookup"><span data-stu-id="427c1-188">Avoid flow control constructs.</span></span>

##### <a name="gfp"></a><span data-ttu-id="427c1-189">/GFP</span><span class="sxs-lookup"><span data-stu-id="427c1-189">/Gfp</span></span>
<span data-ttu-id="427c1-190">Préférer les constructions de contrôle de Flow.</span><span class="sxs-lookup"><span data-stu-id="427c1-190">Prefer flow control constructs.</span></span>

##### <a name="gis"></a><span data-ttu-id="427c1-191">/Gis</span><span class="sxs-lookup"><span data-stu-id="427c1-191">/Gis</span></span>
<span data-ttu-id="427c1-192">Force la strictité IEEE.</span><span class="sxs-lookup"><span data-stu-id="427c1-192">Force IEEE strictness.</span></span>

##### <a name="gpp"></a><span data-ttu-id="427c1-193">/Gpp</span><span class="sxs-lookup"><span data-stu-id="427c1-193">/Gpp</span></span>
<span data-ttu-id="427c1-194">Forcer une précision partielle.</span><span class="sxs-lookup"><span data-stu-id="427c1-194">Force partial precision.</span></span>
    
##### <a name="i-include"></a><span data-ttu-id="427c1-195">/I <*include*></span><span class="sxs-lookup"><span data-stu-id="427c1-195">/I <*include*></span></span>
<span data-ttu-id="427c1-196">Chemin d’accès include supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="427c1-196">Additional include path.</span></span>

##### <a name="lx"></a><span data-ttu-id="427c1-197">/Lx</span><span class="sxs-lookup"><span data-stu-id="427c1-197">/Lx</span></span>
<span data-ttu-id="427c1-198">Littéraux hexadécimaux de sortie.</span><span class="sxs-lookup"><span data-stu-id="427c1-198">Output hexadecimal literals.</span></span> <span data-ttu-id="427c1-199">Requiert le \_47.dll D3dcompiler ou une version ultérieure de la dll.</span><span class="sxs-lookup"><span data-stu-id="427c1-199">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="matchuavs"></a><span data-ttu-id="427c1-200">/matchUAVs</span><span class="sxs-lookup"><span data-stu-id="427c1-200">/matchUAVs</span></span>
<span data-ttu-id="427c1-201">Correspond aux allocations de l’emplacement UAV du nuanceur de modèles dans le nuanceur actuel.</span><span class="sxs-lookup"><span data-stu-id="427c1-201">Match template shader UAV slot allocations in the current shader.</span></span> <span data-ttu-id="427c1-202">Pour plus d’informations, consultez la <a href="#remarks">section Notes</a>.</span><span class="sxs-lookup"><span data-stu-id="427c1-202">For more info, see <a href="#remarks">Remarks</a>.</span></span>

##### <a name="mergeuavs"></a><span data-ttu-id="427c1-203">/mergeUAVs</span><span class="sxs-lookup"><span data-stu-id="427c1-203">/mergeUAVs</span></span>
<span data-ttu-id="427c1-204">Fusionner les allocations d’emplacement UAV du nuanceur de modèles et du nuanceur actuel.</span><span class="sxs-lookup"><span data-stu-id="427c1-204">Merge UAV slot allocations of template shader and the current shader.</span></span> <span data-ttu-id="427c1-205">Pour plus d’informations, consultez la <a href=""></a> <a href="#remarks">section Notes</a>.</span><span class="sxs-lookup"><span data-stu-id="427c1-205">For more info, see <a href=""></a><a href="#remarks">Remarks</a>.</span></span>

##### <a name="ni"></a><span data-ttu-id="427c1-206">/Ni</span><span class="sxs-lookup"><span data-stu-id="427c1-206">/Ni</span></span>
<span data-ttu-id="427c1-207">Numéros d’instruction de sortie dans les listes d’assemblys.</span><span class="sxs-lookup"><span data-stu-id="427c1-207">Output instruction numbers in assembly listings.</span></span>

##### <a name="no"></a><span data-ttu-id="427c1-208">/Non</span><span class="sxs-lookup"><span data-stu-id="427c1-208">/No</span></span>
<span data-ttu-id="427c1-209">Offset d’octet d’instruction de sortie dans les listes d’assemblys.</span><span class="sxs-lookup"><span data-stu-id="427c1-209">Output instruction byte offset in assembly listings.</span></span> <span data-ttu-id="427c1-210">Quand vous générez un assembly, utilisez/non pour l’annoter avec l’offset d’octet pour chaque instruction.</span><span class="sxs-lookup"><span data-stu-id="427c1-210">When you produce assembly, use /No to annotate it with the byte offset for each instruction.</span></span>

##### <a name="nologo"></a><span data-ttu-id="427c1-211">/nologo</span><span class="sxs-lookup"><span data-stu-id="427c1-211">/nologo</span></span>
<span data-ttu-id="427c1-212">Supprime le message de copyright.</span><span class="sxs-lookup"><span data-stu-id="427c1-212">Suppress copyright message.</span></span>

##### <a name="od"></a><span data-ttu-id="427c1-213">/Od</span><span class="sxs-lookup"><span data-stu-id="427c1-213">/Od</span></span>
<span data-ttu-id="427c1-214">Désactivez les optimisations.</span><span class="sxs-lookup"><span data-stu-id="427c1-214">Disable optimizations.</span></span> <span data-ttu-id="427c1-215">/OD implique/GFP, bien que la sortie ne soit pas identique à/OD/GFP.</span><span class="sxs-lookup"><span data-stu-id="427c1-215">/Od implies /Gfp, though output may not be identical to /Od /Gfp.</span></span>

##### <a name="op"></a><span data-ttu-id="427c1-216">/Op</span><span class="sxs-lookup"><span data-stu-id="427c1-216">/Op</span></span>
<span data-ttu-id="427c1-217">Désactiver les prénuanceurs (déconseillé).</span><span class="sxs-lookup"><span data-stu-id="427c1-217">Disable preshaders (deprecated).</span></span>

##### <a name="o0-o1-o2-o3"></a><span data-ttu-id="427c1-218">/O0/O1,/O2,/O3</span><span class="sxs-lookup"><span data-stu-id="427c1-218">/O0 /O1, /O2, /O3</span></span>
<span data-ttu-id="427c1-219">Niveaux d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="427c1-219">Optimization levels.</span></span> <span data-ttu-id="427c1-220">O1 est le paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="427c1-220">O1 is the default setting.</span></span>
- <span data-ttu-id="427c1-221">O0 : désactive la réorganisation des instructions.</span><span class="sxs-lookup"><span data-stu-id="427c1-221">O0 - Disables instruction reordering.</span></span> <span data-ttu-id="427c1-222">Cela permet de réduire la charge des registres et d’accélérer la simulation de boucle.</span><span class="sxs-lookup"><span data-stu-id="427c1-222">This helps reduce register load and enables faster loop simulation.</span></span>
- <span data-ttu-id="427c1-223">O1 : désactive la réorganisation des instructions pour ps_3_0 et vers le haut.</span><span class="sxs-lookup"><span data-stu-id="427c1-223">O1 - Disables instruction reordering for ps_3_0 and up.</span></span>
- <span data-ttu-id="427c1-224">O2-identique à O1.</span><span class="sxs-lookup"><span data-stu-id="427c1-224">O2 - Same as O1.</span></span> <span data-ttu-id="427c1-225">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="427c1-225">Reserved for future use.</span></span>
- <span data-ttu-id="427c1-226">O3-identique à O1.</span><span class="sxs-lookup"><span data-stu-id="427c1-226">O3 - Same as O1.</span></span> <span data-ttu-id="427c1-227">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="427c1-227">Reserved for future use.</span></span>

##### <a name="p-file"></a><span data-ttu-id="427c1-228">/P <*fichier*></span><span class="sxs-lookup"><span data-stu-id="427c1-228">/P <*file*></span></span>
<span data-ttu-id="427c1-229">Prétraiter dans un fichier (doit être utilisé seul).</span><span class="sxs-lookup"><span data-stu-id="427c1-229">Preprocess to file (must be used alone).</span></span>

##### <a name="qstrip_debug"></a><span data-ttu-id="427c1-230">/Qstrip_debug</span><span class="sxs-lookup"><span data-stu-id="427c1-230">/Qstrip_debug</span></span>
<span data-ttu-id="427c1-231">Supprimez les données de débogage du bytecode de nuanceur pour les profils 4_0 +.</span><span class="sxs-lookup"><span data-stu-id="427c1-231">Strip debug data from shader bytecode for 4_0+ profiles.</span></span>

##### <a name="qstrip_priv"></a><span data-ttu-id="427c1-232">/Qstrip_priv</span><span class="sxs-lookup"><span data-stu-id="427c1-232">/Qstrip_priv</span></span>
<span data-ttu-id="427c1-233">Supprimez les données privées de 4_0 + bytecode de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="427c1-233">Strip the private data from 4_0+ shader bytecode.</span></span> <span data-ttu-id="427c1-234">Supprime les données privées (séquence arbitraire d’octets) de l’objet blob de nuanceur (binaire compilé de nuanceur) que vous avez précédemment incorporé avec l' `/setprivate <file>` option.</span><span class="sxs-lookup"><span data-stu-id="427c1-234">Removes private data (arbitrary sequence of bytes) from the shader blob (compiled shader binary) that you previously embedded with the `/setprivate <file>` option.</span></span>

<span data-ttu-id="427c1-235">Vous devez spécifier l’option/DUMPBIN avec/Qstrip_priv.</span><span class="sxs-lookup"><span data-stu-id="427c1-235">You must specify the /dumpbin option with /Qstrip_priv.</span></span> <span data-ttu-id="427c1-236">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="427c1-236">For example:</span></span>

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a><span data-ttu-id="427c1-237">/Qstrip_reflect</span><span class="sxs-lookup"><span data-stu-id="427c1-237">/Qstrip_reflect</span></span>
<span data-ttu-id="427c1-238">Supprimez les données de réflexion du bytecode de nuanceur pour les profils 4_0 +.</span><span class="sxs-lookup"><span data-stu-id="427c1-238">Strip reflection data from shader bytecode for 4_0+ profiles.</span></span>

##### <a name="qstrip_rootsignature"></a><span data-ttu-id="427c1-239">/Qstrip_rootsignature</span><span class="sxs-lookup"><span data-stu-id="427c1-239">/Qstrip_rootsignature</span></span>
<span data-ttu-id="427c1-240">Supprimer la signature racine du bytecode du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="427c1-240">Strip root signature from shader bytecode.</span></span> <span data-ttu-id="427c1-241">Nouveauté de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="427c1-241">New for Direct3D 12.</span></span>

##### <a name="res_may_alias"></a><span data-ttu-id="427c1-242">/res_may_alias</span><span class="sxs-lookup"><span data-stu-id="427c1-242">/res_may_alias</span></span>
<span data-ttu-id="427c1-243">Supposons que UAVs/SRVs peut être un alias pour cs_5_0 +.</span><span class="sxs-lookup"><span data-stu-id="427c1-243">Assume that UAVs/SRVs may alias for cs_5_0+.</span></span> <span data-ttu-id="427c1-244">Requiert le \_47.dll D3dcompiler ou une version ultérieure de la dll.</span><span class="sxs-lookup"><span data-stu-id="427c1-244">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="setprivate-file"></a><span data-ttu-id="427c1-245">*fichier* de </SetPrivate></span><span class="sxs-lookup"><span data-stu-id="427c1-245">/setprivate <*file*></span></span>
<span data-ttu-id="427c1-246">Ajoutez des données privées dans le fichier donné à l’objet BLOB compilé de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="427c1-246">Add private data in the given file to the compiled shader blob.</span></span> <span data-ttu-id="427c1-247">Incorpore le fichier donné, qui est traité comme une mémoire tampon brute, à l’objet blob de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="427c1-247">Embeds the given file, which is treated as a raw buffer, to the shader blob.</span></span> <span data-ttu-id="427c1-248">Utilisez/SetPrivate pour ajouter des données privées quand vous compilez un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="427c1-248">Use /setprivate to add private data when you compile a shader.</span></span> <span data-ttu-id="427c1-249">Vous pouvez également utiliser l’option/DUMPBIN avec/SetPrivate pour charger un objet Shader existant, puis, une fois l’objet en mémoire, ajouter l’objet blob de données privé.</span><span class="sxs-lookup"><span data-stu-id="427c1-249">Or, use the /dumpbin option with /setprivate to load an existing shader object, and then after the object is in memory, to add the private data blob.</span></span> <span data-ttu-id="427c1-250">Par exemple, utilisez une seule commande avec/SetPrivate pour ajouter des données privées à un objet blob de nuanceur compilé :</span><span class="sxs-lookup"><span data-stu-id="427c1-250">For example, use either a single command with /setprivate to add private data to a compiled shader blob:</span></span>

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
<span data-ttu-id="427c1-251">Ou utilisez deux commandes où la deuxième commande charge un objet Shader, puis ajoute des données privées :</span><span class="sxs-lookup"><span data-stu-id="427c1-251">Or, use two commands where the second command loads a shader object and then adds private data:</span></span>

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a><span data-ttu-id="427c1-252">*fichier* de </setrootsignature></span><span class="sxs-lookup"><span data-stu-id="427c1-252">/setrootsignature <*file*></span></span>
<span data-ttu-id="427c1-253">Attachez la signature racine au bytecode du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="427c1-253">Attach root signature to shader bytecode.</span></span> <span data-ttu-id="427c1-254">Nouveauté de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="427c1-254">New for Direct3D 12.</span></span>

##### <a name="shtemplate-file"></a><span data-ttu-id="427c1-255">*fichier* de </shtemplate></span><span class="sxs-lookup"><span data-stu-id="427c1-255">/shtemplate <*file*></span></span>
<span data-ttu-id="427c1-256">Utilisez le fichier de nuanceur de modèle donné pour la fusion (/mergeUAVs) et les ressources (/matchUAVs) correspondantes.</span><span class="sxs-lookup"><span data-stu-id="427c1-256">Use given template shader file for merging (/mergeUAVs) and matching (/matchUAVs) resources.</span></span> <span data-ttu-id="427c1-257">Pour plus d’informations, consultez la <a href="#remarks">section Notes</a>.</span><span class="sxs-lookup"><span data-stu-id="427c1-257">For more info, see <a href="#remarks">Remarks</a>.</span></span>

##### <a name="vd"></a><span data-ttu-id="427c1-258">/VD</span><span class="sxs-lookup"><span data-stu-id="427c1-258">/Vd</span></span>
<span data-ttu-id="427c1-259">Désactivez la validation.</span><span class="sxs-lookup"><span data-stu-id="427c1-259">Disable validation.</span></span>

##### <a name="verifyrootsignature-file"></a><span data-ttu-id="427c1-260">*fichier* de </verifyrootsignature></span><span class="sxs-lookup"><span data-stu-id="427c1-260">/verifyrootsignature <*file*></span></span>
<span data-ttu-id="427c1-261">Vérifiez le bytecode du nuanceur par rapport à la signature racine.</span><span class="sxs-lookup"><span data-stu-id="427c1-261">Verify shader bytecode against root signature.</span></span> <span data-ttu-id="427c1-262">Nouveauté de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="427c1-262">New for Direct3D 12.</span></span>

##### <a name="vi"></a><span data-ttu-id="427c1-263">/Vi</span><span class="sxs-lookup"><span data-stu-id="427c1-263">/Vi</span></span>
<span data-ttu-id="427c1-264">Affichez des détails sur le processus d’inclusion.</span><span class="sxs-lookup"><span data-stu-id="427c1-264">Display details about the include process.</span></span>

##### <a name="vn-name"></a><span data-ttu-id="427c1-265">*Nom* de l' </VN></span><span class="sxs-lookup"><span data-stu-id="427c1-265">/Vn <*name*></span></span>
<span data-ttu-id="427c1-266">Utilisez nom comme nom de variable dans le fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="427c1-266">Use name as variable name in header file.</span></span>

##### <a name="wx"></a><span data-ttu-id="427c1-267">/WX</span><span class="sxs-lookup"><span data-stu-id="427c1-267">/WX</span></span>
<span data-ttu-id="427c1-268">Considérer les avertissements comme des erreurs.</span><span class="sxs-lookup"><span data-stu-id="427c1-268">Treat warnings as errors.</span></span>

##### <a name="zi"></a><span data-ttu-id="427c1-269">/Zi</span><span class="sxs-lookup"><span data-stu-id="427c1-269">/Zi</span></span>
<span data-ttu-id="427c1-270">Activez les informations de débogage.</span><span class="sxs-lookup"><span data-stu-id="427c1-270">Enable debugging information.</span></span>

##### <a name="zpc"></a><span data-ttu-id="427c1-271">/Zpc</span><span class="sxs-lookup"><span data-stu-id="427c1-271">/Zpc</span></span>
<span data-ttu-id="427c1-272">Compresser les matrices dans l’ordre des colonnes.</span><span class="sxs-lookup"><span data-stu-id="427c1-272">Pack matrices in column-major order.</span></span>

##### <a name="zpr"></a><span data-ttu-id="427c1-273">/Zpr</span><span class="sxs-lookup"><span data-stu-id="427c1-273">/Zpr</span></span>
<span data-ttu-id="427c1-274">Compresser les matrices dans l’ordre ligne-principal.</span><span class="sxs-lookup"><span data-stu-id="427c1-274">Pack matrices in row-major order.</span></span>

### <a name="filenames"></a><span data-ttu-id="427c1-275">*Noms de fichiers*</span><span class="sxs-lookup"><span data-stu-id="427c1-275">*Filenames*</span></span>

<span data-ttu-id="427c1-276">\[dans \] les fichiers qui contiennent le ou les nuanceurs et/ou les effets.</span><span class="sxs-lookup"><span data-stu-id="427c1-276">\[in\] The files that contains the shader(s) and/or the effect(s).</span></span>

## <a name="remarks"></a><span data-ttu-id="427c1-277">Notes</span><span class="sxs-lookup"><span data-stu-id="427c1-277">Remarks</span></span>

<span data-ttu-id="427c1-278">Utilisez les `/mergeUAVs` `/matchUAVs` options, et `/shtemplate` pour aligner les emplacements de liaison UAV pour une chaîne de nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="427c1-278">Use the `/mergeUAVs`, `/matchUAVs`, and `/shtemplate` options to align the UAV binding slots for a chain of shaders.</span></span>

<span data-ttu-id="427c1-279">Supposons que vous avez des nuanceurs A. FX, B. FX et C. fx.</span><span class="sxs-lookup"><span data-stu-id="427c1-279">Suppose you have shaders A.fx, B.fx, and C.fx.</span></span> <span data-ttu-id="427c1-280">Pour aligner les emplacements de liaison UAV pour cette chaîne de nuanceurs, vous avez besoin de deux passes de compilation :</span><span class="sxs-lookup"><span data-stu-id="427c1-280">To align the UAV binding slots for this chain of shaders, you need two passes of compilation:</span></span>

<span data-ttu-id="427c1-281">**Pour aligner les emplacements de liaison UAV pour une chaîne de nuanceurs**</span><span class="sxs-lookup"><span data-stu-id="427c1-281">**To align the UAV binding slots for a chain of shaders**</span></span>

1.  <span data-ttu-id="427c1-282">Utilisez/mergeUAVs pour compiler des nuanceurs et spécifiez un objet blob de nuanceur compilé précédemment avec/shtemplate.</span><span class="sxs-lookup"><span data-stu-id="427c1-282">Use /mergeUAVs to compile shaders, and specify a previously-compiled shader blob with /shtemplate.</span></span> <span data-ttu-id="427c1-283">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="427c1-283">For example:</span></span>
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  <span data-ttu-id="427c1-284">Utilisez/matchUAVs pour compiler des nuanceurs et spécifiez le dernier objet blob de nuanceur de la première passe avec/shtemplate.</span><span class="sxs-lookup"><span data-stu-id="427c1-284">Use /matchUAVs to compile shaders, and specify the last shader blob from the first pass with /shtemplate.</span></span> <span data-ttu-id="427c1-285">Vous pouvez compiler dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="427c1-285">You can compile in any order.</span></span> <span data-ttu-id="427c1-286">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="427c1-286">For example:</span></span>
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
<span data-ttu-id="427c1-287">Vous n’avez pas besoin de recompiler C. fx dans la deuxième passe.</span><span class="sxs-lookup"><span data-stu-id="427c1-287">You don't have to recompile C.fx in the second pass.</span></span>

<span data-ttu-id="427c1-288">Après avoir effectué les deux réussites de compilation précédentes, vous pouvez utiliser A. o, B. o et C. o comme objets BLOB de nuanceur finaux avec des emplacements UAV alignés.</span><span class="sxs-lookup"><span data-stu-id="427c1-288">After you perform the preceding two compilation passes, you can use A.o, B.o, and C.o as final shader blobs with aligned UAV slots.</span></span>

## <a name="profiles"></a><span data-ttu-id="427c1-289">Profils</span><span class="sxs-lookup"><span data-stu-id="427c1-289">Profiles</span></span>

<span data-ttu-id="427c1-290">Chaque modèle de nuanceur est étiqueté avec un profil HLSL.</span><span class="sxs-lookup"><span data-stu-id="427c1-290">Each shader model is labeled with an HLSL profile.</span></span> <span data-ttu-id="427c1-291">Pour compiler un nuanceur par rapport à un modèle de nuanceur particulier, choisissez le profil de nuanceur approprié dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="427c1-291">To compile a shader against a particular shader model, choose the appropriate shader profile from the following table.</span></span>

<table><thead><tr class="header"><th><span data-ttu-id="427c1-292">Type de nuanceur</span><span class="sxs-lookup"><span data-stu-id="427c1-292">Shader Type</span></span></th><th><span data-ttu-id="427c1-293">Profils</span><span class="sxs-lookup"><span data-stu-id="427c1-293">Profiles</span></span></th></tr></thead><tbody><tr class="odd"><td><span data-ttu-id="427c1-294">Nuanceur de calcul</span><span class="sxs-lookup"><span data-stu-id="427c1-294">Compute Shader</span></span></td><td><dl> <span data-ttu-id="427c1-295">cs_4_0</span><span class="sxs-lookup"><span data-stu-id="427c1-295">cs_4_0</span></span><br />
<span data-ttu-id="427c1-296">cs_4_1</span><span class="sxs-lookup"><span data-stu-id="427c1-296">cs_4_1</span></span><br />
<span data-ttu-id="427c1-297">cs_5_0</span><span class="sxs-lookup"><span data-stu-id="427c1-297">cs_5_0</span></span><br />
<span data-ttu-id="427c1-298">cs_5_1</span><span class="sxs-lookup"><span data-stu-id="427c1-298">cs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="427c1-299">Nuanceur de domaine</span><span class="sxs-lookup"><span data-stu-id="427c1-299">Domain Shader</span></span></td><td><dl> <span data-ttu-id="427c1-300">ds_5_0</span><span class="sxs-lookup"><span data-stu-id="427c1-300">ds_5_0</span></span><br />
<span data-ttu-id="427c1-301">ds_5_1</span><span class="sxs-lookup"><span data-stu-id="427c1-301">ds_5_1</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="427c1-302">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="427c1-302">Geometry Shader</span></span></td><td><dl> <span data-ttu-id="427c1-303">gs_4_0</span><span class="sxs-lookup"><span data-stu-id="427c1-303">gs_4_0</span></span><br />
<span data-ttu-id="427c1-304">gs_4_1</span><span class="sxs-lookup"><span data-stu-id="427c1-304">gs_4_1</span></span><br />
<span data-ttu-id="427c1-305">gs_5_0</span><span class="sxs-lookup"><span data-stu-id="427c1-305">gs_5_0</span></span><br />
<span data-ttu-id="427c1-306">gs_5_1</span><span class="sxs-lookup"><span data-stu-id="427c1-306">gs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="427c1-307">Liaison de nuanceur HLSL</span><span class="sxs-lookup"><span data-stu-id="427c1-307">HLSL shader linking</span></span> </td><td><dl> <span data-ttu-id="427c1-308">lib_4_0</span><span class="sxs-lookup"><span data-stu-id="427c1-308">lib_4_0</span></span><br />
<span data-ttu-id="427c1-309">lib_4_1</span><span class="sxs-lookup"><span data-stu-id="427c1-309">lib_4_1</span></span><br />
<span data-ttu-id="427c1-310">lib_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="427c1-310">lib_4_0_level_9_1</span></span><br />
<span data-ttu-id="427c1-311">lib_4_0_level_9_1_vs_only</span><span class="sxs-lookup"><span data-stu-id="427c1-311">lib_4_0_level_9_1_vs_only</span></span><br />
<span data-ttu-id="427c1-312">lib_4_0_level_9_1_ps_only</span><span class="sxs-lookup"><span data-stu-id="427c1-312">lib_4_0_level_9_1_ps_only</span></span><br />
<span data-ttu-id="427c1-313">lib_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="427c1-313">lib_4_0_level_9_3</span></span><br />
<span data-ttu-id="427c1-314">lib_4_0_level_9_3_vs_only</span><span class="sxs-lookup"><span data-stu-id="427c1-314">lib_4_0_level_9_3_vs_only</span></span><br />
<span data-ttu-id="427c1-315">lib_4_0_level_9_3_ps_only</span><span class="sxs-lookup"><span data-stu-id="427c1-315">lib_4_0_level_9_3_ps_only</span></span><br />
<span data-ttu-id="427c1-316">lib_5_0</span><span class="sxs-lookup"><span data-stu-id="427c1-316">lib_5_0</span></span><br />
</dl> <span data-ttu-id="427c1-317">Pour plus d’informations sur la liaison de nuanceur, consultez <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> et <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="427c1-317">For more info about shader linking, see <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> and <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>.</span></span> <br/></td></tr><tr class="odd"><td><span data-ttu-id="427c1-318">Nuanceur de coque</span><span class="sxs-lookup"><span data-stu-id="427c1-318">Hull Shader</span></span></td><td><dl> <span data-ttu-id="427c1-319">hs_5_0</span><span class="sxs-lookup"><span data-stu-id="427c1-319">hs_5_0</span></span><br />
<span data-ttu-id="427c1-320">hs_5_1</span><span class="sxs-lookup"><span data-stu-id="427c1-320">hs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="427c1-321">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="427c1-321">Pixel Shader</span></span></td><td><dl> <span data-ttu-id="427c1-322">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="427c1-322">ps_2_0</span></span><br />
<span data-ttu-id="427c1-323">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="427c1-323">ps_2_a</span></span><br />
<span data-ttu-id="427c1-324">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="427c1-324">ps_2_b</span></span><br />
<span data-ttu-id="427c1-325">ps_2_sw</span><span class="sxs-lookup"><span data-stu-id="427c1-325">ps_2_sw</span></span><br />
<span data-ttu-id="427c1-326">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="427c1-326">ps_3_0</span></span><br />
<span data-ttu-id="427c1-327">ps_3_sw</span><span class="sxs-lookup"><span data-stu-id="427c1-327">ps_3_sw</span></span><br />
<span data-ttu-id="427c1-328">ps_4_0</span><span class="sxs-lookup"><span data-stu-id="427c1-328">ps_4_0</span></span><br />
<span data-ttu-id="427c1-329">ps_4_0_level_9_0</span><span class="sxs-lookup"><span data-stu-id="427c1-329">ps_4_0_level_9_0</span></span><br />
<span data-ttu-id="427c1-330">ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="427c1-330">ps_4_0_level_9_1</span></span><br />
<span data-ttu-id="427c1-331">ps_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="427c1-331">ps_4_0_level_9_3</span></span><br />
<span data-ttu-id="427c1-332">ps_4_1</span><span class="sxs-lookup"><span data-stu-id="427c1-332">ps_4_1</span></span><br />
<span data-ttu-id="427c1-333">ps_5_0</span><span class="sxs-lookup"><span data-stu-id="427c1-333">ps_5_0</span></span><br />
<span data-ttu-id="427c1-334">ps_5_1</span><span class="sxs-lookup"><span data-stu-id="427c1-334">ps_5_1</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="427c1-335">Signature racine</span><span class="sxs-lookup"><span data-stu-id="427c1-335">Root Signature</span></span></td><td><dl> <span data-ttu-id="427c1-336">rootsig_1_0</span><span class="sxs-lookup"><span data-stu-id="427c1-336">rootsig_1_0</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="427c1-337">Nuanceur de texture</span><span class="sxs-lookup"><span data-stu-id="427c1-337">Texture Shader</span></span></td><td><dl> <span data-ttu-id="427c1-338">tx_1_0</span><span class="sxs-lookup"><span data-stu-id="427c1-338">tx_1_0</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="427c1-339">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="427c1-339">Vertex Shader</span></span></td><td><dl> <span data-ttu-id="427c1-340">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="427c1-340">vs_1_1</span></span><br />
<span data-ttu-id="427c1-341">vs_2_0</span><span class="sxs-lookup"><span data-stu-id="427c1-341">vs_2_0</span></span><br />
<span data-ttu-id="427c1-342">vs_2_a</span><span class="sxs-lookup"><span data-stu-id="427c1-342">vs_2_a</span></span><br />
<span data-ttu-id="427c1-343">vs_2_sw</span><span class="sxs-lookup"><span data-stu-id="427c1-343">vs_2_sw</span></span><br />
<span data-ttu-id="427c1-344">vs_3_0</span><span class="sxs-lookup"><span data-stu-id="427c1-344">vs_3_0</span></span><br />
<span data-ttu-id="427c1-345">vs_3_sw</span><span class="sxs-lookup"><span data-stu-id="427c1-345">vs_3_sw</span></span><br />
<span data-ttu-id="427c1-346">vs_4_0</span><span class="sxs-lookup"><span data-stu-id="427c1-346">vs_4_0</span></span><br />
<span data-ttu-id="427c1-347">vs_4_0_level_9_0</span><span class="sxs-lookup"><span data-stu-id="427c1-347">vs_4_0_level_9_0</span></span><br />
<span data-ttu-id="427c1-348">vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="427c1-348">vs_4_0_level_9_1</span></span><br />
<span data-ttu-id="427c1-349">vs_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="427c1-349">vs_4_0_level_9_3</span></span><br />
<span data-ttu-id="427c1-350">vs_4_1</span><span class="sxs-lookup"><span data-stu-id="427c1-350">vs_4_1</span></span><br />
<span data-ttu-id="427c1-351">vs_5_0</span><span class="sxs-lookup"><span data-stu-id="427c1-351">vs_5_0</span></span><br />
<span data-ttu-id="427c1-352">vs_5_1</span><span class="sxs-lookup"><span data-stu-id="427c1-352">vs_5_1</span></span><br />
</dl></td></tr></tbody></table>

## <a name="version-notes"></a><span data-ttu-id="427c1-353">Notes de version</span><span class="sxs-lookup"><span data-stu-id="427c1-353">Version notes</span></span>

<span data-ttu-id="427c1-354">Pour Direct3D 12, consultez [spécification de signatures racines en langage HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [liaison de ressources en HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) et [indexation dynamique à l’aide de HLSL 5,1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).</span><span class="sxs-lookup"><span data-stu-id="427c1-354">For Direct3D 12 refer to [Specifying Root Signatures in HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [Resource Binding in HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) and [Dynamic Indexing using HLSL 5.1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).</span></span>

<span data-ttu-id="427c1-355">Dans Direct3D 10, utilisez l’API pour obtenir le sommet, la géométrie et le profil de nuanceur de pixels qui conviennent le mieux à un appareil donné en appelant les fonctions suivantes : [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)et [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).</span><span class="sxs-lookup"><span data-stu-id="427c1-355">In Direct3D 10 use the API to get the vertex, geometry, and pixel-shader profile best suited to a given device by calling these functions: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile), and [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).</span></span>

<span data-ttu-id="427c1-356">Dans Direct3D 9, utilisez les méthodes [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) ou [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) pour récupérer les profils vertex et de nuanceur de pixels pris en charge par un appareil.</span><span class="sxs-lookup"><span data-stu-id="427c1-356">In Direct3D 9 use the [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) or [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) methods to retrieve the vertex and pixel-shader profiles supported by a device.</span></span> <span data-ttu-id="427c1-357">La structure [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) retournée par ces méthodes indique les profils vertex et de nuanceur de pixels pris en charge par un appareil dans ses membres **VertexShaderVersion** et **PixelShaderVersion** .</span><span class="sxs-lookup"><span data-stu-id="427c1-357">The [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure returned by those methods indicates the vertex and pixel-shader profiles supported by a device in its **VertexShaderVersion** and **PixelShaderVersion** members.</span></span>

<span data-ttu-id="427c1-358">Pour obtenir des exemples, consultez [compilation avec le compilateur actuel](dx-graphics-tools-fxc-using.md).</span><span class="sxs-lookup"><span data-stu-id="427c1-358">For examples, see [Compiling with the Current Compiler](dx-graphics-tools-fxc-using.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="427c1-359">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="427c1-359">Related topics</span></span>

* [<span data-ttu-id="427c1-360">Effect-Tool du compilateur</span><span class="sxs-lookup"><span data-stu-id="427c1-360">Effect-Compiler Tool</span></span>](fxc.md)