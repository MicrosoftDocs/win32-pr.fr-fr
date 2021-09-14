---
description: Certaines fonctions de communication peuvent être appelées pour un appareil à l’aide de la fonction EscapeCommFunction.
ms.assetid: 12b92d4b-04b5-4509-9fad-af23fcfd8857
title: Fonctions étendues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0e57c316b521cbc246e5f31dcfb683238e216e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114322"
---
# <a name="extended-functions"></a>Fonctions étendues

Certaines fonctions de communication peuvent être appelées pour un appareil à l’aide de la fonction [**EscapeCommFunction**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction) . Cette fonction envoie un code pour indiquer à l’appareil d’exécuter une fonction étendue. Par exemple, une application peut suspendre la transmission de caractères avec le code SETBREAK et reprendre la transmission avec le code CLRBREAK. Ces opérations particulières peuvent également être démarrées en appelant les fonctions [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) et [**ClearCommBreak**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak) . **EscapeCommFunction** peut également être utilisé pour implémenter le contrôle manuel du modem. Par exemple, les codes CLRDTR et SETDTR peuvent être utilisés pour implémenter le contrôle de Flow manuel DTR (Data-Terminal Ready). Notez, toutefois, qu’une erreur se produit si un processus utilise **EscapeCommFunction** pour manipuler la ligne DTR lorsque l’appareil a été configuré pour activer le protocole de liaison DTR, ou la ligne RTS (demande d’envoi) si le protocole RTS est activé.

La fonction [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) permet à un processus d’envoyer un code de fonction étendue directement à un pilote de périphérique spécifié, ce qui amène l’appareil à effectuer une opération donnée. **DeviceIoControl** fournit un appareil associé à des fonctionnalités de ressources de communication non prises en charge par les fonctions de communication série standard. Il permet à une application de configurer un appareil à l’aide de paramètres propres à cet appareil, ainsi que d’appeler toutes les fonctions spécifiques à l’appareil.

 

 
