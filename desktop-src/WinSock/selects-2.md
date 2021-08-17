---
description: Dans l’interface de socket BSD (Berkeley Software Distribution) d’origine, la fonction Select était la méthode standard (et uniquement) pour obtenir des indications sur les événements réseau.
ms.assetid: f7f42b03-1f89-4801-abf0-396ff8b61cae
title: Sélectionne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c075d2b8b18de79c25852eb0949cc727a8f3474e39392cf6e0a50fc60390d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740921"
---
# <a name="selects"></a>Sélectionne

Dans l’interface de socket BSD (Berkeley Software Distribution) d’origine, la fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) était la méthode standard (et uniquement) pour obtenir des indications sur les événements réseau. Pour chaque socket, les informations sur l’état de lecture, d’écriture ou d’erreur peuvent être interrogées ou attendues. Pour plus d’informations, consultez [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) . Notez que \_ la qualité de service (QoS) de l’événement réseau ne peut pas être obtenue par cette approche.

 

 
