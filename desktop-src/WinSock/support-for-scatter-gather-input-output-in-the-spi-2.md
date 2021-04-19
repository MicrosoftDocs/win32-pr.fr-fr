---
description: Les routines WSPSend, WSPSendTo, WSPRecv et WSPRecvFrom prennent toutes un tableau de mémoires tampon client comme paramètres d’entrée et peuvent donc être utilisées pour les e/s de ventilation/regroupement (ou vectorielle).
ms.assetid: ecd3d2f1-74b1-42f7-8402-3170112e3aca
title: Prise en charge des entrées/sorties de ventilation/regroupement dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3f32e016c5c2e9f990c334716d4177d477c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521510"
---
# <a name="support-for-scattergather-inputoutput-in-the-spi"></a>Prise en charge des entrées/sorties de ventilation/regroupement dans le SPI

Les routines [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)), [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)), [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))et [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) prennent toutes un tableau de mémoires tampon client comme paramètres d’entrée et peuvent donc être utilisées pour les e/s de ventilation/regroupement (ou vectorielle). Cela peut être très utile dans les instances où des parties de chaque message en cours de transmission se composent d’un ou de plusieurs composants d’en-tête de longueur fixe en plus du corps du message. Ces composants d’en-tête n’ont pas besoin d’être concaténés dans une seule mémoire tampon contiguë avant l’envoi. De même, à la réception, les composants d’en-tête peuvent être automatiquement divisés en mémoires tampons distinctes, ce qui laisse le corps du message pur.

L’utilisation de listes de mémoires tampons au lieu d’une seule mémoire tampon ne change pas les limites qui s’appliquent aux opérations de réception. Pour les protocoles orientés message, une opération de réception se termine chaque fois qu’un seul message a été reçu, quel que soit le nombre de tampons fournis et le nombre d’entre eux ayant été utilisé. De la même façon pour les protocoles orientés flux, une réception se termine lorsqu’une quantité non spécifiée d’octets arrive sur le réseau, pas nécessairement lorsque toutes les mémoires tampons fournies sont pleines.

 

 
