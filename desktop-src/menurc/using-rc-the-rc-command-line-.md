---
title: Utilisation de RC (ligne de commande RC)
description: Pour démarrer RC, utilisez la commande suivante.
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34e24fdf7b9b648a9baf9c6db8981f05d5434ef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940918"
---
# <a name="using-rc-the-rc-command-line"></a><span data-ttu-id="e4917-103">Utilisation de RC (ligne de commande RC)</span><span class="sxs-lookup"><span data-stu-id="e4917-103">Using RC (The RC Command Line)</span></span>

<span data-ttu-id="e4917-104">Pour démarrer RC, utilisez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="e4917-104">To start RC, use the following command.</span></span>

<span data-ttu-id="e4917-105">Version **RC** \[ *options* \] *fichier de script*</span><span class="sxs-lookup"><span data-stu-id="e4917-105">**RC** \[*options*\] *script-file*</span></span>

<span data-ttu-id="e4917-106">Le paramètre de *fichier de script* spécifie le nom du fichier de définition de ressource qui contient les noms, types, noms de fichiers et descriptions des ressources à compiler.</span><span class="sxs-lookup"><span data-stu-id="e4917-106">The *script-file* parameter specifies the name of the resource-definition file that contains the names, types, filenames, and descriptions of the resources to be compiled.</span></span>

<span data-ttu-id="e4917-107">RC peut générer des fichiers de ressources distincts pour les applications qui ont à la fois des ressources indépendantes du langage et des ressources spécifiques à une langue.</span><span class="sxs-lookup"><span data-stu-id="e4917-107">RC can generate separate resource files for applications that have both language-neutral and language-specific resources.</span></span> <span data-ttu-id="e4917-108">Les développeurs peuvent utiliser un [fichier de configuration de ressource](/windows/desktop/Intl/preparing-resources) ou définir des options de ligne de commande pour sélectionner les types de ressources et les éléments qui ne sont pas des ressources localisables du fichier indépendant de la [langue (LN)](/windows/desktop/Intl/mui-resource-management) et qui sont des ressources localisables de fichiers MUI spécifiques à une langue.</span><span class="sxs-lookup"><span data-stu-id="e4917-108">Developers can use a [resource configuration file](/windows/desktop/Intl/preparing-resources) or set command-line options to select which resource types and items are non-localizable resources of the [language-neutral (LN) file](/windows/desktop/Intl/mui-resource-management) and which are localizable resources of language-specific MUI files.</span></span> <span data-ttu-id="e4917-109">Pour plus d’informations, consultez l' [interface utilisateur multilingue](/windows/desktop/Intl/multilingual-user-interface).</span><span class="sxs-lookup"><span data-stu-id="e4917-109">For more information, see the [Multilingual User Interface](/windows/desktop/Intl/multilingual-user-interface).</span></span>

<span data-ttu-id="e4917-110">Le paramètre *options* peut être une ou plusieurs des options de ligne de commande suivantes.</span><span class="sxs-lookup"><span data-stu-id="e4917-110">The *options* parameter can be one or more of the following command-line options.</span></span>

## <a name="options"></a><span data-ttu-id="e4917-111">Options</span><span class="sxs-lookup"><span data-stu-id="e4917-111">Options</span></span>

<dl> <dt>

<span data-ttu-id="e4917-112"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="e4917-112"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="e4917-113">Affiche la liste des options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e4917-113">Displays a list of command-line options.</span></span>

</dd> <dt>

<span data-ttu-id="e4917-114"><span id="_c"></span><span id="_C"></span>**commutateur**</span><span class="sxs-lookup"><span data-stu-id="e4917-114"><span id="_c"></span><span id="_C"></span>**/c**</span></span>
</dt> <dd>

<span data-ttu-id="e4917-115">Définit une page de codes utilisée par la conversion NLS.</span><span class="sxs-lookup"><span data-stu-id="e4917-115">Defines a code page used by NLS conversion.</span></span>

</dd> <dt>

<span data-ttu-id="e4917-116"><span id="_d"></span><span id="_D"></span>**/d**</span><span class="sxs-lookup"><span data-stu-id="e4917-116"><span id="_d"></span><span id="_D"></span>**/d**</span></span>
</dt> <dd>

<span data-ttu-id="e4917-117">Définit un symbole pour le préprocesseur que vous pouvez tester avec la directive [**\# ifdef**](-ifdef.md) .</span><span class="sxs-lookup"><span data-stu-id="e4917-117">Defines a symbol for the preprocessor that you can test with the [**\#ifdef**](-ifdef.md) directive.</span></span>

</dd> <dt>

<span data-ttu-id="e4917-118"><span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/FM** *mresname*</span><span class="sxs-lookup"><span data-stu-id="e4917-118"><span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/fm** *mresname*</span></span>
</dt> <dd>

<span data-ttu-id="e4917-119">RC crée un indépendant de la langue. Fichier RES et un fichier dépendant de la langue (MUI). Fichier RES à l’aide du *fichier de script*.</span><span class="sxs-lookup"><span data-stu-id="e4917-119">RC creates one language-neutral .RES file and one language-dependent (MUI) .RES file using *script-file*.</span></span> <span data-ttu-id="e4917-120">Cette option doit être utilisée avec l’option **/FO** *resName* .</span><span class="sxs-lookup"><span data-stu-id="e4917-120">This option must be used together with the **/fo** *resname* option.</span></span> <span data-ttu-id="e4917-121">RC nomme le indépendant de la langue. RES file *resName. res* et nomme la langue dépendante (MUI). Fichier RES *mresname. res*.</span><span class="sxs-lookup"><span data-stu-id="e4917-121">RC names the language-neutral .RES file *resname.res* and names the language-dependent (MUI) .RES file *mresname.res*.</span></span>

<span data-ttu-id="e4917-122">**Windows Server 2003 et Windows XP/2000 :** Cette option n’est pas disponible sans utiliser également les fonctions [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) et [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) sur un système mis à jour.</span><span class="sxs-lookup"><span data-stu-id="e4917-122">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="e4917-123"><span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/FO** *resName*</span><span class="sxs-lookup"><span data-stu-id="e4917-123"><span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/fo** *resname*</span></span>
</dt> <dd>

<span data-ttu-id="e4917-124">RC crée un. Fichier RES nommé *resName* à l’aide du *fichier de script*.</span><span class="sxs-lookup"><span data-stu-id="e4917-124">RC creates a .RES file named *resname* using *script-file*.</span></span>

<span data-ttu-id="e4917-125">Si l’option **/FM** *mresname* est également définie, RC crée un indépendant de la langue. Fichier RES et un fichier dépendant de la langue (MUI). Fichier RES.</span><span class="sxs-lookup"><span data-stu-id="e4917-125">If the **/fm** *mresname* option is also set, RC creates one language-neutral .RES file and one language-dependent (MUI) .RES file.</span></span>

<span data-ttu-id="e4917-126">**Windows Server 2003 et Windows XP/2000 :** Cette option n’est pas disponible sans utiliser également les fonctions [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) et [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) sur un système mis à jour.</span><span class="sxs-lookup"><span data-stu-id="e4917-126">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="e4917-127"><span id="_g1"></span><span id="_G1"></span>**/G1**</span><span class="sxs-lookup"><span data-stu-id="e4917-127"><span id="_g1"></span><span id="_G1"></span>**/g1**</span></span>
</dt> <dd>

<span data-ttu-id="e4917-128">Si/G1 est défini, RC génère un fichier MUI si la seule ressource localisable incluse dans le fichier MUI est une ressource de version.</span><span class="sxs-lookup"><span data-stu-id="e4917-128">If /g1, is set, RC generates a MUI file if the only localizable resource being included in the MUI file is a version resource.</span></span> <span data-ttu-id="e4917-129">Si/G1 n’est pas défini, RC ne génère pas de fichier MUI si la seule ressource localisable incluse dans le fichier MUI est une ressource de version.</span><span class="sxs-lookup"><span data-stu-id="e4917-129">If /g1 is not set, RC will not generate a MUI file if the only localizable resource being included in the MUI file is a version resource.</span></span>

</dd> <dt>

<span data-ttu-id="e4917-130"><span id="_h"></span><span id="_H"></span>**/h**</span><span class="sxs-lookup"><span data-stu-id="e4917-130"><span id="_h"></span><span id="_H"></span>**/h**</span></span>
</dt> <dd>

<span data-ttu-id="e4917-131">Affiche la liste des options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e4917-131">Displays the list of command-line options.</span></span>

</dd> <dt>

<span data-ttu-id="e4917-132"><span id="_I"></span><span id="_i"></span>**/I**</span><span class="sxs-lookup"><span data-stu-id="e4917-132"><span id="_I"></span><span id="_i"></span>**/I**</span></span>
</dt> <dd>

<span data-ttu-id="e4917-133">Recherche le répertoire spécifié avant de rechercher dans les répertoires spécifiés par la variable d’environnement INCLUDe.</span><span class="sxs-lookup"><span data-stu-id="e4917-133">Searches the specified directory before searching the directories specified by the INCLUDE environment variable.</span></span>

</dd> <dt>

<span data-ttu-id="e4917-134"><span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*</span><span class="sxs-lookup"><span data-stu-id="e4917-134"><span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*</span></span>
</dt> <dd>

<span data-ttu-id="e4917-135">Les types de ressources localisables sont des emplacements dans le pack d’interface utilisateur dépendant du langage. Fichier RES.</span><span class="sxs-lookup"><span data-stu-id="e4917-135">Localizable resource types RC places into the language-dependent (MUI) .RES file.</span></span> <span data-ttu-id="e4917-136">Si l’option **/q** est également définie, cette option est ignorée et les informations contenues dans le fichier de configuration RC sont prioritaires.</span><span class="sxs-lookup"><span data-stu-id="e4917-136">If the **/q** option is also set, this option is ignored, and the information in the RC Configuration file takes precedence.</span></span>

<span data-ttu-id="e4917-137">**Windows Server 2003 et Windows XP/2000 :** Cette option n’est pas disponible sans utiliser également les fonctions [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) et [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) sur un système mis à jour.</span><span class="sxs-lookup"><span data-stu-id="e4917-137">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="e4917-138"><span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** , *Refrappe*</span><span class="sxs-lookup"><span data-stu-id="e4917-138"><span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** *overtype*</span></span>
</dt> <dd>

<span data-ttu-id="e4917-139">Le chevauchement des types de ressources par RC place dans le indépendant du langage. RES et le langage dépendant (MUI). Fichiers RES.</span><span class="sxs-lookup"><span data-stu-id="e4917-139">Overlapping resource types that RC places into both the language-neutral .RES and the language-dependent (MUI).RES files.</span></span> <span data-ttu-id="e4917-140">Les types de ressources spécifiés par l’option **/k** doivent être un sous-ensemble de ceux qui sont spécifiés par l’option **/j** .</span><span class="sxs-lookup"><span data-stu-id="e4917-140">The resource types that are specified by the **/k** option must be a subset of those that are specified by the **/j** option.</span></span> <span data-ttu-id="e4917-141">Par exemple, ? J2? J3? K3 spécifie que RC place le type de ressource 3 à la fois dans les fichiers indépendants de la langue et en fonction de la langue (MUI).</span><span class="sxs-lookup"><span data-stu-id="e4917-141">For example, ?J2 ?J3 ?K3 specifies that RC places resource type 3 in both the language-neutral and language-dependent (MUI) files.</span></span> <span data-ttu-id="e4917-142">Si l’option **/q** est également définie, cette option est ignorée et les informations contenues dans le fichier de configuration RC sont prioritaires.</span><span class="sxs-lookup"><span data-stu-id="e4917-142">If the **/q** option is also set, this option is ignored, and the information in the RC Configuration file takes precedence.</span></span>

<span data-ttu-id="e4917-143">**Windows Server 2003 et Windows XP/2000 :** Cette option n’est pas disponible sans utiliser également les fonctions [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) et [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) sur un système mis à jour.</span><span class="sxs-lookup"><span data-stu-id="e4917-143">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="e4917-144"><span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *ID de langue*</span><span class="sxs-lookup"><span data-stu-id="e4917-144"><span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *langid*</span></span>
</dt> <dd>

<span data-ttu-id="e4917-145">Spécifie la langue par défaut pour la compilation.</span><span class="sxs-lookup"><span data-stu-id="e4917-145">Specifies the default language for compilation.</span></span> <span data-ttu-id="e4917-146">Par exemple,-l409 équivaut à inclure l’instruction suivante en haut du fichier de script de ressources : `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`</span><span class="sxs-lookup"><span data-stu-id="e4917-146">For example, -l409 is equivalent to including the following statement at the top of the resource script file: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`</span></span>

<span data-ttu-id="e4917-147">Pour plus d’informations, consultez [identificateurs de langue](/windows/desktop/Intl/language-identifiers).</span><span class="sxs-lookup"><span data-stu-id="e4917-147">For more information, see [Language Identifiers](/windows/desktop/Intl/language-identifiers).</span></span>

</dd> <dt>

<span data-ttu-id="e4917-148"><span id="_n"></span><span id="_N"></span>**/n**</span><span class="sxs-lookup"><span data-stu-id="e4917-148"><span id="_n"></span><span id="_N"></span>**/n**</span></span>
</dt> <dd>

<span data-ttu-id="e4917-149">NULL termine toutes les chaînes dans la table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="e4917-149">Null terminates all strings in the string table.</span></span>

</dd> <dt>

<span data-ttu-id="e4917-150"><span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/Q** *MUI. rcconfig*</span><span class="sxs-lookup"><span data-stu-id="e4917-150"><span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/q** *Mui.RCConfig*</span></span>
</dt> <dd>

<span data-ttu-id="e4917-151">Fichier de configuration RC qui suit le format du fichier de configuration RC.</span><span class="sxs-lookup"><span data-stu-id="e4917-151">An RC configuration file that follows the RC Configuration File format.</span></span> <span data-ttu-id="e4917-152">Le format de fichier de configuration RC permet aux composants de décrire eux-mêmes des informations sur les ressources telles que le contrôle de version des ressources, le chemin d’accès du fichier MUI, les types de ressources et les éléments.</span><span class="sxs-lookup"><span data-stu-id="e4917-152">The RC Configuration File format enables components to self-describe resource information such as resource versioning, MUI file path, resource types and items.</span></span> <span data-ttu-id="e4917-153">Ce fichier spécifie les ressources qui sont déplacées dans le indépendant de la langue. Fichier RES et les ressources qui sont placées dans la langue (MUI). Fichier RES.</span><span class="sxs-lookup"><span data-stu-id="e4917-153">This file specifies which resources go into the language-neutral .RES file and which resources go into the language-dependent (MUI) .RES file.</span></span> <span data-ttu-id="e4917-154">Cette option, et les informations fournies dans le fichier de configuration RC, remplacent les options de ligne de commande **/j** et **/k**.</span><span class="sxs-lookup"><span data-stu-id="e4917-154">This option, and the information provided in the RC Configuration file, override the command line options **/j** and **/k**.</span></span>

<span data-ttu-id="e4917-155">**Windows Server 2003 et Windows XP/2000 :** Cette option n’est pas disponible sans utiliser également les fonctions [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) et [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) sur un système mis à jour.</span><span class="sxs-lookup"><span data-stu-id="e4917-155">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="e4917-156"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="e4917-156"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="e4917-157">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="e4917-157">Ignored.</span></span> <span data-ttu-id="e4917-158">Fourni pour la compatibilité avec les Makefiles existants.</span><span class="sxs-lookup"><span data-stu-id="e4917-158">Provided for compatibility with existing makefiles.</span></span>

</dd> <dt>

<span data-ttu-id="e4917-159"><span id="_u"></span><span id="_U"></span>**/u.**</span><span class="sxs-lookup"><span data-stu-id="e4917-159"><span id="_u"></span><span id="_U"></span>**/u**</span></span>
</dt> <dd>

<span data-ttu-id="e4917-160">Annule la définition d’un symbole pour le préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="e4917-160">Undefines a symbol for the preprocessor.</span></span>

</dd> <dt>

<span data-ttu-id="e4917-161"><span id="_v"></span><span id="_V"></span>**/f**</span><span class="sxs-lookup"><span data-stu-id="e4917-161"><span id="_v"></span><span id="_V"></span>**/v**</span></span>
</dt> <dd>

<span data-ttu-id="e4917-162">Affiche des messages qui indiquent la progression du compilateur.</span><span class="sxs-lookup"><span data-stu-id="e4917-162">Displays messages that report on the progress of the compiler.</span></span>

</dd> <dt>

<span data-ttu-id="e4917-163"><span id="_x"></span><span id="_X"></span>**/Path**</span><span class="sxs-lookup"><span data-stu-id="e4917-163"><span id="_x"></span><span id="_X"></span>**/x**</span></span>
</dt> <dd>

<span data-ttu-id="e4917-164">Empêche RC de vérifier la variable d’environnement INCLUDe lors de la recherche de fichiers d’en-tête ou de fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="e4917-164">Prevents RC from checking the INCLUDE environment variable when searching for header files or resource files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4917-165">Notes</span><span class="sxs-lookup"><span data-stu-id="e4917-165">Remarks</span></span>

<span data-ttu-id="e4917-166">Les options ne respectent pas la casse et un trait d’Union (-) peut être utilisé à la place d’une barre oblique (/).</span><span class="sxs-lookup"><span data-stu-id="e4917-166">Options are not case sensitive, and a hyphen (-) can be used in place of a slash mark (/).</span></span> <span data-ttu-id="e4917-167">Vous pouvez combiner des options à une seule lettre s’ils n’ont pas besoin de paramètres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e4917-167">You can combine single-letter options if they do not require any additional parameters.</span></span>

<span data-ttu-id="e4917-168">RC ne génère pas de fichier MUI dans les cas suivants.</span><span class="sxs-lookup"><span data-stu-id="e4917-168">RC will not generate a MUI file in the following cases.</span></span>

-   <span data-ttu-id="e4917-169">Il n’existe aucune ressource localisable dans le fichier. rc.</span><span class="sxs-lookup"><span data-stu-id="e4917-169">No localizable resources exist in the .rc file.</span></span>
-   <span data-ttu-id="e4917-170">Le seul ID de langue de ressource spécifié dans le fichier. RC est neutre (0x0).</span><span class="sxs-lookup"><span data-stu-id="e4917-170">The only resource language id specified in the .rc file is neutral (0x0).</span></span>
-   <span data-ttu-id="e4917-171">Le fichier. rc contient des ressources spécifiées dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="e4917-171">The .rc file has resources that are specified in more than one language.</span></span> <span data-ttu-id="e4917-172">L’exception est si le fichier. rc contient deux langues et si une langue est neutre (0x0), RC génère un fichier MUI.</span><span class="sxs-lookup"><span data-stu-id="e4917-172">The exception is if the .rc file contains two languages, and one language is neutral (0x0), RC generates a MUI file.</span></span>

<span data-ttu-id="e4917-173">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="e4917-173">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="e4917-174">Définition des noms pour le préprocesseur</span><span class="sxs-lookup"><span data-stu-id="e4917-174">Defining Names for the Preprocessor</span></span>](defining-names-for-the-preprocessor.md)
-   [<span data-ttu-id="e4917-175">Attribution d’un nouveau nom au fichier de ressources compilé</span><span class="sxs-lookup"><span data-stu-id="e4917-175">Renaming the Compiled Resource File</span></span>](renaming-the-compiled-resource-file.md)
-   [<span data-ttu-id="e4917-176">Recherche de fichiers</span><span class="sxs-lookup"><span data-stu-id="e4917-176">Searching for Files</span></span>](searching-for-files.md)
-   [<span data-ttu-id="e4917-177">Affichage des messages de progression</span><span class="sxs-lookup"><span data-stu-id="e4917-177">Displaying Progress Messages</span></span>](displaying-progress-messages.md)
-   [<span data-ttu-id="e4917-178">Messages de diagnostic RC</span><span class="sxs-lookup"><span data-stu-id="e4917-178">RC Diagnostic Messages</span></span>](rc-diagnostic-messages.md)

## <a name="related-topics"></a><span data-ttu-id="e4917-179">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e4917-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4917-180">Interface utilisateur multilingue</span><span class="sxs-lookup"><span data-stu-id="e4917-180">Multilingual User Interface</span></span>](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 