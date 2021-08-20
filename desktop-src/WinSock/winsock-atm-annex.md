---
description: ATM s’applique aux environnements LAN et WAN.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Annexe Winsock ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f55c71b830fa8a5f27f083af0263c62766e7b037e433c04b73bfea5ba12960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822445"
---
# <a name="winsock-atm-annex"></a>Annexe Winsock ATM

ATM s’applique aux environnements LAN et WAN. Un réseau ATM transporte simultanément un large éventail de trafic réseau (voix, données, image et vidéo). Il fournit aux utilisateurs une qualité de service garantie sur la base d’un canal virtuel (VC).



| Élément          | Description                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nom (s) de protocole | ATMPROTO \_ AAL5, ATMPROTO \_ AALUSER                                                                                                                           |
| Description      | La couche AAL5 ATM fournit un service de transport qui est orienté connexion, limite de message conservée et QOS garantie. ATMPROTO \_ AALUSER est une AAL définie par l’utilisateur. |
| Famille d’adresses   | \_ATM AF                                                                                                                                                     |
| Fichier d’en-tête      | Ws2atm. h                                                                                                                                                    |



 

Cette section décrit les extensions spécifiques au mode de transfert asynchrone (ATM) nécessaires pour prendre en charge les services ATM natifs tels qu’ils sont exposés et spécifiés dans la spécification de l’interface réseau utilisateur du Forum ATM version 3. x (3,0 et 3,1). Ce document prend en charge AAL type 5 (mode message) et AAL défini par l’utilisateur. Les versions ultérieures de ce document prendront en charge d’autres types de AAL et UNI 4,0.

 

 



