---
title: Commutateur/i
description: Le commutateur/I spécifie les répertoires dans lesquels rechercher les fichiers IDL importés, les fichiers d’en-tête inclus et les fichiers ACF.
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- MIDL du commutateur/i
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ee48ad1e66caf5ed8facbf09ebf2c517c8c895
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030332"
---
# <a name="i-switch"></a><span data-ttu-id="db69f-104">Commutateur/i</span><span class="sxs-lookup"><span data-stu-id="db69f-104">/I switch</span></span>

<span data-ttu-id="db69f-105">Le commutateur **/i** spécifie les répertoires dans lesquels rechercher les fichiers IDL importés, les fichiers d’en-tête inclus et les fichiers ACF.</span><span class="sxs-lookup"><span data-stu-id="db69f-105">The **/I** switch specifies directories to be searched for imported IDL files, included header files, and ACF files.</span></span>

``` syntax
midl /I include_path
```

## <a name="switch-options"></a><span data-ttu-id="db69f-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="db69f-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="db69f-107">*inclure le \_ chemin*</span><span class="sxs-lookup"><span data-stu-id="db69f-107">*include\_path*</span></span> 
</dt> <dd>

<span data-ttu-id="db69f-108">Spécifie un ou plusieurs répertoires qui contiennent des fichiers d’importation, d’inclusion et de CCP.</span><span class="sxs-lookup"><span data-stu-id="db69f-108">Specifies one or more directories that contain import, include, and ACF files.</span></span> <span data-ttu-id="db69f-109">L’espace blanc entre le commutateur **/i** et le *\_ chemin include* est facultatif.</span><span class="sxs-lookup"><span data-stu-id="db69f-109">White space between the **/I** switch and *include\_path* is optional.</span></span> <span data-ttu-id="db69f-110">Séparez plusieurs répertoires par un point-virgule (;).</span><span class="sxs-lookup"><span data-stu-id="db69f-110">Separate multiple directories with a semicolon character (;).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db69f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="db69f-111">Remarks</span></span>

<span data-ttu-id="db69f-112">Plusieurs répertoires peuvent apparaître avec chaque commutateur **/i** , et plusieurs commutateurs **/i** peuvent apparaître avec chaque appel du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="db69f-112">More than one directory can appear with each **/I** switch, and more than one **/I** switch can appear with each MIDL compiler invocation.</span></span> <span data-ttu-id="db69f-113">Les répertoires sont recherchés dans l’ordre dans lequel ils sont spécifiés.</span><span class="sxs-lookup"><span data-stu-id="db69f-113">Directories are searched in the order they are specified.</span></span>

<span data-ttu-id="db69f-114">Le paramètre de commutateur **/i** est également passé par le compilateur MIDL au préprocesseur c du compilateur c.</span><span class="sxs-lookup"><span data-stu-id="db69f-114">The **/I** switch setting is also passed by the MIDL compiler to the C compiler's C preprocessor.</span></span> <span data-ttu-id="db69f-115">Lorsque le [**commutateur \_ /CPP cmd**](-cpp-cmd.md) est présent et que le commutateur [**/CPP \_ OPT**](-cpp-opt.md) n’est pas, le compilateur MIDL concatène la chaîne spécifiée par le commutateur **/CPP \_ cmd** avec les options **/i**, [**/d**](-d.md)et [**/u**](-u.md) et utilise cette chaîne concaténée pour appeler le préprocesseur C pour chaque fichier source IDL et ACF.</span><span class="sxs-lookup"><span data-stu-id="db69f-115">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the **/I**, [**/D**](-d.md), and [**/U**](-u.md) options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span> <span data-ttu-id="db69f-116">Le commutateur du compilateur MIDL **/i** n’est pas passé au préprocesseur lorsque le commutateur du compilateur MIDL **/non \_ CPP** ou **/CPP \_ OPT** est spécifié.</span><span class="sxs-lookup"><span data-stu-id="db69f-116">The MIDL compiler switch **/I** is not passed to the preprocessor when the MIDL compiler switch **/no\_cpp** or **/cpp\_opt** is specified.</span></span>

<span data-ttu-id="db69f-117">Dans les environnements de système d’exploitation Microsoft (Windows 64 bits, Windows 32 bits, Windows 16 bits et MS-DOS), les répertoires sont recherchés dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="db69f-117">In Microsoft operating-system environments (64-bit Windows, 32-bit Windows, 16-bit Windows, and MS-DOS), directories are searched in the following sequence:</span></span>

1.  <span data-ttu-id="db69f-118">Répertoire actif</span><span class="sxs-lookup"><span data-stu-id="db69f-118">Current directory</span></span>
2.  <span data-ttu-id="db69f-119">Répertoires spécifiés par le commutateur **/i** (dans l’ordre suivant le commutateur)</span><span class="sxs-lookup"><span data-stu-id="db69f-119">Directories specified by the **/I** switch (in the order they follow the switch)</span></span>
3.  <span data-ttu-id="db69f-120">Répertoires spécifiés par la variable d’environnement INCLUDe</span><span class="sxs-lookup"><span data-stu-id="db69f-120">Directories specified by the INCLUDE environment variable</span></span>

<span data-ttu-id="db69f-121">Lorsque les répertoires sont spécifiés avec le commutateur **/i** , le commutateur [**/non \_ Def \_ idir**](-no-def-idir.md) demande au compilateur MIDL d’ignorer le répertoire actif, d’ignorer les répertoires spécifiés par la variable d’environnement include et de rechercher uniquement les répertoires spécifiés.</span><span class="sxs-lookup"><span data-stu-id="db69f-121">When directories are specified with the **/I** switch, the [**/no\_def\_idir**](-no-def-idir.md) switch instructs the MIDL compiler to ignore the current directory, ignore the directories specified by the INCLUDE environment variable, and search only the specified directories.</span></span>

<span data-ttu-id="db69f-122">Quand aucun répertoire n’est spécifié avec le commutateur **/i** , le commutateur [**/non \_ Def \_ idir**](-no-def-idir.md) demande au compilateur MIDL de rechercher uniquement le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="db69f-122">When no directories are specified with the **/I** switch, the [**/no\_def\_idir**](-no-def-idir.md) switch instructs the MIDL compiler to search only the current directory.</span></span>

## <a name="examples"></a><span data-ttu-id="db69f-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="db69f-123">Examples</span></span>

<span data-ttu-id="db69f-124">**MIDL/I c : \\ include ; c : \\ include \\ h/i \\ include2 nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="db69f-124">**midl /I c:\\include;c:\\include\\h /I\\include2 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="db69f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db69f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db69f-126">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="db69f-126">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="db69f-127">**/acf**</span><span class="sxs-lookup"><span data-stu-id="db69f-127">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="db69f-128">**/CPP \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="db69f-128">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="db69f-129">**/CPP \_ opt**</span><span class="sxs-lookup"><span data-stu-id="db69f-129">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="db69f-130">**/non \_ Def \_ idir**</span><span class="sxs-lookup"><span data-stu-id="db69f-130">**/no\_def\_idir**</span></span>](-no-def-idir.md)
</dt> </dl>

 

 




