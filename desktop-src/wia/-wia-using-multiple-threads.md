---
description: Lors de l’utilisation d’une interface WIA (Windows Image Acquisition) dans plusieurs threads au sein d’un même processus, une application doit fournir un marshaling pour cette interface.
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: Utilisation de plusieurs threads dans une application WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb1dbfa552e72dc068aff63a0a316d9af680ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113274"
---
# <a name="using-multiple-threads-in-a-wia-application"></a>Utilisation de plusieurs threads dans une application WIA

Lors de l’utilisation d’une interface WIA (Windows Image Acquisition) dans plusieurs threads au sein d’un même processus, une application doit fournir un marshaling pour cette interface. Si un thread crée un pointeur d’interface, vous ne pouvez pas utiliser ce pointeur dans un thread différent sans marshaling.

Par exemple, si un thread dans une application obtient un pointeur vers l’interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) , un thread distinct ne peut pas utiliser ce pointeur d’interface sans marshaling.

Une technique courante utilisée pour effectuer ce marshaling consiste à utiliser la table d’interface globale. La table d’interface globale est une table gérée sur tous les threads au sein d’un même processus. Tous les threads qui s’exécutent dans le processus peuvent récupérer des interfaces qui sont inscrites dans la table d’interface globale. Cette technique évite d’avoir à créer des flux pour passer des interfaces entre les threads.

Pour plus d’informations sur l’utilisation de la table d’interface globale, consultez [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

Même si vous n’envisagez pas d’utiliser plusieurs threads dans une application WIA, vous devez supposer que toutes les fonctions de transfert de données ou de rappel d’événement d’appareil s’exécutent dans des threads distincts.

 

 
