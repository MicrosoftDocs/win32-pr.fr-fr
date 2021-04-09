---
title: Réflexion de message
description: Réflexion de message
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cb563597e5aa92440e1b1434420e983268d9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028531"
---
# <a name="message-reflection"></a><span data-ttu-id="585e3-103">Réflexion de message</span><span class="sxs-lookup"><span data-stu-id="585e3-103">Message Reflection</span></span>

<span data-ttu-id="585e3-104">Il est fortement recommandé qu’un conteneur de contrôles ActiveX prenne en charge la réflexion de message.</span><span class="sxs-lookup"><span data-stu-id="585e3-104">It is strongly recommended that an ActiveX control container supports message reflection.</span></span> <span data-ttu-id="585e3-105">Cela entraînera une opération plus efficace pour les contrôles sous-classés.</span><span class="sxs-lookup"><span data-stu-id="585e3-105">This will result in more efficient operation for subclassed controls.</span></span> <span data-ttu-id="585e3-106">Si la réflexion de message est prise en charge, la propriété ambiante MessageReflect doit être prise en charge et avoir la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="585e3-106">If message reflection is supported, the MessageReflect ambient property must be supported and have a value of **TRUE**.</span></span> <span data-ttu-id="585e3-107">Si un conteneur n’implémente pas la réflexion de message, le CDK OLE crée deux fenêtres pour chaque contrôle sous-classé, afin de fournir la réflexion de message pour le compte du conteneur de contrôle.</span><span class="sxs-lookup"><span data-stu-id="585e3-107">If a container does not implement message reflection, then the OLE CDK creates two windows for every subclassed control, to provide message reflection on behalf on the control container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="585e3-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="585e3-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="585e3-109">Containers</span><span class="sxs-lookup"><span data-stu-id="585e3-109">Containers</span></span>](containers.md)
</dt> </dl>

 

 




