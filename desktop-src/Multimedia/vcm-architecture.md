---
title: Architecture VCM
description: Architecture VCM
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Video for Windows (VFW), architecture VCM
- VFW (vidéo pour Windows), architecture VCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7676fe7786b8674ddca957a75c33336294b65a9df18d53fe4b9c7f493092b66f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135597"
---
# <a name="vcm-architecture"></a>Architecture VCM

VCM est un intermédiaire entre une application et les pilotes de compression et de décompression. Les pilotes de compression et de décompression compressent et décompressent des frames de données individuels.

Lorsqu’une application effectue un appel à VCM, VCM convertit l’appel en message. Le message est envoyé à l’aide de la fonction [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) vers le compresseur ou décompresseur approprié, qui compresse ou décompresse les données. VCM reçoit la valeur de retour du pilote de compression ou de décompression, puis renvoie le contrôle à l’application.

Si une macro est définie pour un message, la macro se développe en un appel de fonction **ICSendMessage** fournissant les paramètres appropriés pour ce message. Si une macro est définie pour un message, votre application doit l’utiliser plutôt que le message. Dans cette vue d’ensemble, ces macros suivent des messages entre parenthèses.

 

 




