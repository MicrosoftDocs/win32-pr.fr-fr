---
description: La fonction phoneClose ferme l’appareil téléphonique spécifié.
ms.assetid: 7607d779-0715-48a3-a4f2-bcf07026d7c5
title: Fermeture de l’appareil téléphonique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137004e63b4b377e9ee88266d11f9c2b21d0af7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527232"
---
# <a name="closing-the-phone-device"></a>Fermeture de l’appareil téléphonique

La fonction [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) ferme l’appareil téléphonique spécifié. L’appareil téléphonique peut également être fermé de force une fois que l’utilisateur a modifié la configuration de ce téléphone ou de son pilote. Si l’utilisateur souhaite que les modifications de configuration soient effectives immédiatement (par opposition à après le redémarrage du système suivant), et qu’elles affectent la vue actuelle de l’application de l’appareil (par exemple, une modification des fonctionnalités de l’appareil), un fournisseur de services peut forcer la fermeture de l’appareil téléphonique.

Ces messages peuvent également être envoyés sans sollicitation à la suite de la récupération de l’appareil téléphonique d’une autre manière. Une application doit donc être prête à gérer les messages de [**\_ fermeture de téléphone**](phone-close.md) non sollicités. Au moment de la fermeture de l’appareil, les réponses asynchrones en suspens relatives à cet appareil sont supprimées.

 

 



