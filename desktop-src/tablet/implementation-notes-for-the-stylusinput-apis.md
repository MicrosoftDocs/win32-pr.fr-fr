---
description: Les classes RealTimeStylus, GestureRecognizer et DynamicRenderer sont implémentées en tant que wrappers COM et sont disponibles uniquement dans le code managé.
ms.assetid: db8f0f25-3650-4843-92e4-af5460841e7e
title: Remarques sur l’implémentation des API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c106dd0e940cf6fd9e54235af43901d14e511ead5e8908be56b464c483335b74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032377"
---
# <a name="implementation-notes-for-the-stylusinput-apis"></a>Remarques sur l’implémentation des API StylusInput

Les classes [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))et [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) sont implémentées en tant que wrappers com et sont disponibles uniquement dans le code managé.

Lorsque l’objet [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))ou [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) est ajouté en tant que plug-in à un objet **RealTimeStylus** , les objets COM sous-jacents interagissent au niveau com. Par conséquent, l’appel direct des méthodes des interfaces [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) ou [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) n’est pas pris en charge. L’ajout de l’objet **RealTimeStylus**, GestureRecognizer ou DynamicRenderer à l’objet **RealTimeStylus** est la seule façon d’accéder à ces fonctionnalités.

 

 
