---
description: Les classes RealTimeStylus, GestureRecognizer et DynamicRenderer sont implémentées en tant que wrappers COM et sont disponibles uniquement dans le code managé.
ms.assetid: db8f0f25-3650-4843-92e4-af5460841e7e
title: Remarques sur l’implémentation des API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47150d6a9aff5495e89f30d29929fd7d604f9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951013"
---
# <a name="implementation-notes-for-the-stylusinput-apis"></a><span data-ttu-id="d02a8-103">Remarques sur l’implémentation des API StylusInput</span><span class="sxs-lookup"><span data-stu-id="d02a8-103">Implementation Notes for the StylusInput APIs</span></span>

<span data-ttu-id="d02a8-104">Les classes [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))et [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) sont implémentées en tant que wrappers com et sont disponibles uniquement dans le code managé.</span><span class="sxs-lookup"><span data-stu-id="d02a8-104">The [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100)), and [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) classes are implemented as COM wrappers and are available only in managed code.</span></span>

<span data-ttu-id="d02a8-105">Lorsque l’objet [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))ou [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) est ajouté en tant que plug-in à un objet **RealTimeStylus** , les objets COM sous-jacents interagissent au niveau com.</span><span class="sxs-lookup"><span data-stu-id="d02a8-105">When the [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100)), or [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) object is added as a plug-in to a **RealTimeStylus** object, the underlying COM objects interact on the COM level.</span></span> <span data-ttu-id="d02a8-106">Par conséquent, l’appel direct des méthodes des interfaces [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) ou [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d02a8-106">Therefore, directly calling the methods of the [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) or [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) interfaces are not supported.</span></span> <span data-ttu-id="d02a8-107">L’ajout de l’objet **RealTimeStylus**, GestureRecognizer ou DynamicRenderer à l’objet **RealTimeStylus** est la seule façon d’accéder à ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="d02a8-107">Adding the **RealTimeStylus**, GestureRecognizer, or DynamicRenderer object to the **RealTimeStylus** object is the only way to access these features.</span></span>

 

 
