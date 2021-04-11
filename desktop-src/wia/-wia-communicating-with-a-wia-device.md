---
description: Quand un thread communique activement avec un périphérique WIA (Windows Image Acquisition) (par exemple, le transfert de données ou l’écriture de propriétés d’appareil) WIA &\# 0034 ; verrouille&\# 0034 ; l’appareil.
ms.assetid: 59533937-284a-4732-a73b-d2e0b5a9a370
title: Communication avec un appareil WIA dans plusieurs threads ou applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7a4b518093c3a0fc09534d67e22e5349d44d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202893"
---
# <a name="communicating-with-a-wia-device-in-multiple-threads-or-applications"></a>Communication avec un appareil WIA dans plusieurs threads ou applications

Quand un thread communique activement avec un périphérique WIA (Windows Image Acquisition) (par exemple, en transférant des données ou en écrivant des propriétés d’appareil), WIA « verrouille » l’appareil. Quand un appareil est verrouillé, aucun autre thread ou processus ne peut communiquer activement avec cet appareil.

WIA n’interdit pas à plusieurs threads ou processus de maintenir des connexions à un seul appareil. Autrement dit, un appareil est verrouillé uniquement pendant la communication réelle, et au moins deux applications peuvent avoir un seul appareil sélectionné simultanément.

WIA crée une arborescence d’éléments distincte chaque fois qu’un thread ou une application appelle [**IWiaDevMgr :: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) ou [**IWiaDevMgr2 :: CreateDevice**](-wia-iwiadevmgr2-createdevice.md) pour créer une instance de cet appareil. WIA gère des informations d’État distinctes pour chaque arborescence d’éléments. Par exemple, si un thread crée deux instances d’un scanneur particulier, il peut définir différentes résolutions d’analyse pour les deux instances. Quand [**IWiaDataTransfer :: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) est appelé sur une instance particulière, WIA charge les propriétés associées à cette instance sur l’appareil avant que l’analyse proprement dite ait lieu. Cela n’affecte pas l’état de l’autre instance de l’appareil.

Si un thread a actuellement un appareil verrouillé (il communique activement avec cet appareil) et qu’un autre thread tente d’appeler une méthode qui communique activement avec l’appareil, la méthode retourne une erreur d’erreur d’erreur de l’WIA \_ \_ .

En général, la lecture et l’écriture des propriétés de l’appareil prend beaucoup de temps, car ces opérations provoquent rarement un conflit. Toutefois, le transfert de données prend généralement plus de temps, et par conséquent, il est plus probable de créer des conflits d’accès à l’appareil. Il s’agit d’une programmation qui évite de longues opérations de périphérique (transferts de données) simultanément dans des threads distincts au sein d’une application.

Une application ne doit jamais supposer qu’il s’agit de la seule application qui communique avec un appareil WIA au démarrage.

 

 



