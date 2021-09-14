---
title: Utilisation de Teredo avec l’assistance IP
description: L’API d’assistance IP est utilisée par une application pour collecter et fournir des informations importantes sur la configuration réseau de l’ordinateur local.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5936ce9987262fe24cfd6cf718a426b6123b89
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118770"
---
# <a name="using-teredo-with-ip-helper"></a>Utilisation de Teredo avec l’assistance IP

L' [API d’assistance IP](/windows/desktop/IpHlp/about-ip-helper) est utilisée par une application pour collecter et fournir des informations importantes sur la configuration réseau de l’ordinateur local. en cas de fonctionnement sur la plateforme Windows Vista, ces informations incluent le port UDP dynamique affecté à l’interface Teredo et les modifications qui peuvent se produire sur le port désigné.

Les fonctions suivantes sont utilisées par l’API d’assistance IP pour faciliter l’utilisation de l’interface Teredo :

-   [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 