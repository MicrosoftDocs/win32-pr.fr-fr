---
description: 'Cette rubrique explique comment inscrire un programme dans le Registre Windows en tant qu’un des types de client suivants : navigateur, e-mail, lecture multimédia, messagerie instantanée ou machine virtuelle pour Java.'
title: Inscription de programmes avec des types de clients
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 71dd4e3192dc75821fd0a3e8c0d4742e1a8d571a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869626"
---
# <a name="registering-programs-with-client-types"></a><span data-ttu-id="ce525-103">Inscription de programmes avec des types de clients</span><span class="sxs-lookup"><span data-stu-id="ce525-103">Registering Programs with Client Types</span></span>

<span data-ttu-id="ce525-104">Cette rubrique explique comment inscrire un programme dans le Registre Windows en tant qu’un des types de client suivants : navigateur, e-mail, lecture multimédia, messagerie instantanée ou machine virtuelle pour Java.</span><span class="sxs-lookup"><span data-stu-id="ce525-104">This topic explains how to register a program in the Windows registry as one of the following client types: browser, email, media playback, instant messaging, or virtual machine for Java.</span></span>

> [!Note]  
> <span data-ttu-id="ce525-105">Ces informations s’appliquent aux systèmes d’exploitation suivants :</span><span class="sxs-lookup"><span data-stu-id="ce525-105">This information applies to the following operating systems:</span></span>
> 
> -   <span data-ttu-id="ce525-106">Windows 2000 Service Pack 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="ce525-106">Windows 2000 Service Pack 3 (SP3)</span></span>
> -   <span data-ttu-id="ce525-107">Windows 2000 Service Pack 4 (SP4)</span><span class="sxs-lookup"><span data-stu-id="ce525-107">Windows 2000 Service Pack 4 (SP4)</span></span>
> -   <span data-ttu-id="ce525-108">Windows XP Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="ce525-108">Windows XP Service Pack 1 (SP1)</span></span>
> -   <span data-ttu-id="ce525-109">Windows XP Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="ce525-109">Windows XP Service Pack 2 (SP2)</span></span>
> -   <span data-ttu-id="ce525-110">Windows XP Service Pack 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="ce525-110">Windows XP Service Pack 3 (SP3)</span></span>
> -   <span data-ttu-id="ce525-111">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ce525-111">Windows Server 2003</span></span>
> -   <span data-ttu-id="ce525-112">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce525-112">Windows Vista</span></span>
> -   <span data-ttu-id="ce525-113">Windows Vista Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="ce525-113">Windows Vista Service Pack 1 (SP1)</span></span>
> -   <span data-ttu-id="ce525-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ce525-114">Windows 8</span></span>

 

<span data-ttu-id="ce525-115">Cette rubrique comprend les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="ce525-115">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="ce525-116">Éléments d’inscription courants pour tous les types de clients</span><span class="sxs-lookup"><span data-stu-id="ce525-116">Common Registration Elements for All Client Types</span></span>](#common-registration-elements-for-all-client-types)
    -   [<span data-ttu-id="ce525-117">Sélection d’un nom canonique</span><span class="sxs-lookup"><span data-stu-id="ce525-117">Selecting a Canonical Name</span></span>](#selecting-a-canonical-name)
    -   [<span data-ttu-id="ce525-118">Inscription du nom complet d’un programme</span><span class="sxs-lookup"><span data-stu-id="ce525-118">Registering a Program's Display Name</span></span>](#registering-a-programs-display-name)
    -   [<span data-ttu-id="ce525-119">Inscription de l’icône d’un programme</span><span class="sxs-lookup"><span data-stu-id="ce525-119">Registering a Program's Icon</span></span>](#registering-a-programs-icon)
    -   [<span data-ttu-id="ce525-120">Inscription d’un verbe ouvert</span><span class="sxs-lookup"><span data-stu-id="ce525-120">Registering an Open Verb</span></span>](#registering-an-open-verb)
    -   [<span data-ttu-id="ce525-121">Inscription des informations d’installation</span><span class="sxs-lookup"><span data-stu-id="ce525-121">Registering Installation Information</span></span>](#registering-installation-information)
-   [<span data-ttu-id="ce525-122">Éléments d’inscription pour des types de client spécifiques</span><span class="sxs-lookup"><span data-stu-id="ce525-122">Registration Elements for Specific Client Types</span></span>](#registration-elements-for-specific-client-types)
    -   [<span data-ttu-id="ce525-123">Enregistrement du menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="ce525-123">Start Menu Registration</span></span>](#start-menu-registration)
    -   [<span data-ttu-id="ce525-124">Inscription du client de messagerie</span><span class="sxs-lookup"><span data-stu-id="ce525-124">Mail Client Registration</span></span>](#mail-client-registration)
-   [<span data-ttu-id="ce525-125">Compléter les exemples d’inscriptions</span><span class="sxs-lookup"><span data-stu-id="ce525-125">Complete Sample Registrations</span></span>](#complete-sample-registrations)
    -   [<span data-ttu-id="ce525-126">Exemple de navigateur</span><span class="sxs-lookup"><span data-stu-id="ce525-126">A Sample Browser</span></span>](#a-sample-browser)
    -   [<span data-ttu-id="ce525-127">Exemple de navigateur de messagerie</span><span class="sxs-lookup"><span data-stu-id="ce525-127">A Sample Mail Browser</span></span>](#a-sample-mail-browser)
    -   [<span data-ttu-id="ce525-128">Exemple de lecteur multimédia</span><span class="sxs-lookup"><span data-stu-id="ce525-128">A Sample Media Player</span></span>](#a-sample-media-player)
    -   [<span data-ttu-id="ce525-129">Exemple de programme Instant Messenger</span><span class="sxs-lookup"><span data-stu-id="ce525-129">A Sample Instant Messenger Program</span></span>](#a-sample-instant-messenger-program)
    -   [<span data-ttu-id="ce525-130">Exemple de machine virtuelle Java</span><span class="sxs-lookup"><span data-stu-id="ce525-130">A Sample Virtual Machine for Java</span></span>](#a-sample-virtual-machine-for-java)
-   [<span data-ttu-id="ce525-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ce525-131">Related topics</span></span>](#related-topics)

<span data-ttu-id="ce525-132">Cette rubrique étend la documentation existante sur l’inscription d’un programme en tant que type de client particulier.</span><span class="sxs-lookup"><span data-stu-id="ce525-132">This topic extends existing documentation about registering a program as a particular client type.</span></span> <span data-ttu-id="ce525-133">Pour obtenir des liens vers cette documentation, consultez la section Rubriques connexes.</span><span class="sxs-lookup"><span data-stu-id="ce525-133">For links to that documentation, see the Related Topics section.</span></span>

## <a name="common-registration-elements-for-all-client-types"></a><span data-ttu-id="ce525-134">Éléments d’inscription courants pour tous les types de clients</span><span class="sxs-lookup"><span data-stu-id="ce525-134">Common Registration Elements for All Client Types</span></span>

<span data-ttu-id="ce525-135">Lors de l’inscription d’un programme en tant que type de client, la plupart des entrées de Registre sont les mêmes, quel que soit le type de client.</span><span class="sxs-lookup"><span data-stu-id="ce525-135">When registering a program as a client type, most of the registry entries are the same regardless of the client type.</span></span> <span data-ttu-id="ce525-136">Certaines entrées du Registre, toutefois, sont spécifiques au type de client et sont indiquées dans la section [éléments d’inscription pour des types de client spécifiques](#registration-elements-for-specific-client-types) .</span><span class="sxs-lookup"><span data-stu-id="ce525-136">Some registry entries, however, are specific to the client type and these are noted in the [Registration Elements for Specific Client Types](#registration-elements-for-specific-client-types) section.</span></span>

<span data-ttu-id="ce525-137">Cette section aborde les sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="ce525-137">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="ce525-138">Sélection d’un nom canonique</span><span class="sxs-lookup"><span data-stu-id="ce525-138">Selecting a Canonical Name</span></span>](#selecting-a-canonical-name)
-   [<span data-ttu-id="ce525-139">Inscription du nom complet d’un programme</span><span class="sxs-lookup"><span data-stu-id="ce525-139">Registering a Program's Display Name</span></span>](#registering-a-programs-display-name)
-   [<span data-ttu-id="ce525-140">Inscription de l’icône d’un programme</span><span class="sxs-lookup"><span data-stu-id="ce525-140">Registering a Program's Icon</span></span>](#registering-a-programs-icon)
-   [<span data-ttu-id="ce525-141">Inscription d’un verbe ouvert</span><span class="sxs-lookup"><span data-stu-id="ce525-141">Registering an Open Verb</span></span>](#registering-an-open-verb)
-   [<span data-ttu-id="ce525-142">Inscription des informations d’installation</span><span class="sxs-lookup"><span data-stu-id="ce525-142">Registering Installation Information</span></span>](#registering-installation-information)

> [!Note]  
> <span data-ttu-id="ce525-143">Les noms de sous-clés donnés en italiques dans cette rubrique sont des espaces réservés pour les noms de sous-clés définis par l’utilisateur ou un ensemble de valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="ce525-143">Subkey names given in italics throughout this topic are placeholders for user-defined subkey names or a set of possible values.</span></span> <span data-ttu-id="ce525-144">Des exemples complets avec des exemples de noms en place sont fournis dans la section [inscriptions des exemples complets](#complete-sample-registrations) .</span><span class="sxs-lookup"><span data-stu-id="ce525-144">Full examples with example names in place are provided in the [Complete Sample Registrations](#complete-sample-registrations) section.</span></span>

 

<span data-ttu-id="ce525-145">Toutes les informations d’inscription de type client sont stockées sous la sous-clé suivante :</span><span class="sxs-lookup"><span data-stu-id="ce525-145">All client type registration information is stored under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

<span data-ttu-id="ce525-146">*ClientTypeName* est l’un des noms de sous-clés suivants :</span><span class="sxs-lookup"><span data-stu-id="ce525-146">*ClientTypeName* is one of the following subkey names:</span></span>

-   <span data-ttu-id="ce525-147">StartMenuInternet (pour les navigateurs)</span><span class="sxs-lookup"><span data-stu-id="ce525-147">StartMenuInternet (for browsers)</span></span>
-   <span data-ttu-id="ce525-148">Courrier électronique (pour courrier électronique)</span><span class="sxs-lookup"><span data-stu-id="ce525-148">Mail (for email)</span></span>
-   <span data-ttu-id="ce525-149">Média (pour la lecture du média)</span><span class="sxs-lookup"><span data-stu-id="ce525-149">Media (for media playback)</span></span>
-   <span data-ttu-id="ce525-150">MESSAGERIE instantanée (pour la messagerie instantanée)</span><span class="sxs-lookup"><span data-stu-id="ce525-150">IM (for instant messaging)</span></span>
-   <span data-ttu-id="ce525-151">JavaVM (pour machine virtuelle Java)</span><span class="sxs-lookup"><span data-stu-id="ce525-151">JavaVM (for virtual machine for Java)</span></span>

<span data-ttu-id="ce525-152">Tout au long de cette rubrique, vous allez noter des références à un programme informatique fictif nommé « lit View » par Litware Inc., avec un fichier exécutable nommé Litview.exe.</span><span class="sxs-lookup"><span data-stu-id="ce525-152">Throughout this topic, you will note references to a fictional computer program named "Lit View" by Litware Inc., with an executable file named Litview.exe.</span></span> <span data-ttu-id="ce525-153">Ce programme hypothétique est utilisé de manière interchangeable comme une messagerie instantanée, un navigateur ou un autre type de programme client si nécessaire à des fins d’illustration.</span><span class="sxs-lookup"><span data-stu-id="ce525-153">This hypothetical program is used interchangeably as an instant messenger, a browser, or another type of client program as needed for illustrative purposes.</span></span>

### <a name="selecting-a-canonical-name"></a><span data-ttu-id="ce525-154">Sélection d’un nom canonique</span><span class="sxs-lookup"><span data-stu-id="ce525-154">Selecting a Canonical Name</span></span>

<span data-ttu-id="ce525-155">Le fournisseur doit choisir un *nom canonique* pour le programme.</span><span class="sxs-lookup"><span data-stu-id="ce525-155">The vendor must choose a *canonical name* for the program.</span></span> <span data-ttu-id="ce525-156">Le nom canonique n’est jamais présenté à l’utilisateur, il n’est donc pas nécessaire de le localiser.</span><span class="sxs-lookup"><span data-stu-id="ce525-156">The canonical name is never shown to the user, so it does not need to be localized.</span></span> <span data-ttu-id="ce525-157">Son seul objectif est de fournir une chaîne unique qui peut être utilisée pour identifier le programme.</span><span class="sxs-lookup"><span data-stu-id="ce525-157">Its only purpose is to provide a unique string that can be used to identify the program.</span></span> <span data-ttu-id="ce525-158">Il est généralement identique au nom anglais du programme, mais il s’agit simplement d’une convention.</span><span class="sxs-lookup"><span data-stu-id="ce525-158">It is typically the same as the English name of the program, but this is merely a convention.</span></span>

<span data-ttu-id="ce525-159">Pour les types de clients autres que les navigateurs, le nom canonique peut être n’importe quelle chaîne.</span><span class="sxs-lookup"><span data-stu-id="ce525-159">For client types other than browsers, the canonical name can be any string.</span></span> <span data-ttu-id="ce525-160">Choisissez un nom unique, qui n’est pas susceptible d’être utilisé par un autre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ce525-160">Choose a unique name, one that is not likely to be used by another vendor.</span></span>

<span data-ttu-id="ce525-161">Pour les clients de navigateur, le nom canonique doit être le nom, y compris l’extension, du fichier exécutable associé ; par exemple, « Litview.exe ».</span><span class="sxs-lookup"><span data-stu-id="ce525-161">For browser clients, the canonical name must be the name—including the extension—of the associated executable; for instance, "Litview.exe".</span></span>

<span data-ttu-id="ce525-162">Voici quelques exemples de noms canoniques.</span><span class="sxs-lookup"><span data-stu-id="ce525-162">Here are some examples of canonical names.</span></span>

-   <span data-ttu-id="ce525-163">Iexplore.exe (navigateur)</span><span class="sxs-lookup"><span data-stu-id="ce525-163">Iexplore.exe (browser)</span></span>
-   <span data-ttu-id="ce525-164">Messagerie Windows (e-mail)</span><span class="sxs-lookup"><span data-stu-id="ce525-164">Windows Mail (email)</span></span>
-   <span data-ttu-id="ce525-165">Lecteur Windows Media (média)</span><span class="sxs-lookup"><span data-stu-id="ce525-165">Windows Media Player (media)</span></span>
-   <span data-ttu-id="ce525-166">Windows Messenger (messagerie instantanée)</span><span class="sxs-lookup"><span data-stu-id="ce525-166">Windows Messenger (instant messaging)</span></span>

<span data-ttu-id="ce525-167">Inscrivez le nom canonique en créant une sous-clé comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="ce525-167">Register the canonical name by creating a subkey as shown here.</span></span> <span data-ttu-id="ce525-168">Le nom de la sous-clé est le nom canonique.</span><span class="sxs-lookup"><span data-stu-id="ce525-168">The name of the subkey is the canonical name.</span></span> <span data-ttu-id="ce525-169">Toutes les informations relatives à l’inscription de ce programme se trouvent sous cette sous-clé.</span><span class="sxs-lookup"><span data-stu-id="ce525-169">All information relating to that program's registration will exist under this subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a><span data-ttu-id="ce525-170">Inscription du nom complet d’un programme</span><span class="sxs-lookup"><span data-stu-id="ce525-170">Registering a Program's Display Name</span></span>

<span data-ttu-id="ce525-171">L’étape suivante de l’inscription consiste à spécifier le nom d’affichage du programme.</span><span class="sxs-lookup"><span data-stu-id="ce525-171">The next step in registration is to specify the program's display name.</span></span> <span data-ttu-id="ce525-172">Elle est fournie sous la forme d’une valeur sous la clé de nom canonique comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="ce525-172">It is given as a value under the canonical name key as shown here.</span></span> <span data-ttu-id="ce525-173">Notez à nouveau que *CanonicalName* et *ClientTypeName* ne sont pas les noms réels des clés, mais uniquement des espaces réservés pour les véritables noms, tels que *lit View*.</span><span class="sxs-lookup"><span data-stu-id="ce525-173">Note again that *CanonicalName* and *ClientTypeName* are not the actual names of the keys, but only placeholders for the true names, such as *Lit View*.</span></span>

> [!Note]  
> <span data-ttu-id="ce525-174">À compter de Windows 8, le nom utilisé pour l’inscription pour les [paramètres par défaut de l’option définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)](cpl-setprogramaccess.md) et pour les [programmes par défaut](default-programs.md) doit correspondre pour que les modifications de SPAD déclenchent les inscriptions des programmes par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce525-174">As of Windows 8, the name used to register for [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) and for [Default Programs](default-programs.md) should match in order for SPAD changes to trigger Default Programs registrations.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

<span data-ttu-id="ce525-175">La valeur **LocalizedString** est une \_ chaîne sz reg et se compose d’un signe « at » (@), du chemin d’accès complet à un fichier. dll ou. exe, d’une virgule, d’un signe moins et d’un entier décimal.</span><span class="sxs-lookup"><span data-stu-id="ce525-175">The **LocalizedString** value is a REG\_SZ string and consists of an "at" sign (@), the full path to a .dll or .exe file, a comma, a minus sign, and a decimal integer.</span></span> <span data-ttu-id="ce525-176">L’entier décimal est l’ID d’une ressource de type chaîne, contenue dans le fichier. dll ou. exe, dont la valeur doit être affichée à l’utilisateur en tant que nom de ce client.</span><span class="sxs-lookup"><span data-stu-id="ce525-176">The decimal integer is the ID of a string resource—contained within the .dll or .exe file—whose value is to be displayed to the user as the name of this client.</span></span> <span data-ttu-id="ce525-177">Notez que le chemin d’accès du fichier ne requiert pas de guillemets, même s’il contient des espaces.</span><span class="sxs-lookup"><span data-stu-id="ce525-177">Note that the file path does not require quotation marks, even if it contains spaces.</span></span>

<span data-ttu-id="ce525-178">L’inscription de la chaîne de nom complet de cette manière permet d’utiliser la même inscription pour plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="ce525-178">Registering the display name string in this manner allows the same registration to be used for multiple languages.</span></span> <span data-ttu-id="ce525-179">Chaque installation de langue fournit un fichier de ressources différent avec le nom complet stocké au même ID de ressource.</span><span class="sxs-lookup"><span data-stu-id="ce525-179">Each language installation provides a different resource file with the display name stored at the same resource ID.</span></span>

<span data-ttu-id="ce525-180">L’exemple suivant illustre l’inscription d’un programme de messagerie instantanée éclairé.</span><span class="sxs-lookup"><span data-stu-id="ce525-180">The following example shows the registration for a fictional Lit View instant messaging program.</span></span> <span data-ttu-id="ce525-181">Étant donné qu’il s’agit d’un programme de messagerie instantanée, la sous-clé *CanonicalName* (dans ce cas, *lit la vue*) est stockée sous la sous-clé **im** .</span><span class="sxs-lookup"><span data-stu-id="ce525-181">Because it is an instant messaging program, the *CanonicalName* subkey (in this case *Lit View*) is stored under the **IM** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

<span data-ttu-id="ce525-182">Notez l’utilisation de l’entrée (par défaut) comme déclaration secondaire du nom complet du client.</span><span class="sxs-lookup"><span data-stu-id="ce525-182">Note the use of the (Default) entry as a secondary declaration of the client's display name.</span></span> <span data-ttu-id="ce525-183">Si le **LocalizedString** n’est pas présent, la valeur (par défaut) est utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="ce525-183">If the **LocalizedString** is not present, the (Default) value is used instead.</span></span> <span data-ttu-id="ce525-184">Cela fonctionne avec tous les types de clients (navigateurs Internet, navigateurs de messagerie, messagerie instantanée et lecteurs multimédias).</span><span class="sxs-lookup"><span data-stu-id="ce525-184">This works with all client types (Internet browsers, email browsers, instant messengers, and media players).</span></span> <span data-ttu-id="ce525-185">Pour assurer la compatibilité descendante avec la [disposition du Registre du client Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), les programmes de messagerie doivent définir la valeur (par défaut) de la sous-clé *CanonicalName* sur le nom d’affichage du client dans la langue actuellement installée.</span><span class="sxs-lookup"><span data-stu-id="ce525-185">For backward compatibility with the [Internet Explorer Client Registry Layout](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), email programs should set the (Default) value of the *CanonicalName* subkey to the client's display name in the currently installed language.</span></span>

### <a name="registering-a-programs-icon"></a><span data-ttu-id="ce525-186">Inscription de l’icône d’un programme</span><span class="sxs-lookup"><span data-stu-id="ce525-186">Registering a Program's Icon</span></span>

> [!Note]  
> <span data-ttu-id="ce525-187">Cette section ne s’applique pas à Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ce525-187">This section does not apply to Windows 2000.</span></span>

 

<span data-ttu-id="ce525-188">Par défaut, la section supérieure du menu **Démarrer** de Windows XP et Windows Vista contient des icônes **Internet** et de **messagerie** .</span><span class="sxs-lookup"><span data-stu-id="ce525-188">By default, the upper section of the Windows XP and Windows Vista **Start** menu contains **Internet** and **E-mail** icons.</span></span> <span data-ttu-id="ce525-189">Ces icônes ne sont pas présentes dans Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ce525-189">These icons are not present in Windows 7 and later.</span></span> <span data-ttu-id="ce525-190">Pour les clients de messagerie et de navigateur, lorsqu’un programme est attribué par défaut à son type de client, l’icône inscrite de ce programme s’affiche pour ces entrées de menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="ce525-190">For browser and email clients, when a program is assigned as the default for their client type, that program's registered icon is displayed for those **Start** menu entries.</span></span>

<span data-ttu-id="ce525-191">L’inscription de l’icône d’un programme est obligatoire pour les clients de messagerie et de navigateur.</span><span class="sxs-lookup"><span data-stu-id="ce525-191">Registering a program's icon is mandatory for browser and email clients.</span></span> <span data-ttu-id="ce525-192">L’inscription d’une icône pour les types de client lecture du média, messagerie instantanée ou machine virtuelle pour Java est facultative, et les icônes inscrites pour ces types de clients ne sont pas actuellement utilisées par Windows et ne sont pas affichées dans la section supérieure des menus **Démarrer** de Windows XP ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ce525-192">Registering an icon for the media playback, instant messaging, or virtual machine for Java client types is optional, and registered icons for those client types are not currently used by Windows and are not displayed in the upper section of the Windows XP or Windows Vista **Start** menus.</span></span>

<span data-ttu-id="ce525-193">Pour inscrire une icône pour un programme client, ajoutez une sous-clé **DefaultIcon** avec une valeur par défaut, comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="ce525-193">To register an icon for a client program, add a **DefaultIcon** subkey with a default value as shown here.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               DefaultIcon
                  (Default) = FilePath,IconIndex
```

<span data-ttu-id="ce525-194">La valeur **filePath** est le chemin d’accès complet au fichier qui contient l’icône.</span><span class="sxs-lookup"><span data-stu-id="ce525-194">The **FilePath** value is the full path to the file that contains the icon.</span></span> <span data-ttu-id="ce525-195">Ce chemin d’accès ne requiert pas de guillemets, même s’il contient des espaces.</span><span class="sxs-lookup"><span data-stu-id="ce525-195">This path does not require quotation marks, even if it contains spaces.</span></span>

<span data-ttu-id="ce525-196">La valeur **IndexIcône** est interprétée comme suit :</span><span class="sxs-lookup"><span data-stu-id="ce525-196">The **IconIndex** value is interpreted as follows:</span></span>

-   <span data-ttu-id="ce525-197">Si **IndexIcône** est un nombre positif, le nombre est utilisé comme index du tableau de *base zéro* des icônes stockées dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="ce525-197">If **IconIndex** is a positive number, the number is used as the index of the *zero-based* array of icons stored in the file.</span></span> <span data-ttu-id="ce525-198">Par exemple, si **IndexIcône** est 1, la deuxième icône est chargée à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="ce525-198">For example, if **IconIndex** is 1, the second icon is loaded from the file.</span></span>
-   <span data-ttu-id="ce525-199">Si **IndexIcône** est un nombre négatif, la valeur absolue de **IndexIcône** est utilisée comme identificateur de ressource (plutôt que l’index) pour l’icône.</span><span class="sxs-lookup"><span data-stu-id="ce525-199">If **IconIndex** is a negative number, the absolute value of **IconIndex** is used as the resource identifier (rather than the index) for the icon.</span></span> <span data-ttu-id="ce525-200">Par exemple, si **IndexIcône** est-3, l’icône dont l’identificateur de ressource est 3 est chargée à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="ce525-200">For example, if **IconIndex** is -3, the icon whose resource identifier is 3 is loaded from the file.</span></span>

<span data-ttu-id="ce525-201">L’exemple suivant illustre l’inscription d’un navigateur d’affichage lit hypothétique.</span><span class="sxs-lookup"><span data-stu-id="ce525-201">The following example shows the registration of a hypothetical Lit View browser.</span></span> <span data-ttu-id="ce525-202">La deuxième icône stockée dans le fichier Litview.exe est utilisée comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce525-202">The second icon stored in the Litview.exe file is used as the default.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a><span data-ttu-id="ce525-203">Inscription d’un verbe ouvert</span><span class="sxs-lookup"><span data-stu-id="ce525-203">Registering an Open Verb</span></span>

> [!Note]  
> <span data-ttu-id="ce525-204">Cette section ne s’applique pas à Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ce525-204">This section does not apply to Windows 2000.</span></span> <span data-ttu-id="ce525-205">L’étape suivante est nécessaire uniquement pour les clients de messagerie et de navigateur.</span><span class="sxs-lookup"><span data-stu-id="ce525-205">The following step is necessary only for browser and email clients.</span></span>

 

<span data-ttu-id="ce525-206">Supposons qu’un utilisateur a sélectionné votre programme comme programme Internet ou de messagerie par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce525-206">Assume that a user has selected your program as the default Internet or email program.</span></span> <span data-ttu-id="ce525-207">Cet utilisateur clique sur l’icône **Internet** ou **courrier électronique** dans le menu **Démarrer** de Windows XP ou Windows Vista pour ouvrir le programme.</span><span class="sxs-lookup"><span data-stu-id="ce525-207">That user clicks the **Internet** or **E-mail** icon in the Windows XP or Windows Vista **Start** menu to open the program.</span></span> <span data-ttu-id="ce525-208">À ce stade, la ligne de commande enregistrée comme indiqué ici est exécutée.</span><span class="sxs-lookup"><span data-stu-id="ce525-208">At that point, the command line registered as shown here is executed.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               shell
                  open
                     command
                        (Default) = command line
```

<span data-ttu-id="ce525-209">La ligne de commande doit spécifier un chemin d’accès absolu complet au fichier, suivi d’options de ligne de commande facultatives.</span><span class="sxs-lookup"><span data-stu-id="ce525-209">The command line must specify a fully qualified absolute path to the file, followed by optional command-line options.</span></span> <span data-ttu-id="ce525-210">Si le type d’entrée est REG \_ expand \_ SZ, les variables d’environnement peuvent être utilisées dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="ce525-210">If the entry type is REG\_EXPAND\_SZ, environment variables can be used in the path.</span></span> <span data-ttu-id="ce525-211">Utilisez des guillemets pour vous assurer que les espaces dans la ligne de commande ne sont pas interprétés de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="ce525-211">Use quotation marks appropriately to ensure that spaces in the command line are not misinterpreted.</span></span> <span data-ttu-id="ce525-212">La ligne de commande doit exécuter le programme avec les valeurs par défaut appropriées.</span><span class="sxs-lookup"><span data-stu-id="ce525-212">The command line should execute the program with appropriate defaults.</span></span> <span data-ttu-id="ce525-213">Les navigateurs sont généralement par défaut sur la page d’hébergement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce525-213">Browsers generally default to the user's home page.</span></span> <span data-ttu-id="ce525-214">Les programmes de messagerie ouvrent généralement la **boîte de réception** de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce525-214">Email programs generally open the user's **Inbox**.</span></span>

<span data-ttu-id="ce525-215">L’exemple suivant illustre l’inscription d’un `open` verbe pour un Explorateur d’affichages hypothétique.</span><span class="sxs-lookup"><span data-stu-id="ce525-215">The following example shows the registration of an `open` verb for a hypothetical Lit View browser.</span></span> <span data-ttu-id="ce525-216">Elle ne spécifie aucune option de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="ce525-216">It specifies no command-line options.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\Litview.exe"
```

<span data-ttu-id="ce525-217">Notez que, dans cette valeur, des guillemets sont placés autour du chemin d’accès, car il contient des espaces incorporés.</span><span class="sxs-lookup"><span data-stu-id="ce525-217">Note that in this value, quotation marks are placed around the path because it contains embedded spaces.</span></span> <span data-ttu-id="ce525-218">Si vous omettez ces guillemets, la ligne de commande risque d’être interprétée à tort.</span><span class="sxs-lookup"><span data-stu-id="ce525-218">Omitting these quotation marks could cause the command line to be misinterpreted.</span></span>

### <a name="registering-installation-information"></a><span data-ttu-id="ce525-219">Inscription des informations d’installation</span><span class="sxs-lookup"><span data-stu-id="ce525-219">Registering Installation Information</span></span>

> [!Note]  
> <span data-ttu-id="ce525-220">Cette section ne s’applique pas à Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ce525-220">This section does not apply to Windows Server 2003.</span></span>

 

-   [<span data-ttu-id="ce525-221">Commande de réinstallation</span><span class="sxs-lookup"><span data-stu-id="ce525-221">The Reinstall Command</span></span>](#the-reinstall-command)
-   [<span data-ttu-id="ce525-222">Commande masquer les icônes</span><span class="sxs-lookup"><span data-stu-id="ce525-222">The Hide Icons Command</span></span>](#the-hide-icons-command)
-   [<span data-ttu-id="ce525-223">Commande Afficher les icônes</span><span class="sxs-lookup"><span data-stu-id="ce525-223">The Show Icons Command</span></span>](#the-show-icons-command)
-   [<span data-ttu-id="ce525-224">Configuration du programme de groupe</span><span class="sxs-lookup"><span data-stu-id="ce525-224">Group Program Configuration</span></span>](#group-program-configuration)
-   [<span data-ttu-id="ce525-225">Exemple d’inscription de navigateur</span><span class="sxs-lookup"><span data-stu-id="ce525-225">Browser Registration Example</span></span>](#browser-registration-example)

<span data-ttu-id="ce525-226">La fonctionnalité par laquelle l’utilisateur sélectionne les programmes par défaut par ordinateur est nommée et accessible comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ce525-226">The feature by which the user selects per-machine default programs is named and accessed as shown in the following table.</span></span> <span data-ttu-id="ce525-227">(Windows Vista a introduit une nouvelle fonctionnalité, **défini vos programmes par défaut**, par lequel un utilisateur peut définir des valeurs par défaut par utilisateur.)</span><span class="sxs-lookup"><span data-stu-id="ce525-227">(Windows Vista introduced a new feature, **Set your default programs**, by which a user can set per-user defaults.)</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce525-228">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ce525-228">Operating System</span></span></th>
<th><span data-ttu-id="ce525-229">Intitulé</span><span class="sxs-lookup"><span data-stu-id="ce525-229">Title</span></span></th>
<th><span data-ttu-id="ce525-230">Emplacement d’accès</span><span class="sxs-lookup"><span data-stu-id="ce525-230">Access Location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce525-231">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ce525-231">Windows 7</span></span></td>
<td><span data-ttu-id="ce525-232">Définir les paramètres par défaut de l’accès aux programmes et de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="ce525-232">Set Program Access and Computer Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="ce525-233">Option <strong>programmes par défaut</strong> du menu <strong>Démarrer</strong></span><span class="sxs-lookup"><span data-stu-id="ce525-233"><strong>Start</strong> menu <strong>Default Programs</strong> option</span></span></li>
<li><span data-ttu-id="ce525-234"><strong>Programmes par défaut</strong> Élément du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="ce525-234"><strong>Default Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce525-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce525-235">Windows Vista</span></span></td>
<td><span data-ttu-id="ce525-236">Définir les paramètres par défaut de l’accès aux programmes et de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="ce525-236">Set Program Access and Computer Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="ce525-237">Option <strong>programmes par défaut</strong> du menu <strong>Démarrer</strong></span><span class="sxs-lookup"><span data-stu-id="ce525-237"><strong>Start</strong> menu <strong>Default Programs</strong> option</span></span></li>
<li><span data-ttu-id="ce525-238"><strong>Programmes par défaut</strong> Élément du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="ce525-238"><strong>Default Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce525-239">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="ce525-239">Windows XP SP2</span></span></td>
<td><span data-ttu-id="ce525-240">Définir l’accès aux programmes et les valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="ce525-240">Set Program Access and Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="ce525-241">Menu <strong>Démarrer</strong></span><span class="sxs-lookup"><span data-stu-id="ce525-241"><strong>Start</strong> menu</span></span></li>
<li><span data-ttu-id="ce525-242"><strong>Ajout/suppression de programmes</strong> Élément du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="ce525-242"><strong>Add or Remove Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce525-243">Windows XP SP1</span><span class="sxs-lookup"><span data-stu-id="ce525-243">Windows XP SP1</span></span></td>
<td><span data-ttu-id="ce525-244">Configurer des programmes</span><span class="sxs-lookup"><span data-stu-id="ce525-244">Configure Programs</span></span></td>
<td><ul>
<li><span data-ttu-id="ce525-245"><strong>Ajout/suppression de programmes</strong> Élément du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="ce525-245"><strong>Add or Remove Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ce525-246">Par souci de simplicité, cette rubrique utilise le titre Windows 7 de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="ce525-246">For simplicity, this topic uses the Windows 7 title of the feature.</span></span> <span data-ttu-id="ce525-247">Toutes les versions de la fonctionnalité sont communément appelées SPAD.</span><span class="sxs-lookup"><span data-stu-id="ce525-247">All versions of the feature are popularly referred to as SPAD.</span></span>

> [!Note]  
> <span data-ttu-id="ce525-248">Si vous exécutez Windows 2000 ou Windows XP, vous devez disposer au moins de Windows 2000 SP3 ou Windows XP SP1 pour voir la page **configurer les paramètres par défaut** .</span><span class="sxs-lookup"><span data-stu-id="ce525-248">If you are running Windows 2000 or Windows XP, you must have at least Windows 2000 SP3 or Windows XP SP1 installed to see the **Set Program Access and Defaults** page.</span></span> <span data-ttu-id="ce525-249">Dans Windows Vista et versions ultérieures, l’accès à la page **définir les paramètres par défaut de l’accès aux programmes et des ordinateurs** requiert des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="ce525-249">In Windows Vista and later, access to the **Set Program Access and Computer Defaults** page requires Administrator privileges.</span></span> <span data-ttu-id="ce525-250">Pour cette raison, les développeurs sont encouragés à s’inscrire pour l’élément définir votre panneau de configuration [programmes par défaut](default-programs.md) afin que n’importe quel utilisateur puisse gérer les valeurs par défaut de l’application.</span><span class="sxs-lookup"><span data-stu-id="ce525-250">For this reason, developers are encouraged to register for the [Set your default programs](default-programs.md) Control Panel item so that any user can manage application defaults.</span></span>

 

<span data-ttu-id="ce525-251">L’arborescence de Registre suivante affiche la variété des informations qui doivent être inscrites dans la clé **InstallInfo** du programme pour que le programme s’affiche sur la page **définir les paramètres par défaut de l’accès aux programmes et** de l’ordinateur en tant qu’option pour son type de client.</span><span class="sxs-lookup"><span data-stu-id="ce525-251">The following registry tree shows the variety of information that must be registered in the program's **InstallInfo** key in order for the program to appear on the **Set Program Access and Computer Defaults** page as an option for its client type.</span></span> <span data-ttu-id="ce525-252">Chacune de ces valeurs est décrite en détail dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="ce525-252">Each of these values is discussed in detail in the following sections.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  HideIconsCommand = command line
                  ReinstallCommand = command line
                  ShowIconsCommand = command line
                  IconsVisible = 1
```

<span data-ttu-id="ce525-253">La ligne de commande doit spécifier un chemin d’accès absolu complet au fichier, suivi d’options de ligne de commande facultatives.</span><span class="sxs-lookup"><span data-stu-id="ce525-253">The command line must specify a fully qualified absolute path to the file, followed by optional command-line options.</span></span> <span data-ttu-id="ce525-254">Utilisez des guillemets pour vous assurer que les espaces dans la ligne de commande ne sont pas interprétés de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="ce525-254">Use quotation marks appropriately to ensure that spaces in the command line are not misinterpreted.</span></span>

### <a name="the-reinstall-command"></a><span data-ttu-id="ce525-255">Commande de réinstallation</span><span class="sxs-lookup"><span data-stu-id="ce525-255">The Reinstall Command</span></span>

<span data-ttu-id="ce525-256">La ligne de commande de réinstallation déclarée dans la valeur ReinstallCommand est exécutée lorsque l’utilisateur utilise la page **définir les paramètres par défaut de l’accès aux programmes et des ordinateurs** pour sélectionner votre programme comme type de client par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce525-256">The reinstall command line declared in the ReinstallCommand value is executed when the user uses the **Set Program Access and Computer Defaults** page to select your program as the default for its client type.</span></span> <span data-ttu-id="ce525-257">Dans Windows Vista et versions ultérieures, l’accès à cette page nécessite un niveau de privilège d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="ce525-257">In Windows Vista and later, access to this page requires an Administrator privilege level.</span></span> <span data-ttu-id="ce525-258">Dans Windows 8, si vous avez inscrit votre application en utilisant le même nom pour **définir l’accès aux programmes et les paramètres par défaut** de l’ordinateur et des **programmes par défaut**, les valeurs par défaut spécifiées dans **programmes par défaut** pour cette application seront appliquées à l’utilisateur actuel, ainsi que l’exécution de la commande réinstaller.</span><span class="sxs-lookup"><span data-stu-id="ce525-258">In Windows 8, if you have registered your application using the same name for both **Set Program Access and Computer Defaults** and **Default Programs**, the defaults specified in **Default Programs** for that application will be applied for the current user as well as running the reinstall command.</span></span>

<span data-ttu-id="ce525-259">Le programme lancé par la ligne de commande de réinstallation doit associer l’application à l’ensemble complet de types de [fichiers](fa-intro.md) et de [protocoles](/previous-versions//aa767743(v=vs.85)) que l’application peut gérer.</span><span class="sxs-lookup"><span data-stu-id="ce525-259">The program launched by the reinstall command line must associate the application with the complete set of [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types the application can handle.</span></span> <span data-ttu-id="ce525-260">Toutes les applications doivent mettre en place une fonctionnalité de gestionnaire dans la commande de réinstallation.</span><span class="sxs-lookup"><span data-stu-id="ce525-260">All applications must establish handler capability in the reinstall command.</span></span> <span data-ttu-id="ce525-261">Les applications peuvent utiliser la commande réinstaller pour inscrire la fonctionnalité et éventuellement établir l’État par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce525-261">Applications can use the reinstall command to register capability as well as optionally establish default status.</span></span> <span data-ttu-id="ce525-262">Quand une application choisit d’implémenter les fonctionnalités et l’état du gestionnaire par défaut dans la commande de réinstallation, elle doit également rétablir les liens ou les raccourcis visibles souhaités.</span><span class="sxs-lookup"><span data-stu-id="ce525-262">When an application chooses to implement both capability and default handler status in the reinstall command, it should also reinstate any visible links or shortcuts desired.</span></span> <span data-ttu-id="ce525-263">Les points d’entrée visibles pour la plupart des applications sont répertoriés dans [la commande masquer les icônes](#the-hide-icons-command).</span><span class="sxs-lookup"><span data-stu-id="ce525-263">The visible entry points most applications choose are listed in [The Hide Icons Command](#the-hide-icons-command).</span></span>

> [!Note]  
> <span data-ttu-id="ce525-264">Il est vivement recommandé que les applications implémentent la fonctionnalité de gestion dans la commande de réinstallation.</span><span class="sxs-lookup"><span data-stu-id="ce525-264">It is highly recommended that applications implement handling capability in the reinstall command.</span></span>

 

<span data-ttu-id="ce525-265">Une fois le processus de réinstallation terminé, le programme lancé par la ligne de commande de réinstallation doit s’arrêter.</span><span class="sxs-lookup"><span data-stu-id="ce525-265">Once the reinstall process is complete, the program launched by the reinstall command line should exit.</span></span> <span data-ttu-id="ce525-266">Il ne doit pas lancer le programme correspondant. il doit simplement enregistrer les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce525-266">It should not launch the corresponding program; it should merely register defaults.</span></span> <span data-ttu-id="ce525-267">Par exemple, la commande de réinstallation d’un navigateur ne doit pas ouvrir la page d’hébergement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce525-267">For example, the reinstall command for a browser should not open the user's home page.</span></span>

> [!Note]  
> <span data-ttu-id="ce525-268">Pour les clients de messagerie et de navigateur sous Windows XP et Windows Vista, les applications qui choisissent d’établir la capacité de gestion et l’État par défaut dans la commande de réinstallation doivent s’inscrire à l’icône correspondante en haut du menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="ce525-268">For browser and email clients in Windows XP and Windows Vista, applications that choose to establish both handling capability and default status in the reinstall command should register for the corresponding icon at the top of the Start menu.</span></span> <span data-ttu-id="ce525-269">Pour plus d’informations, consultez [enregistrement du menu Démarrer](#start-menu-registration) .</span><span class="sxs-lookup"><span data-stu-id="ce525-269">See [Start Menu Registration](#start-menu-registration) for additional information.</span></span>

 

### <a name="the-hide-icons-command"></a><span data-ttu-id="ce525-270">Commande masquer les icônes</span><span class="sxs-lookup"><span data-stu-id="ce525-270">The Hide Icons Command</span></span>

<span data-ttu-id="ce525-271">La ligne de commande déclarée dans la valeur HideIconsCommand est exécutée lorsque l’utilisateur désactive l’option **activer l’accès à ce programme** dans la page **définir les paramètres par défaut de l’accès aux programmes et** de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ce525-271">The command line declared in the HideIconsCommand value is executed when the user clears the **Enable access to this program** box in the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="ce525-272">Cette ligne de commande doit masquer tous les points d’accès de votre programme qui sont visibles dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce525-272">This command line must hide all of your program's access points that are visible in the user interface.</span></span> <span data-ttu-id="ce525-273">Les instructions spécifiques sont de supprimer des raccourcis et des icônes à partir des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="ce525-273">The specific guidelines are to remove shortcuts and icons from the following locations:</span></span>

-   <span data-ttu-id="ce525-274">Icônes de bureau</span><span class="sxs-lookup"><span data-stu-id="ce525-274">Desktop icons</span></span>
-   <span data-ttu-id="ce525-275">Liens du menu Démarrer, y compris le groupe **démarrage**</span><span class="sxs-lookup"><span data-stu-id="ce525-275">Start menu links, including the **Startup** group</span></span>
-   <span data-ttu-id="ce525-276">Liens vers la barre de lancement rapide</span><span class="sxs-lookup"><span data-stu-id="ce525-276">Quick Launch bar links</span></span>
-   <span data-ttu-id="ce525-277">Zone Notifications</span><span class="sxs-lookup"><span data-stu-id="ce525-277">Notification area</span></span>
-   <span data-ttu-id="ce525-278">Menus contextuels</span><span class="sxs-lookup"><span data-stu-id="ce525-278">Shortcut menus</span></span>
-   <span data-ttu-id="ce525-279">Bande de tâches du dossier</span><span class="sxs-lookup"><span data-stu-id="ce525-279">Folder task band</span></span>

<span data-ttu-id="ce525-280">Cette ligne de commande doit également empêcher les appels automatiques du programme, tels que ceux spécifiés dans la clé de Registre **Run** .</span><span class="sxs-lookup"><span data-stu-id="ce525-280">This command line must also prevent automatic invocations of the program, such as those specified in the **Run** registry key.</span></span> <span data-ttu-id="ce525-281">Les fournisseurs sont encouragés à implémenter ces instructions dans le rappel d’accès de masquage de l’application.</span><span class="sxs-lookup"><span data-stu-id="ce525-281">Vendors are encouraged to implement these guidelines in the application's Hide Access callback.</span></span>

<span data-ttu-id="ce525-282">Vous n’avez pas besoin d’abandonner l’inscription (fonctionnalité d’application) des types de fichiers lorsque les icônes sont masquées.</span><span class="sxs-lookup"><span data-stu-id="ce525-282">You do not need to relinquish registration (application capability) of file types when icons are hidden.</span></span> <span data-ttu-id="ce525-283">Vous n’avez pas non plus besoin de renoncer à l’État par défaut de l’application pour les types de fichiers et de protocoles.</span><span class="sxs-lookup"><span data-stu-id="ce525-283">You also do not need to relinquish the application's default status for file and protocol types.</span></span> <span data-ttu-id="ce525-284">Cela peut entraîner une mauvaise expérience utilisateur lorsque ces types sont rencontrés dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce525-284">Doing so can lead to a bad user experience when these types are encountered in the UI.</span></span>

<span data-ttu-id="ce525-285">Après avoir masqué correctement les icônes, vous devez mettre à jour la valeur de Registre IconsVisible sur 0 comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="ce525-285">After successfully hiding icons, you must update the IconsVisible registry value to 0 as shown:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

<span data-ttu-id="ce525-286">L’entrée IconsVisible est de type **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="ce525-286">The IconsVisible entry is of type **REG\_DWORD**.</span></span>

### <a name="an-alternate-hide-icons-method-in-spad"></a><span data-ttu-id="ce525-287">Une autre méthode masquer les icônes dans SPAD</span><span class="sxs-lookup"><span data-stu-id="ce525-287">An Alternate Hide Icons Method in SPAD</span></span>

<span data-ttu-id="ce525-288">Pour certaines applications héritées, une implémentation complète de l’accès masqué peut ne pas être pratique.</span><span class="sxs-lookup"><span data-stu-id="ce525-288">For some legacy applications, a full implementation of Hide Access may not be practical.</span></span> <span data-ttu-id="ce525-289">Une autre méthode qui atteint le même effet consiste à désinstaller l’application.</span><span class="sxs-lookup"><span data-stu-id="ce525-289">An alternative method that achieves the same effect is to uninstall the application.</span></span> <span data-ttu-id="ce525-290">La section ci-dessous montre un exemple de comportement et un exemple de code pour implémenter cette alternative.</span><span class="sxs-lookup"><span data-stu-id="ce525-290">The section below shows example behavior and sample code to implement this alternative.</span></span> <span data-ttu-id="ce525-291">En général, les éditeurs de logiciels indépendants doivent éviter cette alternative, car ils :</span><span class="sxs-lookup"><span data-stu-id="ce525-291">In general, independent software vendors (ISVs) should avoid this alternative since it will:</span></span>

-   <span data-ttu-id="ce525-292">Désinstallez complètement l’application du système.</span><span class="sxs-lookup"><span data-stu-id="ce525-292">Uninstall the application completely from the system.</span></span>
-   <span data-ttu-id="ce525-293">Supprimer les valeurs par défaut précédemment sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="ce525-293">Remove previously selected defaults.</span></span>
-   <span data-ttu-id="ce525-294">Ne laissez aucune option d’interface utilisateur pour réinstaller l’application.</span><span class="sxs-lookup"><span data-stu-id="ce525-294">Leave no UI option to reinstall the application.</span></span>
-   <span data-ttu-id="ce525-295">Rendez la fonctionnalité activer l’accès plus disponible, car une désinstallation supprime complètement l’application de SPAD.</span><span class="sxs-lookup"><span data-stu-id="ce525-295">Make the enable access feature no longer available, since an uninstallation removes the application completely from SPAD.</span></span>

<span data-ttu-id="ce525-296">L’expérience utilisateur recommandée est la suivante :</span><span class="sxs-lookup"><span data-stu-id="ce525-296">The recommended user experience is as follows:</span></span>

-   <span data-ttu-id="ce525-297">Lorsque l’utilisateur décoche la case **activer l’accès à ce programme** dans SPAD, l’interface utilisateur suivante est présentée.</span><span class="sxs-lookup"><span data-stu-id="ce525-297">When the user unchecks the **Enable access to this program** box in SPAD, the following UI is presented.</span></span>

    ![boîte de dialogue à propos du masquage de l’accès au programme](images/hideaccessvista.png)

-   <span data-ttu-id="ce525-299">Quand l’utilisateur clique sur **OK**, l’élément **programmes et fonctionnalités** du panneau de configuration démarre pour permettre à l’utilisateur de désinstaller l’application.</span><span class="sxs-lookup"><span data-stu-id="ce525-299">When the user selects **OK**, the **Programs and Features** Control Panel item launches to allow the user to uninstall the application.</span></span>
-   <span data-ttu-id="ce525-300">Les utilisateurs de Windows XP doivent être affichés dans cette boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ce525-300">Windows XP users should be presented with this dialog box.</span></span>

    ![boîte de dialogue Windows XP équivalente](images/hideaccessxp.png)

-   <span data-ttu-id="ce525-302">Quand l’utilisateur Windows XP clique sur **OK**, l’élément **Ajouter ou supprimer des programmes** du panneau de configuration démarre pour permettre à l’utilisateur de désinstaller l’application.</span><span class="sxs-lookup"><span data-stu-id="ce525-302">When the Windows XP user selects **OK**, the **Add or Remove Programs** Control Panel item launches to allow the user to uninstall the application.</span></span>

<span data-ttu-id="ce525-303">Le code suivant fournit une implémentation réutilisable pour la fonctionnalité masquer l’accès, comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="ce525-303">The following code provides a reusable implementation for the Hide Access feature as outlined above.</span></span> <span data-ttu-id="ce525-304">Il peut être utilisé sur Windows XP, Windows Vista et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ce525-304">It can be used on Windows XP, Windows Vista, and Windows 7.</span></span>


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // Windows XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



### <a name="the-show-icons-command"></a><span data-ttu-id="ce525-305">Commande Afficher les icônes</span><span class="sxs-lookup"><span data-stu-id="ce525-305">The Show Icons Command</span></span>

<span data-ttu-id="ce525-306">La ligne de commande déclarée dans l’entrée ShowIconsCommand est exécutée lorsque l’utilisateur coche la case **activer l’accès à ce programme** dans la page **définir les paramètres par défaut de l’accès aux programmes et** de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ce525-306">The command line declared in the ShowIconsCommand entry is executed when the user checks the **Enable access to this program** box in the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="ce525-307">Cette ligne de commande peut restaurer les points d’accès de votre programme, y compris ceux qui se trouvent dans le menu **Démarrer** , sur le bureau et dans le groupe **démarrage** , ainsi que les appels automatiques normaux, tels que ceux spécifiés dans la clé de Registre **Run** .</span><span class="sxs-lookup"><span data-stu-id="ce525-307">This command line may restore your program's access points, including those in the **Start** menu, on the desktop, and in the **Startup** group, as well as normal automatic invocations, such as those specified in the **Run** registry key.</span></span> <span data-ttu-id="ce525-308">Les points d’accès visibles intéressants pour la plupart des applications sont répertoriés dans [la commande masquer les icônes](#the-hide-icons-command).</span><span class="sxs-lookup"><span data-stu-id="ce525-308">The visible access points of interest to most applications are listed in [The Hide Icons Command](#the-hide-icons-command).</span></span> <span data-ttu-id="ce525-309">L’application ne doit pas modifier les valeurs par défaut par utilisateur ; Cette modification doit être effectuée par l’utilisateur par le biais de **programmes par défaut**.</span><span class="sxs-lookup"><span data-stu-id="ce525-309">The application should not change per-user defaults; that change should be done by the user through **Default Programs**.</span></span>

<span data-ttu-id="ce525-310">Une fois vos icônes correctement affichées, vous devez mettre à jour la valeur de Registre IconsVisible sur 1, comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="ce525-310">After successfully showing your icons, you must update the IconsVisible registry value to 1 as shown:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

<span data-ttu-id="ce525-311">Notez que si vous avez utilisé l’entrée HideIconsCommand pour inviter une désinstallation de l’application, l’entrée ShowIconsCommand n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ce525-311">Note that if you have used the HideIconsCommand entry to prompt an uninstall of the application, the ShowIconsCommand entry is of no use.</span></span> <span data-ttu-id="ce525-312">Elle doit être supprimée du Registre avec le reste des informations de l’application pendant le processus de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="ce525-312">It should be removed from the registry with the rest of the application's information during the uninstall process.</span></span>

### <a name="group-program-configuration"></a><span data-ttu-id="ce525-313">Configuration du programme de groupe</span><span class="sxs-lookup"><span data-stu-id="ce525-313">Group Program Configuration</span></span>

> [!Note]  
> <span data-ttu-id="ce525-314">Cette section ne s’applique pas à Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ce525-314">This section does not apply to Windows 2000.</span></span>

 

<span data-ttu-id="ce525-315">Dans le cadre de la préparation du système, un fabricant d’ordinateurs OEM peut établir une configuration qui masque les points d’accès pour les programmes du navigateur, de la messagerie, de la lecture multimédia, de la messagerie instantanée ou de la machine virtuelle Microsoft pour les programmes clients Java et spécifie leurs propres programmes par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce525-315">As part of system preparation, an OEM can establish a configuration that hides access points for the Microsoft browser, email, media playback, instant messaging, or virtual machine for Java client programs and specifies their own default programs.</span></span> <span data-ttu-id="ce525-316">Les fabricants OEM peuvent permettre aux utilisateurs de réinitialiser leurs ordinateurs à tout moment dans cette configuration par défaut en définissant les valeurs de Registre suivantes.</span><span class="sxs-lookup"><span data-stu-id="ce525-316">OEMs can enable users to reset their computers at any time to this default configuration by setting the following registry values.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  OEMShowIcons = 1
                  OEMDefault = 1
```

<span data-ttu-id="ce525-317">Si ces clés sont définies, les utilisateurs peuvent restaurer la configuration OEM en sélectionnant l’option fabricant de l' **ordinateur** dans la page **définir les paramètres par défaut de l’accès aux programmes et** de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ce525-317">If these keys are set, users can restore the OEM configuration by selecting the **Computer Manufacturer** option on the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="ce525-318">Si ces clés ne sont pas définies, l’option fabricant de l' **ordinateur** n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="ce525-318">If these keys are not set, the **Computer Manufacturer** option is not shown.</span></span>

<span data-ttu-id="ce525-319">L’entrée **OEMShowIcons** , si elle est présente, définit l’état de l’icône afficher pour le client spécifié qui est appliqué si l’utilisateur sélectionne fabricant de l' **ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="ce525-319">The **OEMShowIcons** entry, if present, sets the icon show state for the specified client that is applied if the user selects **Computer Manufacturer**.</span></span> <span data-ttu-id="ce525-320">La valeur 1 entraîne l’affichage des icônes, tandis que la valeur 0 provoque l’absence d’affichage des icônes.</span><span class="sxs-lookup"><span data-stu-id="ce525-320">A value of 1 causes icons to be shown, and a value of 0 causes icons to not be shown.</span></span> <span data-ttu-id="ce525-321">Si **OEMShowIcons** est absent, le fait de sélectionner le fabricant de l' **ordinateur** n’a aucun effet sur l’icône Afficher le paramètre.</span><span class="sxs-lookup"><span data-stu-id="ce525-321">If **OEMShowIcons** is absent, selecting **Computer Manufacturer** has no effect on the icon show setting.</span></span> <span data-ttu-id="ce525-322">**OEMShowIcons** est de type **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="ce525-322">**OEMShowIcons** is of type **REG\_DWORD**.</span></span>

<span data-ttu-id="ce525-323">L’entrée **OEMDefault** , si elle est présente et définie sur 1, définit la préférence OEM pour le client par défaut du type indiqué.</span><span class="sxs-lookup"><span data-stu-id="ce525-323">The **OEMDefault** entry, if present and set to 1, establishes the OEM preference for the default client of the indicated type.</span></span> <span data-ttu-id="ce525-324">Un seul client d’un type particulier peut être marqué comme valeur par défaut OEM.</span><span class="sxs-lookup"><span data-stu-id="ce525-324">Only one client of a particular type can be marked as the OEM default.</span></span> <span data-ttu-id="ce525-325">Si plus d’une inscription du client contient l’entrée **OEMDefault** , tous sont ignorés et le client actuel continue à être utilisé comme client par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce525-325">If more then one client's registration contains the **OEMDefault** entry, then all are ignored and the current client continues to be used as default client.</span></span> <span data-ttu-id="ce525-326">Si l’entrée **OEMDefault** est absente ou présente et définie sur 0, ce client particulier n’est pas utilisé comme client par défaut si l’utilisateur sélectionne **Computer Manufacturer**.</span><span class="sxs-lookup"><span data-stu-id="ce525-326">If the **OEMDefault** entry is not present or is present and set to 0, then that particular client is not used as the default client if the user selects **Computer Manufacturer**.</span></span> <span data-ttu-id="ce525-327">**OEMDefault** est de type **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="ce525-327">**OEMDefault** is of type **REG\_DWORD**.</span></span>

<span data-ttu-id="ce525-328">Outre l’option de réinitialisation de leurs ordinateurs à la configuration par défaut établie par l’OEM, les utilisateurs disposent de trois autres options de configuration :</span><span class="sxs-lookup"><span data-stu-id="ce525-328">In addition to the option to reset their computers to the default configuration established by the OEM, users have three other configuration options:</span></span>

-   <span data-ttu-id="ce525-329">Définissez leur ordinateur sur une configuration Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ce525-329">Set their computer to a Microsoft Windows configuration.</span></span> <span data-ttu-id="ce525-330">Dans ce cas, la page **définir les paramètres par défaut de l’accès aux programmes et** de l’ordinateur permet d’accéder à tous les logiciels Microsoft et non-Microsoft sur l’ordinateur inscrit dans les catégories de produits appropriées.</span><span class="sxs-lookup"><span data-stu-id="ce525-330">In this case, the **Set Program Access and Computer Defaults** page enables access to all Microsoft and non-Microsoft software on the computer registered in the relevant product categories.</span></span> <span data-ttu-id="ce525-331">Les programmes Microsoft Windows sont sélectionnés comme option par défaut pour chaque catégorie.</span><span class="sxs-lookup"><span data-stu-id="ce525-331">Microsoft Windows programs are selected as the default option for each category.</span></span>
-   <span data-ttu-id="ce525-332">Définissez leur ordinateur sur une configuration non-Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ce525-332">Set their computer to a non-Microsoft configuration.</span></span> <span data-ttu-id="ce525-333">Cette configuration masque les points d’accès (tels que le menu **Démarrer** ) à Windows Internet Explorer, Windows Media Player, Windows Messenger et Microsoft Outlook Express.</span><span class="sxs-lookup"><span data-stu-id="ce525-333">This configuration hides access points (such as the **Start** menu) to Windows Internet Explorer, Windows Media Player, Windows Messenger, and Microsoft Outlook Express.</span></span> <span data-ttu-id="ce525-334">Il permet d’accéder aux logiciels non-Microsoft sur l’ordinateur dans ces catégories.</span><span class="sxs-lookup"><span data-stu-id="ce525-334">It enables access to the non-Microsoft software on the computer in these categories.</span></span> <span data-ttu-id="ce525-335">En outre, si un programme non-Microsoft est disponible dans une catégorie, il est défini comme valeur par défaut pour cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="ce525-335">Furthermore, if a non-Microsoft program is available in a category, it is set as the default for that category.</span></span> <span data-ttu-id="ce525-336">Si plusieurs programmes non-Microsoft sont disponibles dans une catégorie, l’utilisateur est invité à choisir le programme non-Microsoft qui doit être utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce525-336">If more than one non-Microsoft program is available in a category, the user is asked to choose which non-Microsoft program should be used as the default.</span></span>
-   <span data-ttu-id="ce525-337">Établissez une configuration personnalisée.</span><span class="sxs-lookup"><span data-stu-id="ce525-337">Establish a custom configuration.</span></span> <span data-ttu-id="ce525-338">Les utilisateurs effectuent leurs propres sélections pour l’activation ou la suppression de l’accès, en mélangeant les programmes Microsoft et non-Microsoft comme ils le voient.</span><span class="sxs-lookup"><span data-stu-id="ce525-338">Users make their own selections for enabling or removing access, mixing Microsoft and non-Microsoft programs as they see fit.</span></span> <span data-ttu-id="ce525-339">Les utilisateurs établissent des options par défaut en fonction de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="ce525-339">Users establish default options on a category-by-category basis.</span></span>

<span data-ttu-id="ce525-340">Les utilisateurs sont libres de modifier ces options à tout moment.</span><span class="sxs-lookup"><span data-stu-id="ce525-340">Users are free to change any of these options at any time.</span></span>

### <a name="browser-registration-example"></a><span data-ttu-id="ce525-341">Exemple d’inscription de navigateur</span><span class="sxs-lookup"><span data-stu-id="ce525-341">Browser Registration Example</span></span>

<span data-ttu-id="ce525-342">L’exemple suivant montre l’inscription **InstallInfo** complète pour un navigateur de vue éclairé de façon fictive.</span><span class="sxs-lookup"><span data-stu-id="ce525-342">The following example shows the full **InstallInfo** registration for a fictional Lit View browser.</span></span> <span data-ttu-id="ce525-343">Dans ce cas, les commutateurs de ligne de commande permettent au fichier Litview.exe d’effectuer toutes les actions nécessaires pour chaque valeur.</span><span class="sxs-lookup"><span data-stu-id="ce525-343">In this case the command line switches allow the Litview.exe file to perform whatever actions are necessary for each value.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\Litview.exe" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /showicons
                  IconsVisible = 1
```

<span data-ttu-id="ce525-344">Notez que les guillemets sont placés autour des tracés, car ils contiennent des espaces incorporés.</span><span class="sxs-lookup"><span data-stu-id="ce525-344">Note that quotation marks are placed around the paths because they contain embedded spaces.</span></span>

## <a name="registration-elements-for-specific-client-types"></a><span data-ttu-id="ce525-345">Éléments d’inscription pour des types de client spécifiques</span><span class="sxs-lookup"><span data-stu-id="ce525-345">Registration Elements for Specific Client Types</span></span>

<span data-ttu-id="ce525-346">Vous trouverez également les informations suivantes dans les ressources figurant dans la section Rubriques connexes à la fin de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="ce525-346">The following information also can be found in the resources listed in the Related Topics section at the end of this topic.</span></span>

-   [<span data-ttu-id="ce525-347">Enregistrement du menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="ce525-347">Start Menu Registration</span></span>](#start-menu-registration)
-   [<span data-ttu-id="ce525-348">Inscription du client de messagerie</span><span class="sxs-lookup"><span data-stu-id="ce525-348">Mail Client Registration</span></span>](#mail-client-registration)

### <a name="start-menu-registration"></a><span data-ttu-id="ce525-349">Enregistrement du menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="ce525-349">Start Menu Registration</span></span>

<span data-ttu-id="ce525-350">Sous Windows XP, les applications sont généralement inscrites par défaut sur un ordinateur (**HKEY \_ local \_ machine**) plutôt que sur l’étendue utilisateur (**HKEY \_ Current \_ User**).</span><span class="sxs-lookup"><span data-stu-id="ce525-350">Under Windows XP, applications typically registered defaults on a machine-wide (**HKEY\_LOCAL\_MACHINE**) rather than a user (**HKEY\_CURRENT\_USER**) scope.</span></span> <span data-ttu-id="ce525-351">Avec l’introduction de Windows Vista sur le contrôle de compte d’utilisateur, les applications qui réclament l' **Internet** et les emplacements de **messagerie** dans le menu **Démarrer** doivent implémenter la commande de réinstallation dans le contexte d’exécution approprié.</span><span class="sxs-lookup"><span data-stu-id="ce525-351">With the Windows Vista introduction of the User Account Control (UAC), applications that claim the **Internet** and **E-mail** slots in the **Start** menu must implement the reinstall command within the correct execution context.</span></span>

> [!Note]  
> <span data-ttu-id="ce525-352">Le lien de **messagerie** du menu Démarrer a été supprimé à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ce525-352">The Start menu **E-mail** link has been removed as of Windows 7.</span></span> <span data-ttu-id="ce525-353">Toutefois, l’inscription décrite dans cette section doit toujours être effectuée, car elle affecte le client MAPI par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce525-353">However, the registration discussed in this section should still be performed because it assigns the default MAPI client.</span></span>

 

<span data-ttu-id="ce525-354">Un utilisateur limité sur Windows XP, Windows Vista ou Windows 7 ne peut pas accéder à SPAD.</span><span class="sxs-lookup"><span data-stu-id="ce525-354">A limited user on Windows XP, Windows Vista, or Windows 7 cannot access SPAD.</span></span> <span data-ttu-id="ce525-355">Pour cette raison, les développeurs sont encouragés à s’inscrire à l’élément **définir vos programmes par défaut** du panneau de configuration afin que n’importe quel utilisateur puisse gérer les valeurs par défaut des applications par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce525-355">For this reason, developers are encouraged to register for the **Set your default programs** Control Panel item so that any user can manage per-user application defaults.</span></span>

<span data-ttu-id="ce525-356">Les sélections effectuées dans SPAD doivent uniquement affecter les paramètres par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ce525-356">Selections made in SPAD should only affect per-machine settings.</span></span>

<span data-ttu-id="ce525-357">Définissez la valeur de Registre comme suit.</span><span class="sxs-lookup"><span data-stu-id="ce525-357">Set the registry value as follows.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            (Default) = CanonicalName
```

> [!Note]
> 
> <span data-ttu-id="ce525-358">**Les informations suivantes s’appliquent uniquement à Windows XP.**</span><span class="sxs-lookup"><span data-stu-id="ce525-358">**The following information applies to Windows XP only.**</span></span>
> 
> <span data-ttu-id="ce525-359">Si l’inscription de la valeur par défaut au niveau de l’ordinateur sous HKEY \_ local \_ machine comme indiqué ci-dessus est réussie, l’application doit supprimer la valeur assignée à l’entrée par défaut sous la sous-clé suivante :</span><span class="sxs-lookup"><span data-stu-id="ce525-359">If the registration of the computer-level default under HKEY\_LOCAL\_MACHINE as shown above is successful, the application should delete the value assigned to the Default entry under the following subkey:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> <span data-ttu-id="ce525-360">Si l’inscription de la valeur par défaut au niveau de l’ordinateur sous HKEY \_ local \_ machine comme indiqué ci-dessus échoue, généralement parce que l’utilisateur n’a pas d’autorisation d’écriture sur la sous-clé, l’application doit définir la valeur suivante :</span><span class="sxs-lookup"><span data-stu-id="ce525-360">If the registration of the computer-level default under HKEY\_LOCAL\_MACHINE as shown above fails, usually because the user does not have write permission to the subkey, the application should set the following value:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
>             (Default) = CanonicalName
> ```
> 
> <span data-ttu-id="ce525-361">Cela enregistre le nom canonique uniquement pour l’utilisateur actuel, et non pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ce525-361">This registers the canonical name only for the current user, not for all users.</span></span>

 

<span data-ttu-id="ce525-362">Après la mise à jour des clés de Registre, le programme doit diffuser le message [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) avec **wParam** = 0 et **lParam** pointant vers la chaîne terminée par le caractère null « \\ clients logiciels \\ **ClientTypeName**» pour notifier le système d’exploitation que le client par défaut a changé.</span><span class="sxs-lookup"><span data-stu-id="ce525-362">After updating the registry keys, the program should broadcast the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with **wParam** = 0 and **lParam** pointing to the null-terminated string "Software\\Clients\\**ClientTypeName**" to notify the operating system that the default client has changed.</span></span>

### <a name="mail-client-registration"></a><span data-ttu-id="ce525-363">Inscription du client de messagerie</span><span class="sxs-lookup"><span data-stu-id="ce525-363">Mail Client Registration</span></span>

<span data-ttu-id="ce525-364">Pour un client de messagerie, le programme doit avoir des paramètres enregistrés sous la clé de clé mailto de la **\_ \_ racine de classes HKEY** \\  pour pouvoir traiter les URL qui utilisent le `mailto` protocole.</span><span class="sxs-lookup"><span data-stu-id="ce525-364">For a mail client, the program needs to have registered settings under the **HKEY\_CLASSES\_ROOT**\\**mailto** key in order to service URLs that use the `mailto` protocol.</span></span> <span data-ttu-id="ce525-365">Définissez les valeurs et les clés qui reflètent ces paramètres sous la clé suivante.</span><span class="sxs-lookup"><span data-stu-id="ce525-365">Set values and keys that mirror those settings under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

<span data-ttu-id="ce525-366">Cette hiérarchie de Registre remplace la `mailto` hiérarchie de Registre existante trouvée dans **HKEY \_ classes \_ root** \\ **mailto**.</span><span class="sxs-lookup"><span data-stu-id="ce525-366">This registry hierarchy replaces the existing `mailto` registry hierarchy found at **HKEY\_CLASSES\_ROOT**\\**mailto**.</span></span> <span data-ttu-id="ce525-367">La hiérarchie reste la même, seul l’emplacement a changé.</span><span class="sxs-lookup"><span data-stu-id="ce525-367">The hierarchy remains the same, only the location has changed.</span></span> <span data-ttu-id="ce525-368">Le format de cette hiérarchie est documenté sur MSDN sous [vues d’ensemble et didacticiels de protocoles enfichables asynchrones](/previous-versions//aa767913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ce525-368">The format of this hierarchy is documented on MSDN under [Asynchronous Pluggable Protocol Overviews and Tutorials](/previous-versions//aa767913(v=vs.85)).</span></span> <span data-ttu-id="ce525-369">En règle générale, le `mailto` protocole est inscrit à un programme plutôt qu’à un protocole asynchrone, auquel cas la documentation sur l' [enregistrement d’une application dans un schéma d’URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) s’applique.</span><span class="sxs-lookup"><span data-stu-id="ce525-369">Typically, the `mailto` protocol is registered to a program rather than an asynchronous protocol, in which case the documentation on [Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) applies.</span></span>

<span data-ttu-id="ce525-370">L’exemple suivant illustre la `mailto` section de l’inscription d’un `mailto` Gestionnaire inscrit auprès d’un programme.</span><span class="sxs-lookup"><span data-stu-id="ce525-370">The following example shows the `mailto` section of the registration for a `mailto` handler registered to a program.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = %FilePath%,IconIndex
                     shell
                        open
                           command
                              (Default) = command line
```

<span data-ttu-id="ce525-371">La valeur de Registre indicateurs est documentée dans les [types de fichiers](fa-file-types.md) de la section intitulée « définition des attributs de type de fichier ».</span><span class="sxs-lookup"><span data-stu-id="ce525-371">The EditFlags registry value is documented in [File Types](fa-file-types.md) in the section titled "Defining File Type Attributes."</span></span>

## <a name="complete-sample-registrations"></a><span data-ttu-id="ce525-372">Compléter les exemples d’inscriptions</span><span class="sxs-lookup"><span data-stu-id="ce525-372">Complete Sample Registrations</span></span>

<span data-ttu-id="ce525-373">Les exemples suivants sont fournis pour montrer les exigences d’inscription complètes pour les différents types de clients.</span><span class="sxs-lookup"><span data-stu-id="ce525-373">The following examples are provided to show the complete registration requirements for the various client types.</span></span>

-   [<span data-ttu-id="ce525-374">Exemple de navigateur</span><span class="sxs-lookup"><span data-stu-id="ce525-374">A Sample Browser</span></span>](#a-sample-browser)
-   [<span data-ttu-id="ce525-375">Exemple de navigateur de messagerie</span><span class="sxs-lookup"><span data-stu-id="ce525-375">A Sample Mail Browser</span></span>](#a-sample-mail-browser)
-   [<span data-ttu-id="ce525-376">Exemple de lecteur multimédia</span><span class="sxs-lookup"><span data-stu-id="ce525-376">A Sample Media Player</span></span>](#a-sample-media-player)
-   [<span data-ttu-id="ce525-377">Exemple de programme Instant Messenger</span><span class="sxs-lookup"><span data-stu-id="ce525-377">A Sample Instant Messenger Program</span></span>](#a-sample-instant-messenger-program)
-   [<span data-ttu-id="ce525-378">Exemple de machine virtuelle Java</span><span class="sxs-lookup"><span data-stu-id="ce525-378">A Sample Virtual Machine for Java</span></span>](#a-sample-virtual-machine-for-java)

### <a name="a-sample-browser"></a><span data-ttu-id="ce525-379">Exemple de navigateur</span><span class="sxs-lookup"><span data-stu-id="ce525-379">A Sample Browser</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
                  shell
                     open
                        command
                           (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /homepage
```

### <a name="a-sample-mail-browser"></a><span data-ttu-id="ce525-380">Exemple de navigateur de messagerie</span><span class="sxs-lookup"><span data-stu-id="ce525-380">A Sample Mail Browser</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            Lit View
               (Default) = Lit View
               DLLPath = @C:\Program Files\LItwareInc\LitwareMAPI.dll
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /inbox
               protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
                     shell
                        open
                           command
                              (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /mailto:%1
```

### <a name="a-sample-media-player"></a><span data-ttu-id="ce525-381">Exemple de lecteur multimédia</span><span class="sxs-lookup"><span data-stu-id="ce525-381">A Sample Media Player</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Media
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-instant-messenger-program"></a><span data-ttu-id="ce525-382">Exemple de programme Instant Messenger</span><span class="sxs-lookup"><span data-stu-id="ce525-382">A Sample Instant Messenger Program</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-virtual-machine-for-java"></a><span data-ttu-id="ce525-383">Exemple de machine virtuelle Java</span><span class="sxs-lookup"><span data-stu-id="ce525-383">A Sample Virtual Machine for Java</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         JavaVM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

<span data-ttu-id="ce525-384">*Les exemples de sociétés, d’organisations, de produits, de noms de domaine, d’adresses de messagerie, de logos, de personnes, de lieux et d’événements mentionnés dans les exemples sont fictifs. Toute ressemblance avec des sociétés, des organisations, des produits, des noms de domaine, des adresses électroniques, des logos, des personnes, des lieux ou des événements réels est purement fortuite et involontaire.*</span><span class="sxs-lookup"><span data-stu-id="ce525-384">*The example companies, organizations, products, domain names, email addresses, logos, people, places, and events depicted herein are fictitious. No association with any real company, organization, product, domain name, email address, logo, person, place, or event is intended or should be inferred.*</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce525-385">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ce525-385">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce525-386">Programmes par défaut</span><span class="sxs-lookup"><span data-stu-id="ce525-386">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="ce525-387">Inscription d’un navigateur Internet ou d’un client de messagerie à l’aide du menu Démarrer de Windows</span><span class="sxs-lookup"><span data-stu-id="ce525-387">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>](start-menu-reg.md)
</dt> <dt>

<span data-ttu-id="ce525-388">[Disposition du Registre du client Internet Explorer (voir la section « Définitions des clés de Registre du client »)](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ce525-388">[Internet Explorer Client Registry Layout (see the "Client Registry Key Definitions" section)](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="ce525-389">[Vues d’ensemble et didacticiels enfichables de protocoles enfichables asynchrones](/previous-versions//aa767913(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ce525-389">[Asynchronous Pluggable Protocol Overviews and Tutorials](/previous-versions//aa767913(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="ce525-390">[Inscription d’une application dans un schéma d’URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ce525-390">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>
</dt> </dl>

 

 
