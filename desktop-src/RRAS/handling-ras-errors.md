---
title: Gestion des erreurs RAS
description: Lorsqu’une erreur se produit, le gestionnaire de connexions d’accès à distance appelle le gestionnaire de notification du client.
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- RAS du service d’accès à distance, Erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f37c18a795f5675fc6df80da6027526f81a87010
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239549"
---
# <a name="handling-ras-errors"></a>Gestion des erreurs RAS

Lorsqu’une erreur se produit, le gestionnaire de connexions d’accès à distance appelle le gestionnaire de notification du client. La notification indique l’état de la connexion lorsque l’erreur s’est produite, ainsi qu’un code qui identifie l’erreur. Dans ce cas, le gestionnaire de notifications doit appeler [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) pour mettre fin à la connexion RAS.

Les codes d’erreur qui identifient les erreurs RAS sont définis dans le fichier raserror. h. Le client RAS peut utiliser la fonction [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) pour obtenir une chaîne d’affichage décrivant l’erreur. Pour obtenir une description de ces erreurs, consultez [codes d’erreur du routage et de l’accès à distance](routing-and-remote-access-error-codes.md) .

 

 




