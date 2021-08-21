---
title: Considérations sur la programmation des points de contrôle
description: Les développeurs qui créent des applications basées sur UPnP (ou des points de contrôle) doivent utiliser ces applications à partir d’un \_ client APARTMENTTHREADED coinit. Il existe des problèmes connus lors de l’utilisation de l’API de point de contrôle à partir d’un \_ client multithread coinit s’exécutant sous stress.
ms.assetid: a5d79a29-4192-40af-b75d-a31f1f46149c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f719bc75c83bf41b1d381b0d92471db777a9c246686fd21e702b5f5d9c19aabf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126084"
---
# <a name="control-point-programming-considerations"></a>Considérations sur la programmation des points de contrôle

Les développeurs qui créent des applications basées sur UPnP (ou des points de contrôle) doivent utiliser ces applications à partir d’un \_ client APARTMENTTHREADED coinit. Il existe des problèmes connus lors de l’utilisation de l’API de point de contrôle à partir d’un \_ client multithread coinit s’exécutant sous stress.

 

 




