---
description: L’une des fonctionnalités principales des fonctions de l’API d’impression GDI est la prise en charge de l’indépendance des appareils.
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: À propos de l’API d’impression GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6e8a34552a1198ebe618f463003fe28ded6aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523353"
---
# <a name="about-the-gdi-print-api"></a><span data-ttu-id="98f91-103">À propos de l’API d’impression GDI</span><span class="sxs-lookup"><span data-stu-id="98f91-103">About the GDI Print API</span></span>

<span data-ttu-id="98f91-104">L’une des fonctionnalités principales des fonctions de l’API d’impression GDI est la prise en charge de l’indépendance des appareils.</span><span class="sxs-lookup"><span data-stu-id="98f91-104">One of the chief features of the functions in the GDI print API is their support of device independence.</span></span> <span data-ttu-id="98f91-105">Au lieu d’émettre des commandes spécifiques à l’appareil pour dessiner la sortie sur une imprimante ou un traceur particulier, une application appelle des fonctions de haut niveau à partir de l’interface GDI (Graphics Device Interface).</span><span class="sxs-lookup"><span data-stu-id="98f91-105">Instead of issuing device-specific commands to draw output on a particular printer or plotter, an application calls high-level functions from the graphics device interface (GDI).</span></span> <span data-ttu-id="98f91-106">Par exemple, pour imprimer une image bitmap, une application peut appeler la fonction [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) , en fournissant les coordonnées de la bitmap, ainsi que les handles qui identifient les contextes de périphérique (DC) source et de destination.</span><span class="sxs-lookup"><span data-stu-id="98f91-106">For example, to print a bitmapped image, an application can call the [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) function, supplying the coordinates for the bitmap as well as handles identifying the source and destination device contexts (DCs).</span></span> <span data-ttu-id="98f91-107">L’appel à **BitBlt** est ensuite converti en commandes d’appareils brutes par un pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="98f91-107">The call to **BitBlt** is then converted to raw device commands by a printer driver.</span></span> <span data-ttu-id="98f91-108">Un pilote de périphérique est une bibliothèque de liens dynamiques (DLL) qui prend en charge l’interface de pilote de périphérique (DDI).</span><span class="sxs-lookup"><span data-stu-id="98f91-108">A device driver is a dynamic-link library (DLL) that supports the device driver interface (DDI).</span></span> <span data-ttu-id="98f91-109">Un pilote de périphérique génère des commandes d’appareil brutes lors du traitement des appels aux fonctions DDI effectuées par le moteur graphique.</span><span class="sxs-lookup"><span data-stu-id="98f91-109">A device driver generates raw device commands when it processes calls to DDI functions made by the graphics engine.</span></span> <span data-ttu-id="98f91-110">Les commandes sont traitées par l’imprimante lorsqu’elle imprime l’image.</span><span class="sxs-lookup"><span data-stu-id="98f91-110">The commands are processed by the printer when it prints the image.</span></span> <span data-ttu-id="98f91-111">La syntaxe, le nombre et le type de ces commandes varient d’un appareil à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="98f91-111">The syntax, number, and type of these commands vary from device to device.</span></span>

<span data-ttu-id="98f91-112">Cette vue d’ensemble fournit des informations sur les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="98f91-112">This overview provides information on the following topics.</span></span>

<dl>

[<span data-ttu-id="98f91-113">Interface d’impression par défaut</span><span class="sxs-lookup"><span data-stu-id="98f91-113">Default Printing Interface</span></span>](default-printing-interface.md)  
[<span data-ttu-id="98f91-114">Contextes de périphérique d’impression</span><span class="sxs-lookup"><span data-stu-id="98f91-114">Printer Device Contexts</span></span>](printer-output.md)  
[<span data-ttu-id="98f91-115">Échappements de l’imprimante</span><span class="sxs-lookup"><span data-stu-id="98f91-115">Printer Escapes</span></span>](printer-escapes.md)  
[<span data-ttu-id="98f91-116">Affichage et sortie WYSIWYG</span><span class="sxs-lookup"><span data-stu-id="98f91-116">WYSIWYG Display and Output</span></span>](wysiwyg-display-and-output.md)  
[<span data-ttu-id="98f91-117">DEVMODE par utilisateur</span><span class="sxs-lookup"><span data-stu-id="98f91-117">Per-User DEVMODE</span></span>](per-user-devmode.md)  
</dl>

 

 
