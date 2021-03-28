---
description: Pour modifier une image stockée dans un métafichier amélioré, une application doit effectuer les tâches décrites dans la procédure suivante.
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: Modification d’un métafichier amélioré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86dc9cc609d616bf82ae3f0a13d8d63e827e3eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114667"
---
# <a name="editing-an-enhanced-metafile"></a><span data-ttu-id="c20bb-103">Modification d’un métafichier amélioré</span><span class="sxs-lookup"><span data-stu-id="c20bb-103">Editing an Enhanced Metafile</span></span>

<span data-ttu-id="c20bb-104">Pour modifier une image stockée dans un métafichier amélioré, une application doit effectuer les tâches décrites dans la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="c20bb-104">To edit a picture stored in an enhanced metafile, an application must perform the tasks described in the following procedure.</span></span>

<span data-ttu-id="c20bb-105">**Pour modifier une image stockée dans un métafichier amélioré**</span><span class="sxs-lookup"><span data-stu-id="c20bb-105">**To edit a picture stored in an enhanced metafile**</span></span>

1.  <span data-ttu-id="c20bb-106">Utilisez le test de positionnement pour capturer les coordonnées du curseur et récupérer la position de l’objet (trait, arc, Rectangle, ellipse, polygone ou forme irrégulière) que l’utilisateur souhaite modifier.</span><span class="sxs-lookup"><span data-stu-id="c20bb-106">Use hit-testing to capture the cursor coordinates and retrieve the position of the object (line, arc, rectangle, ellipse, polygon, or irregular shape) that the user wants to alter.</span></span>
2.  <span data-ttu-id="c20bb-107">Convertissez ces coordonnées en unités logiques (ou universelles).</span><span class="sxs-lookup"><span data-stu-id="c20bb-107">Convert these coordinates to logical (or world) units.</span></span>
3.  <span data-ttu-id="c20bb-108">Appelez la fonction [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) et examinez chaque enregistrement de métafichier.</span><span class="sxs-lookup"><span data-stu-id="c20bb-108">Call the [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) function and examine each metafile record.</span></span>
4.  <span data-ttu-id="c20bb-109">Détermine si un enregistrement donné correspond à une fonction de dessin GDI.</span><span class="sxs-lookup"><span data-stu-id="c20bb-109">Determine whether a given record corresponds to a GDI drawing function.</span></span>
5.  <span data-ttu-id="c20bb-110">Si c’est le cas, déterminez si les coordonnées stockées dans l’enregistrement correspondent à la ligne, à l’arc, à l’ellipse ou à tout autre élément graphique qui croise les coordonnées spécifiées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c20bb-110">If it does, determine whether the coordinates stored in the record correspond to the line, arc, ellipse, or other graphics element that intersects the coordinates specified by the user.</span></span>
6.  <span data-ttu-id="c20bb-111">Lors de la recherche de l’enregistrement correspondant à la sortie que l’utilisateur souhaite modifier, effacez l’objet sur l’écran qui correspond à l’enregistrement d’origine.</span><span class="sxs-lookup"><span data-stu-id="c20bb-111">Upon finding the record that corresponds to the output that the user wants to alter, erase the object on the screen that corresponds to the original record.</span></span>
7.  <span data-ttu-id="c20bb-112">Supprimez l’enregistrement correspondant du métafichier, en enregistrant un pointeur vers son emplacement.</span><span class="sxs-lookup"><span data-stu-id="c20bb-112">Delete the corresponding record from the metafile, saving a pointer to its location.</span></span>
8.  <span data-ttu-id="c20bb-113">Permet à l’utilisateur de redessiner ou de remplacer l’objet.</span><span class="sxs-lookup"><span data-stu-id="c20bb-113">Permit the user to redraw or replace the object.</span></span>
9.  <span data-ttu-id="c20bb-114">Convertissez les fonctions GDI utilisées pour dessiner le nouvel objet en un ou plusieurs enregistrements de métafichier amélioré.</span><span class="sxs-lookup"><span data-stu-id="c20bb-114">Convert the GDI functions used to draw the new object into one or more enhanced-metafile records.</span></span>
10. <span data-ttu-id="c20bb-115">Stockez ces enregistrements dans le métafichier amélioré.</span><span class="sxs-lookup"><span data-stu-id="c20bb-115">Store these records in the enhanced metafile.</span></span>

 

 



