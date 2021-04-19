---
description: Utilisez les instructions suivantes pour créer une installation de Windows Installer qui affiche un message invitant l’utilisateur à insérer un disque.
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Messages d’invite de création de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f536a27c2adb5896992eb19a86bff64b9498d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519067"
---
# <a name="authoring-disk-prompt-messages"></a><span data-ttu-id="c6a6e-103">Messages d’invite de création de disque</span><span class="sxs-lookup"><span data-stu-id="c6a6e-103">Authoring Disk Prompt Messages</span></span>

<span data-ttu-id="c6a6e-104">Utilisez les instructions suivantes pour créer une installation de Windows Installer qui affiche un message invitant l’utilisateur à insérer un disque.</span><span class="sxs-lookup"><span data-stu-id="c6a6e-104">Use the following guidelines to author a Windows Installer installation that displays a message box prompting the user to insert a disk.</span></span>

<span data-ttu-id="c6a6e-105">**Pour afficher un message invitant l’utilisateur à insérer un disque**</span><span class="sxs-lookup"><span data-stu-id="c6a6e-105">**To display a message box prompting the user to insert a disk**</span></span>

1.  <span data-ttu-id="c6a6e-106">Utilisez les fonctionnalités de création du programme d’installation pour définir la chaîne de propriété [**DiskPrompt**](diskprompt.md) dans la table de [Propriétés](property-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c6a6e-106">Use the authoring capabilities of the installer to set the [**DiskPrompt**](diskprompt.md) property string in the [Property](property-table.md) table.</span></span> <span data-ttu-id="c6a6e-107">Cela doit inclure le nom du produit en cours d’installation et un paramètre d’espace réservé dans la chaîne pour le titre imprimé sur le disque.</span><span class="sxs-lookup"><span data-stu-id="c6a6e-107">This should include the name of the product being installed and a placeholder parameter within the string for the title printed on the disk.</span></span> <span data-ttu-id="c6a6e-108">Par exemple, pour Microsoft Publisher, la propriété **DiskPrompt** peut être « Microsoft Publisher : Disk \[ 1 \] », où \[ 1 \] est l’espace réservé pour le nom du disque.</span><span class="sxs-lookup"><span data-stu-id="c6a6e-108">For example, for Microsoft Publisher the **DiskPrompt** property could be "Microsoft Publisher: Disk \[1\]", where \[1\] is the placeholder for the disk title.</span></span>
2.  <span data-ttu-id="c6a6e-109">Entrez les titres de chacun des disques à demander dans des lignes distinctes de la colonne DiskPrompt de la table [multimédia](media-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c6a6e-109">Enter the titles of each of the disks being prompted for into separate rows of the DiskPrompt column of the [Media](media-table.md) table.</span></span> <span data-ttu-id="c6a6e-110">Par exemple, la première et seule entrée dans la table des médias peut être « 1 – install ».</span><span class="sxs-lookup"><span data-stu-id="c6a6e-110">For example, the first and only entry into the Media table could be "1–Install."</span></span>
3.  <span data-ttu-id="c6a6e-111">Au cours de l’action [InstallFiles](installfiles-action.md) , la valeur de la colonne DiskPrompt de la table [Media](media-table.md) est remplacée par l’espace réservé dans la chaîne de la propriété [**DiskPrompt**](diskprompt.md) .</span><span class="sxs-lookup"><span data-stu-id="c6a6e-111">During the [InstallFiles](installfiles-action.md) action the value from the DiskPrompt column of the [Media](media-table.md) table is substituted for the placeholder in the string of the [**DiskPrompt**](diskprompt.md) property.</span></span>
4.  <span data-ttu-id="c6a6e-112">Le message affiché par la boîte de message est créé à partir d’une chaîne de modèle intégrée dans la [table d’erreurs](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="c6a6e-112">The message displayed by the message box is created from a built-in template string in the [Error table](error-table.md).</span></span> <span data-ttu-id="c6a6e-113">Il s’agit de l’erreur 1302 et la chaîne de modèle est : « Insérez le disque : \[ 2 \] », et le \[ 2 \] représente un espace réservé pour la propriété [**DiskPrompt**](diskprompt.md) .</span><span class="sxs-lookup"><span data-stu-id="c6a6e-113">This is Error 1302 and the template string is: "Please insert the disk: \[2\]", and the \[2\] represents a placeholder for the [**DiskPrompt**](diskprompt.md) property.</span></span>

<span data-ttu-id="c6a6e-114">L’exemple affiche le message suivant à l’utilisateur : « veuillez insérer le disque : Microsoft Publisher : Disk 1 – install ».</span><span class="sxs-lookup"><span data-stu-id="c6a6e-114">The example displays the following message to the user: "Please insert the disk: Microsoft Publisher: Disk 1 – Install."</span></span>

<span data-ttu-id="c6a6e-115">Notez que les messages d’invite de disque sont affichés par tous les niveaux de l' [interface utilisateur](user-interface-levels.md) , sauf aucun.</span><span class="sxs-lookup"><span data-stu-id="c6a6e-115">Note that disk prompt messages get displayed by all [User Interface Levels](user-interface-levels.md) except None.</span></span>

 

 



