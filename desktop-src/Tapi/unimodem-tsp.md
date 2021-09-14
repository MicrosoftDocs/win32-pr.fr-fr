---
description: Le pilote de modem Unimodem ou universel, TSP (unimdm. tsp) permet d’accéder à presque tous les modems standard.
ms.assetid: 1ea60477-f6c9-44ae-969c-515dfb0c607e
title: TSP Unimodem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115cc4fd159b2e62062171131f583bad19dc9b00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118802"
---
# <a name="unimodem-tsp"></a>TSP Unimodem

Le pilote de modem Unimodem ou universel, TSP (unimdm. tsp) permet d’accéder à presque tous les modems standard. Il prend en charge les modems vocaux qui autorisent la diffusion en continu semi-duplex. Ils sont pris en charge par le MSP Wave et le contrôle de flux est possible. (Notez que Unimodem sur Windows NT 4,0 ou version antérieure ne prend pas en charge les modems vocaux, si bien que le contrôle direct stream n’est pas possible.)

Ce TSP prend en charge une valeur de [**type d’adresse**](./lineaddresstype--constants.md) LINEADDRESSTYPE \_ PHONENUMBER. Si le programmeur souhaite utiliser les règles de numérotation, l’interface TAPI 3 [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) ou la fonction [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) TAPI 2 doit être utilisée pour obtenir une chaîne de numérotation à partir d’un numéro de téléphone au format canonique.

le TSP unimodem est installé avec les systèmes d’exploitation Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98 et Windows 95.

 

 
