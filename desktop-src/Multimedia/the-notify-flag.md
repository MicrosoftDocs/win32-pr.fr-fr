---
title: Indicateur Notify
description: Indicateur Notify
ms.assetid: ed5dbb0b-ce4d-4bda-8daa-c62cfda717d1
keywords:
- Indicateur de MCI_NOTIFY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbec671a9810d31078eedf9b8557bcdc4fa7c3e82f688b7fd005f85cb4127476
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688269"
---
# <a name="the-notify-flag"></a>Indicateur Notify

L’indicateur « Notify » (MCI \_ Notify) indique à l’appareil de poster un message [**MCINOTIFY mm**](mm-mcinotify.md) lorsque l’appareil termine une action. Votre application doit avoir une procédure de fenêtre pour traiter le \_ message mm MCINOTIFY pour que la notification ait un effet. Un \_ message mm MCINOTIFY indique que le traitement d’une commande est terminé, mais il n’indique pas si la commande a été exécutée correctement, a échoué ou a été remplacée ou abandonnée.

L’application spécifie le handle vers la fenêtre de destination pour le message lorsqu’il émet une commande. Dans l’interface de chaîne de commande, ce descripteur est le dernier paramètre de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) . Dans l’interface de message de commande, le descripteur est spécifié dans le mot de poids faible du membre **dwCallBack** de la structure envoyée avec le message de commande. (Chaque structure associée à un message de commande contient ce membre.)

 

 