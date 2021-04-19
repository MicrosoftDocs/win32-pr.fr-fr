---
description: Description de l’utilisation d’Active Accessibility pour exposer des contrôles personnalisés pour le Tablet PC.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Utilisation de Active Accessibility pour exposer des contrôles personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d33d4c2b57a881cfbdc15f14e71e339ed7f9e84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515013"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a><span data-ttu-id="7037f-103">Utilisation de Active Accessibility pour exposer des contrôles personnalisés</span><span class="sxs-lookup"><span data-stu-id="7037f-103">Using Active Accessibility to Expose Custom Controls</span></span>

<span data-ttu-id="7037f-104">Vous pouvez utiliser Microsoft Active Accessibility comme méthode efficace pour rendre les contrôles personnalisés compatibles avec les aides à l’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="7037f-104">You can use Microsoft Active Accessibility as an effective way to make custom controls compatible with accessibility aids.</span></span> <span data-ttu-id="7037f-105">Active Accessibility nécessite que l’application :</span><span class="sxs-lookup"><span data-stu-id="7037f-105">Active Accessibility requires that the application:</span></span>

-   <span data-ttu-id="7037f-106">Créez des objets COM (Component Object Model) qui représentent des contrôles personnalisés individuels ou des groupes de contrôles qui prennent correctement en charge l’interface **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="7037f-106">Create Component Object Model (COM) objects that represent individual custom controls or groups of controls that properly support the **IAccessible** interface.</span></span> <span data-ttu-id="7037f-107">(L’objet peut être créé à la demande lorsqu’il est demandé par un client Active Accessibility.)</span><span class="sxs-lookup"><span data-stu-id="7037f-107">(The object may be created on demand when it is requested by an Active Accessibility client.)</span></span>
-   <span data-ttu-id="7037f-108">Appelez [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) lorsque les contrôles sont créés ou détruits, gagnez ou perdez le focus ou modifiez l’État.</span><span class="sxs-lookup"><span data-stu-id="7037f-108">Call [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) when the controls are created or destroyed, gain or lose focus, or otherwise change state.</span></span>
-   <span data-ttu-id="7037f-109">Gérez le \_ message WM GETOBJECT lorsqu’il est utilisé pour interroger les propriétés de l’objet ou des objets.</span><span class="sxs-lookup"><span data-stu-id="7037f-109">Handle the WM\_GETOBJECT message when used to query properties of the object or objects.</span></span>

<span data-ttu-id="7037f-110">Dans le cadre de cette discussion, une fenêtre contenant d’autres objets personnalisés doit également être exposée à Active Accessibility, ce qui permet au client de découvrir et d’accéder aux objets enfants.</span><span class="sxs-lookup"><span data-stu-id="7037f-110">For the purposes of this discussion, a window containing other custom objects also needs to be exposed to Active Accessibility, allowing the client to discover and navigate to the child objects.</span></span> <span data-ttu-id="7037f-111">Pour plus d’informations sur la façon de rendre les contrôles personnalisés compatibles avec les aides à l’accessibilité, consultez [accessibilité](../accessibility/accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="7037f-111">For more information about how to make custom controls compatible with accessibility aids, see [Accessibility](../accessibility/accessibility.md).</span></span>

 

 
