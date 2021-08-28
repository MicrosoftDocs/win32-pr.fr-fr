---
description: Un processus peut appeler WSPCloseSocket sur un socket dupliqué et le descripteur est libéré. Toutefois, le Socket sous-jacent reste ouvert jusqu’à ce que WSPCloseSocket soit appelé sur le dernier descripteur restant.
ms.assetid: dff1e932-5e87-4ec5-995d-686d20ba6236
title: Décompte de références
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8cd281363636cc2022725b4921d3b2d2b300e7262173e157a2be1610f6af0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996659"
---
# <a name="reference-counting"></a>Décompte de références

Un processus peut appeler [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) sur un socket dupliqué et le descripteur est libéré. Toutefois, le Socket sous-jacent reste ouvert jusqu’à ce que **WSPCloseSocket** soit appelé sur le dernier descripteur restant.

 

 
