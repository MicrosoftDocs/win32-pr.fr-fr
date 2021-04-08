---
title: Opérations StoClien
description: L’exemple StoClien montre comment le client utilise le stockage structuré. L’exemple suivant résume les opérations StoClien.
ms.assetid: 55498665-520b-4a83-a3d1-22d3ed15863e
keywords:
- Opérations StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1068fcf1e377456211e08020f41279be9b5e3b0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729068"
---
# <a name="stoclien-operations"></a><span data-ttu-id="7e8f6-105">Opérations StoClien</span><span class="sxs-lookup"><span data-stu-id="7e8f6-105">StoClien Operations</span></span>

<span data-ttu-id="7e8f6-106">L’exemple [StoClien](structured-storage-client-sample--stoclien-.md) montre comment le client utilise le stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-106">The [StoClien](structured-storage-client-sample--stoclien-.md) sample demonstrates how the client uses structured storage.</span></span> <span data-ttu-id="7e8f6-107">L’exemple suivant résume les opérations StoClien.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-107">The following summarizes the StoClien operations.</span></span>

<span data-ttu-id="7e8f6-108">La zone cliente de la fenêtre d’application [StoClien](structured-storage-client-sample--stoclien-.md) est utilisée pour l’affichage visuel d’un dessin libre créé avec une souris ou un périphérique tablette.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-108">The [StoClien](structured-storage-client-sample--stoclien-.md) application window client area is used for visual display of freeform drawing created with a mouse or tablet device.</span></span> <span data-ttu-id="7e8f6-109">Pour dessiner avec la souris, appuyez sur le bouton gauche de la souris et maintenez-le enfoncé pendant que vous déplacez la souris.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-109">To draw with the mouse, press and hold the left mouse button while moving the mouse.</span></span> <span data-ttu-id="7e8f6-110">Le relâchement du bouton gauche de la souris termine le dessin d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-110">Releasing the left mouse button ends the drawing of a line.</span></span>

<span data-ttu-id="7e8f6-111">Voici un résumé des opérations du point de vue de Stoclien.exe en tant que client COM du serveur COM Stoserve.dll :</span><span class="sxs-lookup"><span data-stu-id="7e8f6-111">Here is a summary of operations from the standpoint of Stoclien.exe as a COM client of the Stoserve.dll COM server:</span></span>

<dl> <dt>

<span data-ttu-id="7e8f6-112"><span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>Fichier/ouvrir</span><span class="sxs-lookup"><span data-stu-id="7e8f6-112"><span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>File/Open</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-113">Affiche la boîte de dialogue Ouvrir pour obtenir un nom et un chemin d’accès pour un fichier de dessin papier existant à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-113">Shows the Open dialog box to obtain a name and path for an existing paper drawing file to open.</span></span> <span data-ttu-id="7e8f6-114">Valeur par défaut. L’extension de nom de fichier PAP pour ces fichiers est supposée.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-114">A default .PAP file name extension for these files is assumed.</span></span> <span data-ttu-id="7e8f6-115">Si des modifications ont été apportées au dessin existant lorsque cet élément de menu est choisi, une boîte de dialogue distincte s’affiche pour demander à l’utilisateur si le dessin actif doit être enregistré dans son fichier composé associé.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-115">If changes were made to the existing drawing when this menu item is chosen, a separate dialog will first be shown asking the user if the current drawing should be saved into its associated compound file.</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-116"><span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>Fichier/enregistrer</span><span class="sxs-lookup"><span data-stu-id="7e8f6-116"><span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>File/Save</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-117">Enregistre le dessin actuel dans son fichier composé associé.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-117">Saves the current drawing into its associated compound file.</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-118"><span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>Fichier/enregistrer sous</span><span class="sxs-lookup"><span data-stu-id="7e8f6-118"><span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>File/Save As</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-119">Affiche la boîte de dialogue Enregistrer sous pour obtenir un nom et un chemin d’accès pour un nouveau fichier de dessin papier à créer.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-119">Shows the Save As dialog box to obtain a name and path for a new paper drawing file to create.</span></span> <span data-ttu-id="7e8f6-120">Le dessin actuel devient le contenu enregistré du nouveau fichier, et le nouveau fichier devient le nouveau fichier composé associé pour le dessin.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-120">The current drawing becomes the saved content of the new file, and the new file becomes the new associated compound file for the drawing.</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-121"><span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>Fichier/quitter</span><span class="sxs-lookup"><span data-stu-id="7e8f6-121"><span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>File/Exit</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-122">Quitte [StoClien](structured-storage-client-sample--stoclien-.md).</span><span class="sxs-lookup"><span data-stu-id="7e8f6-122">Exits [StoClien](structured-storage-client-sample--stoclien-.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-123"><span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Dessin/dessin sur</span><span class="sxs-lookup"><span data-stu-id="7e8f6-123"><span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Draw/Drawing On</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-124">Active le dessin entre le client [StoClien](structured-storage-client-sample--stoclien-.md) et l’objet du colivre dans le serveur.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-124">Turns on drawing between the [StoClien](structured-storage-client-sample--stoclien-.md) client and the COPaper object in the server.</span></span> <span data-ttu-id="7e8f6-125">Cette commande verrouille l’objet du colivre pour une utilisation exclusive par ce client et empêche les autres clients d’accéder à la même instance de codocument sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-125">This command locks the COPaper object for exclusive use by this client and prevents other clients from accessing the same COPaper instance in the server.</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-126"><span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Dessin/dessin désactivé</span><span class="sxs-lookup"><span data-stu-id="7e8f6-126"><span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Draw/Drawing Off</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-127">Désactive le dessin entre le client [StoClien](structured-storage-client-sample--stoclien-.md) et l’objet du colivre dans le serveur.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-127">Turns off drawing between the [StoClien](structured-storage-client-sample--stoclien-.md) client and the COPaper object in the server.</span></span> <span data-ttu-id="7e8f6-128">Cette commande déverrouille le colivre en vue d’une utilisation exclusive par ce client et permet à d’autres clients d’accéder à la même instance de codocument sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-128">This command unlocks the COPaper for exclusive use by this client and allows other clients to access the same COPaper instance in the server.</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-129"><span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Dessin/redessin</span><span class="sxs-lookup"><span data-stu-id="7e8f6-129"><span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Draw/Redraw</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-130">Redessine dans le client les données de dessin actuelles contenues dans l’objet du coarticle du serveur.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-130">Redraws in the client the current drawing data held in the COPaper object in the server.</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-131"><span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Dessin/effacement</span><span class="sxs-lookup"><span data-stu-id="7e8f6-131"><span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Draw/Erase</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-132">Efface le contenu de dessin actuel et efface l’image de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-132">Erases the current drawing content and clears the window image.</span></span> <span data-ttu-id="7e8f6-133">Sélection du menu : la plume/couleur affiche la boîte de dialogue choisir une couleur pour obtenir une nouvelle couleur de stylet pour le dessin.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-133">Menu Selection: Pen/Color Shows the Choose Color dialog box to obtain a new pen color for drawing.</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-134"><span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Stylet/moyen</span><span class="sxs-lookup"><span data-stu-id="7e8f6-134"><span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Pen/Medium</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-135">Choisit la largeur moyenne pour le dessin.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-135">Chooses the medium width for drawing.</span></span> <span data-ttu-id="7e8f6-136">Une coche sur cette option de menu indique que moyenne est la largeur actuelle du stylet.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-136">A check mark on this menu choice indicates that medium is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-137"><span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Plume/épais</span><span class="sxs-lookup"><span data-stu-id="7e8f6-137"><span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Pen/Thick</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-138">Choisit la largeur épaisse pour le dessin.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-138">Chooses the thick width for drawing.</span></span> <span data-ttu-id="7e8f6-139">Une coche sur cette option de menu indique que l’épaisseur est la largeur actuelle du stylet.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-139">A check mark on this menu choice indicates that thick is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-140"><span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Plume/fin</span><span class="sxs-lookup"><span data-stu-id="7e8f6-140"><span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Pen/Thin</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-141">Choisit la largeur fine du dessin.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-141">Chooses the thin width for drawing.</span></span> <span data-ttu-id="7e8f6-142">Une coche sur cette option de menu indique que fin correspond à la largeur actuelle du stylet.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-142">A check mark on this menu choice indicates that thin is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-143"><span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Récepteur/connexion</span><span class="sxs-lookup"><span data-stu-id="7e8f6-143"><span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Sink/Connect</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-144">Connecte l’interface COPaperSink IPaperSink au point de connexion PaperSink de l’objet du coarticle.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-144">Connects the COPaperSink IPaperSink interface to the COPaper object PaperSink connection point.</span></span> <span data-ttu-id="7e8f6-145">Le redessin de l’image de dessin actuelle dans [StoClien](structured-storage-client-sample--stoclien-.md) s’appuie sur la connexion du récepteur.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-145">Repainting of the current drawing image in [StoClien](structured-storage-client-sample--stoclien-.md) relies on the sink connection.</span></span> <span data-ttu-id="7e8f6-146">Une coche sur cette option de menu indique que le redessin est connecté.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-146">A check mark on this menu choice indicates that repainting is connected.</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-147"><span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Récepteur/déconnexion</span><span class="sxs-lookup"><span data-stu-id="7e8f6-147"><span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Sink/Disconnect</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-148">Déconnecte l’interface COPaperSink IPaperSink du point de connexion PaperSink de l’objet du coarticle.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-148">Disconnects the COPaperSink IPaperSink interface from the COPaper object PaperSink connection point.</span></span> <span data-ttu-id="7e8f6-149">Le redessin de l’image de dessin actuelle dans [StoClien](structured-storage-client-sample--stoclien-.md) s’appuie sur la connexion du récepteur.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-149">Repainting of the current drawing image in [StoClien](structured-storage-client-sample--stoclien-.md) relies on the sink connection.</span></span> <span data-ttu-id="7e8f6-150">Une coche sur cette option de menu indique que le redessin est déconnecté.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-150">A check mark on this menu choice indicates that repainting is disconnected.</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-151"><span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Didacticiel aide/StoClien</span><span class="sxs-lookup"><span data-stu-id="7e8f6-151"><span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Help/StoClien Tutorial</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-152">Ouvre le fichier du didacticiel de STOCLIEN.HTM dans le navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-152">Opens the STOCLIEN.HTM tutorial file in the Web browser.</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-153"><span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Didacticiel aide/StoServe</span><span class="sxs-lookup"><span data-stu-id="7e8f6-153"><span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Help/StoServe Tutorial</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-154">Ouvre le fichier du didacticiel de STOSERVE.HTM dans le navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-154">Opens the STOSERVE.HTM tutorial file in the Web browser.</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-155"><span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Aide/lecture du fichier source</span><span class="sxs-lookup"><span data-stu-id="7e8f6-155"><span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Help/Read Source File</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-156">Affiche la boîte de dialogue Ouvrir pour vous permettre d’ouvrir un fichier source à partir de cette leçon ou un autre dans le bloc-notes Windows.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-156">Displays the Open dialog box so you can open a source file from this lesson or another one in the Windows Notepad.</span></span>

</dd> <dt>

<span data-ttu-id="7e8f6-157"><span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Aide/à propos de StoClien</span><span class="sxs-lookup"><span data-stu-id="7e8f6-157"><span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Help/About StoClien</span></span>
</dt> <dd>

<span data-ttu-id="7e8f6-158">Affiche la boîte de dialogue à propos de pour cette application.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-158">Displays the About dialog box for this application.</span></span>

</dd> </dl>

<span data-ttu-id="7e8f6-159">L’exemple [StoClien](structured-storage-client-sample--stoclien-.md) utilise de nombreux services et classes utilitaires fournis par [apputil](./using-visual-studio.md).</span><span class="sxs-lookup"><span data-stu-id="7e8f6-159">The [StoClien](structured-storage-client-sample--stoclien-.md) sample uses many of the utility classes and services provided by [APPUTIL](./using-visual-studio.md).</span></span> <span data-ttu-id="7e8f6-160">Pour plus d’informations sur [apputil](./using-visual-studio.md), consultez le code source de la bibliothèque [apputil](./using-visual-studio.md) dans le répertoire [apputil](./using-visual-studio.md) frère et apputil.MD dans le répertoire principal du didacticiel.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-160">For more information about [APPUTIL](./using-visual-studio.md), see the [APPUTIL](./using-visual-studio.md) library source code in the sibling [APPUTIL](./using-visual-studio.md) directory and Apputil.md in the main tutorial directory.</span></span> <span data-ttu-id="7e8f6-161">Pour plus d’informations sur [apputil](./using-visual-studio.md), consultez [Comment générer des exemples](how-to-build-samples.md).</span><span class="sxs-lookup"><span data-stu-id="7e8f6-161">For more information about [APPUTIL](./using-visual-studio.md), see [How to Build Samples](how-to-build-samples.md).</span></span>

 

 