---
description: ATM s’applique aux environnements LAN et WAN.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Annexe Winsock ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ec056cc2b84c9449ed466a60a15683df29744b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918920"
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

 

 



