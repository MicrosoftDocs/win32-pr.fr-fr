---
description: Description des manières d’améliorer les performances lors de l’utilisation des interfaces de programmation d’applications (API) StylusInput.
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: Considérations relatives aux performances de l’API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef40ab389687cd42ef516a61f61ab86a7eb79d4efac9ae6e9dd698e93e54bff0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856491"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a>Considérations relatives aux performances de l’API StylusInput

La liste suivante décrit quelques méthodes permettant d’améliorer les performances des applications qui utilisent les API StylusInput.

-   Utilisez la propriété [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) pour vous abonner uniquement aux données pertinentes pour votre plug-in. Cela réduit le nombre total d’appels de méthode que l’objet [**RealTimeStylus**](realtimestylus-class.md) effectue et réduit également la complexité de votre plug-in. L’objet **RealTimeStylus** vérifie uniquement la propriété DataInterest lorsque le plug-in est attaché.
-   Réduisez la complexité des plug-ins synchrones. Les plug-ins synchrones sont généralement appelés par le thread de l’objet [**RealTimeStylus**](realtimestylus-class.md) et peuvent contribuer aux retards dans la collection d’encres.
-   Envisagez de rendre votre plug-in asynchrone. Si votre plug-in est complexe et doit ajouter des données personnalisées à la file d’attente de l’objet [**RealTimeStylus**](realtimestylus-class.md) , envisagez d’utiliser un modèle **RealTimeStylus** monté en cascade et d’ajouter le plug-in à la collection de plug-in synchrone de l’objet **RealTimeStylus** secondaire. Pour plus d’informations sur le modèle **RealTimeStylus** monté en cascade, consultez [le modèle RealTimeStylus monté en cascade](the-cascaded-realtimestylus-model.md).

 

 
