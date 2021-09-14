---
description: Les documents suivants fournissent des instructions sur l’utilisation de l’interface TAPI pour écrire des applications de communication d’utilisateur final ou de serveur. Ces informations sont également très utiles pour les programmeurs de fournisseurs de services.
ms.assetid: fb97aff7-910e-451f-b183-36324a459423
title: Applications TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6836f33af120171016b080693ae7a8315f9b9d7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011060"
---
# <a name="tapi-applications"></a>Applications TAPI

Les documents suivants fournissent des instructions sur l’utilisation de l’interface TAPI pour écrire des applications de communication d’utilisateur final ou de serveur. Ces informations sont également très utiles pour les programmeurs de fournisseurs de services.

La première décision qu’un programmeur doit effectuer dans à l’aide de l’interface TAPI est le niveau de service requis. Par exemple, si une application nécessite une sélection de menu qui peut composer un numéro de téléphone, une application TAPI complète n’est probablement pas nécessaire. La téléphonie assistée peut activer cette option rapidement et simplement. Pour plus d’informations sur la distinction entre les applications TAPI complètes et la téléphonie assistée, consultez [niveaux de service TAPI](tapi-levels-of-service.md) .

La deuxième décision importante est d’utiliser TAPI 2. x, l’API basée sur C ou TAPI 3. x, qui est basé sur COM. Pour plus d’informations sur les considérations importantes à utiliser, consultez [TAPI 3. x et TAPI 2. x](tapi-3-x-versus-tapi-2-x.md) .

Le diagramme suivant illustre les blocs de construction de base d’une application TAPI complète. TAPI 2. x et TAPI 3. x sont tous deux traités dans ces sections. Les documents qui sont très spécifiques à un élément sont traités dans les sections de vue d’ensemble pour TAPI 2. x ou TAPI 3. x.

![blocs de construction d’une application TAPI](images/tapior3.png)

Les liens suivants fournissent du contenu qui correspond aux chiffres de l’image ci-dessus :

| Configuration | Documentation                                                                    |
|--------|----------------------------------------------------------------------------------|
| 1      | [Initialisation TAPI](tapi-initialization.md)                                   |
| 2      | [Contrôle de session](session-control.md)                                           |
| 3      | [Contrôle de l’appareil](device-control.md)                                             |
| 4      | [Contrôle multimédia](media-control.md)                                               |
| 5      | [À propos des contrôles de centre d’appels](about-call-center-controls.md)                     |
| 6      | [Conférence de téléphonie IP Rendezvous](rendezvous-ip-telephony-conferencing.md) |
| 7      | [Arrêt de l’interface TAPI](tapi-shutdown.md)                                               |



 

 

 



