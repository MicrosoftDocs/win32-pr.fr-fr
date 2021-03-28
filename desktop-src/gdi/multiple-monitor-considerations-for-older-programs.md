---
description: En règle générale, les applications plus anciennes n’ont pas besoin de modifications pour fonctionner sur plusieurs systèmes de surveillance.
ms.assetid: 908cf88c-69ed-4855-817d-ba749e14ff85
title: Considérations relatives à la surveillance multiple pour les anciens programmes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feebb356cb2f9c5480c84f1718b51d6e866ef621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972634"
---
# <a name="multiple-monitor-considerations-for-older-programs"></a><span data-ttu-id="6fd7b-103">Considérations relatives à la surveillance multiple pour les anciens programmes</span><span class="sxs-lookup"><span data-stu-id="6fd7b-103">Multiple Monitor Considerations for Older Programs</span></span>

<span data-ttu-id="6fd7b-104">En règle générale, les applications plus anciennes n’ont pas besoin de modifications pour fonctionner sur plusieurs systèmes de surveillance.</span><span class="sxs-lookup"><span data-stu-id="6fd7b-104">Generally, older applications do not need changes to work on multiple monitor systems.</span></span> <span data-ttu-id="6fd7b-105">Pour la plupart, le système semble avoir un seul affichage.</span><span class="sxs-lookup"><span data-stu-id="6fd7b-105">For most, the system will appear to have only one display.</span></span> <span data-ttu-id="6fd7b-106">Les métriques système reflètent l’affichage principal et les applications plein écran apparaissent sur le serveur principal.</span><span class="sxs-lookup"><span data-stu-id="6fd7b-106">System metrics reflect the primary display and fullscreen applications show up on the primary.</span></span> <span data-ttu-id="6fd7b-107">Le système gère la minimisation, l’agrandissement, les menus et les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6fd7b-107">The system handles minimization, maximization, menus, and dialog boxes.</span></span>

<span data-ttu-id="6fd7b-108">Toutefois, certains programmes rencontrent des problèmes.</span><span class="sxs-lookup"><span data-stu-id="6fd7b-108">However, some programs will have problems.</span></span> <span data-ttu-id="6fd7b-109">Certains peuvent avoir des problèmes : les applications de contrôle à distance, celles qui disposent d’un accès direct au matériel et celles qui ont corrigé le GDI ou le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="6fd7b-109">Some that could have problems are remote control applications, those that have direct hardware access, and those that have patched the GDI or DISPLAY driver.</span></span> <span data-ttu-id="6fd7b-110">Dans ce cas, l’utilisateur peut être amené à désactiver une analyse au-delà du moniteur principal.</span><span class="sxs-lookup"><span data-stu-id="6fd7b-110">In these cases, the user may be required to disable any monitor beyond the primary monitor.</span></span>

 

 



