---
title: Architecture VCM
description: Architecture VCM
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Video for Windows (VFW), architecture VCM
- VFW (vidéo pour Windows), architecture VCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b672c86053086f63127aae586517fac4906326
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310569"
---
# <a name="vcm-architecture"></a>Architecture VCM

VCM est un intermédiaire entre une application et les pilotes de compression et de décompression. Les pilotes de compression et de décompression compressent et décompressent des frames de données individuels.

Lorsqu’une application effectue un appel à VCM, VCM convertit l’appel en message. Le message est envoyé à l’aide de la fonction [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) vers le compresseur ou décompresseur approprié, qui compresse ou décompresse les données. VCM reçoit la valeur de retour du pilote de compression ou de décompression, puis renvoie le contrôle à l’application.

Si une macro est définie pour un message, la macro se développe en un appel de fonction **ICSendMessage** fournissant les paramètres appropriés pour ce message. Si une macro est définie pour un message, votre application doit l’utiliser plutôt que le message. Dans cette vue d’ensemble, ces macros suivent des messages entre parenthèses.

 

 




