---
description: Windows Les objets d’événement sockets sont des constructions simples qui peuvent être créées et fermées, définies et désactivées, attendues et interrogées.
ms.assetid: 65a7627e-150e-4ca3-bc17-d2b380ee02d1
title: utilisation d’objets d’événement (Windows sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d500656279d328046e2792b47a296bc2347e3478e36c7d81a5e781023887dc51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121159"
---
# <a name="using-event-objects-windows-sockets-2"></a>utilisation d’objets d’événement (Windows sockets 2)

Windows Les objets d’événement sockets sont des constructions simples qui peuvent être créées et fermées, définies et désactivées, attendues et interrogées. Le modèle accepté permet aux clients de créer un objet d’événement et de fournir le descripteur en tant que paramètre (ou en tant que composant d’une structure de paramètres) dans des fonctions telles que [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) et [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). Lorsque la condition nommée s’est produite, le fournisseur de services utilise le handle pour définir l’objet d’événement en appelant [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent). Pendant ce temps, le client Winsock SPI peut bloquer et attendre ou interroger jusqu’à ce que l’objet d’événement soit défini (signalé). Le client peut ensuite effacer ou réinitialiser l’objet d’événement et l’utiliser à nouveau.

 

 
