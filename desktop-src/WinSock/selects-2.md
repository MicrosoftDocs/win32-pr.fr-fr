---
description: Dans l’interface de socket BSD (Berkeley Software Distribution) d’origine, la fonction Select était la méthode standard (et uniquement) pour obtenir des indications sur les événements réseau.
ms.assetid: f7f42b03-1f89-4801-abf0-396ff8b61cae
title: Sélectionne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e50339f298c18c75ad6451590f191fc1bd8afba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534435"
---
# <a name="selects"></a>Sélectionne

Dans l’interface de socket BSD (Berkeley Software Distribution) d’origine, la fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) était la méthode standard (et uniquement) pour obtenir des indications sur les événements réseau. Pour chaque socket, les informations sur l’état de lecture, d’écriture ou d’erreur peuvent être interrogées ou attendues. Pour plus d’informations, consultez [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) . Notez que \_ la qualité de service (QoS) de l’événement réseau ne peut pas être obtenue par cette approche.

 

 
