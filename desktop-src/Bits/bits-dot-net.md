---
title: Utilisation de BITS à partir de .NET à l’aide de dll de référence
description: Les exemples suivants montrent comment appeler l’interface COM BITS à partir d’un programme .NET
ms.assetid: 1058970C-CE81-47D6-950E-3B6289E956B6
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: c359bafe4f1937d49a6ec21896af32606a2ae894
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103679254"
---
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a><span data-ttu-id="4355b-103">Appel de BITS à partir de .NET et C# à l’aide de dll de référence</span><span class="sxs-lookup"><span data-stu-id="4355b-103">Calling into BITS from .NET and C# using Reference DLLs</span></span>

<span data-ttu-id="4355b-104">L’une des façons d’appeler les classes COM BITS à partir d’un programme .NET consiste à créer un fichier DLL de référence à partir des fichiers [IDL](/windows/desktop/Midl/midl-start-page) bits (Interface Definition Language) dans le SDK Windows, à l’aide des outils [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) et [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) .</span><span class="sxs-lookup"><span data-stu-id="4355b-104">One way to call into the BITS COM classes from a .NET program is to create a reference DLL file starting with the BITS [IDL](/windows/desktop/Midl/midl-start-page) (Interface Definition Language) files in the Windows SDK, using the [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) and [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) tools.</span></span> <span data-ttu-id="4355b-105">La DLL de référence est un ensemble de wrappers de classe pour les classes COM BITS ; vous pouvez ensuite utiliser les classes wrapper directement à partir de .NET.</span><span class="sxs-lookup"><span data-stu-id="4355b-105">The reference DLL is a set of class wrappers for the BITS COM classes; you can then use the wrapper classes directly from .NET.</span></span>

<span data-ttu-id="4355b-106">Une alternative à l’utilisation de dll de référence créées automatiquement consiste à utiliser un wrapper .NET BITS tiers à partir de [GitHub](https://github.com/) et [NuGet](https://www.nuget.org/).</span><span class="sxs-lookup"><span data-stu-id="4355b-106">An alternative to using automatically-created reference DLLs is to use a 3rd party .NET BITS wrapper from [GitHub](https://github.com/) and [NuGet](https://www.nuget.org/).</span></span> <span data-ttu-id="4355b-107">Ces wrappers ont souvent un style de programmation .NET plus naturel, mais ils peuvent dépasser les modifications et les mises à jour dans les interfaces BITS.</span><span class="sxs-lookup"><span data-stu-id="4355b-107">These wrappers often have a more natural .NET programming style but they might lag behind the changes and updates in the BITS interfaces.</span></span>

## <a name="creating-the-reference-dlls"></a><span data-ttu-id="4355b-108">Création des dll de référence</span><span class="sxs-lookup"><span data-stu-id="4355b-108">Creating the reference DLLs</span></span>
### <a name="bits-idl-files"></a><span data-ttu-id="4355b-109">Fichiers IDL BITS</span><span class="sxs-lookup"><span data-stu-id="4355b-109">BITS IDL files</span></span>

<span data-ttu-id="4355b-110">Vous allez commencer par le jeu de fichiers IDL BITS.</span><span class="sxs-lookup"><span data-stu-id="4355b-110">You will start with the set of BITS IDL files.</span></span> <span data-ttu-id="4355b-111">Il s’agit de fichiers qui définissent entièrement l’interface COM BITS.</span><span class="sxs-lookup"><span data-stu-id="4355b-111">These are files that fully define the BITS COM interface.</span></span> <span data-ttu-id="4355b-112">Les fichiers se trouvent dans le répertoire des **Kits Windows** et sont nommés bits *version*. idl (par exemple, bits10_2. idl), à l’exception du fichier version 1,0 qui est simplement bits. idl.</span><span class="sxs-lookup"><span data-stu-id="4355b-112">The files are located in the **Windows Kits** directory and are named bits *version*.idl (for example, bits10_2.idl) except for the version 1.0 file which is just Bits.idl.</span></span> <span data-ttu-id="4355b-113">À mesure que de nouvelles versions de BITS sont créées, de nouveaux fichiers IDL BITS sont également créés.</span><span class="sxs-lookup"><span data-stu-id="4355b-113">As new versions of BITS are created, new BITS IDL files are also created.</span></span>

<span data-ttu-id="4355b-114">Vous pouvez également modifier une copie des fichiers IDL du kit de développement logiciel (SDK) BITS pour utiliser les fonctionnalités BITS qui ne sont pas automatiquement converties en équivalents .NET.</span><span class="sxs-lookup"><span data-stu-id="4355b-114">You may also want to modify a copy of the SDK BITS IDL files to use BITS features that aren't automatically converted into .NET equivalents.</span></span> <span data-ttu-id="4355b-115">Les modifications possibles des fichiers IDL sont décrites plus loin sur.</span><span class="sxs-lookup"><span data-stu-id="4355b-115">Possible IDL file changes are discussed later on.</span></span>

<span data-ttu-id="4355b-116">Les fichiers IDL BITS incluent plusieurs autres fichiers IDL par référence.</span><span class="sxs-lookup"><span data-stu-id="4355b-116">The BITS IDL files include several other IDL files by reference.</span></span> <span data-ttu-id="4355b-117">Elles s’imbriquent également, de sorte que si vous utilisez une version, elle comprend toutes les versions inférieures.</span><span class="sxs-lookup"><span data-stu-id="4355b-117">They also nest, so that if you use one version, it includes all the lower versions.</span></span>

<span data-ttu-id="4355b-118">Pour chaque version de BITS que vous souhaitez cibler dans votre programme, vous avez besoin d’une DLL de référence pour cette version.</span><span class="sxs-lookup"><span data-stu-id="4355b-118">For each version of BITS that you want to target in your program you will need one reference DLL for that version.</span></span> <span data-ttu-id="4355b-119">Par exemple, si vous souhaitez écrire un programme qui fonctionne sur BITS 1,5 et versions, mais qui a des fonctionnalités supplémentaires lorsque BITS 10,2 est présent, vous devez convertir les fichiers bits1_5. idl et bits10_2. idl.</span><span class="sxs-lookup"><span data-stu-id="4355b-119">For example, if you want to write a program that works on BITS 1.5 and up but has additional features when BITS 10.2 is present, you need to convert both the bits1_5.idl and bits10_2.idl files.</span></span>


### <a name="midl-and-tlbimp-utilities"></a><span data-ttu-id="4355b-120">Utilitaires MIDL et TLBIMP</span><span class="sxs-lookup"><span data-stu-id="4355b-120">MIDL and TLBIMP utilities</span></span>

<span data-ttu-id="4355b-121">L’utilitaire [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (Microsoft Interface Definition Language) convertit les fichiers IDL qui décrivent l’interface com bits en un fichier TLB (bibliothèque de types).</span><span class="sxs-lookup"><span data-stu-id="4355b-121">The [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (Microsoft Interface Definition Language) utility converts the IDL files that describe the BITS COM interface into a TLB (Type Library) file.</span></span> <span data-ttu-id="4355b-122">L’outil MIDL dépend de l’utilitaire CL (préprocesseur C) pour lire correctement le fichier de langage IDL.</span><span class="sxs-lookup"><span data-stu-id="4355b-122">The MIDL tool depends on the CL utility (C preprocessor) to correctly read the IDL language file.</span></span> <span data-ttu-id="4355b-123">L’utilitaire CL fait partie de Visual Studio et est installé lorsque vous incluez des fonctionnalités C/C++ dans l’installation de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4355b-123">The CL utility is part of Visual Studio and is installed when you include C/C++ features in the Visual Studio installation.</span></span>

<span data-ttu-id="4355b-124">L’utilitaire MIDL crée normalement un ensemble de fichiers C et H (code de langage C et en-tête de langage C).</span><span class="sxs-lookup"><span data-stu-id="4355b-124">The MIDL utility will normally create a set of C and H (C language code and C language header) files.</span></span> <span data-ttu-id="4355b-125">Vous pouvez supprimer ces fichiers supplémentaires en envoyant la sortie à l’appareil NUL :.</span><span class="sxs-lookup"><span data-stu-id="4355b-125">You can suppress these extra files by sending the output to the NUL: device.</span></span> <span data-ttu-id="4355b-126">Par exemple, si vous définissez le commutateur/dlldata NUL :, vous supprimez la création d’un fichier dlldata. c.</span><span class="sxs-lookup"><span data-stu-id="4355b-126">For example, setting the /dlldata NUL: switch will suppress creating a dlldata.c file.</span></span> <span data-ttu-id="4355b-127">Les exemples de commandes ci-dessous montrent les commutateurs qui doivent être définis sur NUL :.</span><span class="sxs-lookup"><span data-stu-id="4355b-127">The sample commands below shows which switches should be set to NUL:.</span></span>

<span data-ttu-id="4355b-128">L’utilitaire [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (importateur de bibliothèques de types) lit un fichier TLB et crée le fichier dll de référence correspondant.</span><span class="sxs-lookup"><span data-stu-id="4355b-128">The [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (Type Library Importer) utility reads in a TLB file and creates the corresponding reference DLL file.</span></span> 


### <a name="example-commands-for-midl-and-tlbimp"></a><span data-ttu-id="4355b-129">Exemples de commandes pour MIDL et TLBIMP</span><span class="sxs-lookup"><span data-stu-id="4355b-129">Example commands for MIDL and TLBIMP</span></span>

<span data-ttu-id="4355b-130">Voici un exemple de l’ensemble complet de commandes permettant de générer un ensemble de fichiers de référence.</span><span class="sxs-lookup"><span data-stu-id="4355b-130">This is an example of the complete set of commands to generate a set of reference files.</span></span> <span data-ttu-id="4355b-131">Vous devrez peut-être modifier les commandes en fonction de votre installation de Visual Studio et de SDK Windows et en fonction des fonctionnalités BITS et des versions de système d’exploitation que vous ciblez.</span><span class="sxs-lookup"><span data-stu-id="4355b-131">You may need to modify the commands based on your Visual Studio and Windows SDK installation and based on the BITS features and OS versions you are targeting.</span></span> 

<span data-ttu-id="4355b-132">L’exemple crée un répertoire pour placer les fichiers DLL de référence et crée une variable d’environnement BITSTEMP pour pointer vers ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="4355b-132">The example creates a directory to place the reference DLL files and creates an environment variable BITSTEMP to point to that directory.</span></span> 

<span data-ttu-id="4355b-133">Les exemples de commandes exécutent ensuite le fichier vsdevcmd.bat créé par le programme d’installation de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4355b-133">The example commands then run the vsdevcmd.bat file that's created by the Visual Studio installer.</span></span> <span data-ttu-id="4355b-134">Ce fichier BAT configure vos chemins d’accès et certaines variables d’environnement afin que les commandes MIDL et TLBIMP s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="4355b-134">This BAT file will set up your paths and some environment variables so that the MIDL and TLBIMP commands will run.</span></span> <span data-ttu-id="4355b-135">Il configure également les variables WindowsSdkDir et WindowsSDKLibVersion pour qu’elles pointent vers les répertoires SDK Windows les plus récents.</span><span class="sxs-lookup"><span data-stu-id="4355b-135">It also sets up the WindowsSdkDir and WindowsSDKLibVersion variables to point to the most recent Windows SDK directories.</span></span>

```console
REM Create a working directory
REM You can select a different directory based on your needs.
SET BITSTEMP=C:\BITSTEMPDIR
MKDIR "%BITSTEMP%"

REM Run the VsDevCmd.bat file to locate the Windows
REM SDK directory and the tools directories
REM This will be different for different versions of
REM Visual Studio

CALL "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\Tools\vsdevcmd.bat"

REM Run the MIDL command on the desired BITS IDL file
REM This will generate a TLB file for the TLBIMP command
REM The IDL file will be different depending on which
REM set of BITS interfaces you need to use.
REM Run the MIDL command once per reference file
REM that you will need to explicitly use.
PUSHD .
CD /D "%WindowsSdkDir%Include\%WindowsSDKLibVersion%um"

MIDL  /I ..\shared /out "%BITSTEMP%" bits1_5.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits4_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits5_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_1.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_2.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:

REM Run the TLBIMP command on the resulting TLB file(s)
REM Try to keep a parallel set of names.
TLBIMP "%BITSTEMP%"\bits1_5.tlb /out: "%BITSTEMP%"\BITSReference1_5.dll
TLBIMP "%BITSTEMP%"\bits4_0.tlb /out: "%BITSTEMP%"\BITSReference4_0.dll
TLBIMP "%BITSTEMP%"\bits5_0.tlb /out: "%BITSTEMP%"\BITSReference5_0.dll
TLBIMP "%BITSTEMP%"\bits10_1.tlb /out: "%BITSTEMP%"\BITSReference10_1.dll
TLBIMP "%BITSTEMP%"\bits10_2.tlb /out: "%BITSTEMP%"\BITSReference10_2.dll
DEL "%BITSTEMP%"\bits*.tlb
POPD

```
<span data-ttu-id="4355b-136">Une fois ces commandes exécutées, vous disposez d’un ensemble de dll de référence dans le répertoire BITSTEMP.</span><span class="sxs-lookup"><span data-stu-id="4355b-136">Once these commands are run you will have a set of reference DLLs in the BITSTEMP directory.</span></span>

### <a name="adding-the-reference-dlls-to-your-project"></a><span data-ttu-id="4355b-137">Ajout des dll de référence à votre projet</span><span class="sxs-lookup"><span data-stu-id="4355b-137">Adding the reference DLLs to your project</span></span>

<span data-ttu-id="4355b-138">Pour utiliser une DLL de référence dans un projet C#, ouvrez votre projet C# dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4355b-138">To use a reference DLL in a C# project, open your C# project in Visual Studio.</span></span> <span data-ttu-id="4355b-139">Dans le Explorateur de solutions, cliquez avec le bouton droit sur les références, puis cliquez sur Ajouter une référence.</span><span class="sxs-lookup"><span data-stu-id="4355b-139">In the Solution Explorer, right-click the References and click Add Reference.</span></span> <span data-ttu-id="4355b-140">Cliquez ensuite sur le bouton Parcourir, puis sur le bouton Ajouter.</span><span class="sxs-lookup"><span data-stu-id="4355b-140">Then click the Browse button and then the Add button.</span></span> <span data-ttu-id="4355b-141">Accédez au répertoire contenant les dll de référence, sélectionnez-les, puis cliquez sur Ajouter.</span><span class="sxs-lookup"><span data-stu-id="4355b-141">Navigate to the directory with the reference DLLs, select them, and click Add.</span></span> <span data-ttu-id="4355b-142">Dans la fenêtre Gestionnaire de références, les dll de référence sont vérifiées.</span><span class="sxs-lookup"><span data-stu-id="4355b-142">In the Reference Manager window the reference DLLs will be checked.</span></span> <span data-ttu-id="4355b-143">Puis cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="4355b-143">Then click OK.</span></span>

<span data-ttu-id="4355b-144">Les dll de référence BITS sont maintenant ajoutées à votre projet.</span><span class="sxs-lookup"><span data-stu-id="4355b-144">The BITS reference DLLs are now added to your project.</span></span>

<span data-ttu-id="4355b-145">Les informations contenues dans les fichiers DLL de référence sont incorporées dans votre programme final.</span><span class="sxs-lookup"><span data-stu-id="4355b-145">The information in the reference DLL files will be embedded into your final program.</span></span> <span data-ttu-id="4355b-146">Vous n’avez pas besoin d’expédier les fichiers DLL de référence avec votre programme ; vous devez simplement expédier le. Exécutable.</span><span class="sxs-lookup"><span data-stu-id="4355b-146">You do not have to ship the reference DLL files with your program; you just need to ship the .EXE.</span></span> 

<span data-ttu-id="4355b-147">Vous pouvez modifier si les dll de référence sont incorporées dans le fichier EXE final.</span><span class="sxs-lookup"><span data-stu-id="4355b-147">You can change whether the reference DLLs are embedded into the final EXE.</span></span> <span data-ttu-id="4355b-148">Utilisez la propriété [incorporer les types Interop](/dotnet/framework/interop/how-to-add-references-to-type-libraries) pour déterminer si les dll de référence seront incorporées.</span><span class="sxs-lookup"><span data-stu-id="4355b-148">Use the [Embed Interop Types](/dotnet/framework/interop/how-to-add-references-to-type-libraries) property to set whether or not the reference DLLs will be embedded.</span></span> <span data-ttu-id="4355b-149">Cette opération peut être effectuée en fonction de la référence.</span><span class="sxs-lookup"><span data-stu-id="4355b-149">This can be done on a per-reference basis.</span></span> <span data-ttu-id="4355b-150">La valeur par défaut est true pour incorporer les dll.</span><span class="sxs-lookup"><span data-stu-id="4355b-150">The default is True to embed the DLLs.</span></span>

## <a name="modifying-idl-files-for-more-complete-net-code"></a><span data-ttu-id="4355b-151">Modification des fichiers IDL pour obtenir du code .NET plus complet</span><span class="sxs-lookup"><span data-stu-id="4355b-151">Modifying IDL files for more complete .NET code</span></span>

<span data-ttu-id="4355b-152">Les fichiers IDL BITS (Microsoft Interface Definition Language) peuvent être utilisés sans modification pour créer le fichier DLL BackgroundCopyManager.</span><span class="sxs-lookup"><span data-stu-id="4355b-152">The BITS IDL (Microsoft Interface Definition Language) files can be used unchanged to make the BackgroundCopyManager DLL file.</span></span> <span data-ttu-id="4355b-153">Toutefois, il manque des unions non convertibles à la DLL de référence .NET obtenue et des noms difficiles à utiliser s’affichent pour certaines structures et certains enums.</span><span class="sxs-lookup"><span data-stu-id="4355b-153">However, the resulting .NET reference DLL will be missing some untranslatable unions and has hard-to-use names for some structures and enums.</span></span> <span data-ttu-id="4355b-154">Cette section décrit quelques-unes des modifications que vous pouvez apporter pour rendre la DLL .NET plus complète et plus facile à utiliser.</span><span class="sxs-lookup"><span data-stu-id="4355b-154">This section will describe some of the changes that you can make to make the .NET DLL more complete and easier to use.</span></span>

### <a name="simpler-enum-names"></a><span data-ttu-id="4355b-155">Noms d’ENUM plus simples</span><span class="sxs-lookup"><span data-stu-id="4355b-155">Simpler ENUM names</span></span>

<span data-ttu-id="4355b-156">Les fichiers IDL BITS définissent généralement des valeurs enum comme suit :</span><span class="sxs-lookup"><span data-stu-id="4355b-156">The BITS IDL files typically define enum values like this:</span></span>
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
<span data-ttu-id="4355b-157">Le BG_AUTH_TARGET est le nom du typedef ; l’enum réel n’est pas nommé.</span><span class="sxs-lookup"><span data-stu-id="4355b-157">The BG_AUTH_TARGET is the name of the typedef; the actual enum is not named.</span></span> <span data-ttu-id="4355b-158">Cela ne provoque généralement pas de problèmes avec le code C, mais ne se traduit pas correctement pour une utilisation avec un programme .NET.</span><span class="sxs-lookup"><span data-stu-id="4355b-158">This doesn’t typically cause problems with C code but doesn’t translate well for use with a .NET program.</span></span> <span data-ttu-id="4355b-159">Un nouveau nom est créé automatiquement, mais il peut ressembler à _MIDL___MIDL_itf_bits4_0_0005_0001_0001 au lieu d’une valeur explicite.</span><span class="sxs-lookup"><span data-stu-id="4355b-159">A new name will be automatically created, but it might look something like _MIDL___MIDL_itf_bits4_0_0005_0001_0001 instead of a human-readable value.</span></span> <span data-ttu-id="4355b-160">Vous pouvez résoudre ce problème en mettant à jour les fichiers MIDL pour inclure un nom d’enum.</span><span class="sxs-lookup"><span data-stu-id="4355b-160">You can fix this problem by updating the MIDL files to include an enum name.</span></span>

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

<span data-ttu-id="4355b-161">Le nom enum peut être le même que le nom typedef.</span><span class="sxs-lookup"><span data-stu-id="4355b-161">The enum name is allowed to be the same as the typedef name.</span></span> <span data-ttu-id="4355b-162">Certains programmeurs ont une convention d’affectation de noms dans laquelle ils sont conservés différents (par exemple, en plaçant un trait de soulignement avant le nom de l’enum), mais cela ne perturbe que les traductions .NET.</span><span class="sxs-lookup"><span data-stu-id="4355b-162">Some programmers have a naming convention where they are kept different (for example, by putting an underscore before the enum name), but this will only confuse the .NET translations.</span></span> 

### <a name="string-types-in-unions"></a><span data-ttu-id="4355b-163">Types chaîne dans les unions</span><span class="sxs-lookup"><span data-stu-id="4355b-163">String types in unions</span></span>

<span data-ttu-id="4355b-164">Les fichiers IDL BITS passent des chaînes à l’aide de la Convention LPWSTR (long pointer vers une chaîne de caractères larges).</span><span class="sxs-lookup"><span data-stu-id="4355b-164">The BITS IDL files pass strings using the LPWSTR (long pointer to wide-character string) convention.</span></span> <span data-ttu-id="4355b-165">Bien que cela fonctionne lors du passage de paramètres de fonction (tels que la méthode Job. GetDisplayName ([out] LPWSTR \* pVal)), cela ne fonctionne pas lorsque les chaînes font partie d’unions.</span><span class="sxs-lookup"><span data-stu-id="4355b-165">Although this works when passing function parameters (like the Job.GetDisplayName([out] LPWSTR \*pVal) method), it doesn’t work when the strings are part of unions.</span></span> <span data-ttu-id="4355b-166">Par exemple, le fichier bits5_0. idl comprend le BITS_FILE_PROPERTY_VALUE Union :</span><span class="sxs-lookup"><span data-stu-id="4355b-166">For example, the bits5_0.idl file includes the BITS_FILE_PROPERTY_VALUE union:</span></span>

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

<span data-ttu-id="4355b-167">Le champ LPWSTR n’est pas inclus dans la version .NET de l’Union.</span><span class="sxs-lookup"><span data-stu-id="4355b-167">The LPWSTR field won’t be included in the .NET version of the union.</span></span> <span data-ttu-id="4355b-168">Pour résoudre ce problème, remplacez le LPWSTR par un WCHAR \*.</span><span class="sxs-lookup"><span data-stu-id="4355b-168">To fix this, change the LPWSTR to a WCHAR\*.</span></span> <span data-ttu-id="4355b-169">Le champ résultant (appelé chaîne) est passé en tant que IntPtr.</span><span class="sxs-lookup"><span data-stu-id="4355b-169">The resulting field (called String) will be passed as a IntPtr.</span></span> <span data-ttu-id="4355b-170">Convertissez-le en une chaîne à l’aide de System. Runtime. InteropServices. Marshal. PtrToStringAuto (valeur. Chaîne); méthode.</span><span class="sxs-lookup"><span data-stu-id="4355b-170">Convert this into a string using the  System.Runtime.InteropServices.Marshal.PtrToStringAuto(value.String); method.</span></span>

### <a name="unions-in-structures"></a><span data-ttu-id="4355b-171">Unions dans les structures</span><span class="sxs-lookup"><span data-stu-id="4355b-171">Unions in structures</span></span>

<span data-ttu-id="4355b-172">Parfois, les unions incorporées dans des structures ne sont pas incluses dans la structure.</span><span class="sxs-lookup"><span data-stu-id="4355b-172">Sometimes unions that are embedded in structures won't be included in the structure at all.</span></span> <span data-ttu-id="4355b-173">Par exemple, dans le Bits1_5. idl, la BG_AUTH_CREDENTIALS est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="4355b-173">For example, in the Bits1_5.idl the BG_AUTH_CREDENTIALS is defined as follows:</span></span>
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

<span data-ttu-id="4355b-174">La BG_AUTH_CREDENTIALS_UNION est définie comme étant une Union comme suit :</span><span class="sxs-lookup"><span data-stu-id="4355b-174">The BG_AUTH_CREDENTIALS_UNION is defined to be a union as follows:</span></span>
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
<span data-ttu-id="4355b-175">Le champ des informations d’identification dans le BG_AUTH_CREDENTIALS ne sera pas inclus dans la définition de la classe .NET.</span><span class="sxs-lookup"><span data-stu-id="4355b-175">The Credentials field in the BG_AUTH_CREDENTIALS will not be included in the .NET class definition.</span></span>

<span data-ttu-id="4355b-176">Notez que l’Union est définie pour toujours être une BG_BASIC_CREDENTIALS indépendamment des BG_AUTH_SCHEME.</span><span class="sxs-lookup"><span data-stu-id="4355b-176">Note that the union is defined to always be a BG_BASIC_CREDENTIALS regardless of the BG_AUTH_SCHEME.</span></span> <span data-ttu-id="4355b-177">Étant donné que l’Union n’est pas utilisée en tant qu’Union, nous pouvons simplement transmettre un BG_BASIC_CREDENTIALS comme suit :</span><span class="sxs-lookup"><span data-stu-id="4355b-177">Because the union isn’t used as a union, we can just pass a BG_BASIC_CREDENTIALS like this:</span></span>
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a><span data-ttu-id="4355b-178">Utilisation de BITS à partir de C #</span><span class="sxs-lookup"><span data-stu-id="4355b-178">Using BITS from C#</span></span>

### <a name="recommended-using-statement"></a><span data-ttu-id="4355b-179">Instruction using recommandée</span><span class="sxs-lookup"><span data-stu-id="4355b-179">Recommended using statement</span></span>

<span data-ttu-id="4355b-180">La configuration d’instructions using en C# réduira le nombre de caractères que vous devez taper pour utiliser les différentes versions BITS.</span><span class="sxs-lookup"><span data-stu-id="4355b-180">Setting up some using statements in C# will reduce the number of characters you need to type to use the different BITS versions.</span></span> <span data-ttu-id="4355b-181">Le nom « BITSReference » provient du nom de la DLL de référence.</span><span class="sxs-lookup"><span data-stu-id="4355b-181">The name "BITSReference" comes from the name of the reference DLL.</span></span>

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a><span data-ttu-id="4355b-182">Exemple rapide : télécharger un fichier</span><span class="sxs-lookup"><span data-stu-id="4355b-182">Quick Sample: download a file</span></span>

<span data-ttu-id="4355b-183">Un extrait de code C# pour télécharger un fichier à partir d’une URL est fourni ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4355b-183">A short but complete snippet of C# code to download a file from a URL is given below.</span></span> 

```csharp
    var mgr = new BITS.BackgroundCopyManager1_5();
    BITS.GUID jobGuid;
    BITS.IBackgroundCopyJob job;
    mgr.CreateJob("Quick download", BITS.BG_JOB_TYPE.BG_JOB_TYPE_DOWNLOAD, out jobGuid, out job);
    job.AddFile("https://aka.ms/WinServ16/StndPDF", @"C:\Server2016.pdf");
    job.Resume();
    bool jobIsFinal = false;
    while (!jobIsFinal)
    {
        BITS.BG_JOB_STATE state;
        job.GetState(out state);
        switch (state)
        {
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ERROR:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_TRANSFERRED:
                job.Complete();
                break;

            case BITS.BG_JOB_STATE.BG_JOB_STATE_CANCELLED:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ACKNOWLEDGED:
                jobIsFinal = true;
                break;
            default:
                Task.Delay(500); // delay a little bit
                break;
        }
    }
    // Job is complete
```

<span data-ttu-id="4355b-184">Dans cet exemple de code, un gestionnaire de BITS nommé Mgr est créé.</span><span class="sxs-lookup"><span data-stu-id="4355b-184">In this sample code, a BITS manager named mgr is created.</span></span> <span data-ttu-id="4355b-185">Il correspond directement à l’interface [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) .</span><span class="sxs-lookup"><span data-stu-id="4355b-185">It directly corresponds to the [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) interface.</span></span> 

<span data-ttu-id="4355b-186">À partir du gestionnaire, un nouveau travail est créé.</span><span class="sxs-lookup"><span data-stu-id="4355b-186">From the manager a new job is created.</span></span> <span data-ttu-id="4355b-187">Le travail est un paramètre de sortie sur la méthode CreateJob.</span><span class="sxs-lookup"><span data-stu-id="4355b-187">The job is an out parameter on the CreateJob method.</span></span> <span data-ttu-id="4355b-188">Le nom du travail (qui n’a pas besoin d’être unique) et le type de téléchargement, qui est un travail de téléchargement, sont également transmis.</span><span class="sxs-lookup"><span data-stu-id="4355b-188">Also passed in is the job name (which doesn't have to be unique) and the download type, which is a download job.</span></span> <span data-ttu-id="4355b-189">Un GUID BITS pour l’identificateur de tâche est également renseigné.</span><span class="sxs-lookup"><span data-stu-id="4355b-189">A BITS GUID for the job identifier is also filled in.</span></span>

<span data-ttu-id="4355b-190">Une fois la tâche créée, vous ajoutez un nouveau fichier de téléchargement au travail avec la méthode AddFile.</span><span class="sxs-lookup"><span data-stu-id="4355b-190">Once the job is created you add a new download file to the job with the AddFile method.</span></span> <span data-ttu-id="4355b-191">Vous devez passer deux chaînes, une pour le fichier distant (l’URL ou le partage de fichiers) et l’autre pour le fichier local.</span><span class="sxs-lookup"><span data-stu-id="4355b-191">You need to pass in two strings, one for the remote file (the URL or file share) and one for the local file.</span></span> 

<span data-ttu-id="4355b-192">Après avoir ajouté le fichier, appelez Resume sur le travail pour le démarrer.</span><span class="sxs-lookup"><span data-stu-id="4355b-192">After adding the file, call Resume on the job to start it.</span></span> <span data-ttu-id="4355b-193">Ensuite, le code attend jusqu’à ce que le travail soit dans un état final (erreur ou transféré), puis soit terminé.</span><span class="sxs-lookup"><span data-stu-id="4355b-193">Then the code waits until the job is in a final state (ERROR or TRANSFERRED) and is then completed.</span></span>

### <a name="bits-versions-casting-and-queryinterface"></a><span data-ttu-id="4355b-194">Versions BITS, Cast et QueryInterface</span><span class="sxs-lookup"><span data-stu-id="4355b-194">BITS Versions, Casting and QueryInterface</span></span>

<span data-ttu-id="4355b-195">Vous constaterez que vous devez souvent utiliser une version antérieure d’un objet BITS et une version plus récente dans votre programme.</span><span class="sxs-lookup"><span data-stu-id="4355b-195">You'll find that you often have to use both an early version of a BITS object and a more recent version in your program.</span></span>  

<span data-ttu-id="4355b-196">Par exemple, lorsque vous créez un objet de traitement, vous obtiendrez un méthode ibackgroundcopyjob (partie de la version de BITS 1,0) même si vous le faites à l’aide d’un objet gestionnaire plus récent et qu’un objet méthode ibackgroundcopyjob plus récent est disponible.</span><span class="sxs-lookup"><span data-stu-id="4355b-196">For example, when you make a job object, you will get an IBackgroundCopyJob (part of BITS version 1.0) even when you're making it using a more recent manager object and a more recent IBackgroundCopyJob object is available.</span></span> <span data-ttu-id="4355b-197">Étant donné que la méthode CreateJob n’accepte pas d’interface pour la version la plus récente, vous ne pouvez pas créer directement la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="4355b-197">Because the CreateJob method doesn't accept an interface for the more recent version, you can't directly make the more recent version.</span></span>

<span data-ttu-id="4355b-198">Utilisez un cast .NET pour convertir un objet de type antérieur en un objet de type plus récent.</span><span class="sxs-lookup"><span data-stu-id="4355b-198">Use a .NET cast to convert from an older type object to a newer type object.</span></span> <span data-ttu-id="4355b-199">Le cast appellera automatiquement une QueryInterface COM si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4355b-199">The cast will automatically call a COM QueryInterface as appropriate.</span></span> 

<span data-ttu-id="4355b-200">Dans cet exemple, il existe un objet méthode ibackgroundcopyjob BITS nommé « job » et nous voulons le convertir en un objet IBackgroundCopyJob5 nommé « JOB5 » afin de pouvoir appeler la méthode BITS 5,0 GetProperty.</span><span class="sxs-lookup"><span data-stu-id="4355b-200">In this example, there's a BITS IBackgroundCopyJob object named "job", and we want to convert it to an IBackgroundCopyJob5 object named "job5" so that we can call the BITS 5.0 GetProperty method.</span></span> <span data-ttu-id="4355b-201">Nous venons d’effectuer un cast vers le type IBackgroundCopyJob5 comme suit :</span><span class="sxs-lookup"><span data-stu-id="4355b-201">We just cast to the IBackgroundCopyJob5 type like this:</span></span>

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

<span data-ttu-id="4355b-202">La variable JOB5 sera initialisée par .NET à l’aide de la fonction QueryInterface correcte.</span><span class="sxs-lookup"><span data-stu-id="4355b-202">The job5 variable will be initialized by .NET by using the correct QueryInterface.</span></span> 

<span data-ttu-id="4355b-203">Si votre code peut s’exécuter sur un système qui ne prend pas en charge une version particulière de BITS, vous pouvez essayer le cast et intercepter System. InvalidCastException.</span><span class="sxs-lookup"><span data-stu-id="4355b-203">If your code might run on a system that doesn't support a particular version of BITS, you can try the cast and catch the System.InvalidCastException.</span></span> 

```csharp
BITS5.IBackgroundCopyJob5 job5 = null;
try
{
    job5 = (BITS5.IBackgroundCopyJob5)Job;
}
catch (System.InvalidCastException)
{
    ; // Must be running an earlier version of BITS
}
```

<span data-ttu-id="4355b-204">Un problème courant se pose lorsque vous essayez d’effectuer un cast en un type d’objet incorrect.</span><span class="sxs-lookup"><span data-stu-id="4355b-204">A common problem is when you try to cast into the wrong kind of object.</span></span> <span data-ttu-id="4355b-205">Le système .NET ne connaît pas la relation réelle entre les interfaces BITS.</span><span class="sxs-lookup"><span data-stu-id="4355b-205">The .NET system doesn't know about the real relationship between the BITS interfaces.</span></span> <span data-ttu-id="4355b-206">Si vous demandez un genre d’interface incorrect, .NET tentera de le faire pour vous et échouera avec une exception InvalidCastException et HResult 0x80004002 (E_NOINTERFACE).</span><span class="sxs-lookup"><span data-stu-id="4355b-206">If you ask for the wrong kind of interface, .NET will try to make it for you and will fail with an InvalidCastException and HResult 0x80004002 (E_NOINTERFACE).</span></span>

### <a name="working-with-bits-versions-10_1-and-10_2"></a><span data-ttu-id="4355b-207">Utilisation des versions BITS 10_1 et 10_2</span><span class="sxs-lookup"><span data-stu-id="4355b-207">Working with BITS Versions 10_1 and 10_2</span></span>

<span data-ttu-id="4355b-208">Sur certaines versions de Windows 10, vous ne pouvez pas créer directement un objet IBackgroundCopyManager BITS à l’aide des interfaces 10,1 ou 10,2.</span><span class="sxs-lookup"><span data-stu-id="4355b-208">On some versions of Windows 10 you can't directly create a BITS IBackgroundCopyManager object using the 10.1 or 10.2 interfaces.</span></span> <span data-ttu-id="4355b-209">Au lieu de cela, vous devrez utiliser plusieurs versions des fichiers de référence de la DLL BackgroundCopyManager.</span><span class="sxs-lookup"><span data-stu-id="4355b-209">Instead, you'll have to use multiple versions of the BackgroundCopyManager DLL reference files.</span></span> <span data-ttu-id="4355b-210">Par exemple, vous pouvez utiliser la version 1,5 pour créer un objet IBackgroundCopyManager, puis effectuer un cast des objets de tâche ou de fichier résultants à l’aide des versions 10,1 ou 10,2.</span><span class="sxs-lookup"><span data-stu-id="4355b-210">For example, you can use the 1.5 version to make an IBackgroundCopyManager object, and then cast the resulting job or file objects using the 10.1 or 10.2 versions.</span></span>

