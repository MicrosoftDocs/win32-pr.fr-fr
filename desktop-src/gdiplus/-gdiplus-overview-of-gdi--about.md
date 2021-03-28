---
description: Windows GDI+ est le sous-système du système d’exploitation Windows XP ou Windows Server 2003 qui est responsable de l’affichage des informations sur les écrans et les imprimantes. GDI+ est une API exposée par le biais d’un ensemble de classes C++.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Vue d’ensemble de GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6eb3885d33ad332ac61454525367788d7aed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991317"
---
# <a name="overview-of-gdi"></a><span data-ttu-id="d5dc6-104">Vue d’ensemble de GDI+</span><span class="sxs-lookup"><span data-stu-id="d5dc6-104">Overview of GDI+</span></span>

<span data-ttu-id="d5dc6-105">Windows GDI+ est le sous-système du système d’exploitation Windows XP ou Windows Server 2003 qui est responsable de l’affichage des informations sur les écrans et les imprimantes.</span><span class="sxs-lookup"><span data-stu-id="d5dc6-105">Windows GDI+ is the subsystem of the Windows XP operating system or Windows Server 2003 that is responsible for displaying information on screens and printers.</span></span> <span data-ttu-id="d5dc6-106">GDI+ est une API exposée par le biais d’un ensemble de classes C++.</span><span class="sxs-lookup"><span data-stu-id="d5dc6-106">GDI+ is an API that is exposed through a set of C++ classes.</span></span>

<span data-ttu-id="d5dc6-107">Comme son nom l’indique, GDI+ est le successeur de Windows Graphics Device Interface (GDI), l’interface de périphérique graphique incluse avec les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="d5dc6-107">As its name suggests, GDI+ is the successor to Windows Graphics Device Interface (GDI), the graphics device interface included with earlier versions of Windows.</span></span> <span data-ttu-id="d5dc6-108">Windows XP ou Windows Server 2003 prend en charge GDI pour la compatibilité avec les applications existantes, mais les programmeurs de nouvelles applications doivent utiliser GDI+ pour tous leurs besoins graphiques, car GDI+ optimise la plupart des fonctionnalités de GDI et fournit également des fonctionnalités supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d5dc6-108">Windows XP or Windows Server 2003 supports GDI for compatibility with existing applications, but programmers of new applications should use GDI+ for all their graphics needs because GDI+ optimizes many of the capabilities of GDI and also provides additional features.</span></span>

<span data-ttu-id="d5dc6-109">Une interface de périphérique graphique, telle que GDI+, permet aux programmeurs d’applications d’afficher des informations sur un écran ou une imprimante sans se préoccuper des détails d’un périphérique d’affichage particulier.</span><span class="sxs-lookup"><span data-stu-id="d5dc6-109">A graphics device interface, such as GDI+, allows application programmers to display information on a screen or printer without having to be concerned about the details of a particular display device.</span></span> <span data-ttu-id="d5dc6-110">Le programmeur d’applications effectue des appels aux méthodes fournies par les classes GDI+ et ces méthodes effectuent à leur tour les appels appropriés à des pilotes de périphérique spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d5dc6-110">The application programmer makes calls to methods provided by GDI+ classes and those methods in turn make the appropriate calls to specific device drivers.</span></span> <span data-ttu-id="d5dc6-111">GDI+ isole l’application du matériel graphique, et c’est cette isolation qui permet aux développeurs de créer des applications indépendantes du périphérique.</span><span class="sxs-lookup"><span data-stu-id="d5dc6-111">GDI+ insulates the application from the graphics hardware, and it is this insulation that allows developers to create device-independent applications.</span></span>

 

 



