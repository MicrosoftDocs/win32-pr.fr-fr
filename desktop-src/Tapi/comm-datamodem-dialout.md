---
description: comm/datamodem/dialout
ms.assetid: b1cc19d2-4a9f-4d3f-a868-d5928654ad75
title: comm/datamodem/dialout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 553e998acdfe77509d62050b825dae6ea88d3b3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952483"
---
# <a name="commdatamodemdialout"></a>comm/datamodem/dialout

La classe d’appareil **comm/datamodem/dialout** se compose d’appareils datamodem utilisés uniquement pour les appels sortants. Cette classe remplace la classe [**comm/datamodem**](comm-datamodem.md) sur les systèmes d’exploitation Windows 2000 et versions ultérieures.

Avant Windows 2000, le TSP Unimodem ne prenait en charge que la classe de l’appareil [**comm/datamodem**](comm-datamodem.md) . Un comportement inattendu peut se produire lorsqu’une application qui compose un appel sortant modifie le jeu de configuration par un service en attente d’un appel entrant. Les applications utilisant Windows 2000 et les systèmes d’exploitation ultérieurs doivent spécifier [**comm/datamodem/Dial**](comm-datamodem-dialin.md) , ou **comm/datamodem/dialout** dans les appels à [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) ou [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig). Cela permet à Unimodem de conserver une configuration d’accès à distance indépendante de la configuration de la numérotation à distance.

Alors que **comm/datamodem/dialout** est utilisé par Unimodem sur Windows 2000 et versions ultérieures, il peut également être utilisé par d’autres tsps sur n’importe quelle plateforme. Les applications qui doivent s’exécuter sur toutes les plateformes doivent d’abord utiliser **comm/datamodem/dialout** dans les appels à l’API qui requièrent une classe de périphérique et utiliser uniquement [**comm/DATAMODEM**](comm-datamodem.md) si l’API retourne **LINEERR \_ INVALCALLSTATE**.

Le fournisseur de services Unimodem traduit la classe de l’appareil [**comm/datamodem**](comm-datamodem.md) dans les appels à [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) et [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) en [**comm/datamodem/Dialy**](comm-datamodem-dialin.md) ou **comm/datamodem/dialout** comme suit :

-   Windows 2000 et versions ultérieures :
    -   Si la **valeur null** est spécifiée dans le paramètre *lpszDeviceClass* de l’appel à [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), Unimodem suppose [**comm/datamodem/Dial**](comm-datamodem-dialin.md). Si [**comm/datamodem**](comm-datamodem.md) ou [**TAPI/Line**](tapi-line.md) est spécifié dans l’appel à **lineConfigDialog**, Unimodem convertit ce en **comm/datamodem/dialout**.
    -   Dans l’appel à [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) ou [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig), [**comm/datamodem**](comm-datamodem.md) est géré comme **comm/datamodem/dialout**. La **valeur null** indique une classe d’appareil non valide.
-   Avant Windows 2000 :
    -   Si **null** ou [**TAPI/Line**](tapi-line.md) est spécifié dans [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), Unimodem suppose [**comm/datamodem**](comm-datamodem.md).

La classe **comm/datamodem/dialout** utilise les structures et les configurations décrites dans la classe de l’appareil [**comm/datamodem**](comm-datamodem.md) .

 

 



