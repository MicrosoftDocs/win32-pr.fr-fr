---
title: Instructions du serveur
description: Pour que Microsoft Active Accessibility fonctionne comme prévu, les serveurs doivent fournir des informations d’accessibilité aux clients.
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344721428c94e2ea3d9e9ff78e194851ba9304db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379705"
---
# <a name="server-guidelines"></a><span data-ttu-id="e6453-103">Instructions du serveur</span><span class="sxs-lookup"><span data-stu-id="e6453-103">Server Guidelines</span></span>

<span data-ttu-id="e6453-104">Pour que Microsoft Active Accessibility fonctionne comme prévu, les serveurs doivent fournir des informations d’accessibilité aux clients.</span><span class="sxs-lookup"><span data-stu-id="e6453-104">For Microsoft Active Accessibility to work as designed, servers must provide accessibility information to clients.</span></span>

<span data-ttu-id="e6453-105">Pour implémenter [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), les développeurs de serveurs doivent suivre ce processus de base.</span><span class="sxs-lookup"><span data-stu-id="e6453-105">To implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), server developers must follow this basic process.</span></span>

1.  <span data-ttu-id="e6453-106">Créez des objets accessibles en implémentant les propriétés et les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour vos éléments d’interface utilisateur personnalisés et pour le client de votre application.</span><span class="sxs-lookup"><span data-stu-id="e6453-106">Create accessible objects by implementing the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods for your custom user interface elements and for your application's client.</span></span> <span data-ttu-id="e6453-107">Veillez à fournir une interface double qui prend en charge à la fois **IAccessible** et [**IDispatch**](idispatch-interface.md) afin que les clients écrits dans Microsoft Visual Basic et divers langages de script puissent obtenir des informations sur les objets.</span><span class="sxs-lookup"><span data-stu-id="e6453-107">Be sure to provide a dual interface that supports both **IAccessible** and [**IDispatch**](idispatch-interface.md) so that clients written in Microsoft Visual Basic and various scripting languages can get information about the objects.</span></span>
2.  <span data-ttu-id="e6453-108">Appelez [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) pour informer les clients des modifications apportées à vos éléments d’interface utilisateur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="e6453-108">Call [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) to notify clients of changes to your custom user interface elements.</span></span>
3.  <span data-ttu-id="e6453-109">Gérez [**WM \_ GETOBJECT**](wm-getobject.md) pour fournir l’accès à vos objets accessibles.</span><span class="sxs-lookup"><span data-stu-id="e6453-109">Handle [**WM\_GETOBJECT**](wm-getobject.md) to provide access to your accessible objects.</span></span>

<span data-ttu-id="e6453-110">Pour obtenir des suggestions et des conseils sur la conception d’objets accessibles, consultez le [Guide du développeur pour les serveurs Active Accessibility](developer-s-guide-for-active-accessibility-servers.md).</span><span class="sxs-lookup"><span data-stu-id="e6453-110">For suggestions and guidelines for designing accessible objects, see [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e6453-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e6453-111">In this section</span></span>

-   [<span data-ttu-id="e6453-112">Comment les serveurs implémentent des ID enfants</span><span class="sxs-lookup"><span data-stu-id="e6453-112">How Servers Implement Child IDs</span></span>](how-servers-implement-child-ids.md)

 

 




