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
# <a name="stoclien-operations"></a>Opérations StoClien

L’exemple [StoClien](structured-storage-client-sample--stoclien-.md) montre comment le client utilise le stockage structuré. L’exemple suivant résume les opérations StoClien.

La zone cliente de la fenêtre d’application [StoClien](structured-storage-client-sample--stoclien-.md) est utilisée pour l’affichage visuel d’un dessin libre créé avec une souris ou un périphérique tablette. Pour dessiner avec la souris, appuyez sur le bouton gauche de la souris et maintenez-le enfoncé pendant que vous déplacez la souris. Le relâchement du bouton gauche de la souris termine le dessin d’une ligne.

Voici un résumé des opérations du point de vue de Stoclien.exe en tant que client COM du serveur COM Stoserve.dll :

<dl> <dt>

<span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>Fichier/ouvrir
</dt> <dd>

Affiche la boîte de dialogue Ouvrir pour obtenir un nom et un chemin d’accès pour un fichier de dessin papier existant à ouvrir. Valeur par défaut. L’extension de nom de fichier PAP pour ces fichiers est supposée. Si des modifications ont été apportées au dessin existant lorsque cet élément de menu est choisi, une boîte de dialogue distincte s’affiche pour demander à l’utilisateur si le dessin actif doit être enregistré dans son fichier composé associé.

</dd> <dt>

<span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>Fichier/enregistrer
</dt> <dd>

Enregistre le dessin actuel dans son fichier composé associé.

</dd> <dt>

<span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>Fichier/enregistrer sous
</dt> <dd>

Affiche la boîte de dialogue Enregistrer sous pour obtenir un nom et un chemin d’accès pour un nouveau fichier de dessin papier à créer. Le dessin actuel devient le contenu enregistré du nouveau fichier, et le nouveau fichier devient le nouveau fichier composé associé pour le dessin.

</dd> <dt>

<span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>Fichier/quitter
</dt> <dd>

Quitte [StoClien](structured-storage-client-sample--stoclien-.md).

</dd> <dt>

<span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Dessin/dessin sur
</dt> <dd>

Active le dessin entre le client [StoClien](structured-storage-client-sample--stoclien-.md) et l’objet du colivre dans le serveur. Cette commande verrouille l’objet du colivre pour une utilisation exclusive par ce client et empêche les autres clients d’accéder à la même instance de codocument sur le serveur.

</dd> <dt>

<span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Dessin/dessin désactivé
</dt> <dd>

Désactive le dessin entre le client [StoClien](structured-storage-client-sample--stoclien-.md) et l’objet du colivre dans le serveur. Cette commande déverrouille le colivre en vue d’une utilisation exclusive par ce client et permet à d’autres clients d’accéder à la même instance de codocument sur le serveur.

</dd> <dt>

<span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Dessin/redessin
</dt> <dd>

Redessine dans le client les données de dessin actuelles contenues dans l’objet du coarticle du serveur.

</dd> <dt>

<span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Dessin/effacement
</dt> <dd>

Efface le contenu de dessin actuel et efface l’image de fenêtre. Sélection du menu : la plume/couleur affiche la boîte de dialogue choisir une couleur pour obtenir une nouvelle couleur de stylet pour le dessin.

</dd> <dt>

<span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Stylet/moyen
</dt> <dd>

Choisit la largeur moyenne pour le dessin. Une coche sur cette option de menu indique que moyenne est la largeur actuelle du stylet.

</dd> <dt>

<span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Plume/épais
</dt> <dd>

Choisit la largeur épaisse pour le dessin. Une coche sur cette option de menu indique que l’épaisseur est la largeur actuelle du stylet.

</dd> <dt>

<span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Plume/fin
</dt> <dd>

Choisit la largeur fine du dessin. Une coche sur cette option de menu indique que fin correspond à la largeur actuelle du stylet.

</dd> <dt>

<span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Récepteur/connexion
</dt> <dd>

Connecte l’interface COPaperSink IPaperSink au point de connexion PaperSink de l’objet du coarticle. Le redessin de l’image de dessin actuelle dans [StoClien](structured-storage-client-sample--stoclien-.md) s’appuie sur la connexion du récepteur. Une coche sur cette option de menu indique que le redessin est connecté.

</dd> <dt>

<span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Récepteur/déconnexion
</dt> <dd>

Déconnecte l’interface COPaperSink IPaperSink du point de connexion PaperSink de l’objet du coarticle. Le redessin de l’image de dessin actuelle dans [StoClien](structured-storage-client-sample--stoclien-.md) s’appuie sur la connexion du récepteur. Une coche sur cette option de menu indique que le redessin est déconnecté.

</dd> <dt>

<span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Didacticiel aide/StoClien
</dt> <dd>

Ouvre le fichier du didacticiel de STOCLIEN.HTM dans le navigateur Web.

</dd> <dt>

<span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Didacticiel aide/StoServe
</dt> <dd>

Ouvre le fichier du didacticiel de STOSERVE.HTM dans le navigateur Web.

</dd> <dt>

<span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Aide/lecture du fichier source
</dt> <dd>

Affiche la boîte de dialogue Ouvrir pour vous permettre d’ouvrir un fichier source à partir de cette leçon ou un autre dans le bloc-notes Windows.

</dd> <dt>

<span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Aide/à propos de StoClien
</dt> <dd>

Affiche la boîte de dialogue à propos de pour cette application.

</dd> </dl>

L’exemple [StoClien](structured-storage-client-sample--stoclien-.md) utilise de nombreux services et classes utilitaires fournis par [apputil](./using-visual-studio.md). Pour plus d’informations sur [apputil](./using-visual-studio.md), consultez le code source de la bibliothèque [apputil](./using-visual-studio.md) dans le répertoire [apputil](./using-visual-studio.md) frère et apputil.MD dans le répertoire principal du didacticiel. Pour plus d’informations sur [apputil](./using-visual-studio.md), consultez [Comment générer des exemples](how-to-build-samples.md).

 

 