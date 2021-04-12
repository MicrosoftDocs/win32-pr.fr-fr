---
title: Contrôles de conteneur
description: Contrôles de conteneur
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69228bcc03017442880d41156f67397ee26bb13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462479"
---
# <a name="container-controls"></a><span data-ttu-id="fef48-103">Contrôles de conteneur</span><span class="sxs-lookup"><span data-stu-id="fef48-103">Container Controls</span></span>

<span data-ttu-id="fef48-104">Comme décrit ci-dessus, les contrôles de conteneur sont des contrôles ActiveX qui contiennent visuellement d’autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="fef48-104">As described above, container controls are ActiveX controls that visually contain other controls.</span></span> <span data-ttu-id="fef48-105">L’architecture des contrôles ActiveX spécifie l’interface [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) pour activer les contrôles de conteneur.</span><span class="sxs-lookup"><span data-stu-id="fef48-105">The ActiveX controls architecture specifies the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface to enable container controls.</span></span> <span data-ttu-id="fef48-106">Les conteneurs peuvent également prendre en charge les contrôles de conteneur sans prendre en charge **IsimpleFrameSite**, bien que le comportement ne puisse pas être garanti.</span><span class="sxs-lookup"><span data-stu-id="fef48-106">Containers may also support container controls without supporting **ISimpleFrameSite**, although the behavior cannot be guaranteed.</span></span> <span data-ttu-id="fef48-107">C’est pour cette raison qu’il existe une catégorie de composant pour les contrôles SimpleFrameSite où les fonctionnalités complètes de cette interface sont requises.</span><span class="sxs-lookup"><span data-stu-id="fef48-107">For this reason, a component category exists for SimpleFrameSite controls where the full functionality of this interface is required.</span></span>

<span data-ttu-id="fef48-108">Pour prendre en charge les contrôles de conteneur sans implémenter [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), un conteneur de contrôles ActiveX doit :</span><span class="sxs-lookup"><span data-stu-id="fef48-108">To support container controls without implementing [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), an ActiveX control container must:</span></span>

-   <span data-ttu-id="fef48-109">Activez tous les contrôles à tout moment.</span><span class="sxs-lookup"><span data-stu-id="fef48-109">Activate all controls at all times.</span></span>
-   <span data-ttu-id="fef48-110">Reparenter les contrôles contenus au hWnd du contrôle conteneur.</span><span class="sxs-lookup"><span data-stu-id="fef48-110">Reparent the contained controls to the hWnd of the containing control.</span></span>
-   <span data-ttu-id="fef48-111">Restez le parent du contrôle conteneur.</span><span class="sxs-lookup"><span data-stu-id="fef48-111">Remain the parent of the container control.</span></span>

 

 




