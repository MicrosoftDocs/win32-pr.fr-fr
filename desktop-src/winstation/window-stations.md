---
title: Stations Windows
description: Une station Windows contient un presse-papiers, une table Atom et un ou plusieurs objets de bureau. Chaque objet de station Windows est un objet sécurisable. Quand une station Windows est créée, elle est associée au processus appelant et assignée à la session active.
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- objets de station Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2048015e4b0c687932c4d01aafe31127e2141e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031412"
---
# <a name="window-stations"></a><span data-ttu-id="f9ba0-106">Stations Windows</span><span class="sxs-lookup"><span data-stu-id="f9ba0-106">Window Stations</span></span>

<span data-ttu-id="f9ba0-107">Une *station Windows* contient un presse-papiers, une table Atom et un ou plusieurs objets de [Bureau](desktops.md) .</span><span class="sxs-lookup"><span data-stu-id="f9ba0-107">A *window station* contains a clipboard, an atom table, and one or more [desktop](desktops.md) objects.</span></span> <span data-ttu-id="f9ba0-108">Chaque objet de station Windows est un objet sécurisable.</span><span class="sxs-lookup"><span data-stu-id="f9ba0-108">Each window station object is a securable object.</span></span> <span data-ttu-id="f9ba0-109">Quand une station Windows est créée, elle est associée au processus appelant et assignée à la session active.</span><span class="sxs-lookup"><span data-stu-id="f9ba0-109">When a window station is created, it is associated with the calling process and assigned to the current session.</span></span>

<span data-ttu-id="f9ba0-110">La *station Windows Interactive* est la seule station Windows qui peut afficher une interface utilisateur ou recevoir une entrée d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f9ba0-110">The *interactive window station* is the only window station that can display a user interface or receive user input.</span></span> <span data-ttu-id="f9ba0-111">Elle est assignée à la session d’ouverture de session de l’utilisateur interactif et contient le clavier, la souris et le périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f9ba0-111">It is assigned to the logon session of the interactive user, and contains the keyboard, mouse, and display device.</span></span> <span data-ttu-id="f9ba0-112">Elle est toujours nommée « WinSta0 ».</span><span class="sxs-lookup"><span data-stu-id="f9ba0-112">It is always named "WinSta0".</span></span> <span data-ttu-id="f9ba0-113">Toutes les autres stations Windows ne sont pas interactives, ce qui signifie qu’elles ne peuvent pas afficher une interface utilisateur ni recevoir d’entrée d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f9ba0-113">All other window stations are noninteractive, which means they cannot display a user interface or receive user input.</span></span>

<span data-ttu-id="f9ba0-114">Lorsqu’un utilisateur se connecte à un ordinateur à l’aide de Services Bureau à distance, une session est démarrée pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f9ba0-114">When a user logs on to a computer using Remote Desktop Services, a session is started for the user.</span></span> <span data-ttu-id="f9ba0-115">Chaque session est associée à sa propre station de fenêtre interactive nommée « WinSta0 ».</span><span class="sxs-lookup"><span data-stu-id="f9ba0-115">Each session is associated with its own interactive window station named "WinSta0".</span></span> <span data-ttu-id="f9ba0-116">Pour plus d’informations, consultez [Bureau à distance des sessions](/windows/desktop/TermServ/terminal-services-sessions).</span><span class="sxs-lookup"><span data-stu-id="f9ba0-116">For more information, see [Remote Desktop Sessions](/windows/desktop/TermServ/terminal-services-sessions).</span></span>

<span data-ttu-id="f9ba0-117">Pour plus d’informations sur les stations de Windows, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9ba0-117">For more information on window stations, see the following topics:</span></span>

-   [<span data-ttu-id="f9ba0-118">Station Windows et création de bureau</span><span class="sxs-lookup"><span data-stu-id="f9ba0-118">Window Station and Desktop Creation</span></span>](window-station-and-desktop-creation.md)
-   [<span data-ttu-id="f9ba0-119">Traiter la connexion à une station Windows</span><span class="sxs-lookup"><span data-stu-id="f9ba0-119">Process Connection to a Window Station</span></span>](process-connection-to-a-window-station.md)
-   [<span data-ttu-id="f9ba0-120">Sécurité de station Windows et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="f9ba0-120">Window Station Security and Access Rights</span></span>](window-station-security-and-access-rights.md)

 

 