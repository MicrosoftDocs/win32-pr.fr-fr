---
description: Gestion des éjections de disque
ms.assetid: c43dd795-749b-4ca7-8510-71d62e0076b3
title: Gestion des éjections de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8964c8fd18395e932e1536e885bae1814d5952fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119905"
---
# <a name="handling-disc-ejections"></a>Gestion des éjections de disque

Lorsque l’utilisateur éjecte un DVD du lecteur, le navigateur DVD envoie à votre application un message d' \_ \_ éjection du disque DVD \_ . L’application peut ignorer ce message en toute sécurité et laisser le navigateur DVD gérer l’état du graphique. Une application peut également gérer la \_ \_ méthode d’éjection du disque DVD EC \_ pour implémenter un comportement personnalisé lorsqu’un disque est éjecté. Si vous gérez le message, vous devez définir l' \_ indicateur DVD ResetOnStop sur **true** avec la méthode [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) , puis appeler [**IMediaControl :: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) avant de fermer l’application ou de regarder un autre disque.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 



