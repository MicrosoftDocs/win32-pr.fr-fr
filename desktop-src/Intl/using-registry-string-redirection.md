---
description: Le stockage de chaînes codées en dur dans le registre fait partie d’un modèle de localisation antérieur à Windows Vista.
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: Utilisation de la redirection de chaînes de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f6e1420aae0ff41c386e19852bebbd1a322c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523058"
---
# <a name="using-registry-string-redirection"></a><span data-ttu-id="396b0-103">Utilisation de la redirection de chaînes de Registre</span><span class="sxs-lookup"><span data-stu-id="396b0-103">Using Registry String Redirection</span></span>

<span data-ttu-id="396b0-104">Le stockage de chaînes codées en dur dans le registre fait partie d’un modèle de localisation antérieur à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="396b0-104">Storage of hard-coded strings in the registry is part of a pre-Windows Vista localization model.</span></span> <span data-ttu-id="396b0-105">Elle n’est pas prise en charge par MUI.</span><span class="sxs-lookup"><span data-stu-id="396b0-105">It is not supported by MUI.</span></span> <span data-ttu-id="396b0-106">Dans le modèle actuel, l’interface utilisateur du système d’exploitation s’exécute dans des fichiers de ressources spécifiques à une langue, en plus d’une base indépendante du langage.</span><span class="sxs-lookup"><span data-stu-id="396b0-106">In the current model, the user interface for the operating system runs in language-specific resource files on top of a language-neutral base.</span></span> <span data-ttu-id="396b0-107">Les composants du système d’exploitation utilisent le registre de manière indépendante de la langue.</span><span class="sxs-lookup"><span data-stu-id="396b0-107">The components of the operating system use the registry in a language-neutral manner.</span></span>

<span data-ttu-id="396b0-108">MUI utilise uniquement les chaînes de Registre redirigées définies par les ressources Win32 PE dans le fichier de ressources de langue de base.</span><span class="sxs-lookup"><span data-stu-id="396b0-108">MUI uses only redirected registry strings defined by Win32 PE resources in the base language resource file.</span></span> <span data-ttu-id="396b0-109">La redirection est définie séparément, par exemple dans un fichier. inf.</span><span class="sxs-lookup"><span data-stu-id="396b0-109">Redirection is defined separately, for example, in an .inf file.</span></span> <span data-ttu-id="396b0-110">Ce type de stockage permet au chargeur de ressources de sélectionner automatiquement les ressources de langue appropriées lors du chargement du module de ressources.</span><span class="sxs-lookup"><span data-stu-id="396b0-110">This type of storage allows the resource loader to select the correct language resources automatically during resource module loading.</span></span>

> [!Note]  
> <span data-ttu-id="396b0-111">Cette rubrique se rapporte uniquement aux ressources Win32 PE.</span><span class="sxs-lookup"><span data-stu-id="396b0-111">This topic pertains only to Win32 PE resources.</span></span> <span data-ttu-id="396b0-112">Si vous utilisez des ressources PE non Win32, vous devez fournir une redirection de chaîne de Registre personnalisée, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="396b0-112">If using non-Win32 PE resources, you must provide customized registry string redirection, if required.</span></span>

 

## <a name="create-a-language-neutral-resource"></a><span data-ttu-id="396b0-113">Créer une ressource Language-Neutral</span><span class="sxs-lookup"><span data-stu-id="396b0-113">Create a Language-Neutral Resource</span></span>

<span data-ttu-id="396b0-114">Une application MUI s’exécutant sur Windows Vista et versions ultérieures utilise une ressource de chaîne indépendante du langage pour autoriser l’accès aux chaînes spécifiques à la langue stockées dans une table de ressources de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="396b0-114">A MUI application running on Windows Vista and later uses a language-neutral string resource to allow access to language-specific strings stored in a string resource table.</span></span> <span data-ttu-id="396b0-115">Le code d’application qui lit ces valeurs à partir du Registre est décrit dans la section chargement d’un Language-Neutral valeur de registre de [localisation des chaînes redirigées](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="396b0-115">Application code that reads these values from the registry is described in the Load a Language-Neutral Registry Value section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

<span data-ttu-id="396b0-116">Les données d’une valeur de Registre indépendante du langage ont le format « `@<PE-path>,-<stringID>[;<comment>]` », où :</span><span class="sxs-lookup"><span data-stu-id="396b0-116">The data for a language-neutral registry value has the format "`@<PE-path>,-<stringID>[;<comment>]`", where:</span></span>

-   <span data-ttu-id="396b0-117">*PE-Path* spécifie le chemin d’accès de l’exécutable.</span><span class="sxs-lookup"><span data-stu-id="396b0-117">*PE-path* specifies the path of the executable.</span></span> <span data-ttu-id="396b0-118">Vous pouvez spécifier le chemin d’accès à l’aide d’une variable d’environnement, telle que% ProgramFiles%, pour prendre en charge le déploiement.</span><span class="sxs-lookup"><span data-stu-id="396b0-118">You can specify the path using an environment variable, such as %ProgramFiles%, to support deployment.</span></span> <span data-ttu-id="396b0-119">Pour faire référence à votre chaîne, vous pouvez également conserver les informations de chemin d’accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="396b0-119">An alternative for making your string reference is to leave out the file path information.</span></span> <span data-ttu-id="396b0-120">Dans ce cas, votre application doit avoir des moyens, par exemple, une autre valeur de Registre, pour communiquer son propre répertoire d’installation.</span><span class="sxs-lookup"><span data-stu-id="396b0-120">In this case, your application must have some means, for example, another registry value, to communicate its own install directory.</span></span>
-   <span data-ttu-id="396b0-121">*stringID* spécifie l’identificateur de ressource numérique de la ressource de chaîne appropriée, qui est implémentée comme n’importe quelle autre ressource de chaîne localisable.</span><span class="sxs-lookup"><span data-stu-id="396b0-121">*stringID* specifies the numeric resource identifier of the relevant string resource, which is implemented just like any other localizable string resource.</span></span>
-   <span data-ttu-id="396b0-122">le *Commentaire* spécifie des informations facultatives pour le débogage ou la lisibilité de la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="396b0-122">*comment* specifies optional information for debugging or readability of the registry value.</span></span> <span data-ttu-id="396b0-123">Les fonctions de l’API du Registre ignorent le commentaire lors du chargement de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="396b0-123">The registry API functions ignore the comment when loading the string.</span></span>

> [!Note]  
> <span data-ttu-id="396b0-124">Les données de la valeur de registre ne font pas de référence explicite au fichier de ressources spécifique au langage.</span><span class="sxs-lookup"><span data-stu-id="396b0-124">The data for the registry value makes no explicit reference to the language-specific resource file.</span></span> <span data-ttu-id="396b0-125">Le fichier approprié est déterminé au moment de l’exécution, en fonction des préférences de langue de l’interface utilisateur actuelle.</span><span class="sxs-lookup"><span data-stu-id="396b0-125">The correct file is determined at runtime, based on the current user interface language preferences.</span></span>

 

<span data-ttu-id="396b0-126">Une valeur de Registre est entrée sans espace entre les valeurs « , » et « - ».</span><span class="sxs-lookup"><span data-stu-id="396b0-126">A registry value is entered without a space between the "," and "-".</span></span> <span data-ttu-id="396b0-127">Une valeur de Registre correcte est :</span><span class="sxs-lookup"><span data-stu-id="396b0-127">A correct registry value is:</span></span>

`shell32.dll,-22912`

<span data-ttu-id="396b0-128">Une valeur de Registre incorrecte est :</span><span class="sxs-lookup"><span data-stu-id="396b0-128">An incorrect registry value is:</span></span>

`shell32.dll, -22912`

<span data-ttu-id="396b0-129">Un exemple de Windows Vista est la valeur de Registre avec les données suivantes :</span><span class="sxs-lookup"><span data-stu-id="396b0-129">An example from Windows Vista is the registry value with the following data:</span></span>

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a><span data-ttu-id="396b0-130">Créer des ressources pour les chaînes de raccourci</span><span class="sxs-lookup"><span data-stu-id="396b0-130">Create Resources for Shortcut Strings</span></span>

<span data-ttu-id="396b0-131">Lorsque l’application MUI affiche son nom dans l’interface utilisateur de l’interpréteur de commandes, une chaîne d’info-bulle s’affiche pour l’icône de l’application.</span><span class="sxs-lookup"><span data-stu-id="396b0-131">When the MUI application displays its name in the shell user interface, an InfoTip string is displayed for the application icon.</span></span> <span data-ttu-id="396b0-132">Vous devez créer des ressources de type chaîne pour le nom d’affichage de votre application et la chaîne d’info-bulle associée pour chaque langue prise en charge.</span><span class="sxs-lookup"><span data-stu-id="396b0-132">You should create string resources for your application display name and associated InfoTip string for each supported language.</span></span> <span data-ttu-id="396b0-133">Lorsque les ressources sont prêtes, votre application peut utiliser les chaînes comme décrit dans la section utiliser l’API Shell pour charger des chaînes de raccourci à partir du registre de [localisation des chaînes redirigées](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="396b0-133">When the resources are ready, your application can use the strings as described in the Use Shell API to Load Shortcut Strings from the Registry section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a><span data-ttu-id="396b0-134">Préparer les ressources pour un raccourci créé avec Windows Installer</span><span class="sxs-lookup"><span data-stu-id="396b0-134">Prepare Resources for a Shortcut Created with Windows Installer</span></span>

<span data-ttu-id="396b0-135">Si vous utilisez Windows Installer (MSI) pour créer un raccourci, les ressources de type chaîne incluent le nom complet et la description du raccourci.</span><span class="sxs-lookup"><span data-stu-id="396b0-135">If you use Windows Installer (MSI) to create a shortcut, string resources include shortcut display name and description.</span></span> <span data-ttu-id="396b0-136">Dans la [table de raccourcis MSI](../msi/shortcut-table.md), la dll de ressource est référencée dans les colonnes appropriées et les identificateurs de ressource pour le nom complet et la description de votre raccourci sont utilisés dans les colonnes correspondantes de l’identificateur de ressource.</span><span class="sxs-lookup"><span data-stu-id="396b0-136">In the [MSI shortcut table](../msi/shortcut-table.md), the resource DLL is referenced in the appropriate columns and the resource identifiers for your shortcut display name and description are used in the corresponding resource identifier columns.</span></span>

<span data-ttu-id="396b0-137">Pour que le raccourci de l’application fonctionne correctement avec la technologie de ressources MUI, gardez les points suivants à l’esprit lors de la préparation des chaînes de raccourci :</span><span class="sxs-lookup"><span data-stu-id="396b0-137">So that the application shortcut works properly with MUI resource technology, keep the following points in mind when preparing the shortcut strings:</span></span>

-   <span data-ttu-id="396b0-138">Utilisez des variables d’environnement ou un chemin d’accès relatif pour inscrire la DLL.</span><span class="sxs-lookup"><span data-stu-id="396b0-138">Use either environment variables or a relative path to register the DLL.</span></span> <span data-ttu-id="396b0-139">Vous pouvez spécifier @% systemroot% \\ system32 \\shell32.dll tant que le type de chaîne de Registre est reg \_ expand \_ sz.</span><span class="sxs-lookup"><span data-stu-id="396b0-139">You can specify @%systemroot%\\system32\\shell32.dll as long as the registry string type is REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="396b0-140">L’identificateur de ressource de chaîne pour « document texte » dans Shell32.dll est 12345.</span><span class="sxs-lookup"><span data-stu-id="396b0-140">The string resource identifier for "Text Document" in Shell32.dll is 12345.</span></span>
-   <span data-ttu-id="396b0-141">N’utilisez pas d’espaces autour des symboles « , » et « - ».</span><span class="sxs-lookup"><span data-stu-id="396b0-141">Do not use spaces around the "," and "-" symbols.</span></span> <span data-ttu-id="396b0-142">Un exemple correct est « shell32.dll,-22912 ».</span><span class="sxs-lookup"><span data-stu-id="396b0-142">A correct example is "shell32.dll,-22912".</span></span>
-   <span data-ttu-id="396b0-143">N’utilisez pas de nom de fichier courts.</span><span class="sxs-lookup"><span data-stu-id="396b0-143">Do not use a short file name.</span></span> <span data-ttu-id="396b0-144">Ce type de nom ne fonctionne pas avec le chargeur de ressources.</span><span class="sxs-lookup"><span data-stu-id="396b0-144">This type of name does not work with the resource loader.</span></span>

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a><span data-ttu-id="396b0-145">Préparer des ressources pour un raccourci à l’aide du format INF</span><span class="sxs-lookup"><span data-stu-id="396b0-145">Prepare Resources for a Shortcut Using INF Format</span></span>

<span data-ttu-id="396b0-146">Si vous utilisez le format de fichier INF pour créer des chaînes de raccourci, le fichier de ressources doit apporter les paramètres de registre suivants.</span><span class="sxs-lookup"><span data-stu-id="396b0-146">If you use the INF file format to create shortcut strings, the resource file should make the following registry settings.</span></span> <span data-ttu-id="396b0-147">Ces instructions supposent l’utilisation de la syntaxe ProfileItems de l’API d’installation.</span><span class="sxs-lookup"><span data-stu-id="396b0-147">These instructions assume the use of the ProfileItems syntax of Setup API.</span></span>

1.  <span data-ttu-id="396b0-148">Modifiez la valeur de l’info-bulle pour pointer vers la référence de redirection de chaînes à l’aide du chemin d’accès et de l’identificateur de ressource.</span><span class="sxs-lookup"><span data-stu-id="396b0-148">Change the InfoTip value to point to the string redirection reference, using the path and resource identifier.</span></span>
2.  <span data-ttu-id="396b0-149">Ajoutez la nouvelle valeur DisplayResource sous les sections installation de ProfileItems.</span><span class="sxs-lookup"><span data-stu-id="396b0-149">Add the new value DisplayResource under the ProfileItems installation sections.</span></span>

<span data-ttu-id="396b0-150">Voici un exemple qui illustre l’ajout de l’application Calculatrice au menu **Démarrer** :</span><span class="sxs-lookup"><span data-stu-id="396b0-150">The following is an example showing the addition of the Calculator application to the **Start** menu:</span></span>


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



<span data-ttu-id="396b0-151">Utilisez la syntaxe indiquée ci-dessous lorsque vous utilisez INF pour ajouter des éléments, par exemple, un dossier de groupe d’accès, au menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="396b0-151">Use the syntax shown below when using INF to add items, for example, an Access Group folder, to the **Start** menu.</span></span> <span data-ttu-id="396b0-152">Cette syntaxe suppose l’utilisation de la \[ \] prise en charge de StartMenuItems par le programme d’installation, similaire à la syntaxe utilisée dans syssetup. inf.</span><span class="sxs-lookup"><span data-stu-id="396b0-152">This syntax assumes the use of \[StartMenuItems\] support from Setup, similar to the syntax used in Syssetup.inf.</span></span>


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



<span data-ttu-id="396b0-153">Définissez la valeur *info-bulle* sur la référence de chaîne « `@<path>,-resID` ».</span><span class="sxs-lookup"><span data-stu-id="396b0-153">Set the value *infotip* to the string reference "`@<path>,-resID`".</span></span>

<span data-ttu-id="396b0-154">Le nom d’affichage est déterminé par les valeurs *resDLL* et *resID* .</span><span class="sxs-lookup"><span data-stu-id="396b0-154">The display name is determined by the *resDLL* and *resID* values.</span></span> <span data-ttu-id="396b0-155">La valeur *resID* spécifie l’identificateur de ressource pour une ressource de type chaîne associée au fichier indépendant de la langue.</span><span class="sxs-lookup"><span data-stu-id="396b0-155">The *resID* value specifies the resource identifier for a string resource associated with the language-neutral file.</span></span> <span data-ttu-id="396b0-156">La valeur *resDLL* spécifie le chemin d’accès au fichier indépendant du langage.</span><span class="sxs-lookup"><span data-stu-id="396b0-156">The *resDLL* value specifies the path to the language-neutral file.</span></span>

## <a name="create-resources-for-friendly-document-type-names"></a><span data-ttu-id="396b0-157">Créer des ressources pour les noms de type de document conviviaux</span><span class="sxs-lookup"><span data-stu-id="396b0-157">Create Resources for Friendly Document Type Names</span></span>

<span data-ttu-id="396b0-158">Vous devez implémenter des chaînes nom convivial et info-bulle pour votre application en tant que ressources de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="396b0-158">You must implement friendly name and InfoTip strings for your application as string resources.</span></span> <span data-ttu-id="396b0-159">Pour permettre aux noms de type de document conviviaux de réagir à la langue de l’interface utilisateur, l’application doit inscrire les noms à l’aide de la valeur FriendlyTypeName sous la clé de l’identificateur de programme pour le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="396b0-159">To allow friendly document type names to react to the user interface language, the application must register the names using the FriendlyTypeName value under the program identifier key for the file type.</span></span> <span data-ttu-id="396b0-160">La valeur par défaut de la clé d’identificateur de programme doit être conservée pour assurer la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="396b0-160">The default value for the program identifier key should be retained to keep backward compatibility.</span></span> <span data-ttu-id="396b0-161">Pour plus d’informations sur l’accès aux noms à partir de votre application, consultez la section relative aux noms de types de document conviviaux dans le registre de [localisation des chaînes redirigées](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="396b0-161">For information about accessing the names from your application, see the Query Friendly Document Type Names in the Registry section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

<span data-ttu-id="396b0-162">Le travail spécifique implique les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="396b0-162">The specific work involves the following steps:</span></span>

1.  <span data-ttu-id="396b0-163">Implémentez les chaînes nom convivial et info-bulle en tant que ressources de chaîne spécifiques au langage.</span><span class="sxs-lookup"><span data-stu-id="396b0-163">Implement the friendly name and InfoTip strings as language-specific string resources.</span></span>
2.  <span data-ttu-id="396b0-164">Ajoutez la valeur FriendlyTypeName sous la clé de Registre type de document.</span><span class="sxs-lookup"><span data-stu-id="396b0-164">Add the FriendlyTypeName value under the document type registry key.</span></span> <span data-ttu-id="396b0-165">Les données de la valeur suivent le modèle « `@<path>,-<resID>` », où *chemin d’accès* indique l’exécutable et *resID* est l’identificateur de ressource d’une ressource de type chaîne localisable associée à cet exécutable.</span><span class="sxs-lookup"><span data-stu-id="396b0-165">The data for the value follows the pattern "`@<path>,-<resID>`", where *path* indicates the executable and *resID* is the resource identifier of a localizable string resource associated with that executable.</span></span>
3.  <span data-ttu-id="396b0-166">Spécifiez la valeur de registre d’info-bulle en fonction du format « `@<path>,-<resID>` ».</span><span class="sxs-lookup"><span data-stu-id="396b0-166">Specify the InfoTip registry value according to the format "`@<path>,-<resID>`".</span></span>

<span data-ttu-id="396b0-167">L’exemple suivant montre les paramètres de registre d’un fichier. txt :</span><span class="sxs-lookup"><span data-stu-id="396b0-167">The following example shows the registry settings for a .txt file:</span></span>


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a><span data-ttu-id="396b0-168">Fournir des ressources pour les chaînes d’action de verbe de Shell</span><span class="sxs-lookup"><span data-stu-id="396b0-168">Provide Resources for Shell Verb Action Strings</span></span>

<span data-ttu-id="396b0-169">Les chaînes d’action de certains verbes, par exemple « ouvrir » et « modifier », sont affichées dans le menu contextuel qui s’affiche lorsque l’utilisateur clique avec le bouton droit sur un fichier dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="396b0-169">Action strings for certain verbs, for example, "open" and "edit", are shown in the pop-up menu displayed when the user right-clicks a file in Windows Explorer.</span></span> <span data-ttu-id="396b0-170">Votre application n’a pas besoin de spécifier des chaînes pour les verbes d’interpréteur de commandes courants, car l’interpréteur de commandes possède ses propres valeurs par défaut compatibles MUI pour ces verbes.</span><span class="sxs-lookup"><span data-stu-id="396b0-170">Your application does not have to specify strings for common shell verbs, as the shell has its own MUI-enabled defaults for these verbs.</span></span> <span data-ttu-id="396b0-171">Toutefois, vous devez fournir des ressources de type chaîne localisables pour les chaînes qui représentent des verbes rares.</span><span class="sxs-lookup"><span data-stu-id="396b0-171">However, you should provide localizable string resources for strings representing uncommon verbs.</span></span>

<span data-ttu-id="396b0-172">Sur les systèmes d’exploitation antérieurs à Windows XP, les chaînes pour les verbes de Shell dans le Registre sont restituées à l’aide de la syntaxe suivante, où *verb* spécifie le nom de verbe réel :</span><span class="sxs-lookup"><span data-stu-id="396b0-172">On pre-Windows XP operating systems, strings for shell verbs in the registry are rendered using the following syntax, where *verb* specifies the actual verb name:</span></span>


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



<span data-ttu-id="396b0-173">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="396b0-173">Here's an example:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



<span data-ttu-id="396b0-174">Sur Windows XP et versions ultérieures, vous pouvez utiliser un niveau d’indirection pour que la chaîne d’action dépende de la langue de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="396b0-174">On Windows XP and later, you can use a level of indirection to make an action string depend on user interface language.</span></span> <span data-ttu-id="396b0-175">Ces systèmes d’exploitation prennent en charge une valeur MUIVerb pour la définition d’une chaîne compatible MUI.</span><span class="sxs-lookup"><span data-stu-id="396b0-175">These operating systems support a MUIVerb value for definition of a MUI-compatible string.</span></span> <span data-ttu-id="396b0-176">Voici un exemple d’entrée de Registre pour un verbe rare :</span><span class="sxs-lookup"><span data-stu-id="396b0-176">Here's an example of a registry entry for an uncommon verb:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



<span data-ttu-id="396b0-177">Votre application MUI doit également être en mesure d’enregistrer l’ancienne valeur par défaut en tant que chaîne localisable, comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="396b0-177">Your MUI application should also be able to register the old default value as a localizable string, as shown below:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> <span data-ttu-id="396b0-178">L’inscription de l’ancienne valeur par défaut n’est pas recommandée, car elle nécessite une installation différente sur Windows XP et versions ultérieures à partir de la configuration utilisée sur les systèmes d’exploitation antérieurs.</span><span class="sxs-lookup"><span data-stu-id="396b0-178">Registration of the old default value is not recommended because it requires a different setup on Windows XP and later from the setup used on earlier operating systems.</span></span>

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a><span data-ttu-id="396b0-179">Créer des ressources pour les chaînes Verb, Protocol et AuxUserType</span><span class="sxs-lookup"><span data-stu-id="396b0-179">Create Resources for Verb, Protocol, and AuxUserType Strings</span></span>

<span data-ttu-id="396b0-180">Vous devez créer des ressources de type chaîne localisables pour les chaînes Verb, Protocol et AuxUserType.</span><span class="sxs-lookup"><span data-stu-id="396b0-180">You should create localizable string resources for Verb, Protocol, and AuxUserType strings.</span></span> <span data-ttu-id="396b0-181">Utilisez les paramètres de registre suivants :</span><span class="sxs-lookup"><span data-stu-id="396b0-181">Use the following registry settings:</span></span>


```C++
HKCR\CLSID\{<Your_CLSID>}\Verb\<number> @="<Your Verb>, <menu_flag>, <verb_flag>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...

HKCR\CLSID\{<Your_CLSID>}\AuxUserType\<number>
@="<Your Short Name>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID1"
...

HKCR\<Your_Name>\protocol\StdFileEditing\verb\<number>
@="<Your Verb>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...
```



<span data-ttu-id="396b0-182">La valeur spécifiée pour LocalizedString contient ou remplace uniquement la valeur de *votre verbe*, pas les deux valeurs d’indicateur.</span><span class="sxs-lookup"><span data-stu-id="396b0-182">The value specified for LocalizedString only contains or replaces the value for *Your Verb*, not the two flag values.</span></span>

<span data-ttu-id="396b0-183">Voici un résumé pour vous aider à vérifier les paramètres de registre appropriés :</span><span class="sxs-lookup"><span data-stu-id="396b0-183">Here is a summary to help you ensure correct registry settings:</span></span>

-   <span data-ttu-id="396b0-184">Si CLSID a une \\ \\ clé Insertable de HKCR CLSID {CLSID} \\ , définissez la valeur de CLSID par défaut à l’aide de HKCR \\ CLSID \\ {CLSID} \\ LocalizedString.</span><span class="sxs-lookup"><span data-stu-id="396b0-184">If CLSID has a HKCR\\CLSID\\{clsid}\\Insertable key, define the default CLSID value using HKCR\\CLSID\\{clsid}\\LocalizedString.</span></span>
-   <span data-ttu-id="396b0-185">Si CLSID contient une ou plusieurs sous-clés sous \\ le \\ verbe HKCR CLSID {CLSID} \\ , définissez chaque chaîne de verbe individuelle à l’aide du \\ verbe HKCR CLSID \\ {CLSID} \\ \\ \\ LocalizedString.</span><span class="sxs-lookup"><span data-stu-id="396b0-185">If CLSID has one or more subkeys under HKCR\\CLSID\\{clsid}\\Verb, define each individual Verb string using HKCR\\CLSID\\{clsid}\\Verb\\xxx\\LocalizedString.</span></span>
-   <span data-ttu-id="396b0-186">Si CLSID contient une ou plusieurs sous-clés sous le \\ verbe Stdfileediting du protocole HKCR {ProgID} \\ \\ \\ , définissez chaque chaîne de verbe individuelle à l’aide du \\ verbe Stdfileediting du protocole HKCR {ProgID} \\ \\ \\ \\ \\ LocalizedString.</span><span class="sxs-lookup"><span data-stu-id="396b0-186">If CLSID has one or more subkeys under HKCR\\{progid}\\Protocol\\Stdfileediting\\Verb, define each individual Verb string using HKCR\\{progid}\\Protocol\\Stdfileediting\\Verb\\xxx\\LocalizedString.</span></span>
-   <span data-ttu-id="396b0-187">Si CLSID contient une ou plusieurs sous-clés AuxUserType listées sous HKCR \\ CLSID \\ {CLSID} \\ AuxUserType, définissez chaque entrée AuxUserType à l’aide de HKCR \\ CLSID \\ {CLSID} \\ AuxUserType \\ xxx \\ LocalizedString.</span><span class="sxs-lookup"><span data-stu-id="396b0-187">If CLSID has one or more listed AuxUserType subkeys under HKCR\\CLSID\\{clsid}\\AuxUserType, define each AuxUserType entry using HKCR\\CLSID\\{clsid}\\AuxUserType\\xxx\\LocalizedString.</span></span>

## <a name="create-a-resource-for-the-uninstall-program"></a><span data-ttu-id="396b0-188">Créer une ressource pour le programme de désinstallation</span><span class="sxs-lookup"><span data-stu-id="396b0-188">Create a Resource for the Uninstall Program</span></span>

<span data-ttu-id="396b0-189">Pour inscrire le programme de désinstallation de l’application, vous pouvez créer des valeurs de Registre dans la sous-clé de l’identificateur unique de l’application sous la clé de Registre HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Uninstall.</span><span class="sxs-lookup"><span data-stu-id="396b0-189">To register the uninstall program for the application, you can create registry values in the unique identifier subkey for the application under the registry key HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\Uninstall.</span></span> <span data-ttu-id="396b0-190">Les valeurs à définir sont les suivantes : DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, contact, Comments, DisplayIcon, README, UrlUpdateInfo.</span><span class="sxs-lookup"><span data-stu-id="396b0-190">Values to set include: DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, Contact, Comments, DisplayIcon, Readme, UrlUpdateInfo.</span></span>

> [!Note]  
> <span data-ttu-id="396b0-191">Pour activer la technologie MUI pour chaque valeur, vous pouvez ajouter « \_ Localized » au nom de la valeur.</span><span class="sxs-lookup"><span data-stu-id="396b0-191">To enable MUI technology for each value, you can append "\_Localized" to the value name.</span></span>

 

<span data-ttu-id="396b0-192">Les composants du système d’exploitation sont requis pour fournir une valeur pour DisplayName \_ localisée de manière spécifique à MUI.</span><span class="sxs-lookup"><span data-stu-id="396b0-192">Operating system components are required to provide a value for DisplayName\_Localized in a MUI-specific way.</span></span> <span data-ttu-id="396b0-193">Vous devez placer le nom complet dans une DLL, par exemple Res.dll, en tant que ressource de type chaîne, en supposant que l’identificateur soit 1245.</span><span class="sxs-lookup"><span data-stu-id="396b0-193">You should place the display name in a DLL, such as Res.dll, as a string resource, assuming the identifier to be 1245.</span></span> <span data-ttu-id="396b0-194">L’application peut ensuite enregistrer le nom complet comme DisplayName \_ localisé avec la valeur « @ \\res.DLL,-1245 ».</span><span class="sxs-lookup"><span data-stu-id="396b0-194">Then the application can register the display name as DisplayName\_Localized with value "@\\res.DLL,-1245".</span></span> <span data-ttu-id="396b0-195">Tous les autres paramètres du Registre doivent être conservés tels quels, y compris la valeur d’origine de DisplayName.</span><span class="sxs-lookup"><span data-stu-id="396b0-195">All the other registry settings should be retained as they are, including the original value for DisplayName.</span></span>

## <a name="create-resources-for-sound-events"></a><span data-ttu-id="396b0-196">Créer des ressources pour les événements sonores</span><span class="sxs-lookup"><span data-stu-id="396b0-196">Create Resources for Sound Events</span></span>

<span data-ttu-id="396b0-197">Windows associe certains événements à des fichiers son, par exemple, un événement de notification de courrier ou un événement d’alarme de batterie critique.</span><span class="sxs-lookup"><span data-stu-id="396b0-197">Windows associates certain events with sound files, for example, a New Mail Notification event or a Critical Battery Alarm event.</span></span> <span data-ttu-id="396b0-198">Les noms des événements doivent être affichés par l’interface utilisateur et doivent prendre en charge la globalisation.</span><span class="sxs-lookup"><span data-stu-id="396b0-198">The event names must be displayed by the user interface and must support globalization.</span></span> <span data-ttu-id="396b0-199">Par conséquent, vous devez implémenter une ressource de type chaîne localisable pour la description de chaque description d’événement.</span><span class="sxs-lookup"><span data-stu-id="396b0-199">Therefore, you should implement a localizable string resource for the description of each event description.</span></span> <span data-ttu-id="396b0-200">Ajoutez une nouvelle valeur de Registre pour chaque nom d’événement, en plus de la valeur par défaut codée en dur.</span><span class="sxs-lookup"><span data-stu-id="396b0-200">Add a new registry value for each event name, in addition to the hard-coded default value.</span></span>

<span data-ttu-id="396b0-201">Pour activer un événement sonore, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="396b0-201">Do the following to enable a sound event:</span></span>

1.  <span data-ttu-id="396b0-202">Implémentez la description en tant que ressource de chaîne localisable.</span><span class="sxs-lookup"><span data-stu-id="396b0-202">Implement the description as a localizable string resource.</span></span>
2.  <span data-ttu-id="396b0-203">Ajoutez une nouvelle valeur de Registre pour le nom complet, en plus de la valeur par défaut codée en dur.</span><span class="sxs-lookup"><span data-stu-id="396b0-203">Add a new registry value for the display name, in addition to the hard-coded default value.</span></span> <span data-ttu-id="396b0-204">La disposition du registre associée est indiquée ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="396b0-204">The associated registry layout is shown below:</span></span>


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



<span data-ttu-id="396b0-205">Si l’interpréteur de commandes ne peut pas trouver ou récupérer la valeur de DispFileName, il utilise la description par défaut.</span><span class="sxs-lookup"><span data-stu-id="396b0-205">If the shell cannot find or retrieve the value of DispFileName, it uses the default description.</span></span>

## <a name="create-resources-for-keyboard-layout-strings"></a><span data-ttu-id="396b0-206">Créer des ressources pour les chaînes de disposition du clavier</span><span class="sxs-lookup"><span data-stu-id="396b0-206">Create Resources for Keyboard Layout Strings</span></span>

<span data-ttu-id="396b0-207">Si votre application implémente une disposition de clavier, elle requiert une ressource de chaîne localisable pour le nom de la disposition pour l’affichage à l’écran, par exemple, dans les listes de dispositions de clavier.</span><span class="sxs-lookup"><span data-stu-id="396b0-207">If your application implements a keyboard layout, it requires a localizable string resource for the name of the layout for screen display, for example, in lists of keyboard layouts.</span></span> <span data-ttu-id="396b0-208">Chaque disposition de clavier a une clé de Registre sous HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ layouts.</span><span class="sxs-lookup"><span data-stu-id="396b0-208">Each keyboard layout has a registry key under HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Keyboard Layouts.</span></span>

<span data-ttu-id="396b0-209">Parmi les valeurs de cette clé figurent le texte de disposition, un nom explicite pour la compatibilité descendante et le nom d’affichage de la disposition.</span><span class="sxs-lookup"><span data-stu-id="396b0-209">Among the values for that key are Layout Text, a human-readable name for backward compatibility, and Layout Display Name.</span></span> <span data-ttu-id="396b0-210">Les données fournies pour le nom complet de la disposition doivent être une référence de chaîne sous la forme « `@<path>,-resID` », qui fait référence à une ressource de chaîne localisable associée à la disposition du clavier.</span><span class="sxs-lookup"><span data-stu-id="396b0-210">The data supplied for Layout Display Name should be a string reference of the form "`@<path>,-resID`", referring to a localizable string resource associated with the keyboard layout.</span></span>

<span data-ttu-id="396b0-211">Voici un exemple de paramètre de Registre pour la disposition de clavier espagnol (Espagne) :</span><span class="sxs-lookup"><span data-stu-id="396b0-211">Here is an example of a registry setting for the Spanish (Spain) keyboard layout:</span></span>

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a><span data-ttu-id="396b0-212">Représenter les chaînes de boîte de dialogue commune d’objet OLE Insert</span><span class="sxs-lookup"><span data-stu-id="396b0-212">Represent OLE Insert Object Common Dialog Strings</span></span>

<span data-ttu-id="396b0-213">Vous pouvez implémenter le nom complet d’un objet OLE pouvant être inséré en tant que ressource de chaîne localisable associée au code qui implémente cet objet.</span><span class="sxs-lookup"><span data-stu-id="396b0-213">You can implement the display name of an OLE insertable object as a localizable string resource associated with the code implementing that object.</span></span> <span data-ttu-id="396b0-214">La [boîte de dialogue OLE Insert Object](/cpp/mfc/reference/coleinsertdialog-class) obtient un nom complet à partir de la clé de Registre HKCR \\ CLSID \\ { *<GUID>* }, où *GUID* identifie l’identificateur de classe d’un objet OLE à insérer.</span><span class="sxs-lookup"><span data-stu-id="396b0-214">The [OLE Insert Object dialog box](/cpp/mfc/reference/coleinsertdialog-class) gets a display name from the registry key HKCR\\CLSID\\{*<GUID>*}, where *GUID* identifies the class identifier of an insertable OLE object.</span></span> <span data-ttu-id="396b0-215">Windows Vista et versions ultérieures implémentent ce type d’objet de façon localisable, à l’aide d’un nom d’affichage compatible avec MUI qui permet la personnalisation de la langue de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="396b0-215">Windows Vista and later implement this type of object in a localizable way, using a MUI-compliant display name that allows customization to the user interface language.</span></span> <span data-ttu-id="396b0-216">En revanche, les systèmes d’exploitation antérieurs à Windows Vista implémentent le nom complet de ce type d’objet à l’aide de la valeur par défaut de la clé de Registre correspondante.</span><span class="sxs-lookup"><span data-stu-id="396b0-216">In contrast, pre-Windows Vista operating systems implement the display name for this type of object using the default value of the corresponding registry key.</span></span> <span data-ttu-id="396b0-217">En général, il s’agit d’un nom anglais (États-Unis) ou d’un nom dans la langue de l’interface utilisateur par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="396b0-217">Typically this name is either an English (United States) name or a name in the system default UI language.</span></span>

> [!Note]  
> <span data-ttu-id="396b0-218">Tous les objets qui correspondent aux sous-clés de la clé de registre ne peuvent pas être insérés.</span><span class="sxs-lookup"><span data-stu-id="396b0-218">Not all objects that correspond to subkeys of the registry key are insertable.</span></span>

 

<span data-ttu-id="396b0-219">La valeur par défaut de la \\ clé HKCR CLSID \\ { *<GUID>* } doit conserver un nom explicite pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="396b0-219">The default value of the HKCR\\CLSID\\{*<GUID>*} key should retain a human-readable name for backward compatibility.</span></span> <span data-ttu-id="396b0-220">Toutefois, il doit également définir la valeur LocalizedString, au format « `@<path>,-ResID` », où Path identifie le fichier exécutable qui implémente l’objet.</span><span class="sxs-lookup"><span data-stu-id="396b0-220">However, it should also define the LocalizedString value, in the format "`@<path>,-ResID`", where path identifies the executable file implementing the object.</span></span> <span data-ttu-id="396b0-221">La valeur ResID spécifie l’identificateur de ressource de la chaîne localisable pour le nom complet.</span><span class="sxs-lookup"><span data-stu-id="396b0-221">The ResID value specifies the resource identifier of the localizable string for the display name.</span></span>

<span data-ttu-id="396b0-222">Par exemple, le script d’inscription de l’objet clip Media pouvant être inséré contient les lignes suivantes :</span><span class="sxs-lookup"><span data-stu-id="396b0-222">For example, the registration script for the insertable Media Clip object includes the following lines:</span></span>


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



<span data-ttu-id="396b0-223">La première ligne fournit une compatibilité descendante en plaçant une chaîne de texte simple dans le Registre sous la forme d’un nom d’affichage par défaut.</span><span class="sxs-lookup"><span data-stu-id="396b0-223">The first line provides backward compatibility by placing a simple text string in the registry as a default display name.</span></span> <span data-ttu-id="396b0-224">La deuxième ligne fournit l’accès au nom complet compatible MUI.</span><span class="sxs-lookup"><span data-stu-id="396b0-224">The second line provides access to the MUI-compliant display name.</span></span> <span data-ttu-id="396b0-225">Elle indique l’identificateur de chaîne stocké dans Mplay32.exe.</span><span class="sxs-lookup"><span data-stu-id="396b0-225">It indicates the string identifier stored in Mplay32.exe.</span></span> <span data-ttu-id="396b0-226">La chaîne avec l’identificateur 9217 dans Mplay32.exe peut être associée à des valeurs de ressource de type chaîne pour un nombre quelconque de langues.</span><span class="sxs-lookup"><span data-stu-id="396b0-226">The string with identifier 9217 in Mplay32.exe can be associated with string resource values for any number of languages.</span></span> <span data-ttu-id="396b0-227">Son nom anglais (États-Unis) est « clip multimédia ».</span><span class="sxs-lookup"><span data-stu-id="396b0-227">Its English (United States) name is "Media Clip".</span></span>

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a><span data-ttu-id="396b0-228">Créer des ressources de type chaîne pour Microsoft Management Console Snap-Ins</span><span class="sxs-lookup"><span data-stu-id="396b0-228">Create String Resources for Microsoft Management Console Snap-Ins</span></span>

<span data-ttu-id="396b0-229">Vous devez créer une ressource de type chaîne localisable pour chaque composant logiciel enfichable MMC (Microsoft Management Console) utilisé par votre application MUI.</span><span class="sxs-lookup"><span data-stu-id="396b0-229">You should create a localizable string resource for each Microsoft Management Console (MMC) snap-in used by your MUI application.</span></span> <span data-ttu-id="396b0-230">Comme un composant logiciel enfichable fait partie d’une console, il dispose d’une interface utilisateur et doit être globalisé pour fonctionner dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="396b0-230">Because a snap-in is part of a console, it has a user interface and must be globalized to operate in more than one language.</span></span>

<span data-ttu-id="396b0-231">La plupart du temps, les composants logiciels enfichables MMC génèrent les mêmes problèmes de globalisation et de localisation que l’application MUI elle-même.</span><span class="sxs-lookup"><span data-stu-id="396b0-231">For the most part, MMC snap-ins raise the same globalization and localization issues as the MUI application itself.</span></span> <span data-ttu-id="396b0-232">Un composant logiciel enfichable MMC doit refléter son nom dans le registre pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="396b0-232">An MMC snap-in must reflect its name in the registry for display.</span></span> <span data-ttu-id="396b0-233">L’entrée de registre doit inclure à la fois une référence indirecte à une ressource de chaîne localisable et une chaîne littérale pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="396b0-233">The registry entry should include both an indirect reference to a localizable string resource and a literal string for backward compatibility.</span></span>

<span data-ttu-id="396b0-234">Chaque composant logiciel enfichable MMC possède une clé de Registre sous HKEY \_ local \_ machine \\ Software \\ Microsoft \\ MMC \\ composants logiciels enfichables.</span><span class="sxs-lookup"><span data-stu-id="396b0-234">Each MMC snap-in has a registry key under HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MMC\\SnapIns.</span></span> <span data-ttu-id="396b0-235">Parmi les valeurs de cette clé, citons NameString, en spécifiant un nom explicite pour la compatibilité descendante, et NameStringIndirect, en spécifiant une référence indirecte à une ressource de type chaîne localisable.</span><span class="sxs-lookup"><span data-stu-id="396b0-235">Among the values for that key are NameString, specifying a human-readable name for backward compatibility, and NameStringIndirect, specifying an indirect reference to a localizable string resource.</span></span> <span data-ttu-id="396b0-236">Pour NameStringIndirect, vous devez fournir une référence de chaîne sous la forme « `@<path>,-resID` », représentant une ressource de chaîne localisable.</span><span class="sxs-lookup"><span data-stu-id="396b0-236">For NameStringIndirect, you should provide a string reference of the form "`@<path>,-resID`", representing a localizable string resource.</span></span>

<span data-ttu-id="396b0-237">Par exemple, vous pouvez définir le paramètre suivant pour Mymmc.dll, où 12345 est l’identificateur de la ressource de chaîne correspondante contenant le nom localisable du composant logiciel enfichable :</span><span class="sxs-lookup"><span data-stu-id="396b0-237">For example, you might make the following setting for Mymmc.dll, where 12345 is the identifier of the corresponding string resource containing the localizable name of the snap-in:</span></span>


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



<span data-ttu-id="396b0-238">Certains composants logiciels enfichables inscrivent d’autres valeurs de chaîne de registre que MMC ne lit pas à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="396b0-238">Some snap-ins register other registry string values that MMC does not read from the registry.</span></span> <span data-ttu-id="396b0-239">Pour plus d’informations sur l’utilisation de ces valeurs, consultez inscrire la console de gestion Microsoft Snap-In chaînes non lues dans le registre dans [localisation de chaînes redirigées](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="396b0-239">For more information about using these values, see Register Microsoft Management Console Snap-In Strings Not Read from the Registry in [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

## <a name="create-string-resources-for-a-windows-service"></a><span data-ttu-id="396b0-240">Créer des ressources de type chaîne pour un service Windows</span><span class="sxs-lookup"><span data-stu-id="396b0-240">Create String Resources for a Windows Service</span></span>

<span data-ttu-id="396b0-241">Bien qu’un service Windows ait généralement peu ou pas d’interface utilisateur, il doit afficher un nom compatible MUI et fournit généralement une description spécifique à une langue compatible MUI.</span><span class="sxs-lookup"><span data-stu-id="396b0-241">Although a Windows service typically has little or no user interface, it must display a MUI-compliant name and usually provides a MUI-compliant language-specific description.</span></span> <span data-ttu-id="396b0-242">La clé de Registre qui décrit un service Windows prend en charge uniquement la valeur DisplayName pour le nom du service et la valeur Description pour la description du service.</span><span class="sxs-lookup"><span data-stu-id="396b0-242">The registry key that describes a Windows service supports only the DisplayName value for the service name and the Description value for the service description.</span></span>

<span data-ttu-id="396b0-243">Les paramètres du service Windows sont créés à partir de l’application, comme décrit dans définir le nom complet et la description d’un service Windows à partir du Registre dans [localisation des chaînes redirigées](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="396b0-243">Settings for the Windows service are made from the application, as described in Set the Display Name and Description for a Windows Service from the Registry in [Locating Redirected Strings](locating-redirected-strings.md).</span></span> <span data-ttu-id="396b0-244">Si votre application ne définit pas les valeurs de Registre pour l’interface utilisateur du service, les valeurs du Registre restent définies sur l’anglais, même si l’interface utilisateur est dans une autre langue.</span><span class="sxs-lookup"><span data-stu-id="396b0-244">If your application does not set the registry values for the service user interface, values in the registry remain set to English, even if the user interface is in another language.</span></span>

## <a name="related-topics"></a><span data-ttu-id="396b0-245">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="396b0-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="396b0-246">Préparation des ressources</span><span class="sxs-lookup"><span data-stu-id="396b0-246">Preparing Resources</span></span>](preparing-resources.md)
</dt> <dt>

[<span data-ttu-id="396b0-247">Recherche de chaînes redirigées</span><span class="sxs-lookup"><span data-stu-id="396b0-247">Locating Redirected Strings</span></span>](locating-redirected-strings.md)
</dt> </dl>

 

 
