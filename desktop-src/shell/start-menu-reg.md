---
description: Le menu Démarrer de Windows XP et Windows Vista contient des emplacements réservés pour les clients Internet (navigateur) et de messagerie électronique (messagerie) par défaut, communément appelés applications Internet du menu Démarrer.
ms.assetid: a3d7416f-0dbd-4af2-ab38-758f9cc8aec5
title: Inscription d’un navigateur Internet ou d’un client de messagerie à l’aide du menu Démarrer de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccdd8fb8efe32522947b30ab2ce1a50b7058e97
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104211298"
---
# <a name="how-to-register-an-internet-browser-or-email-client-with-the-windows-start-menu"></a><span data-ttu-id="29e3e-103">Inscription d’un navigateur Internet ou d’un client de messagerie à l’aide du menu Démarrer de Windows</span><span class="sxs-lookup"><span data-stu-id="29e3e-103">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>

> [!Note]  
> <span data-ttu-id="29e3e-104">Cette rubrique s’applique à Windows XP, Windows Vista et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="29e3e-104">This topic applies to Windows XP, Windows Vista, and Windows 7.</span></span>

 

<span data-ttu-id="29e3e-105">Le menu Démarrer de Windows XP et Windows Vista contient des emplacements réservés pour les clients **Internet** (navigateur) et de **messagerie électronique** (messagerie) par défaut, communément appelés *applications Internet du menu Démarrer*.</span><span class="sxs-lookup"><span data-stu-id="29e3e-105">The Start menu in Windows XP and Windows Vista contains reserved slots for the default **Internet** (browser) and **E-mail** (mail) clients, together commonly known as *Start Menu Internet Applications*.</span></span> <span data-ttu-id="29e3e-106">Les applications qui s’inscrivent en tant qu’applications Internet du menu Démarrer le font sur l’ensemble du système (par ordinateur).</span><span class="sxs-lookup"><span data-stu-id="29e3e-106">Applications which register as Start Menu Internet Applications do so across the entire system (per-machine).</span></span> <span data-ttu-id="29e3e-107">Dans Windows Vista, l’utilisateur peut utiliser la fonctionnalité **programmes par défaut** pour définir une valeur par défaut pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29e3e-107">In Windows Vista, the user may use the **Default Programs** feature to set a per-user default.</span></span>

<span data-ttu-id="29e3e-108">Lorsque les applications s’inscrivent en tant qu’applications Internet du menu Démarrer, Windows XP et Windows Vista créent des icônes **Internet** et de **messagerie électronique** dans le menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="29e3e-108">When applications register as Start Menu Internet Applications, Windows XP and Windows Vista create **Internet** and **E-mail** icons on the Start menu.</span></span> <span data-ttu-id="29e3e-109">En cliquant sur ces icônes, le menu Démarrer vérifie la sous-arborescence du Registre par utilisateur (**HKEY \_ Current \_ User**).</span><span class="sxs-lookup"><span data-stu-id="29e3e-109">Clicking these icons causes the Start menu to check the per-user registry subtree (**HKEY\_CURRENT\_USER**).</span></span> <span data-ttu-id="29e3e-110">Si aucun paramètre par défaut par utilisateur n’est trouvé, le menu Démarrer recherche la sous-clé par défaut par ordinateur dans la sous-arborescence de l' **\_ \_ ordinateur local HKEY** .</span><span class="sxs-lookup"><span data-stu-id="29e3e-110">If no per-user default setting is found, the Start menu looks for the per-machine default subkey in the **HKEY\_LOCAL\_MACHINE** subtree.</span></span>

> [!Note]  
> <span data-ttu-id="29e3e-111">L’installation par défaut de Windows n’inscrit pas un programme Internet ou de messagerie par défaut par utilisateur, mais uniquement une valeur par défaut à l’ensemble du système.</span><span class="sxs-lookup"><span data-stu-id="29e3e-111">The default installation of Windows does not register a per-user default Internet or email program, only a system-wide default.</span></span> <span data-ttu-id="29e3e-112">Cela offre un chemin de mise à niveau fluide à partir des versions précédentes du système d’exploitation, dans lequel seule la sous-arborescence de la \_ machine locale HKEY \_ est prise en charge pour les inscriptions du client.</span><span class="sxs-lookup"><span data-stu-id="29e3e-112">This provides a smooth upgrade path from previous versions of the operating system, in which only the HKEY\_LOCAL\_MACHINE subtree is supported for client registrations.</span></span>

 

<span data-ttu-id="29e3e-113">Cette rubrique présente les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="29e3e-113">This topic discusses the following items:</span></span>

-   [<span data-ttu-id="29e3e-114">Inscription pour le lien Internet du menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="29e3e-114">Registering for the Start Menu Internet Link</span></span>](#registering-for-the-start-menu-internet-link)
    -   [<span data-ttu-id="29e3e-115">Comment s’inscrire en tant que client Internet par défaut</span><span class="sxs-lookup"><span data-stu-id="29e3e-115">How to Register as the Default Internet Client</span></span>](#how-to-register-as-the-default-internet-client)
-   [<span data-ttu-id="29e3e-116">Inscription pour le lien de messagerie du menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="29e3e-116">Registering for the Start Menu Email Link</span></span>](#registering-for-the-start-menu-email-link)
    -   [<span data-ttu-id="29e3e-117">Comment le menu Démarrer affiche le client de messagerie par défaut</span><span class="sxs-lookup"><span data-stu-id="29e3e-117">How the Start Menu Displays the Default Email Client</span></span>](#how-the-start-menu-displays-the-default-email-client)
    -   [<span data-ttu-id="29e3e-118">Comment s’inscrire en tant que client de messagerie par défaut</span><span class="sxs-lookup"><span data-stu-id="29e3e-118">How to Register as the Default EMail Client</span></span>](#how-to-register-as-the-default-email-client)
-   [<span data-ttu-id="29e3e-119">Personnalisation du menu contextuel</span><span class="sxs-lookup"><span data-stu-id="29e3e-119">Customizing the Context Menu</span></span>](#customizing-the-context-menu)

## <a name="registering-for-the-start-menu-internet-link"></a><span data-ttu-id="29e3e-120">Inscription pour le lien Internet du menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="29e3e-120">Registering for the Start Menu Internet Link</span></span>

> [!Note]  
> <span data-ttu-id="29e3e-121">Cette inscription est déconseillée à partir de Windows 7, qui ne fournit plus de lien Internet dans le menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="29e3e-121">This registration is deprecated as of Windows 7, which no longer provides a Start menu Internet link.</span></span> <span data-ttu-id="29e3e-122">Les inscriptions existantes sont ignorées dans Windows 7 et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="29e3e-122">Existing registrations are ignored in Windows 7 and later.</span></span> <span data-ttu-id="29e3e-123">L’inscription de l’application Internet par défaut dans le menu Démarrer n’est pas la même que celle du navigateur Web par défaut.</span><span class="sxs-lookup"><span data-stu-id="29e3e-123">Being registered as the default Start menu Internet application is not the same as being registered as the default web browser.</span></span> <span data-ttu-id="29e3e-124">Le navigateur Web par défaut est utilisé pour lancer des URL arbitraires depuis n’importe où dans le système.</span><span class="sxs-lookup"><span data-stu-id="29e3e-124">The default web browser is used for launching arbitrary URLs from anywhere in the system.</span></span> <span data-ttu-id="29e3e-125">L’application Internet du menu Démarrer contrôle simplement le programme qui est démarré lorsque l’utilisateur clique sur l’icône Internet dans le menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="29e3e-125">The Start menu Internet application merely controls the program that is started when the user clicks the Internet icon on the Start menu.</span></span>

 

<span data-ttu-id="29e3e-126">Toute application de navigateur Web peut s’inscrire pour apparaître en tant que client Internet dans le menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="29e3e-126">Any web browser application can register to appear as an Internet client on the Start menu.</span></span> <span data-ttu-id="29e3e-127">Cette visibilité, couplée à une inscription correcte pour les types de [fichier](fa-intro.md) et de [protocole](/previous-versions//aa767743(v=vs.85)) d’une application, donne un État du navigateur par défaut de l’application.</span><span class="sxs-lookup"><span data-stu-id="29e3e-127">This visibility, coupled with proper registration for an application's [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types, gives an application default browser status.</span></span>

<span data-ttu-id="29e3e-128">Les inscriptions effectuées dans la sous-arborescence de la sous-arborescence de l' **\_ \_ utilisateur actuel** ont une priorité plus élevée pour l’utilisateur de la console que les inscriptions correspondantes effectuées sur l' **\_ \_ ordinateur local HKEY**.</span><span class="sxs-lookup"><span data-stu-id="29e3e-128">Registrations made in the **HKEY\_CURRENT\_USER** subtree have higher precedence for the console user than corresponding registrations made in the **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="29e3e-129">Pour les nouveaux utilisateurs sur le système, les paramètres stockés dans **HKEY \_ local \_ machine** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="29e3e-129">For new users on the system, the settings stored in **HKEY\_LOCAL\_MACHINE** are used.</span></span> <span data-ttu-id="29e3e-130">À compter de Windows XP, le menu démarrer les paramètres Internet sont conservés dans les entrées par défaut de deux emplacements du Registre :</span><span class="sxs-lookup"><span data-stu-id="29e3e-130">As of Windows XP, Start menu Internet settings are kept in the default entries of two registry locations:</span></span>

-   <span data-ttu-id="29e3e-131">**HKEY \_ Clients du logiciel \_ utilisateur actuel** \\  \\  \\ **StartMenuInternet**</span><span class="sxs-lookup"><span data-stu-id="29e3e-131">**HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet**</span></span>
-   <span data-ttu-id="29e3e-132">**HKEY \_ \_** Clients de logiciels de l’ordinateur local \\  \\  \\ **StartMenuInternet**</span><span class="sxs-lookup"><span data-stu-id="29e3e-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet**</span></span>

<span data-ttu-id="29e3e-133">La sous-clé **HKEY \_ Current \_ User** \\ **Software** \\ **clients** \\ **StartMenuInternet** décrit le navigateur Internet qui est démarré lorsque l’utilisateur clique sur l’icône **Internet** dans le menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="29e3e-133">The subkey **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** describes the Internet browser that is started when the user clicks the **Internet** icon on the Start menu.</span></span> <span data-ttu-id="29e3e-134">Si cette sous-clé est vide ou manquante, l’icône **Internet** dans le menu Démarrer est définie sur la valeur système par défaut stockée dans le deuxième emplacement de la clé **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **StartMenuInternet** , qui décrit toutes les applications de navigateur Internet installées sur le système.</span><span class="sxs-lookup"><span data-stu-id="29e3e-134">If that subkey is blank or missing, then the **Internet** icon on the Start menu is set to the system default stored in the second location at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** , which describes all Internet browser applications that are installed on the system.</span></span>

<span data-ttu-id="29e3e-135">Quand un nouvel utilisateur se connecte au système, le menu Démarrer utilise la valeur par défaut dans la sous-clé de la clé **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **StartMenuInternet** pour afficher le client Internet par défaut et démarrer l’application inscrite lorsque l’utilisateur clique sur cette icône.</span><span class="sxs-lookup"><span data-stu-id="29e3e-135">When a new user logs onto the system, the Start menu uses the default value in the subkey at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** to display the default Internet client and starts the registered application when that icon is clicked.</span></span>

### <a name="how-to-register-as-the-default-internet-client"></a><span data-ttu-id="29e3e-136">Comment s’inscrire en tant que client Internet par défaut</span><span class="sxs-lookup"><span data-stu-id="29e3e-136">How to Register as the Default Internet Client</span></span>

<span data-ttu-id="29e3e-137">Sous la sous-clé **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **StartMenuInternet** , il peut y avoir zéro, une ou plusieurs sous-clés, une pour chaque application de navigateur Internet inscrite.</span><span class="sxs-lookup"><span data-stu-id="29e3e-137">Below the subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** there can be zero or more subkeys, one for each registered Internet browser application.</span></span> <span data-ttu-id="29e3e-138">Par exemple, un système hypothétique peut avoir cette organisation :</span><span class="sxs-lookup"><span data-stu-id="29e3e-138">For example, a hypothetical system might have this arrangement:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            IEXPLORE.EXE
            BROWSER2.EXE
            BROWSER3.EXE
```

<span data-ttu-id="29e3e-139">Nous présenterons les entrées de Registre avec un navigateur hypothétique appelé « lit View » à partir d’une société fictive appelée Litware Inc. Supposons que le nom de l’exécutable pour lit View est Litview.exe.</span><span class="sxs-lookup"><span data-stu-id="29e3e-139">We will demonstrate registry entries with a hypothetical browser called "Lit View" from a fictional company called Litware Inc. Suppose that the executable name for Lit View is Litview.exe.</span></span> <span data-ttu-id="29e3e-140">L’inscription de la vue lit se produit comme indiqué ici :</span><span class="sxs-lookup"><span data-stu-id="29e3e-140">The registration of Lit View occurs as shown here:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

<span data-ttu-id="29e3e-141">Les données LocalizedString sont de type REG \_ SZ, ou reg \_ expand \_ SZ si les variables de chemin d’accès telles que `%programfiles%` sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="29e3e-141">The LocalizedString data is of type REG\_SZ, or REG\_EXPAND\_SZ if path variables such as `%programfiles%` are used.</span></span> <span data-ttu-id="29e3e-142">LocalizedString fournit le chemin d’un fichier exécutable (. exe) ou d’un fichier de bibliothèque (. dll).</span><span class="sxs-lookup"><span data-stu-id="29e3e-142">LocalizedString provides the path to an executable (.exe) or library (.dll) file.</span></span> <span data-ttu-id="29e3e-143">Notez que la chaîne de chemin d’accès commence par un signe « at » (@) et qu’aucun guillemet n’est requis autour du chemin d’accès, quels que soient les espaces qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="29e3e-143">Note that the path string begins with an "at" sign (@) and that no quotation marks are required around the path regardless of spaces within it.</span></span> <span data-ttu-id="29e3e-144">L’entier décimal est l’ID d’une ressource de type chaîne, contenue dans la DLL spécifiée, dont la valeur doit être affichée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29e3e-144">The decimal integer is the ID of a string resource, contained within the specified DLL, whose value is to be displayed to the user.</span></span> <span data-ttu-id="29e3e-145">Cela permet d’utiliser la même inscription pour plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="29e3e-145">This enables the same registration to be used for multiple languages.</span></span> <span data-ttu-id="29e3e-146">Chaque langue fournit une ResourceDLL.dll différente.</span><span class="sxs-lookup"><span data-stu-id="29e3e-146">Each language provides a different ResourceDLL.dll.</span></span> <span data-ttu-id="29e3e-147">Cela permet au système d’afficher la chaîne correcte en fonction de la langue actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="29e3e-147">This enables the system to display the correct string based on the currently selected language.</span></span>

<span data-ttu-id="29e3e-148">La \_ valeur de l’option reg SZ ou reg \_ expand développée suivante \_ indique au menu Démarrer de l’icône par défaut de s’afficher lorsque l’utilisateur sélectionne l’affichage allumé comme menu Démarrer navigateur Internet.</span><span class="sxs-lookup"><span data-stu-id="29e3e-148">The following REG\_SZ or REG\_EXPAND\_SZ value informs the Start menu of the default icon to display when the user selects Lit View as the Start menu Internet browser.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitView.exe,1
```

<span data-ttu-id="29e3e-149">La sous-clé de Registre suivante spécifie une ligne de commande à exécuter quand l’utilisateur clique sur la commande de menu Internet dans le menu Démarrer, en supposant que lit View est le navigateur Internet sélectionné pour le menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="29e3e-149">The following registry subkey specifies a command line to run when the user clicks the Internet menu command on the Start menu, assuming that Lit View is the selected Start menu Internet browser.</span></span> <span data-ttu-id="29e3e-150">Par exemple, la commande peut ouvrir le navigateur avec la page d’hébergement de l’utilisateur, ou la commande peut lancer une interface utilisateur d’introduction que l’éditeur de logiciels indépendant (ISV) estime être approprié.</span><span class="sxs-lookup"><span data-stu-id="29e3e-150">For example, the command might open the browser with the user's home page or the command could launch an introductory user interface that the independent software vendor (ISV) feels is appropriate.</span></span> <span data-ttu-id="29e3e-151">Les données sont de type REG \_ SZ ou reg \_ expand \_ SZ, mais notez qu’étant donné qu’il y a un espace dans le chemin d’accès à la ligne de commande, le chemin d’accès de l’exécutable est placé entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="29e3e-151">The data is of type REG\_SZ or REG\_EXPAND\_SZ, but notice that because there is a space in the command-line path, the executable path is enclosed in quotation marks.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     (Default) = "C:\Program Files\LitwareInc\LitView.exe" -welcome
```

<span data-ttu-id="29e3e-152">Lorsque l’utilisateur spécifie par le biais de l’option [définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)](cpl-setprogramaccess.md) qui lit l’affichage doit être utilisé comme navigateur Web par défaut au niveau de l’ordinateur, l’application doit définir l’entrée de Registre \_ SZ suivante.</span><span class="sxs-lookup"><span data-stu-id="29e3e-152">When the user specifies through [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) that Lit View should be used as the computer-level default web browser, the application should set the following REG\_SZ entry.</span></span> <span data-ttu-id="29e3e-153">Notez que le paramètre SPAD s’exécutant avec des privilèges d’administrateur, l’accès à cette sous-clé est autorisé.</span><span class="sxs-lookup"><span data-stu-id="29e3e-153">Note that because SPAD runs with Administrator privileges, access to this subkey is allowed.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            (Default) = LITVIEW.EXE
```

> [!Note]
> <span data-ttu-id="29e3e-154">Dans Windows Vista, le navigateur Web par défaut au niveau de l’utilisateur doit être défini à l’aide de l’outil **programmes par défaut** , et non de [SPAD](cpl-setprogramaccess.md).</span><span class="sxs-lookup"><span data-stu-id="29e3e-154">In Windows Vista, the user-level default web browser should be set using the **Default Programs** tool, not [SPAD](cpl-setprogramaccess.md).</span></span>
> 
> <span data-ttu-id="29e3e-155">**Les informations suivantes s’appliquent uniquement à Windows XP.**</span><span class="sxs-lookup"><span data-stu-id="29e3e-155">**The following information applies to Windows XP only.**</span></span>
> 
> <span data-ttu-id="29e3e-156">Si l’inscription du navigateur Web par défaut au niveau de l’ordinateur sous HKEY \_ local \_ machine comme indiqué ci-dessus réussit, l’application doit supprimer l’entrée par défaut sous la sous-clé suivante :</span><span class="sxs-lookup"><span data-stu-id="29e3e-156">If the registration of the computer-level default web browser under HKEY\_LOCAL\_MACHINE as shown above is successful, the application should delete the Default entry under the following subkey:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          StartMenuInternet
> ```
> 
> <span data-ttu-id="29e3e-157">Si l’inscription du navigateur Web par défaut au niveau de l’ordinateur sous HKEY \_ local \_ machine échoue, l’application doit définir les données de reg \_ SZ comme indiqué dans cet exemple pour l’application de vue allumée :</span><span class="sxs-lookup"><span data-stu-id="29e3e-157">If the registration of the computer-level default web browser under HKEY\_LOCAL\_MACHINE fails, the application should set the REG\_SZ data as shown in this example for the Lit View application:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          (Default) = LITVIEW.EXE
> ```

 

<span data-ttu-id="29e3e-158">Après la mise à jour des sous-clés appropriées, l’application diffuse le message [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) avec son paramètre *wParam* défini sur 0 et son paramètre *lParam* pointant vers la chaîne terminée par le caractère null `"Software\Clients\StartMenuInternet"` .</span><span class="sxs-lookup"><span data-stu-id="29e3e-158">After updating the appropriate subkeys, the application broadcasts the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with its *wParam* parameter set to 0 and its *lParam* parameter pointing to the null-terminated string `"Software\Clients\StartMenuInternet"`.</span></span> <span data-ttu-id="29e3e-159">Cela indique au système d’exploitation que le client par défaut a changé.</span><span class="sxs-lookup"><span data-stu-id="29e3e-159">This notifies the operating system that the default client has changed.</span></span>

<span data-ttu-id="29e3e-160">La définition de ces sous-clés pour le menu démarrer par défaut navigateur Internet est nécessaire pour préserver la compatibilité descendante avec les anciens navigateurs Web qui ne prennent pas en charge les inscriptions par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29e3e-160">Setting these subkeys for the default Start menu Internet browser is necessary to preserve backward compatibility with old web browsers that do not support per-user registrations.</span></span>

## <a name="registering-for-the-start-menu-email-link"></a><span data-ttu-id="29e3e-161">Inscription pour le lien de messagerie du menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="29e3e-161">Registering for the Start Menu Email Link</span></span>

> [!Note]  
> <span data-ttu-id="29e3e-162">Le lien de messagerie du menu Démarrer a été supprimé à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="29e3e-162">The Start menu Email link has been removed as of Windows 7.</span></span> <span data-ttu-id="29e3e-163">Toutefois, cette inscription décrite dans cette section doit toujours être effectuée pour son effet lors de l’attribution du client MAPI par défaut.</span><span class="sxs-lookup"><span data-stu-id="29e3e-163">However, this registration discussed in this section should still be performed for its effect in assigning the default MAPI client.</span></span>

 

### <a name="how-the-start-menu-displays-the-default-email-client"></a><span data-ttu-id="29e3e-164">Comment le menu Démarrer affiche le client de messagerie par défaut</span><span class="sxs-lookup"><span data-stu-id="29e3e-164">How the Start Menu Displays the Default Email Client</span></span>

<span data-ttu-id="29e3e-165">Toutes les applications de messagerie peuvent s’inscrire pour apparaître en tant que client de messagerie dans le menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="29e3e-165">Any email application can register to appear as an email client on the Start menu.</span></span> <span data-ttu-id="29e3e-166">Cette visibilité, couplée à une inscription correcte pour les types de [fichier](fa-intro.md) et de [protocole](/previous-versions//aa767743(v=vs.85)) d’une application, donne l’état de messagerie par défaut de l’application.</span><span class="sxs-lookup"><span data-stu-id="29e3e-166">This visibility, coupled with proper registration for an application's [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types, gives an application default mail status.</span></span>

<span data-ttu-id="29e3e-167">Les inscriptions effectuées dans la sous-arborescence de la sous-arborescence de l' **\_ \_ utilisateur actuel** ont une priorité plus élevée pour l’utilisateur de la console que les inscriptions correspondantes effectuées sur l' **\_ \_ ordinateur local HKEY**.</span><span class="sxs-lookup"><span data-stu-id="29e3e-167">Registrations made in the **HKEY\_CURRENT\_USER** subtree have higher precedence for the console user than corresponding registrations made in the **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="29e3e-168">Pour les nouveaux utilisateurs sur le système, les paramètres stockés dans **HKEY \_ local \_ machine** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="29e3e-168">For new users on the system, the settings stored in **HKEY\_LOCAL\_MACHINE** are used.</span></span> <span data-ttu-id="29e3e-169">À compter de Windows XP, les paramètres de messagerie du menu Démarrer sont conservés dans les entrées par défaut de deux emplacements du Registre :</span><span class="sxs-lookup"><span data-stu-id="29e3e-169">As of Windows XP, Start menu Email settings are kept in the default entries of two registry locations:</span></span>

-   <span data-ttu-id="29e3e-170">**HKEY \_ \_** Messagerie des \\  \\ **clients** \\  logiciels des utilisateurs actuels</span><span class="sxs-lookup"><span data-stu-id="29e3e-170">**HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail**</span></span>
-   <span data-ttu-id="29e3e-171">**HKEY \_ \_** Messagerie des \\  \\ **clients** \\  logiciels de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="29e3e-171">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail**</span></span>

<span data-ttu-id="29e3e-172">La sous-clé **HKEY \_ Current \_ User** \\ **Software** \\ **clients** \\ **mail** décrit le client de messagerie qui est démarré lorsque l’utilisateur clique sur l’icône de **courrier électronique** dans le menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="29e3e-172">The subkey **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail** describes the email client that is started when the user clicks the **E-mail** icon on the Start menu.</span></span>

<span data-ttu-id="29e3e-173">La sous-clé **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **mail** décrit les applications de messagerie qui sont installées sur le système, ainsi que l’application de messagerie par défaut.</span><span class="sxs-lookup"><span data-stu-id="29e3e-173">The subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** describes the email applications that are installed on the system, as well as the default email application.</span></span>

<span data-ttu-id="29e3e-174">Si la **messagerie HKEY \_ Current \_ User** \\ **Software** \\ **clients** \\  est vide ou manquante, la valeur par défaut définie dans **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **mail** est utilisée pour sélectionner l’application de messagerie qui apparaît dans le menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="29e3e-174">If the **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail** is blank or missing, the default value defined in **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** is used to select the email application that appears on the Start menu.</span></span>

<span data-ttu-id="29e3e-175">Quand un nouvel utilisateur se connecte au système, le menu Démarrer utilise la valeur par défaut dans la sous-clé de la clé **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **mail** pour afficher le client de messagerie par défaut et démarre l’application inscrite lorsque l’utilisateur clique sur cette icône.</span><span class="sxs-lookup"><span data-stu-id="29e3e-175">When a new user logs onto the system, the Start menu uses the default value in the subkey at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** to display the default email client and starts the registered application when that icon is clicked.</span></span>

### <a name="how-to-register-as-the-default-email-client"></a><span data-ttu-id="29e3e-176">Comment s’inscrire en tant que client de messagerie par défaut</span><span class="sxs-lookup"><span data-stu-id="29e3e-176">How to Register as the Default EMail Client</span></span>

<span data-ttu-id="29e3e-177">**HKEY \_ La \_** \\  \\  \\ **messagerie** des clients de logiciels de l’ordinateur local peut contenir zéro, une ou plusieurs sous-clés, une pour chaque application de messagerie inscrite.</span><span class="sxs-lookup"><span data-stu-id="29e3e-177">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** can contain zero or more subkeys, one for each registered email application.</span></span> <span data-ttu-id="29e3e-178">Par exemple, un système hypothétique peut définir les sous-clés suivantes :</span><span class="sxs-lookup"><span data-stu-id="29e3e-178">For example, a hypothetical system might define the following subkeys:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            Eudora
            Windows Mail
```

<span data-ttu-id="29e3e-179">Nous présenterons les entrées de Registre avec un client de messagerie hypothétique appelé « lit mail » de la société fictive nommée Litware Inc. Litware Inc. Décide d’inscrire ce client de messagerie sous le nom interne « LitMail ».</span><span class="sxs-lookup"><span data-stu-id="29e3e-179">We will demonstrate registry entries with a hypothetical email client called "Lit Mail" from the fictional company called Litware Inc. Litware Inc. decides to register this email client under the internal name "LitMail".</span></span> <span data-ttu-id="29e3e-180">Comme avec un navigateur, le nom interne est une chaîne unique utilisée comme nom de sous-clé, mais elle n’est jamais affichée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29e3e-180">As with a browser, the internal name is a unique string used as the subkey name, but it is never shown to the user.</span></span>

<span data-ttu-id="29e3e-181">Pour installer le client de messagerie lit mail comme par défaut, il utilise la sous-clé suivante et ses entrées :</span><span class="sxs-lookup"><span data-stu-id="29e3e-181">To install the Lit Mail email client as the default, they use the following subkey and its entries:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               (Default) = Lit Mail
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-456
```

<span data-ttu-id="29e3e-182">Les données LocalizedString sont de type REG \_ SZ, ou reg \_ expand \_ SZ si les variables de chemin d’accès telles que `%programfiles%` sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="29e3e-182">The LocalizedString data is of type REG\_SZ, or REG\_EXPAND\_SZ if path variables such as `%programfiles%` are used.</span></span> <span data-ttu-id="29e3e-183">LocalizedString fournit le chemin d’un fichier exécutable (. exe) ou d’un fichier de bibliothèque (. dll).</span><span class="sxs-lookup"><span data-stu-id="29e3e-183">LocalizedString provides the path to an executable (.exe) or library (.dll) file.</span></span> <span data-ttu-id="29e3e-184">Notez que la chaîne de chemin d’accès commence par un signe « at » (@) et qu’aucun guillemet n’est requis autour du chemin d’accès, quels que soient les espaces qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="29e3e-184">Note that the path string begins with an "at" sign (@) and that no quotation marks are required around the path regardless of spaces within it.</span></span> <span data-ttu-id="29e3e-185">L’entier décimal est l’ID d’une ressource de type chaîne, contenue dans la DLL spécifiée, dont la valeur doit être affichée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29e3e-185">The decimal integer is the ID of a string resource, contained within the specified DLL, whose value is to be displayed to the user.</span></span> <span data-ttu-id="29e3e-186">Cela permet d’utiliser la même inscription pour plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="29e3e-186">This enables the same registration to be used for multiple languages.</span></span> <span data-ttu-id="29e3e-187">Chaque langue fournit une ResourceDLL.dll différente.</span><span class="sxs-lookup"><span data-stu-id="29e3e-187">Each language provides a different ResourceDLL.dll.</span></span> <span data-ttu-id="29e3e-188">Cela permet au système d’afficher la chaîne correcte en fonction de la langue actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="29e3e-188">This enables the system to display the correct string based on the currently selected language.</span></span>

<span data-ttu-id="29e3e-189">Après la mise à jour des sous-clés appropriées, l’application diffuse le message [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) avec son paramètre *wParam* défini sur 0 et son paramètre *lParam* pointant vers la chaîne terminée par le caractère null `"Software\Clients\Mail"` .</span><span class="sxs-lookup"><span data-stu-id="29e3e-189">After updating the appropriate subkeys, the application broadcasts the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with its *wParam* parameter set to 0 and its *lParam* parameter pointing to the null-terminated string `"Software\Clients\Mail"`.</span></span> <span data-ttu-id="29e3e-190">Cela indique au système d’exploitation que le client par défaut a changé.</span><span class="sxs-lookup"><span data-stu-id="29e3e-190">This notifies the operating system that the default client has changed.</span></span>

<span data-ttu-id="29e3e-191">Pour assurer la compatibilité descendante avec les applications qui ne prennent pas en charge les chaînes localisées, le nom de l’application dans la langue installée doit également être défini comme valeur par défaut de la sous-clé.</span><span class="sxs-lookup"><span data-stu-id="29e3e-191">For backward compatibility with applications that do not support localized strings, the name of the application in the installed language should also be set as the default value for the subkey.</span></span>

<span data-ttu-id="29e3e-192">La valeur de la commande **reg \_ SZ** ou **reg \_ expand développée \_** suivante indique au menu Démarrer de l’icône par défaut de s’afficher lorsque l’utilisateur sélectionne lit mail comme programme de messagerie du menu Démarrer :</span><span class="sxs-lookup"><span data-stu-id="29e3e-192">The following **REG\_SZ** or **REG\_EXPAND\_SZ** value informs the Start menu of the default icon to display when the user selects Lit Mail as the Start menu mail program:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitMail.exe,1
```

<span data-ttu-id="29e3e-193">L’entrée suivante spécifie une ligne de commande à exécuter lorsque l’utilisateur clique sur l’élément de menu de **messagerie** dans le menu Démarrer, en supposant que lit mail est le programme de messagerie du menu Démarrer sélectionné.</span><span class="sxs-lookup"><span data-stu-id="29e3e-193">The following entry specifies a command line to run when the user clicks the **E-mail** menu item on the Start menu, assuming that Lit Mail is the selected Start menu email program.</span></span> <span data-ttu-id="29e3e-194">Cette ligne de commande s’exécute également si l’utilisateur sélectionne **lire le courrier électronique** dans le menu **Outils** de Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="29e3e-194">This command line is also run if the user selects **Read email** from the Windows Internet Explorer **Tools** menu.</span></span> <span data-ttu-id="29e3e-195">Les données sont de type **reg \_ SZ** ou **reg \_ expand \_ SZ**, mais notez qu’étant donné qu’il y a un espace dans le chemin d’accès à la ligne de commande, le chemin d’accès de l’exécutable est placé entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="29e3e-195">The data is of type **REG\_SZ** or **REG\_EXPAND\_SZ**, but notice that because there is a space in the command-line path, the executable path is enclosed in quotation marks.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            shell
               open
                  command
                     (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -inbox
```

<span data-ttu-id="29e3e-196">Si (et seulement si) *l’utilisateur* spécifie lit mail comme l’application de messagerie du menu démarrer par défaut, l’application de messagerie lit peut écrire son nom interne à la valeur de **reg \_ SZ** suivante :</span><span class="sxs-lookup"><span data-stu-id="29e3e-196">If (and only if) *the user* specifies Lit Mail to be the default Start menu email application, the Lit Mail application may write its internal name to the following **REG\_SZ** value:</span></span>

```
HKEY_CURRENT_USER
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

<span data-ttu-id="29e3e-197">Si (et seulement si) *l’utilisateur* spécifie lit mail comme étant l’application de messagerie par défaut au niveau du système, l’application lit mail peut écrire son nom interne sur la valeur **reg \_ SZ** spécifiée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="29e3e-197">If (and only if) *the user* specifies Lit Mail to be the system-wide default email application, the Lit Mail application may write its internal name to the **REG\_SZ** value specified below.</span></span> <span data-ttu-id="29e3e-198">Notez que l’accès à cette sous-clé peut être restreint.</span><span class="sxs-lookup"><span data-stu-id="29e3e-198">Note that access to this subkey might be restricted.</span></span> <span data-ttu-id="29e3e-199">Les applications ne doivent pas supposer que tous les utilisateurs sont autorisés à modifier l’application de messagerie par défaut au niveau du système.</span><span class="sxs-lookup"><span data-stu-id="29e3e-199">Applications should not assume that all users have permission to change the system-wide default email application.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

<span data-ttu-id="29e3e-200">L’inscription en tant qu’application de messagerie du menu démarrer par défaut n’est pas équivalente à l’inscription en tant que client de messagerie par défaut système ou le gestionnaire *mailto* inscrit.</span><span class="sxs-lookup"><span data-stu-id="29e3e-200">Registration as the default Start menu email application is not equivalent to registration as the system default email client or the registered *mailto* handler.</span></span>

-   <span data-ttu-id="29e3e-201">Le client de messagerie par défaut du système est démarré lorsque l’utilisateur clique sur **lire le courrier électronique** dans le menu **Outils** d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="29e3e-201">The system default email client is started when the user clicks **Read email** from the Internet Explorer **Tools** menu.</span></span>
-   <span data-ttu-id="29e3e-202">Le gestionnaire *mailto* inscrit est démarré lorsque l’utilisateur clique sur une URL au format `mailto:someone@example.com` .</span><span class="sxs-lookup"><span data-stu-id="29e3e-202">The registered *mailto* handler is started when the user clicks a URL of the form `mailto:someone@example.com`.</span></span>
-   <span data-ttu-id="29e3e-203">L’application de messagerie du menu Démarrer démarre lorsque l’utilisateur clique sur l’icône de **courrier électronique** dans le menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="29e3e-203">The Start menu email application is started when the user clicks the **E-mail** icon on the Start menu.</span></span>

<span data-ttu-id="29e3e-204">Si aucune application de messagerie du menu démarrer par défaut n’est spécifiée, l’icône de courrier électronique dans le menu Démarrer lance le client de messagerie par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="29e3e-204">If no default Start menu email application is specified, the Email icon on the Start menu launches the system default email client.</span></span>

<span data-ttu-id="29e3e-205">Cette rubrique ne couvre pas l’inscription de l’application en tant que gestionnaire de protocole *mailto* par défaut.</span><span class="sxs-lookup"><span data-stu-id="29e3e-205">This topic does not cover registration of the application as the default *mailto* protocol handler.</span></span> <span data-ttu-id="29e3e-206">Les applications qui veulent s’inscrire de cette manière doivent continuer à suivre les spécifications existantes sur ce sujet.</span><span class="sxs-lookup"><span data-stu-id="29e3e-206">Applications that want to register in such a manner should continue to follow existing specifications on this subject.</span></span>

## <a name="customizing-the-context-menu"></a><span data-ttu-id="29e3e-207">Personnalisation du menu contextuel</span><span class="sxs-lookup"><span data-stu-id="29e3e-207">Customizing the Context Menu</span></span>

<span data-ttu-id="29e3e-208">Une application peut personnaliser les pages de propriétés qui s’affichent lorsque l’utilisateur sélectionne des **Propriétés** dans le menu contextuel de l’icône **courrier électronique** (ou **Internet**).</span><span class="sxs-lookup"><span data-stu-id="29e3e-208">An application can customize the property pages that are displayed when the user selects **Properties** from the **E-mail** (or **Internet**) icon's shortcut menu.</span></span> <span data-ttu-id="29e3e-209">Par exemple, l’application de messagerie Litware ajoute les données **reg \_ SZ** ou **reg \_ développé \_** suivantes pour afficher une feuille de propriétés personnalisée pour l’icône de **courrier électronique** plutôt que sa feuille de propriétés par défaut.</span><span class="sxs-lookup"><span data-stu-id="29e3e-209">For example, the Litware email application adds the following **REG\_SZ** or **REG\_EXPAND\_SZ** data to display a custom property sheet for the **E-mail** icon rather than its default property sheet.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  properties
                     MUIVerb = @C:\Program Files\LitwareInc\ResourceDLL.dll,-789
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -properties
```

<span data-ttu-id="29e3e-210">L’élément de données MUIVerb est construit à partir d’un signe « at » (@), suivi du chemin d’accès complet à la DLL de ressource, d’une virgule, d’un signe moins (-), puis de l’identificateur de ressource de chaîne décimale à afficher.</span><span class="sxs-lookup"><span data-stu-id="29e3e-210">The MUIVerb data item is constructed beginning with an "at" sign (@), followed by the full path to the resource DLL, a comma, a minus sign (-), and then the decimal string resource identifier to display.</span></span> <span data-ttu-id="29e3e-211">Notez que le chemin d’accès au programme LitMail.exe contient des espaces, donc la chaîne du chemin d’accès est placée entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="29e3e-211">Note that the path to the LitMail.exe program contains spaces, so the path string is placed inside quotation marks.</span></span>

<span data-ttu-id="29e3e-212">Une application peut également ajouter des commandes supplémentaires au menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="29e3e-212">An application can also add additional commands to the context menu.</span></span> <span data-ttu-id="29e3e-213">Par exemple, l’application de messagerie Litware ajoute une commande **Find** avec les données de **reg \_ SZ** suivantes :</span><span class="sxs-lookup"><span data-stu-id="29e3e-213">For example, the Litware email application adds a **find** command with the following **REG\_SZ** data:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  find
                     MUIVerb = @C:\Program File\LitwareInc\ResourceDLL.dll,-790
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -contacts
```

<span data-ttu-id="29e3e-214">Le nom de la sous-clé sous l' **interpréteur** de commandes (dans le cas présent, « Find ») est un nom arbitraire et non localisé.</span><span class="sxs-lookup"><span data-stu-id="29e3e-214">The subkey name below **shell** (in this case, "find") is an arbitrary, nonlocalized name.</span></span> <span data-ttu-id="29e3e-215">Une fois encore, les données MUIVerb contiennent un signe « at » (@) comme premier élément, suivi du chemin d’accès à une DLL de ressource, d’un séparateur de virgule, puis d’un signe moins avant l’identificateur de ressource de chaîne décimale.</span><span class="sxs-lookup"><span data-stu-id="29e3e-215">Once again the MUIVerb data contains an "at" sign (@) as the first element, followed by the path to a resource DLL, a comma separator, and then a minus sign preceding the decimal string resource identifier.</span></span> <span data-ttu-id="29e3e-216">Par exemple, cette ressource de type chaîne peut être « ouvrir le carnet d’adresses ».</span><span class="sxs-lookup"><span data-stu-id="29e3e-216">For example, that string resource might be "Open Address Book".</span></span> <span data-ttu-id="29e3e-217">Enfin, Notez que la chaîne de ligne de commande contient des espaces, donc elle est placée entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="29e3e-217">Finally, note that the command-line string contains spaces, so it is enclosed in quotation marks.</span></span>

 

 
