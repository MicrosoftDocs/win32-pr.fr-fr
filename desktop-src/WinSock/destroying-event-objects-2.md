---
description: Utilisation de WPUCloseEvent pour détruire un objet d’événement (application ou fournisseur de services) lorsque l’objet d’événement n’est plus nécessaire.
ms.assetid: ad6f7018-3647-4ab8-9a77-d833d18cd4b6
title: Destruction d’objets d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 255413de4b058e01f82db654efd8b27f35bf249f553e26095800ad3938b1ac0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858509"
---
# <a name="destroying-event-objects"></a>Destruction d’objets d’événement

L’entité qui crée un objet d’événement (application ou fournisseur de services) est chargée de la détruire lorsqu’elle n’est plus nécessaire. Les fournisseurs de services le font par le biais de **WPUCloseEvent**.

 

 



