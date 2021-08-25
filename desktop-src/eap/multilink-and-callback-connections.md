---
title: Connexions à liaisons multiples et rappels
description: Pour le premier lien d’une connexion à liaisons multiples, le service d’authentification définit l’indicateur de lien d’abord de l’indicateur EAP d’accès distant \_ \_ \_ \_ dans le membre fFlags de la \_ \_ structure d’entrée EAP PPP.
ms.assetid: a6aee73b-43b2-43b4-a6f1-ac7b293c44ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7493550863a755a87668c96dbe0ce600d524a111b7e7300b97c307f4d30c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852319"
---
# <a name="multilink-and-callback-connections"></a>Connexions à liaisons multiples et rappels

Pour le premier lien d’une connexion à liaisons multiples, le service d’authentification définit l’indicateur de lien d’abord de l’indicateur EAP d’accès distant \_ \_ \_ \_ dans le membre **fFlags** de la structure [**\_ \_ d’entrée EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) . Le protocole d’authentification peut utiliser la présence de cet indicateur pour déterminer s’il faut présenter une interface utilisateur spécifiquement pour le premier lien d’une connexion à liaisons multiples.

Si la connexion est configurée de sorte que le serveur rappelle l’ordinateur client, l' \_ indicateur d’abord de l’indicateur EAP EAP n’est \_ \_ \_ pas défini sur le rappel.

Si le protocole d’authentification affecte la **valeur true** au membre **fSaveConnectionData** de la [**\_ \_ sortie EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) , les liens suivants de la connexion multilien reçoivent les nouvelles données spécifiques à la connexion. Toutefois, dans le cas de données spécifiques à l’utilisateur, le protocole d’authentification continue à récupérer les données d’origine propres à l’utilisateur, même s’il affecte la **valeur true** au membre **fSaveUserData** de la **\_ \_ sortie EAP PPP** .

Le protocole d’authentification peut utiliser une [interface utilisateur interactive](interactive-user-interface.md) pour collecter des données pour un lien spécifique d’une connexion à liaisons multiples. Dans ce cas, le service d’authentification rend les données obtenues disponibles au protocole d’authentification lors des liens suivants. Toutefois, ces données ne sont jamais enregistrées dans un stockage persistant.

 

 




