---
title: Inscription aux technologies d’assistance d’ergonomie
description: Cet article explique comment inscrire une application d’accessibilité à l’aide de la facilité d’accès du centre d’accès. Il explique également comment adapter votre application d’accessibilité de manière à ce qu’elle fonctionne correctement avec le Bureau sécurisé.
ms.assetid: 6F1F2AAE-B2E4-4F26-8BDF-A3DE8F5C5460
ms.topic: article
ms.date: 04/02/2019
ms.openlocfilehash: 66901cd899fc578b032f86e3752fcdcac0788ba1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106518025"
---
# <a name="ease-of-access---assistive-technology-registration"></a><span data-ttu-id="22d53-104">Inscription aux technologies d’assistance d’ergonomie</span><span class="sxs-lookup"><span data-stu-id="22d53-104">Ease of Access   Assistive Technology Registration</span></span>

<span data-ttu-id="22d53-105">Cet article explique comment inscrire une application d’accessibilité à l’aide de la facilité d’accès du centre d’accès.</span><span class="sxs-lookup"><span data-stu-id="22d53-105">This article explains how to register an accessibility application with the Ease of Access Center.</span></span> <span data-ttu-id="22d53-106">Il explique également comment adapter votre application d’accessibilité de manière à ce qu’elle fonctionne correctement avec le Bureau sécurisé.</span><span class="sxs-lookup"><span data-stu-id="22d53-106">It also explains how to tailor your accessibility application so it works well with the secure desktop.</span></span>

<span data-ttu-id="22d53-107">La facilité d’accès est une application de panneau de configuration pour Microsoft Windows qui rassemble des fonctionnalités d’accessibilité et de facilité d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="22d53-107">The Ease of Access Center is a Control Panel application for Microsoft Windows brings together functionality for accessibility and ease of use.</span></span> <span data-ttu-id="22d53-108">Grâce à la facilité d’accès, les utilisateurs peuvent configurer leurs ordinateurs en fonction de leurs besoins physiques et cognitifs.</span><span class="sxs-lookup"><span data-stu-id="22d53-108">By using the Ease of Access Center, users can configure their computers to suit their physical and cognitive needs.</span></span>

<span data-ttu-id="22d53-109">L’une des fonctions de la facilité d’accès du centre d’accès est d’aider les utilisateurs à lancer des applications d’accessibilité, notamment le narrateur, le clavier visuel et la loupe.</span><span class="sxs-lookup"><span data-stu-id="22d53-109">One function of the Ease of Access Center is to help users launch accessibility applications, including Narrator, On-Screen Keyboard, and Magnifier.</span></span> <span data-ttu-id="22d53-110">Les applications tierces inscrites apparaissent également dans la facilité d’accès du centre d’accès et peuvent être lancées directement à partir de là.</span><span class="sxs-lookup"><span data-stu-id="22d53-110">Registered third-party applications also appear in the Ease of Access Center and can be launched directly from there.</span></span>

<span data-ttu-id="22d53-111">Les applications d’accessibilité doivent fonctionner correctement avec le Bureau sécurisé.</span><span class="sxs-lookup"><span data-stu-id="22d53-111">Accessibility applications need to work smoothly with the secure desktop.</span></span> <span data-ttu-id="22d53-112">Le Bureau sécurisé est l’interface utilisateur qui s’affiche lorsque l’ordinateur est verrouillé (au moment de l’ouverture de session ou lorsque l’utilisateur a verrouillé le bureau), et lorsque l’utilisateur est invité à autoriser une action potentiellement dangereuse.</span><span class="sxs-lookup"><span data-stu-id="22d53-112">The secure desktop is the user interface that appears when the computer is locked (at log-on or when the user has locked the desktop), and when the user is prompted to allow a potentially unsafe action.</span></span> <span data-ttu-id="22d53-113">Pour des raisons de sécurité, Windows place les limites sur les logiciels tiers s’exécutant sur le Bureau sécurisé.</span><span class="sxs-lookup"><span data-stu-id="22d53-113">For security reasons, Windows places limits on third-party software running on the secure desktop.</span></span> <span data-ttu-id="22d53-114">Si vous souhaitez que votre application d’accessibilité s’exécute sur le Bureau sécurisé, vous devez inscrire l’application à l’aide de la facilité d’accès du centre d’accès.</span><span class="sxs-lookup"><span data-stu-id="22d53-114">If you want your accessibility application to run on the secure desktop, you need to register the application with the Ease of Access Center.</span></span>

## <a name="registering-with-the-ease-of-access-center"></a><span data-ttu-id="22d53-115">Inscription avec la facilité d’accès du centre d’accès</span><span class="sxs-lookup"><span data-stu-id="22d53-115">Registering with the Ease of Access Center</span></span>

<span data-ttu-id="22d53-116">Les applications d’accessibilité s’inscrivent dans la facilité d’accès du centre d’accès en créant une ou plusieurs clés de registre lors de l’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="22d53-116">Accessibility applications register with the Ease of Access Center by creating one or more registry keys when the application is installed.</span></span> <span data-ttu-id="22d53-117">Le tableau suivant répertorie les informations contenues dans les clés de registre.</span><span class="sxs-lookup"><span data-stu-id="22d53-117">The following table lists the information contained in the registry keys.</span></span>



| <span data-ttu-id="22d53-118">Nom</span><span class="sxs-lookup"><span data-stu-id="22d53-118">Name</span></span>                        | <span data-ttu-id="22d53-119">Description</span><span class="sxs-lookup"><span data-stu-id="22d53-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="22d53-120">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="22d53-120">Mandatory/Optional</span></span> | <span data-ttu-id="22d53-121">Language</span><span class="sxs-lookup"><span data-stu-id="22d53-121">Language</span></span>      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
| <span data-ttu-id="22d53-122">Nom de l’application</span><span class="sxs-lookup"><span data-stu-id="22d53-122">Application Name</span></span>            | <span data-ttu-id="22d53-123">Nom de l’application, qui se trouve dans un fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="22d53-123">The name of the application, which is in a resource file.</span></span> <span data-ttu-id="22d53-124">Cette valeur de registre contient une chaîne dans un format spécifié.</span><span class="sxs-lookup"><span data-stu-id="22d53-124">This registry value contains a string in a specified format.</span></span> <span data-ttu-id="22d53-125">Il peut s’agir d’une version localisée du nom de l’application, si l’application est localisée dans une langue autre que l’anglais.</span><span class="sxs-lookup"><span data-stu-id="22d53-125">This could be a localized version of the application name, if the application is localized in languages other than English.</span></span> <span data-ttu-id="22d53-126">Le nom s’affiche dans la facilité d’accès du centre d’accès.</span><span class="sxs-lookup"><span data-stu-id="22d53-126">The name appears in the Ease of Access Center.</span></span><br/>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="22d53-127">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="22d53-127">Mandatory</span></span>          | <span data-ttu-id="22d53-128">Localisée</span><span class="sxs-lookup"><span data-stu-id="22d53-128">Localized</span></span>     |
| <span data-ttu-id="22d53-129">ATExe</span><span class="sxs-lookup"><span data-stu-id="22d53-129">ATExe</span></span>                       | <span data-ttu-id="22d53-130">Nom de l’image ou du fichier exécutable de l’application.</span><span class="sxs-lookup"><span data-stu-id="22d53-130">The name of the application executable file or image.</span></span> <span data-ttu-id="22d53-131">Windows utilise cette valeur pour déterminer si l’application d’accessibilité est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="22d53-131">Windows uses this value to determine whether the accessibility application is running.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="22d53-132">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="22d53-132">Mandatory</span></span>          | <span data-ttu-id="22d53-133">Non localisé</span><span class="sxs-lookup"><span data-stu-id="22d53-133">Not localized</span></span> |
| <span data-ttu-id="22d53-134">CopySettingsToLockedDesktop</span><span class="sxs-lookup"><span data-stu-id="22d53-134">CopySettingsToLockedDesktop</span></span> | <span data-ttu-id="22d53-135">Valeur **DWORD** qui indique s’il faut copier les paramètres de l’application d’accessibilité sur le bureau verrouillé.</span><span class="sxs-lookup"><span data-stu-id="22d53-135">A **DWORD** value that indicates whether to copy the accessibility application's settings to the locked desktop.</span></span><br/> <span data-ttu-id="22d53-136">Si cette valeur est 1, l’application peut écrire des paramètres à un emplacement dans le registre de l’utilisateur, et Windows copie les paramètres dans le même emplacement dans le registre de l’utilisateur pour le bureau verrouillé.</span><span class="sxs-lookup"><span data-stu-id="22d53-136">If this value is 1, the application can write settings to a location in the user registry, and Windows copies the settings to the same location in the user registry for the locked desktop.</span></span> <span data-ttu-id="22d53-137">Cela permet à l’application de conserver son état du bureau « normal » sur le bureau verrouillé.</span><span class="sxs-lookup"><span data-stu-id="22d53-137">This enables the application to persist its state from the "normal" desktop to the locked desktop.</span></span><br/>                                                                                                                                                             | <span data-ttu-id="22d53-138">Facultatif</span><span class="sxs-lookup"><span data-stu-id="22d53-138">Optional</span></span>           | <span data-ttu-id="22d53-139">Non localisé</span><span class="sxs-lookup"><span data-stu-id="22d53-139">Not localized</span></span> |
| <span data-ttu-id="22d53-140">Description</span><span class="sxs-lookup"><span data-stu-id="22d53-140">Description</span></span>                 | <span data-ttu-id="22d53-141">Brève description de l’application, à partir d’un fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="22d53-141">A brief description of the application, from a resource file.</span></span> <span data-ttu-id="22d53-142">Cette valeur de registre contient une chaîne dans un format spécifié.</span><span class="sxs-lookup"><span data-stu-id="22d53-142">This registry value contains a string in a specified format.</span></span> <span data-ttu-id="22d53-143">Il peut s’agir d’une version localisée de la description, si l’application est localisée dans des langues autres que l’anglais.</span><span class="sxs-lookup"><span data-stu-id="22d53-143">This could be a localized version of the description, if the application is localized in languages other than English.</span></span> <span data-ttu-id="22d53-144">La longueur de cette chaîne doit être inférieure à 512 caractères.</span><span class="sxs-lookup"><span data-stu-id="22d53-144">The length of this string must be less than 512 characters.</span></span><br/> <span data-ttu-id="22d53-145">La description s’affiche dans la facilité d’accès du centre d’accès pour fournir à l’utilisateur des informations supplémentaires sur l’application d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="22d53-145">The description appears in the Ease of Access Center to provide additional information about the accessibility application to the user.</span></span><br/> <span data-ttu-id="22d53-146">Cette valeur peut également être utilisée pour informer l’utilisateur que l’application n’est pas utilisée sur le Bureau sécurisé.</span><span class="sxs-lookup"><span data-stu-id="22d53-146">This value can also be used to notify the user that the application is not used on the secure desktop.</span></span><br/>      | <span data-ttu-id="22d53-147">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="22d53-147">Mandatory</span></span>          | <span data-ttu-id="22d53-148">Localisée</span><span class="sxs-lookup"><span data-stu-id="22d53-148">Localized</span></span>     |
| <span data-ttu-id="22d53-149">Profil</span><span class="sxs-lookup"><span data-stu-id="22d53-149">Profile</span></span>                     | <span data-ttu-id="22d53-150">Bref morceau de code XML qui spécifie les logements fournis par l’application.</span><span class="sxs-lookup"><span data-stu-id="22d53-150">A short piece of XML that specifies the accommodations that the application provides.</span></span> <span data-ttu-id="22d53-151">Il garantit que l’application apparaît sous la catégorie appropriée dans la section facilité d’accès du centre d’accès.</span><span class="sxs-lookup"><span data-stu-id="22d53-151">It ensures that the application appears under the correct category in the Ease of Access Center.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="22d53-152">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="22d53-152">Mandatory</span></span>          | <span data-ttu-id="22d53-153">Non localisé</span><span class="sxs-lookup"><span data-stu-id="22d53-153">Not localized</span></span> |
| <span data-ttu-id="22d53-154">PassiveAutoStartBehavior</span><span class="sxs-lookup"><span data-stu-id="22d53-154">PassiveAutoStartBehavior</span></span>    | <p><span data-ttu-id="22d53-155">Valeur **DWORD** qui indique si le comportement de démarrage automatique hérité est activé.</span><span class="sxs-lookup"><span data-stu-id="22d53-155">A **DWORD** value that indicates whether legacy auto-start behavior is enabled.</span></span></p><p><span data-ttu-id="22d53-156">La valeur par défaut est 0, ce qui indique qu’un à nécessite un comportement de démarrage automatique hérité.</span><span class="sxs-lookup"><span data-stu-id="22d53-156">The default value is 0, which indicates that an AT requires legacy auto-start behavior.</span></span> <span data-ttu-id="22d53-157">Dans ce cas, le paramètre « démarrer après la connexion » de ce paramètre est activé dans l’OOBE (out of Box Experience) et le panneau de configuration (voir **panneau de configuration-> facilité d’accès-> facilité d’accès du centre d’accès-> modifier les paramètres de connexion**) et démarre automatiquement le à après l’affichage de l’UAC et l’écran de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="22d53-157">This  causes the “Start after sign-in” setting for that AT to be checked in the Out Of Box Experience (OOBE) and Control Panel (see **Control Panel -> Ease of Access -> Ease of Access Center -> Change sign-in settings**), and automatically starts the AT after UAC and lock-screen.</span></span></p><p><span data-ttu-id="22d53-158">La valeur 1 indique que le à doit utiliser le nouveau comportement de démarrage automatique lorsque le paramètre « démarrer après la connexion » de cet emplacement n’est pas activé dans l’expérience OOBE (out of Box Experience) et le panneau de configuration, et que le est démarré automatiquement une fois par session utilisateur (au moment de la connexion) uniquement si le paramètre « démarrer après la connexion » est activé.</span><span class="sxs-lookup"><span data-stu-id="22d53-158">A value of 1 indicates that the AT should use the new auto-start behavior where the “Start after sign-in” setting for that AT is not checked in the Out Of Box Experience (OOBE) and Control Panel, and the AT is automatically started once per user session (at login) only if the “start after sign-in” setting is checked.</span></span></p>                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="22d53-159">Facultatif</span><span class="sxs-lookup"><span data-stu-id="22d53-159">Optional</span></span>          | <span data-ttu-id="22d53-160">Non localisé</span><span class="sxs-lookup"><span data-stu-id="22d53-160">Not localized</span></span> |
| <span data-ttu-id="22d53-161">SecureDesktopAccommodation</span><span class="sxs-lookup"><span data-stu-id="22d53-161">SecureDesktopAccommodation</span></span>  | <span data-ttu-id="22d53-162">Nom d’une autre application d’accessibilité à exécuter sur le Bureau sécurisé à la place de cette application.</span><span class="sxs-lookup"><span data-stu-id="22d53-162">The name of an alternate accessibility application to run on the secure desktop in the place of this application.</span></span> <span data-ttu-id="22d53-163">L’alternative peut être une application différente, une version différente de la même application, l’une des applications d’accessibilité qui est incluse dans Windows, ou « None » si vous ne souhaitez pas exécuter une application d’accessibilité sur le Bureau sécurisé.</span><span class="sxs-lookup"><span data-stu-id="22d53-163">The alternate can be a different application, a different version of the same application, one of the accessibility applications that is included in Windows, or "none" if you do not want to run any accessibility application on the secure desktop.</span></span> <br/>                                                                                                                                                                                                               | <span data-ttu-id="22d53-164">Facultatif</span><span class="sxs-lookup"><span data-stu-id="22d53-164">Optional</span></span>           | <span data-ttu-id="22d53-165">Non localisé</span><span class="sxs-lookup"><span data-stu-id="22d53-165">Not localized</span></span> |
| <span data-ttu-id="22d53-166">Profil simple</span><span class="sxs-lookup"><span data-stu-id="22d53-166">Simple Profile</span></span>              | <span data-ttu-id="22d53-167">Valeur qui décrit comment classer l’application dans un ou deux mots : un lecteur d’écran, une loupe ou un clavier visuel, par exemple.</span><span class="sxs-lookup"><span data-stu-id="22d53-167">A value that describes how to classify the application in a word or two: Screen reader, Magnifier, or On-screen keyboard, for example.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="22d53-168">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="22d53-168">Mandatory</span></span>          | <span data-ttu-id="22d53-169">Non localisé</span><span class="sxs-lookup"><span data-stu-id="22d53-169">Not localized</span></span> |
| <span data-ttu-id="22d53-170">Variable startexe</span><span class="sxs-lookup"><span data-stu-id="22d53-170">StartExe</span></span>                    | <span data-ttu-id="22d53-171">Chemin d’accès complet de l’exécutable.</span><span class="sxs-lookup"><span data-stu-id="22d53-171">The full path of the executable.</span></span> <span data-ttu-id="22d53-172">Cette valeur est utilisée pour lancer l’application d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="22d53-172">This value is used to launch the accessibility application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="22d53-173">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="22d53-173">Mandatory</span></span>          | <span data-ttu-id="22d53-174">Non localisé</span><span class="sxs-lookup"><span data-stu-id="22d53-174">Not localized</span></span> |
| <span data-ttu-id="22d53-175">StartParams</span><span class="sxs-lookup"><span data-stu-id="22d53-175">StartParams</span></span>                 | <span data-ttu-id="22d53-176">Arguments de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="22d53-176">Command-line arguments.</span></span> <span data-ttu-id="22d53-177">Ces valeurs sont utilisées avec variable startexe pour démarrer l’application.</span><span class="sxs-lookup"><span data-stu-id="22d53-177">These values are used along with StartExe to start the application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="22d53-178">Facultatif</span><span class="sxs-lookup"><span data-stu-id="22d53-178">Optional</span></span>           | <span data-ttu-id="22d53-179">Non localisé</span><span class="sxs-lookup"><span data-stu-id="22d53-179">Not localized</span></span> |
| <span data-ttu-id="22d53-180">TerminateOnDesktopSwitch</span><span class="sxs-lookup"><span data-stu-id="22d53-180">TerminateOnDesktopSwitch</span></span>    | <span data-ttu-id="22d53-181">Valeur **DWORD** qui spécifie la manière dont l’application d’accessibilité répond aux transitions vers ou à partir du Bureau sécurisé.</span><span class="sxs-lookup"><span data-stu-id="22d53-181">A **DWORD** value that specifies how the accessibility application responds to transitions to or from the secure desktop.</span></span><br/> <span data-ttu-id="22d53-182">Si cette valeur n’existe pas ou est 1, Windows termine et redémarre l’application à chaque transition vers ou à partir du Bureau sécurisé.</span><span class="sxs-lookup"><span data-stu-id="22d53-182">If this value does not exist or is 1, Windows terminates and restarts the application on each transition to or from the secure desktop.</span></span> <span data-ttu-id="22d53-183">Il s'agit du comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="22d53-183">This is the default behavior.</span></span><br/> <span data-ttu-id="22d53-184">Si cette valeur est égale à 0, Windows ne met pas fin à l’application d’accessibilité sur une transition sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="22d53-184">If this value is 0, Windows does not terminate the accessibility application on a desktop transition.</span></span> <span data-ttu-id="22d53-185">L’application continue de s’exécuter sur le poste de travail précédent, et Windows démarre une nouvelle instance sur le nouveau bureau si aucune instance n’est déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="22d53-185">The application continues to run on the previous desktop, and Windows starts a new instance on the new desktop if an instance is not already running there.</span></span><br/> | <span data-ttu-id="22d53-186">Facultatif</span><span class="sxs-lookup"><span data-stu-id="22d53-186">Optional</span></span>           | <span data-ttu-id="22d53-187">Non localisé</span><span class="sxs-lookup"><span data-stu-id="22d53-187">Not localized</span></span> |


 

### <a name="localization"></a><span data-ttu-id="22d53-188">Localisation</span><span class="sxs-lookup"><span data-stu-id="22d53-188">Localization</span></span>

<span data-ttu-id="22d53-189">Les valeurs de Registre du nom et de la description de l’application doivent être localisables pour prendre en charge l’interface utilisateur multilingue (MUI).</span><span class="sxs-lookup"><span data-stu-id="22d53-189">The registry values of Application Name and Description need to be localizable to support Multilingual User Interface (MUI).</span></span>

<span data-ttu-id="22d53-190">Ces chaînes sont au format suivant, où les crochets pointent les éléments requis et les crochets signifient un élément facultatif.</span><span class="sxs-lookup"><span data-stu-id="22d53-190">These strings are in the following format, where angle brackets signify required elements and square brackets signify an optional element.</span></span>

<span data-ttu-id="22d53-191">*@ <ResDllPath \\ ResDLLFilename>,- <resID> \[ ;<comment>\]*</span><span class="sxs-lookup"><span data-stu-id="22d53-191">*@<ResDllPath\\ResDLLFilename>,-<resID>\[;<comment>\]*</span></span>

<span data-ttu-id="22d53-192">*<ResDllPath \\ ResDLLFilename>* est le chemin d’accès à la dll de ressource.</span><span class="sxs-lookup"><span data-stu-id="22d53-192">*<ResDllPath\\ResDLLFilename>* is the path to the resource DLL.</span></span> <span data-ttu-id="22d53-193">Le chemin d’accès peut contenir des variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="22d53-193">The path can contain environmental variables.</span></span>

<span data-ttu-id="22d53-194">*<resID>* ID de ressource de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="22d53-194">*<resID>* is the resource ID for the string.</span></span>

<span data-ttu-id="22d53-195">le *\[ Commentaire \]* contient des commentaires facultatifs.</span><span class="sxs-lookup"><span data-stu-id="22d53-195">*\[comment\]* contains any optional comments.</span></span>

<span data-ttu-id="22d53-196">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="22d53-196">Here is an example:</span></span>


```
@%SystemRoot%\system32\anyAT.dll,-5020
```



<span data-ttu-id="22d53-197">Pour plus d’informations sur MUI, voir [Centre de connaissances Windows MUI](../intl/about-multilingual-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="22d53-197">For more information about MUI, see [Windows MUI Knowledge Center](../intl/about-multilingual-user-interface.md).</span></span>

### <a name="hci-profile"></a><span data-ttu-id="22d53-198">Profil HCI</span><span class="sxs-lookup"><span data-stu-id="22d53-198">HCI Profile</span></span>

<span data-ttu-id="22d53-199">Le profil HCI est un moyen de déterminer les logements à fournir en fonction des besoins de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="22d53-199">The Human Computer Interaction (HCI) profile is a way to determine what accommodations to provide based on the needs of the user.</span></span> <span data-ttu-id="22d53-200">Les applications d’accessibilité doivent enregistrer des informations sur le type de handicap que l’application aide à prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="22d53-200">Accessibility applications should register information about the kind of disability the application helps to accommodate.</span></span>

<span data-ttu-id="22d53-201">La valeur de Registre du profil contient du code XML qui décrit le type d’invalidité ciblé par l’application d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="22d53-201">The Profile registry value contains XML that describes the kind of disability targeted by the accessibility application.</span></span> <span data-ttu-id="22d53-202">Ce code XML a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="22d53-202">This XML has the following format:</span></span>


```XML
<HCIModel>
<Accommodation type="disability"/>
</HCIModel>
```



<span data-ttu-id="22d53-203">Les valeurs valides pour l’attribut de **type d’hébergement** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="22d53-203">The valid values for the **Accommodation type** attribute are as follows:</span></span>

-   <span data-ttu-id="22d53-204">vision légère</span><span class="sxs-lookup"><span data-stu-id="22d53-204">mild vision</span></span>
-   <span data-ttu-id="22d53-205">vision sérieuse</span><span class="sxs-lookup"><span data-stu-id="22d53-205">severe vision</span></span>
-   <span data-ttu-id="22d53-206">cognitive légère</span><span class="sxs-lookup"><span data-stu-id="22d53-206">mild cognitive</span></span>
-   <span data-ttu-id="22d53-207">grave cognitive</span><span class="sxs-lookup"><span data-stu-id="22d53-207">severe cognitive</span></span>
-   <span data-ttu-id="22d53-208">dextérité légère</span><span class="sxs-lookup"><span data-stu-id="22d53-208">mild dexterity</span></span>
-   <span data-ttu-id="22d53-209">dextérité grave</span><span class="sxs-lookup"><span data-stu-id="22d53-209">severe dexterity</span></span>
-   <span data-ttu-id="22d53-210">audition légère</span><span class="sxs-lookup"><span data-stu-id="22d53-210">mild hearing</span></span>
-   <span data-ttu-id="22d53-211">audition grave</span><span class="sxs-lookup"><span data-stu-id="22d53-211">severe hearing</span></span>
-   <span data-ttu-id="22d53-212">discours modéré</span><span class="sxs-lookup"><span data-stu-id="22d53-212">mild speech</span></span>
-   <span data-ttu-id="22d53-213">discours grave</span><span class="sxs-lookup"><span data-stu-id="22d53-213">severe speech</span></span>

> [!Note]  
> <span data-ttu-id="22d53-214">Ces valeurs respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="22d53-214">These values are case sensitive.</span></span>

 

<span data-ttu-id="22d53-215">Si une application d’accessibilité prend en charge plusieurs logements, la valeur de registre de profil doit inclure un attribut de **type d’hébergement** pour chaque hébergement.</span><span class="sxs-lookup"><span data-stu-id="22d53-215">If an accessibility application supports multiple accommodations, the Profile registry value should include an **Accommodation type** attribute for each accommodation.</span></span>

### <a name="ease-of-access-registry-details"></a><span data-ttu-id="22d53-216">Détails du registre d’ergonomie</span><span class="sxs-lookup"><span data-stu-id="22d53-216">Ease of Access registry details</span></span>

<span data-ttu-id="22d53-217">Pour inscrire votre application d’accessibilité, vous devez créer une clé pour votre application à l’emplacement de Registre suivant et la remplir avec des paires nom-valeur.</span><span class="sxs-lookup"><span data-stu-id="22d53-217">To register your accessibility application, you need to create a key for your application at the following registry location and populate it with name-value pairs.</span></span>

<span data-ttu-id="22d53-218">**HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS\\**</span><span class="sxs-lookup"><span data-stu-id="22d53-218">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\**</span></span>

<span data-ttu-id="22d53-219">Nommez la clé de registre de votre application en utilisant le format suivant :</span><span class="sxs-lookup"><span data-stu-id="22d53-219">Name your application's registry key using the following format:</span></span>

<span data-ttu-id="22d53-220">*« CompanyName \_ ProductName \_ v \# »*</span><span class="sxs-lookup"><span data-stu-id="22d53-220">*"CompanyName\_ProductName\_v\#"*</span></span>

<span data-ttu-id="22d53-221">Par exemple, « Contoso \_ magnifier \_ v 2.0 ».</span><span class="sxs-lookup"><span data-stu-id="22d53-221">For example, "Contoso\_Magnifier\_v2.0".</span></span>

<span data-ttu-id="22d53-222">Pour ajouter des valeurs de Registre, votre programme d’installation doit être exécuté avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="22d53-222">To add registry values, your installation program must be running with elevated privileges.</span></span>

### <a name="secure-desktop-accommodation"></a><span data-ttu-id="22d53-223">Hébergement de postes de travail sécurisé</span><span class="sxs-lookup"><span data-stu-id="22d53-223">Secure desktop accommodation</span></span>

<span data-ttu-id="22d53-224">La clé de Registre **SecureDesktopAccommodation** vous permet de spécifier la manière dont votre application d’accessibilité répond au Bureau sécurisé.</span><span class="sxs-lookup"><span data-stu-id="22d53-224">The **SecureDesktopAccommodation** registry key lets you specify how your accessibility application responds to the secure desktop.</span></span> <span data-ttu-id="22d53-225">Par défaut, le centre d’ergonomie lance votre application sur le Bureau sécurisé s’il était déjà en cours d’exécution sur le bureau normal, ou s’il est configuré pour s’exécuter sur le Bureau d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="22d53-225">By default, the Ease of Access Center launches your application on the secure desktop if it was already running on the normal desktop, or if it is configured to run on the logon desktop.</span></span> <span data-ttu-id="22d53-226">À l’aide de la clé **SecureDesktopAccommodation** , vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="22d53-226">By using the **SecureDesktopAccommodation** key, you can:</span></span>

-   <span data-ttu-id="22d53-227">Spécifiez une autre version de votre application pour une utilisation sur le Bureau sécurisé.</span><span class="sxs-lookup"><span data-stu-id="22d53-227">Specify an alternate version of your application for use on the secure desktop.</span></span> <span data-ttu-id="22d53-228">Par exemple, vous pouvez avoir une autre version qui désactive les fonctionnalités non sécurisées ou qui est optimisée pour utiliser moins de mémoire et démarrer plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="22d53-228">For example, you might have an alternate version that disables unsecured features, or is optimized to use less memory and launch faster.</span></span>

    <span data-ttu-id="22d53-229">Pour spécifier la version alternative, définissez la clé **SecureDesktopAccommodation** sur le nom de l’autre version.</span><span class="sxs-lookup"><span data-stu-id="22d53-229">To specify the alternate version, set the **SecureDesktopAccommodation** key to the name of the alternate version.</span></span> <span data-ttu-id="22d53-230">Par exemple, si vous avez inscrit votre application à la \_ clé de lecteur d’écran Contoso \_ v 1.0, vous pouvez inscrire la version alternative sur l' \_ écran contoso ReaderSecure \_ v 1.0.</span><span class="sxs-lookup"><span data-stu-id="22d53-230">For example, if you registered your application at the Contoso\_Screen Reader\_v1.0 key, you could register the alternate version at Contoso\_Screen ReaderSecure\_v1.0.</span></span> <span data-ttu-id="22d53-231">Ensuite, définissez la clé **SecureDesktopAccommodation** du \_ lecteur d’écran Contoso \_ v 1.0 sur « Contoso \_ Screen ReaderSecure \_ v 1.0 ».</span><span class="sxs-lookup"><span data-stu-id="22d53-231">Then, set the **SecureDesktopAccommodation** key of Contoso\_Screen Reader\_v1.0 to "Contoso\_Screen ReaderSecure\_v1.0".</span></span>

-   <span data-ttu-id="22d53-232">Spécifiez une application d’accessibilité Microsoft à utiliser sur le Bureau sécurisé à la place de votre application.</span><span class="sxs-lookup"><span data-stu-id="22d53-232">Specify a Microsoft accessibility application to use on the secure desktop in place of your application.</span></span> <span data-ttu-id="22d53-233">Pour cette option, définissez **SecureDesktopAccommodation** sur le nom de l’application d’accessibilité Microsoft : « OSK », « magnifierpane » ou « Narrator ».</span><span class="sxs-lookup"><span data-stu-id="22d53-233">For this option, set **SecureDesktopAccommodation** to the name of the particular Microsoft accessibility application: "osk", "magnifierpane", or "Narrator".</span></span>
-   <span data-ttu-id="22d53-234">Spécifiez que votre application ne doit pas s’exécuter sur le Bureau sécurisé et aucune autre application.</span><span class="sxs-lookup"><span data-stu-id="22d53-234">Specify that your application should not run on the secure desktop, and neither should any alternate application.</span></span> <span data-ttu-id="22d53-235">Pour cette option, affectez à **SecureDesktopAccommodation** la valeur « None » (recommandé) ou le nom d’une application inexistante.</span><span class="sxs-lookup"><span data-stu-id="22d53-235">For this option, set **SecureDesktopAccommodation** to "none" (recommend) or the name of a nonexistent application.</span></span>

<span data-ttu-id="22d53-236">Si la clé de Registre **SecureDesktopAccommodation** pour votre application d’accessibilité spécifie une application d’accessibilité Microsoft à exécuter sur le Bureau sécurisé à la place de votre application, Windows en avertit l’utilisateur lors de la transition vers le Bureau sécurisé.</span><span class="sxs-lookup"><span data-stu-id="22d53-236">If the **SecureDesktopAccommodation** registry key for your accessibility application specifies a Microsoft accessibility application to run on the secure desktop in place of your application, Windows notifies the user of this when making the transition to the secure desktop.</span></span> <span data-ttu-id="22d53-237">Pour avertir l’utilisateur, Windows affiche la chaîne spécifiée dans la clé de Registre Description de votre application.</span><span class="sxs-lookup"><span data-stu-id="22d53-237">To notify the user, Windows displays the string specified in the Description registry key for your application.</span></span> <span data-ttu-id="22d53-238">Par exemple, si l’application ScreenReader Deluxe 1,0 utilise le narrateur Microsoft sur le Bureau sécurisé, elle inclut une chaîne de description telle que « Microsoft Narrator sera utilisé dans les bureaux verrouillés, de connexion et autres postes de travail sécurisés à la place de ScreenReader Deluxe 1,0 ».</span><span class="sxs-lookup"><span data-stu-id="22d53-238">For example, if the ScreenReader Deluxe 1.0 application uses Microsoft Narrator on the secure desktop, it would include a Description string such as, "Microsoft Narrator will be used in the locked, logon, and other secure desktops in place of ScreenReader Deluxe 1.0."</span></span>

<span data-ttu-id="22d53-239">Si la clé **SecureDesktopAccommodation** de votre application est définie sur « None », utilisez la clé **Description** pour indiquer à l’utilisateur que votre application n’est pas disponible sur le Bureau sécurisé et qu’aucune autre solution n’est fournie.</span><span class="sxs-lookup"><span data-stu-id="22d53-239">If your application's **SecureDesktopAccommodation** key is set to "none", use the **Description** key to tell the user your application is not available on the secure desktop and no alternative is provided.</span></span>

<span data-ttu-id="22d53-240">Windows affiche le texte de description aux emplacements appropriés dans la facilité d’accès du centre d’accès.</span><span class="sxs-lookup"><span data-stu-id="22d53-240">Windows displays the Description text in the relevant locations in the Ease of Access Center.</span></span>

### <a name="running-at-installation-and-on-the-logon-desktop"></a><span data-ttu-id="22d53-241">En cours d’exécution au moment de l’installation et sur le Bureau d’ouverture de session</span><span class="sxs-lookup"><span data-stu-id="22d53-241">Running at installation and on the logon desktop</span></span>

<span data-ttu-id="22d53-242">Si vous ajoutez le nom de clé inscrite de votre application d’accessibilité à la chaîne à l’emplacement de Registre suivant, Windows lance votre application immédiatement après son installation.</span><span class="sxs-lookup"><span data-stu-id="22d53-242">If you append your accessibility application's registered key name to the string at the following registry location, Windows will launch your application immediately after it is installed.</span></span> <span data-ttu-id="22d53-243">En outre, Windows exécutera automatiquement votre application chaque fois que le Bureau d’ouverture de session sera actif.</span><span class="sxs-lookup"><span data-stu-id="22d53-243">Also, Windows will automatically run your application whenever the logon desktop is active.</span></span>

<span data-ttu-id="22d53-244">**\\Logiciel HKCU \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ Configuration**</span><span class="sxs-lookup"><span data-stu-id="22d53-244">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\Configuration**</span></span>

<span data-ttu-id="22d53-245">La clé de configuration est une chaîne délimitée par des virgules.</span><span class="sxs-lookup"><span data-stu-id="22d53-245">The Configuration key is a comma-delimited string.</span></span> <span data-ttu-id="22d53-246">Pour ajouter votre application, ajoutez une chaîne identique à celle de la clé de registre de votre application dans HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS \\ .</span><span class="sxs-lookup"><span data-stu-id="22d53-246">To add your application, append a string that is the same as your application's registry key at HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\.</span></span>

### <a name="running-in-a-job"></a><span data-ttu-id="22d53-247">Exécution dans un travail</span><span class="sxs-lookup"><span data-stu-id="22d53-247">Running in a job</span></span>

<span data-ttu-id="22d53-248">Si la clé de Registre **TerminateOnDesktopSwitch** est absente ou si elle est définie sur une valeur différente de zéro, Windows exécute l’application dans le contexte d’un travail, en terminant et en redémarrant l’application avec chaque transition de bureau.</span><span class="sxs-lookup"><span data-stu-id="22d53-248">If the **TerminateOnDesktopSwitch** registry key is not present or is set to non-zero, Windows runs the application in the context of a job, terminating and restarting the application with each desktop transition.</span></span> <span data-ttu-id="22d53-249">L’exécution dans un travail garantit qu’une seule instance de l’application s’exécute à un moment donné et libère l’application de l’analyse de l’état du bureau.</span><span class="sxs-lookup"><span data-stu-id="22d53-249">Running in a job ensures that only a single instance of the application is running at a particular time, and frees the application from having to monitor the desktop state.</span></span> <span data-ttu-id="22d53-250">Les inconvénients liés à l’exécution d’un travail sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="22d53-250">The disadvantages of running in a job include:</span></span>

-   <span data-ttu-id="22d53-251">L’application entraîne un coût de démarrage avec chaque transition de bureau.</span><span class="sxs-lookup"><span data-stu-id="22d53-251">The application incurs a startup cost with each desktop transition.</span></span>
-   <span data-ttu-id="22d53-252">L’application peut être démarrée uniquement par le biais de la facilité d’accès du centre d’accès.</span><span class="sxs-lookup"><span data-stu-id="22d53-252">The application can be started only through the Ease of Access Center.</span></span>
-   <span data-ttu-id="22d53-253">L’application doit continuellement enregistrer ses paramètres, car elle peut être arrêtée à tout moment par une transition sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="22d53-253">The application must continually save its settings because it can be terminated at any time by a desktop transition.</span></span>

<span data-ttu-id="22d53-254">Si la clé **TerminateOnDesktopSwitch** existe et est définie sur 0, Windows n’exécute pas l’application d’accessibilité dans un travail.</span><span class="sxs-lookup"><span data-stu-id="22d53-254">If the **TerminateOnDesktopSwitch** key exists and is set to 0, Windows doesn't run the accessibility application in a job.</span></span> <span data-ttu-id="22d53-255">Les avantages sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="22d53-255">This has the following advantages:</span></span>

-   <span data-ttu-id="22d53-256">Aucun coût de démarrage n’est associé aux transitions sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="22d53-256">No startup costs are associated with desktop transitions.</span></span>
-   <span data-ttu-id="22d53-257">L’application peut être démarrée en dehors de la facilité d’accès du centre d’accès.</span><span class="sxs-lookup"><span data-stu-id="22d53-257">The application can be started outside of the Ease of Access Center.</span></span>

<span data-ttu-id="22d53-258">Les inconvénients liés à l’absence de fonctionnement dans un travail sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="22d53-258">The disadvantages of not running in a job include:</span></span>

-   <span data-ttu-id="22d53-259">Étant donné que l’application n’est pas redémarrée lors des transitions sur le bureau, elle doit détecter le moment où le Bureau actuel est inactif et y répondre de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="22d53-259">Because the application isn t restarted on desktop transitions, it must detect when the current desktop is inactive and respond appropriately.</span></span> <span data-ttu-id="22d53-260">Par exemple, l’application doit renoncer au contrôle du matériel afin que la version de bureau sécurisée de l’application puisse l’utiliser, et l’application doit passer en mode veille pour éviter d’utiliser les ressources du processeur.</span><span class="sxs-lookup"><span data-stu-id="22d53-260">For example, the application must relinquish control of hardware so the secure desktop version of the application can use it, and the application should enter sleep mode to avoid using processor resources.</span></span>
-   <span data-ttu-id="22d53-261">Si l’application peut être démarrée par le biais du menu Démarrer, de l’Explorateur Windows ou de la ligne de commande, la facilité d’accès du centre d’accès doit être informée.</span><span class="sxs-lookup"><span data-stu-id="22d53-261">If the application can be started through the Start menu, Windows Explorer, or the command line, the Ease of Access Center needs to be informed.</span></span> <span data-ttu-id="22d53-262">Pour plus d’informations, consultez **touche de logo Windows + U**.</span><span class="sxs-lookup"><span data-stu-id="22d53-262">For more information, see **Windows Logo key + U**.</span></span>
-   <span data-ttu-id="22d53-263">Étant donné que plusieurs copies de l’application peuvent s’exécuter simultanément sur différents bureaux, l’application doit être écrite pour prendre en charge plusieurs copies en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="22d53-263">Because multiple copies of the application can run simultaneously on different desktops, the application must be written to support multiple running copies.</span></span>

### <a name="windows-logo-key--u"></a><span data-ttu-id="22d53-264">Touche Windows + U</span><span class="sxs-lookup"><span data-stu-id="22d53-264">Windows Logo key + U</span></span>

<span data-ttu-id="22d53-265">Si votre application d’accessibilité est configurée pour s’exécuter dans un travail, le code de démarrage de votre application doit inclure un appel à la fonction [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) pour déterminer si l’application démarre dans un travail.</span><span class="sxs-lookup"><span data-stu-id="22d53-265">If your accessibility application is configured to run in a job, your application's startup code should include a call to the [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) function to determine whether the application is starting in a job.</span></span> <span data-ttu-id="22d53-266">Si c’est le cas, l’application doit démarrer l’ergonomie du centre d’accès, puis quitter.</span><span class="sxs-lookup"><span data-stu-id="22d53-266">If it is, the application should start the Ease of Access Center and then exit.</span></span> <span data-ttu-id="22d53-267">L’exemple suivant montre comment appeler **IsProcessInJob**.</span><span class="sxs-lookup"><span data-stu-id="22d53-267">The following example shows how to call **IsProcessInJob**.</span></span>


```C++
BOOL fAlreadyInJob;
BOOL fSuccess = IsProcessInJob(GetCurrentProcess(), NULL, &fAlreadyInJob); 
```



<span data-ttu-id="22d53-268">Si l’application d’accessibilité est configurée pour s’exécuter en dehors d’un travail, elle doit avertir l’ergonomie du centre d’accès que l’application démarre et se poursuit normalement.</span><span class="sxs-lookup"><span data-stu-id="22d53-268">If the accessibility application is configured to run outside of a job, it should notify the Ease of Access Center that the application is starting and continue as normal.</span></span>

<span data-ttu-id="22d53-269">Quelle que soit la façon dont l’application est configurée, si elle offre un moyen de quitter l’application, par exemple un bouton Fermer, l’application doit notifier la facilité d’accès du centre d’accès qu’elle est en cours de fermeture.</span><span class="sxs-lookup"><span data-stu-id="22d53-269">Regardless of how the application is configured, if it provides a way to exit from within the application, such as a Close button, the application must notify the Ease of Access Center that it is exiting.</span></span>

<span data-ttu-id="22d53-270">Une application notifie la facilité d’accès du centre d’accès en définissant une clé de registre temporaire, puis en injectant la combinaison de touches Windows + U dans le flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="22d53-270">An application notifies the Ease of Access Center by setting a temporary registry key and then injecting the Windows Logo key + U key combination into the input stream.</span></span>

<span data-ttu-id="22d53-271">L’application doit créer la clé temporaire à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="22d53-271">The application should create the temporary key at the following location.</span></span>

<span data-ttu-id="22d53-272">**\\Logiciel HKCU \\ Microsoft \\ Windows NT \\ CurrentVersion \\ AccessibilityTemp**</span><span class="sxs-lookup"><span data-stu-id="22d53-272">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\AccessibilityTemp**</span></span>

<span data-ttu-id="22d53-273">La clé temporaire doit avoir le même nom que le nom de l’application inscrite, par exemple « \_ lecteur d’écran Contoso \_ v 1.0 ».</span><span class="sxs-lookup"><span data-stu-id="22d53-273">The temporary key should have the same name as the registered application name, such as "Contoso\_Screen Reader\_v1.0".</span></span> <span data-ttu-id="22d53-274">La valeur de la clé est un **DWORD** défini sur 0x0003 lors du démarrage ou 0x0002 lorsque l’application est en cours de fermeture.</span><span class="sxs-lookup"><span data-stu-id="22d53-274">The value of the key is a **DWORD** set to 0x0003 when it is starting, or 0x0002 when the application is exiting.</span></span>


```C++
INPUT input[4] = {0};

input[0].type = INPUT_KEYBOARD;
input[0].ki.wVk = VK_LWIN;
input[0].ki.dwFlags = 0;

input[1].type = INPUT_KEYBOARD;
input[1].ki.wVk = 0x55; // U key
input[1].ki.dwFlags = 0;

input[2].type = INPUT_KEYBOARD;
input[2].ki.wVk = 0x55; // U key
input[2].ki.dwFlags = KEYEVENTF_KEYUP;

input[3].type = INPUT_KEYBOARD;
input[3].ki.wVk = VK_LWIN;
input[3].ki.dwFlags = KEYEVENTF_KEYUP;

SendInput(ARRAYSIZE(input), input, sizeof(input[0]));
```



### <a name="windows-logo-key--volume-up"></a><span data-ttu-id="22d53-275">Touche Windows + volume vers le haut</span><span class="sxs-lookup"><span data-stu-id="22d53-275">Windows Logo key + Volume Up</span></span>

<span data-ttu-id="22d53-276">Lorsque l’utilisateur démarre votre application d’accessibilité en appuyant sur la touche Windows + volume vers le haut (par exemple, sur un appareil tablette), la facilité d’accès passe l’argument de ligne de commande suivant à l’application :</span><span class="sxs-lookup"><span data-stu-id="22d53-276">When the user starts your accessibility application by pressing the Windows Logo key + Volume Up key combination (such as on a tablet device), the Ease of Access Center passes the following command-line argument to the application:</span></span>

<span data-ttu-id="22d53-277">**/hardwarebuttonlaunch**</span><span class="sxs-lookup"><span data-stu-id="22d53-277">**/hardwarebuttonlaunch**</span></span>

<span data-ttu-id="22d53-278">Votre application peut utiliser cet argument pour déterminer s’il faut démarrer normalement ou ajuster le comportement en conséquence.</span><span class="sxs-lookup"><span data-stu-id="22d53-278">Your application can use this argument to determine whether to start normally, or to adjust behavior accordingly.</span></span>

### <a name="transferring-secure-desktop-settings"></a><span data-ttu-id="22d53-279">Transfert des paramètres de bureau sécurisés</span><span class="sxs-lookup"><span data-stu-id="22d53-279">Transferring secure desktop settings</span></span>

<span data-ttu-id="22d53-280">Si votre application d’accessibilité prend en charge le Bureau sécurisé, vous pouvez utiliser le registre pour copier les paramètres lors de la transition de l’application vers le Bureau sécurisé.</span><span class="sxs-lookup"><span data-stu-id="22d53-280">If your accessibility application supports the secure desktop, you can use the registry to copy settings when the application transitions to the secure desktop.</span></span> <span data-ttu-id="22d53-281">La copie des paramètres permet de rendre la transition vers le Bureau sécurisé plus transparente pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="22d53-281">Copying settings helps makes the transition to the secure desktop more seamless for the user.</span></span>

<span data-ttu-id="22d53-282">Pour copier les paramètres, affectez la valeur 1 à la clé de Registre CopySettingsToLockedDesktop de l’application, puis stockez les paramètres à l’emplacement de Registre suivant.</span><span class="sxs-lookup"><span data-stu-id="22d53-282">To copy settings, set the application's CopySettingsToLockedDesktop registry key to 1, and store the settings in the following registry location.</span></span>

<span data-ttu-id="22d53-283">**\\Logiciel HKCU \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATConfig\\<AT Key Name>**</span><span class="sxs-lookup"><span data-stu-id="22d53-283">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATConfig\\<AT Key Name>**</span></span>

<span data-ttu-id="22d53-284">La facilité d’accès surveille cet emplacement du Registre pendant que l’application est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="22d53-284">The Ease of Access Center monitors this registry location while the application is running.</span></span> <span data-ttu-id="22d53-285">Quand une transition vers le Bureau sécurisé se produit, le centre d’ergonomie copie les paramètres dans le même emplacement dans la ruche HKCU du Bureau sécurisé.</span><span class="sxs-lookup"><span data-stu-id="22d53-285">When a transition to the secure desktop occurs, the Ease of Access Center copies the settings to the same location in the secure desktop s HKCU hive.</span></span> <span data-ttu-id="22d53-286">L’application peut ensuite lire les paramètres et reprendre son état.</span><span class="sxs-lookup"><span data-stu-id="22d53-286">The application can then read the settings and resume its state.</span></span>

<span data-ttu-id="22d53-287">Votre application d’accessibilité doit écrire ses paramètres à intervalles réguliers ou chaque fois que les valeurs changent.</span><span class="sxs-lookup"><span data-stu-id="22d53-287">Your accessibility application should write its settings at regular intervals or whenever the values change.</span></span> <span data-ttu-id="22d53-288">L’écriture des paramètres sur la sortie de l’application ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="22d53-288">Writing settings on application exit will not work.</span></span> <span data-ttu-id="22d53-289">Si l’application s’exécute dans un travail, elle se termine à la transition en dehors du Bureau sécurisé, avant que le code de sortie ne puisse être exécuté.</span><span class="sxs-lookup"><span data-stu-id="22d53-289">If the application is running in a job, it is terminated on the transition away from the secure desktop, before the exit code has a chance to run.</span></span> <span data-ttu-id="22d53-290">Si l’application ne s’exécute pas dans un travail, l’application ne se termine pas à la transition à partir du Bureau sécurisé.</span><span class="sxs-lookup"><span data-stu-id="22d53-290">If the application is not running in a job, the application is not terminated on the transition away from the secure desktop.</span></span>

### <a name="caution"></a><span data-ttu-id="22d53-291">Attention</span><span class="sxs-lookup"><span data-stu-id="22d53-291">Caution</span></span>

<span data-ttu-id="22d53-292">Étant donné que les clés de Registre décrites ici sont écrites en mode utilisateur, elles ne sont pas sécurisées.</span><span class="sxs-lookup"><span data-stu-id="22d53-292">Because the registry keys described here are written in user mode, they are not secure.</span></span> <span data-ttu-id="22d53-293">Si votre application d’accessibilité lit le contenu de ces clés, elle doit vérifier soigneusement les données et les utiliser avec précaution.</span><span class="sxs-lookup"><span data-stu-id="22d53-293">If your accessibility application reads the contents of these keys, it should carefully check the data and use it with caution.</span></span> <span data-ttu-id="22d53-294">Plus précisément, votre application doit effectuer une vérification des limites sur les valeurs **DWORD** , faire attention aux longueurs de chaîne, ne doit pas lire les noms de dll de plug-in et ne doit pas exécuter de commandes trouvées dans des chaînes.</span><span class="sxs-lookup"><span data-stu-id="22d53-294">Specifically, your application should do a bounds check on **DWORD** values, be careful with string lengths, should not read plug-in DLL names, and should not execute any commands found in strings.</span></span>

## <a name="registry-examples"></a><span data-ttu-id="22d53-295">Exemples de Registre</span><span class="sxs-lookup"><span data-stu-id="22d53-295">Registry Examples</span></span>

<span data-ttu-id="22d53-296">L’exemple suivant montre les valeurs de Registre possibles pour un produit fictif appelé contoso ScreenReader version 2,0, dont le nom localisé est stocké en tant que ressource.</span><span class="sxs-lookup"><span data-stu-id="22d53-296">The following example shows the possible registry values for a fictitious product called Contoso ScreenReader version 2.0, whose localized name is stored as a resource.</span></span>

<span data-ttu-id="22d53-297">Les valeurs de la table se trouvent sous la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="22d53-297">The values in the table are under the following key:</span></span>

<span data-ttu-id="22d53-298">**HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS \\ Contoso \_ Screen Reader \_ v 2.0**</span><span class="sxs-lookup"><span data-stu-id="22d53-298">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\Contoso\_Screen Reader\_v2.0**</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22d53-299">Nom</span><span class="sxs-lookup"><span data-stu-id="22d53-299">Name</span></span></th>
<th><span data-ttu-id="22d53-300">Type</span><span class="sxs-lookup"><span data-stu-id="22d53-300">Type</span></span></th>
<th><span data-ttu-id="22d53-301">Données</span><span class="sxs-lookup"><span data-stu-id="22d53-301">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22d53-302">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="22d53-302">ApplicationName</span></span></td>
<td><span data-ttu-id="22d53-303">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-303">REG_SZ</span></span></td>
<td><span data-ttu-id="22d53-304">@% SystemRoot% \system32\ContosoRes.dll,-5020</span><span class="sxs-lookup"><span data-stu-id="22d53-304">@%SystemRoot%\system32\ContosoRes.dll,-5020</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22d53-305">Description</span><span class="sxs-lookup"><span data-stu-id="22d53-305">Description</span></span></td>
<td><span data-ttu-id="22d53-306">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-306">REG_SZ</span></span></td>
<td><span data-ttu-id="22d53-307">@% SystemRoot% \system32\ContosoRes.dll,-5040</span><span class="sxs-lookup"><span data-stu-id="22d53-307">@%SystemRoot%\system32\ContosoRes.dll,-5040</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22d53-308">Profil</span><span class="sxs-lookup"><span data-stu-id="22d53-308">Profile</span></span></td>
<td><span data-ttu-id="22d53-309">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-309">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22d53-310">XML</span><span class="sxs-lookup"><span data-stu-id="22d53-310">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="22d53-311">SimpleProfile</span><span class="sxs-lookup"><span data-stu-id="22d53-311">SimpleProfile</span></span></td>
<td><span data-ttu-id="22d53-312">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-312">REG_SZ</span></span></td>
<td><span data-ttu-id="22d53-313">ScreenReader</span><span class="sxs-lookup"><span data-stu-id="22d53-313">ScreenReader</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22d53-314">Variable startexe</span><span class="sxs-lookup"><span data-stu-id="22d53-314">StartExe</span></span></td>
<td><span data-ttu-id="22d53-315">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-315">REG_SZ</span></span></td>
<td><span data-ttu-id="22d53-316">C:\ContosoTools\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="22d53-316">C:\ContosoTools\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22d53-317">StartParams</span><span class="sxs-lookup"><span data-stu-id="22d53-317">StartParams</span></span></td>
<td><span data-ttu-id="22d53-318">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-318">REG_SZ</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="22d53-319">SecureDesktopAccommodation</span><span class="sxs-lookup"><span data-stu-id="22d53-319">SecureDesktopAccommodation</span></span></td>
<td><span data-ttu-id="22d53-320">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-320">REG_SZ</span></span></td>
<td><span data-ttu-id="22d53-321">Narrateur</span><span class="sxs-lookup"><span data-stu-id="22d53-321">Narrator</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="22d53-322">Si l’application fournit à la fois un lecteur d’écran et une loupe d’écran dans un exécutable unique, les valeurs du composant de lecteur d’écran peuvent se présenter comme suit :</span><span class="sxs-lookup"><span data-stu-id="22d53-322">If the application provides both a screen reader and a screen magnifier in a single executable, the values for the screen reader component might look like this:</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22d53-323">Nom</span><span class="sxs-lookup"><span data-stu-id="22d53-323">Name</span></span></th>
<th><span data-ttu-id="22d53-324">Type</span><span class="sxs-lookup"><span data-stu-id="22d53-324">Type</span></span></th>
<th><span data-ttu-id="22d53-325">Données</span><span class="sxs-lookup"><span data-stu-id="22d53-325">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22d53-326">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="22d53-326">ApplicationName</span></span></td>
<td><span data-ttu-id="22d53-327">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-327">REG_SZ</span></span></td>
<td><span data-ttu-id="22d53-328">@C:\Program Files\Contoso\Contosores.dll,-30</span><span class="sxs-lookup"><span data-stu-id="22d53-328">@C:\Program Files\Contoso\Contosores.dll,-30</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22d53-329">Description</span><span class="sxs-lookup"><span data-stu-id="22d53-329">Description</span></span></td>
<td><span data-ttu-id="22d53-330">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-330">REG_SZ</span></span></td>
<td><span data-ttu-id="22d53-331">@C:\Program Files\Contoso\Contosores.dll,-32</span><span class="sxs-lookup"><span data-stu-id="22d53-331">@C:\Program Files\Contoso\Contosores.dll,-32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22d53-332">Profil</span><span class="sxs-lookup"><span data-stu-id="22d53-332">Profile</span></span></td>
<td><span data-ttu-id="22d53-333">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-333">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22d53-334">XML</span><span class="sxs-lookup"><span data-stu-id="22d53-334">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="22d53-335">SimpleProfile</span><span class="sxs-lookup"><span data-stu-id="22d53-335">SimpleProfile</span></span></td>
<td><span data-ttu-id="22d53-336">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-336">REG_SZ</span></span></td>
<td><span data-ttu-id="22d53-337">ScreenReader</span><span class="sxs-lookup"><span data-stu-id="22d53-337">ScreenReader</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22d53-338">Variable startexe</span><span class="sxs-lookup"><span data-stu-id="22d53-338">StartExe</span></span></td>
<td><span data-ttu-id="22d53-339">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-339">REG_SZ</span></span></td>
<td><span data-ttu-id="22d53-340">C:\Program Files\Contoso\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="22d53-340">C:\Program Files\Contoso\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22d53-341">StartParams</span><span class="sxs-lookup"><span data-stu-id="22d53-341">StartParams</span></span></td>
<td><span data-ttu-id="22d53-342">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-342">REG_SZ</span></span></td>
<td><span data-ttu-id="22d53-343">/r</span><span class="sxs-lookup"><span data-stu-id="22d53-343">/r</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="22d53-344">Les valeurs du composant loupe se trouvent dans la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="22d53-344">The values for the magnifier component would be in the following key:</span></span>

<span data-ttu-id="22d53-345">**HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Contosoibility \\ ATS \\ Contoso \_ magnifier \_ v 2.0**</span><span class="sxs-lookup"><span data-stu-id="22d53-345">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Contosoibility\\ATs\\Contoso\_Magnifier\_v2.0**</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22d53-346">Nom</span><span class="sxs-lookup"><span data-stu-id="22d53-346">Name</span></span></th>
<th><span data-ttu-id="22d53-347">Type</span><span class="sxs-lookup"><span data-stu-id="22d53-347">Type</span></span></th>
<th><span data-ttu-id="22d53-348">Données</span><span class="sxs-lookup"><span data-stu-id="22d53-348">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22d53-349">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="22d53-349">ApplicationName</span></span></td>
<td><span data-ttu-id="22d53-350">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-350">REG_SZ</span></span></td>
<td><span data-ttu-id="22d53-351">@c:\Program Files\Contoso\Contosores.dll,-31</span><span class="sxs-lookup"><span data-stu-id="22d53-351">@c:\Program Files\Contoso\Contosores.dll,-31</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22d53-352">Description</span><span class="sxs-lookup"><span data-stu-id="22d53-352">Description</span></span></td>
<td><span data-ttu-id="22d53-353">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-353">REG_SZ</span></span></td>
<td><span data-ttu-id="22d53-354">@c:\Program Files\Contoso\Contosores.dll,-42</span><span class="sxs-lookup"><span data-stu-id="22d53-354">@c:\Program Files\Contoso\Contosores.dll,-42</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22d53-355">Profil</span><span class="sxs-lookup"><span data-stu-id="22d53-355">Profile</span></span></td>
<td><span data-ttu-id="22d53-356">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-356">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22d53-357">XML</span><span class="sxs-lookup"><span data-stu-id="22d53-357">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;mild vision&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="22d53-358">SimpleProfile</span><span class="sxs-lookup"><span data-stu-id="22d53-358">SimpleProfile</span></span></td>
<td><span data-ttu-id="22d53-359">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-359">REG_SZ</span></span></td>
<td><span data-ttu-id="22d53-360">Agrandissement</span><span class="sxs-lookup"><span data-stu-id="22d53-360">Magnification</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22d53-361">Variable startexe</span><span class="sxs-lookup"><span data-stu-id="22d53-361">StartExe</span></span></td>
<td><span data-ttu-id="22d53-362">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-362">REG_SZ</span></span></td>
<td><span data-ttu-id="22d53-363">c:\Program Files\Contoso\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="22d53-363">c:\Program Files\Contoso\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22d53-364">StartParams</span><span class="sxs-lookup"><span data-stu-id="22d53-364">StartParams</span></span></td>
<td><span data-ttu-id="22d53-365">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="22d53-365">REG_SZ</span></span></td>
<td><span data-ttu-id="22d53-366">/m</span><span class="sxs-lookup"><span data-stu-id="22d53-366">/m</span></span></td>
</tr>
</tbody>
</table>



 

 

