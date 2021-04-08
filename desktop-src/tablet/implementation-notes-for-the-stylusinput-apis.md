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
# <a name="implementation-notes-for-the-stylusinput-apis"></a>Remarques sur l’implémentation des API StylusInput

Les classes [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))et [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) sont implémentées en tant que wrappers com et sont disponibles uniquement dans le code managé.

Lorsque l’objet [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))ou [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) est ajouté en tant que plug-in à un objet **RealTimeStylus** , les objets COM sous-jacents interagissent au niveau com. Par conséquent, l’appel direct des méthodes des interfaces [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) ou [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) n’est pas pris en charge. L’ajout de l’objet **RealTimeStylus**, GestureRecognizer ou DynamicRenderer à l’objet **RealTimeStylus** est la seule façon d’accéder à ces fonctionnalités.

 

 
