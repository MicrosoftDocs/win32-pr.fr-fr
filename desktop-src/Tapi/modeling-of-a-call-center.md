---
description: Les fournisseurs de services peuvent exposer chaque ressource sur le PBX comme un périphérique de ligne et éventuellement un appareil téléphonique associé.
ms.assetid: 25394b19-bf75-4adc-b07d-41bc781931b6
title: Modélisation d’un centre d’appels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2763a1baafa41cf2d9b3b9b3c9d13be675a02d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393339"
---
# <a name="modeling-of-a-call-center"></a>Modélisation d’un centre d’appels

Les fournisseurs de services peuvent exposer chaque ressource sur le PBX comme un périphérique de ligne et éventuellement un appareil téléphonique associé. Les terminaux qui prennent en charge plusieurs apparences d’appels le font par le biais de plusieurs adresses, comme dans le contrôle d’appel interne. En fait, l’affichage tiers d’un appareil est identique à celui de la première vue ; les applications sur le serveur peuvent voir et contrôler tous les appareils internes, tandis qu’un PC client individuel connecté au serveur ne peut voir que les périphériques qui y sont visibles via les contrôles d’accès administrés par TAPISRV sur le serveur. Les ressources autres que les terminaux peuvent également être modélisées comme des appareils en ligne. Par exemple, une file d’attente ou un point de route ACD est modélisé comme un périphérique de ligne qui peut avoir de nombreux appels actifs ; un serveur IVR, un serveur de messagerie vocale ou un ensemble de ports de numérotation prédictifs peut également être modélisé comme un périphérique de ligne qui prend en charge plusieurs appels.

Dans ce modèle, l’état de l’appareil adressé et les appels associés à ce dernier peuvent être surveillés via des messages TAPI existants tels que [**line \_ LINEDEVSTATE**](line-linedevstate.md), [**line \_ ADDRESSSTATE**](line-addressstate.md), [**line \_ CALLSTATE**](line-callstate.md)et [**line \_ CALLINFO**](line-callinfo.md), ainsi que des détails obtenus via des fonctions telles que [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus), [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus), [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)et [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo). Chaque fois qu’un objet TAPI est utilisé par le biais d’une application tierce s’exécutant sur le serveur, le résultat est identique à ce qui aurait eu lieu si le même objet avait été traité de manière similaire par une application de première partie s’exécutant sur un PC client associé à cet appareil. Les indications d’État envoyées par le fournisseur de services de serveur contrôlant l’infrastructure de commutation (ou commutateur) sont remises aux applications qui s’exécutent sur le serveur et à celles qui s’exécutent sur les clients autorisés et associés.

 

 



