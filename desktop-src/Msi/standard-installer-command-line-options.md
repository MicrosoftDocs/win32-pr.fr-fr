---
<span data-ttu-id="56caa-101">Description : le programme exécutable qui interprète les packages et installe les produits est Msiexec.exe. Remarque Msiexec définit également un niveau d’erreur au retour qui correspond aux codes d’erreur système.</span><span class="sxs-lookup"><span data-stu-id="56caa-101">description: The executable program that interprets packages and installs products is Msiexec.exe.Note  Msiexec also sets an error level on return that corresponds to System Error Codes.</span></span> <span data-ttu-id="56caa-102">Le tableau suivant identifie les options de ligne de commande standard pour ce programme.</span><span class="sxs-lookup"><span data-stu-id="56caa-102">The following table identifies the standard command-line options for this program.</span></span> <span data-ttu-id="56caa-103">Les options de ligne de commande ne respectent pas la casse. Windows Installer 2,0 : les options de ligne de commande qui sont identifiées dans cette rubrique sont disponibles à partir de Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="56caa-103">Command-line options are case insensitive.Windows Installer 2.0:  The command-line options that are identified in this topic are available beginning with Windows Installer 3.0.</span></span> <span data-ttu-id="56caa-104">Les options de Command-Line Windows Installer sont disponibles avec Windows Installer&\# 160 ; 3.0 et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="56caa-104">The Windows Installer Command-Line Options are available with Windows Installer&\#160;3.0 and earlier versions.</span></span>
<span data-ttu-id="56caa-105">ms. AssetID : b1707c88-1cca-45ab-bb23-6002bfd5204e title : programme d’installation standard Command-Line options ms. topic : article ms. Date : 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="56caa-105">ms.assetid: b1707c88-1cca-45ab-bb23-6002bfd5204e title: Standard Installer Command-Line Options ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="standard-installer-command-line-options"></a><span data-ttu-id="56caa-106">Options du programme d’installation standard Command-Line</span><span class="sxs-lookup"><span data-stu-id="56caa-106">Standard Installer Command-Line Options</span></span>

<span data-ttu-id="56caa-107">Le programme exécutable qui interprète les packages et installe les produits est Msiexec.exe.</span><span class="sxs-lookup"><span data-stu-id="56caa-107">The executable program that interprets packages and installs products is Msiexec.exe.</span></span>

> [!Note]  
> <span data-ttu-id="56caa-108">Msiexec définit également un niveau d’erreur au retour qui correspond aux [codes d’erreur système](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="56caa-108">Msiexec also sets an error level on return that corresponds to [System Error Codes](../debug/system-error-codes.md).</span></span>

 

<span data-ttu-id="56caa-109">Le tableau suivant identifie les options de ligne de commande standard pour ce programme.</span><span class="sxs-lookup"><span data-stu-id="56caa-109">The following table identifies the standard command-line options for this program.</span></span> <span data-ttu-id="56caa-110">Les options de ligne de commande ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="56caa-110">Command-line options are case insensitive.</span></span>

<span data-ttu-id="56caa-111">**Windows Installer 2,0 :** Les options de ligne de commande qui sont identifiées dans cette rubrique sont disponibles à partir de Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="56caa-111">**Windows Installer 2.0:** The command-line options that are identified in this topic are available beginning with Windows Installer 3.0.</span></span> <span data-ttu-id="56caa-112">Les [options de ligne de commande](command-line-options.md) Windows Installer sont disponibles avec Windows Installer 3,0 et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="56caa-112">The Windows Installer [Command-Line Options](command-line-options.md) are available with Windows Installer 3.0 and earlier versions.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56caa-113">Option</span><span class="sxs-lookup"><span data-stu-id="56caa-113">Option</span></span></th>
<th><span data-ttu-id="56caa-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56caa-114">Parameters</span></span></th>
<th><span data-ttu-id="56caa-115">Signification</span><span class="sxs-lookup"><span data-stu-id="56caa-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56caa-116"><strong>/Help</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-116"><strong>/help</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="56caa-117">Aide et aide-mémoire.</span><span class="sxs-lookup"><span data-stu-id="56caa-117">Help and quick reference option.</span></span> <span data-ttu-id="56caa-118">Affiche l’utilisation correcte de la commande d’installation, y compris la liste de tous les commutateurs et comportements.</span><span class="sxs-lookup"><span data-stu-id="56caa-118">Displays the correct usage of the setup command including a list of all switches and behavior.</span></span> <span data-ttu-id="56caa-119">La description de l’utilisation peut être affichée dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56caa-119">The description of usage can be displayed in the user interface.</span></span> <span data-ttu-id="56caa-120">Une utilisation incorrecte de toute option appelle cette option d’aide.</span><span class="sxs-lookup"><span data-stu-id="56caa-120">Incorrect use of any option invokes this help option.</span></span><br/> <span data-ttu-id="56caa-121">Exemple : <strong>msiexec/Help</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-121">Example: <strong>msiexec /help</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="56caa-122">L' <a href="command-line-options.md">option de ligne de commande</a> équivalente Windows Installer est <strong>/ ?</strong>.</span><span class="sxs-lookup"><span data-stu-id="56caa-122">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/?</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56caa-123"><strong>/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-123"><strong>/quiet</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="56caa-124">Option Display quiet.</span><span class="sxs-lookup"><span data-stu-id="56caa-124">Quiet display option.</span></span> <span data-ttu-id="56caa-125">Le programme d’installation exécute une installation sans afficher d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56caa-125">The installer runs an installation without displaying a user interface.</span></span> <span data-ttu-id="56caa-126">Aucune invite, aucun message ou boîte de dialogue n’est affiché à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56caa-126">No prompts, messages, or dialog boxes are displayed to the user.</span></span> <span data-ttu-id="56caa-127">L’utilisateur ne peut pas annuler l’installation.</span><span class="sxs-lookup"><span data-stu-id="56caa-127">The user cannot cancel the installation.</span></span> <span data-ttu-id="56caa-128">Utilisez les options de ligne de commande <strong>/norestart</strong> ou <strong>/forcerestart</strong> standard pour contrôler les redémarrages.</span><span class="sxs-lookup"><span data-stu-id="56caa-128">Use the <strong>/norestart</strong> or <strong>/forcerestart</strong> standard command-line options to control reboots.</span></span> <span data-ttu-id="56caa-129">Si aucune option de redémarrage n’est spécifiée, le programme d’installation redémarre l’ordinateur chaque fois que nécessaire sans afficher d’invite ou d’avertissement à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56caa-129">If no reboot options are specified, the installer restarts the computer whenever necessary without displaying any prompt or warning to the user.</span></span><br/> <span data-ttu-id="56caa-130">Exemples :</span><span class="sxs-lookup"><span data-stu-id="56caa-130">Examples:</span></span> <br/> <span data-ttu-id="56caa-131"><strong>msiexec/package Application.msi/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-131"><strong>msiexec /package Application.msi /quiet</strong></span></span><br/> <span data-ttu-id="56caa-132"><strong>Msiexec/Uninstall Application.msi/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-132"><strong>Msiexec /uninstall Application.msi /quiet</strong></span></span><br/> <span data-ttu-id="56caa-133"><strong>Msiexec/Update msipatch. msp/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-133"><strong>Msiexec /update msipatch.msp /quiet</strong></span></span><br/> <span data-ttu-id="56caa-134"><strong>Msiexec/Uninstall msipatch. msp/package Application.msi/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-134"><strong>Msiexec /uninstall msipatch.msp /package Application.msi / quiet</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="56caa-135">L’équivalent <a href="command-line-options.md">de l’option de ligne de commande</a> Windows Installer est <strong>/qn</strong>.</span><span class="sxs-lookup"><span data-stu-id="56caa-135">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/qn</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56caa-136"><strong>/passive</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-136"><strong>/passive</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="56caa-137">Option d’affichage passif.</span><span class="sxs-lookup"><span data-stu-id="56caa-137">Passive display option.</span></span> <span data-ttu-id="56caa-138">Le programme d’installation affiche une barre de progression à l’utilisateur qui indique qu’une installation est en cours, mais aucune invite ni aucun message d’erreur ne s’affiche pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56caa-138">The installer displays a progress bar to the user that indicates that an installation is in progress but no prompts or error messages are displayed to the user.</span></span> <span data-ttu-id="56caa-139">L’utilisateur ne peut pas annuler l’installation.</span><span class="sxs-lookup"><span data-stu-id="56caa-139">The user cannot cancel the installation.</span></span> <span data-ttu-id="56caa-140">Utilisez les options de ligne de commande <strong>/norestart</strong> ou <strong>/forcerestart</strong> standard pour contrôler les redémarrages.</span><span class="sxs-lookup"><span data-stu-id="56caa-140">Use the <strong>/norestart</strong> or <strong>/forcerestart</strong> standard command-line options to control reboots.</span></span> <span data-ttu-id="56caa-141">Si aucune option de redémarrage n’est spécifiée, le programme d’installation redémarre l’ordinateur chaque fois que nécessaire sans afficher d’invite ou d’avertissement à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56caa-141">If no reboot option is specified, the installer restarts the computer whenever necessary without displaying any prompt or warning to the user.</span></span> <br/> <span data-ttu-id="56caa-142">Exemple : <strong>msiexec/package Application.msi/passive</strong> </span><span class="sxs-lookup"><span data-stu-id="56caa-142">Example: <strong>msiexec /package Application.msi /passive</strong> </span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="56caa-143">L’équivalent de l' <a href="command-line-options.md">option de ligne de commande</a> Windows Installer est <strong>/qb !-</strong> with <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>= S défini sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="56caa-143">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/qb!-</strong> with <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>=S set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56caa-144"><strong>/norestart</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-144"><strong>/norestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="56caa-145">Option ne jamais redémarrer.</span><span class="sxs-lookup"><span data-stu-id="56caa-145">Never restart option.</span></span> <span data-ttu-id="56caa-146">Le programme d’installation ne redémarre jamais l’ordinateur après l’installation.</span><span class="sxs-lookup"><span data-stu-id="56caa-146">The installer never restarts the computer after the installation.</span></span><br/> <span data-ttu-id="56caa-147">Exemple : msiexec/package Application.msi <strong>/norestart</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-147">Example: msiexec /package Application.msi <strong>/norestart</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="56caa-148">L’équivalent de la ligne de commande Windows Installer a <a href="reboot.md"><strong>reboot</strong></a>= ReallySuppress défini sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="56caa-148">The equivalent Windows Installer command line has <a href="reboot.md"><strong>REBOOT</strong></a>=ReallySuppress set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56caa-149"><strong>/forcerestart</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-149"><strong>/forcerestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="56caa-150">Option Always restart.</span><span class="sxs-lookup"><span data-stu-id="56caa-150">Always restart option.</span></span> <span data-ttu-id="56caa-151">Le programme d’installation redémarre toujours l’ordinateur après chaque installation.</span><span class="sxs-lookup"><span data-stu-id="56caa-151">The installer always restarts the computer after every installation.</span></span><br/> <span data-ttu-id="56caa-152">Exemple : msiexec/package Application.msi <strong>/forcerestart</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-152">Example: msiexec /package Application.msi <strong>/forcerestart</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="56caa-153">L’équivalent de la ligne de commande Windows Installer est <a href="reboot.md"><strong>reboot</strong></a>= force définie sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="56caa-153">The equivalent Windows Installer command line has <a href="reboot.md"><strong>REBOOT</strong></a>=Force set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56caa-154"><strong>/promptrestart</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-154"><strong>/promptrestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="56caa-155">Invite avant le redémarrage de l’option.</span><span class="sxs-lookup"><span data-stu-id="56caa-155">Prompt before restarting option.</span></span> <span data-ttu-id="56caa-156">Affiche un message indiquant qu’un redémarrage est nécessaire pour terminer l’installation et demande à l’utilisateur s’il faut redémarrer le système maintenant.</span><span class="sxs-lookup"><span data-stu-id="56caa-156">Displays a message that a restart is required to complete the installation and asks the user whether to restart the system now.</span></span> <span data-ttu-id="56caa-157">Cette option ne peut pas être utilisée avec l’option <strong>/Quiet</strong> .</span><span class="sxs-lookup"><span data-stu-id="56caa-157">This option cannot be used together with the <strong>/quiet</strong> option.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="56caa-158">L’équivalent de la ligne de commande Windows Installer a <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>  =  &quot; &quot; sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="56caa-158">The equivalent Windows Installer command line has <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a> = &quot;&quot; set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56caa-159"><strong>/Uninstall</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-159"><strong>/uninstall</strong></span></span></td>
<td><em><Package.msi|ProductCode></em></td>
<td><span data-ttu-id="56caa-160">Option de désinstallation du produit.</span><span class="sxs-lookup"><span data-stu-id="56caa-160">Uninstall product option.</span></span> <span data-ttu-id="56caa-161">Désinstalle un produit.</span><span class="sxs-lookup"><span data-stu-id="56caa-161">Uninstalls a product.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="56caa-162">L’équivalent <a href="command-line-options.md">de l’option de ligne de commande</a> Windows Installer est <strong>/x</strong>.</span><span class="sxs-lookup"><span data-stu-id="56caa-162">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/x</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56caa-163"><strong>/Uninstall</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-163"><strong>/uninstall</strong></span></span></td>
<td><span data-ttu-id="56caa-164"><em>/package <Package.msi | ProductCode> /Uninstall <Update1.msp | PatchGUID1> [; Update2. msp | PatchGUID2]</em></span><span class="sxs-lookup"><span data-stu-id="56caa-164"><em>/package <Package.msi | ProductCode> /uninstall <Update1.msp | PatchGUID1>[;Update2.msp | PatchGUID2]</em></span></span></td>
<td><span data-ttu-id="56caa-165">Option de désinstallation de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="56caa-165">Uninstall update option.</span></span> <span data-ttu-id="56caa-166">Désinstalle un correctif de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="56caa-166">Uninstalls an update patch.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="56caa-167">L’équivalent de l' <a href="command-line-options.md">option de ligne de commande</a> Windows Installer est <strong>/i</strong> avec <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>= Update 1. msp | PatchGUID1[; Update2. msp | PatchGUID2] défini sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="56caa-167">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/I</strong> with <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>=Update1.msp | PatchGUID1[;Update2.msp | PatchGUID2] set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56caa-168"><strong>/log</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-168"><strong>/log</strong></span></span></td>
<td><em><logfile></em></td>
<td><span data-ttu-id="56caa-169">Option de journalisation.</span><span class="sxs-lookup"><span data-stu-id="56caa-169">Log option.</span></span> <span data-ttu-id="56caa-170">Écrit les informations de journalisation dans un fichier journal au niveau du chemin d’accès existant spécifié.</span><span class="sxs-lookup"><span data-stu-id="56caa-170">Writes logging information into a log file at the specified existing path.</span></span> <span data-ttu-id="56caa-171">Le chemin d’accès à l’emplacement du fichier journal doit déjà exister.</span><span class="sxs-lookup"><span data-stu-id="56caa-171">The path to the log file location must already exist.</span></span> <span data-ttu-id="56caa-172">Le programme d’installation ne crée pas la structure de répertoire pour le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="56caa-172">The installer does not create the directory structure for the logfile.</span></span><br/> <span data-ttu-id="56caa-173">Les informations suivantes sont entrées dans le journal :</span><span class="sxs-lookup"><span data-stu-id="56caa-173">The following information is entered into the log:</span></span><br/>
<ul>
<li><span data-ttu-id="56caa-174">Messages d'état</span><span class="sxs-lookup"><span data-stu-id="56caa-174">Status messages</span></span></li>
<li><span data-ttu-id="56caa-175">Avertissements récupérables</span><span class="sxs-lookup"><span data-stu-id="56caa-175">Nonfatal warnings</span></span></li>
<li><span data-ttu-id="56caa-176">Tous les messages d’erreur</span><span class="sxs-lookup"><span data-stu-id="56caa-176">All error messages</span></span></li>
<li><span data-ttu-id="56caa-177">Démarrer des actions</span><span class="sxs-lookup"><span data-stu-id="56caa-177">Start up of actions</span></span></li>
<li><span data-ttu-id="56caa-178">Enregistrements spécifiques aux actions</span><span class="sxs-lookup"><span data-stu-id="56caa-178">Action-specific records</span></span></li>
<li><span data-ttu-id="56caa-179">Demandes de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="56caa-179">User requests</span></span></li>
<li><span data-ttu-id="56caa-180">Paramètres initiaux de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="56caa-180">Initial UI parameters</span></span></li>
<li><span data-ttu-id="56caa-181">Informations de sortie insuffisantes ou irrécupérables</span><span class="sxs-lookup"><span data-stu-id="56caa-181">Out-of-memory or fatal exit information</span></span></li>
<li><span data-ttu-id="56caa-182">Messages d’espace disque insuffisant</span><span class="sxs-lookup"><span data-stu-id="56caa-182">Out-of-disk-space messages</span></span></li>
<li><span data-ttu-id="56caa-183">Propriétés du terminal</span><span class="sxs-lookup"><span data-stu-id="56caa-183">Terminal properties</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="56caa-184">L’équivalent <a href="command-line-options.md">de l’option de ligne de commande</a> Windows Installer est <strong>/l \*</strong>.</span><span class="sxs-lookup"><span data-stu-id="56caa-184">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/L\*</strong>.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="56caa-185">Pour plus d’informations sur toutes les méthodes qui sont disponibles pour définir le mode de journalisation, consultez <a href="normal-logging.md">journalisation normale</a> dans la section <a href="windows-installer-logging.md">journalisation Windows Installer</a> .</span><span class="sxs-lookup"><span data-stu-id="56caa-185">For more information about all the methods that are available for setting the logging mode, see <a href="normal-logging.md">Normal Logging</a> in the <a href="windows-installer-logging.md">Windows Installer Logging</a> section.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56caa-186"><strong>/package</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-186"><strong>/package</strong></span></span></td>
<td><em><Package.msi|ProductCode></em></td>
<td><span data-ttu-id="56caa-187">Option d’installation du produit.</span><span class="sxs-lookup"><span data-stu-id="56caa-187">Install product option.</span></span> <span data-ttu-id="56caa-188">Installe ou configure un produit.</span><span class="sxs-lookup"><span data-stu-id="56caa-188">Installs or configures a product.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="56caa-189">L’équivalent <a href="command-line-options.md">de l’option de ligne de commande</a> Windows Installer est <strong>/i</strong>.</span><span class="sxs-lookup"><span data-stu-id="56caa-189">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/I</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56caa-190"><strong>/Update</strong></span><span class="sxs-lookup"><span data-stu-id="56caa-190"><strong>/update</strong></span></span></td>
<td><span data-ttu-id="56caa-191"><em><Update1.msp>[; Update2. msp]</em></span><span class="sxs-lookup"><span data-stu-id="56caa-191"><em><Update1.msp>[;Update2.msp]</em></span></span></td>
<td><span data-ttu-id="56caa-192">Option installer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="56caa-192">Install patches option.</span></span> <span data-ttu-id="56caa-193">Installe un ou plusieurs correctifs.</span><span class="sxs-lookup"><span data-stu-id="56caa-193">Installs one or multiple patches.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="56caa-194">L’équivalent de la ligne de commande Windows Installer contient <a href="patch.md"><strong>patch</strong></a> = [msipatch. msp] < ; PatchGuid2> défini sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="56caa-194">The equivalent Windows Installer command line has <a href="patch.md"><strong>PATCH</strong></a> = [msipatch.msp]<;PatchGuid2> set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
