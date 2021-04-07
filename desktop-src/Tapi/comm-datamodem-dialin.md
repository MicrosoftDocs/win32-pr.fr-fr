---
description: comm/datamodem/Dialin
ms.assetid: 7330db08-5064-47c9-9d28-c5b2b15c3ac6
title: comm/datamodem/Dialin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb66d72b5d9f2c75af361153d46f5cac9abdfd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952484"
---
# <a name="commdatamodemdialin"></a>comm/datamodem/Dialin

La classe d’appareil **comm/datamodem/Dial** est composée d’appareils datamodem utilisés uniquement pour les appels entrants. Cette classe remplace la classe [**comm/datamodem**](comm-datamodem.md) sur les systèmes d’exploitation Windows 2000 et versions ultérieures.

Avant Windows 2000, le TSP Unimodem ne prenait en charge que la classe de l’appareil [**comm/datamodem**](comm-datamodem.md) . Un comportement inattendu peut se produire lorsqu’une application qui compose un appel sortant modifie le jeu de configuration par un service en attente d’un appel entrant. Les applications utilisant Windows 2000 et les systèmes d’exploitation ultérieurs doivent spécifier **comm/datamodem/Dial** , ou [**comm/datamodem/dialout**](comm-datamodem-dialout.md) dans les appels à [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) ou [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig). Cela permet à Unimodem de conserver une configuration d’accès à distance indépendante de la configuration de la numérotation à distance.

Alors que **comm/datamodem/Dial** est utilisé par Unimodem sur Windows 2000 et versions ultérieures, il peut également être utilisé par d’autres tsps sur n’importe quelle plateforme. Les applications qui doivent s’exécuter sur toutes les plateformes doivent d’abord utiliser **comm/datamodem/Dial** dans les appels aux API qui requièrent une classe de périphérique et utiliser uniquement [**comm/DATAMODEM**](comm-datamodem.md) si l’API retourne **LINEERR \_ INVALCALLSTATE**.

Le fournisseur de services Unimodem traduit la classe de l’appareil [**comm/datamodem**](comm-datamodem.md) dans les appels à [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) et [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) en **comm/datamodem/Dialy** ou [**comm/datamodem/dialout**](comm-datamodem-dialout.md) comme suit :

-   Windows 2000 et versions ultérieures :
    -   Si la **valeur null** est spécifiée dans le paramètre *lpszDeviceClass* de l’appel à [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), Unimodem suppose **comm/datamodem/Dial**. Si [**comm/datamodem**](comm-datamodem.md) ou [**TAPI/Line**](tapi-line.md) est spécifié dans l’appel à **lineConfigDialog**, Unimodem convertit ce en [**comm/datamodem/dialout**](comm-datamodem-dialout.md).
    -   Dans l’appel à [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) ou [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig), [**comm/datamodem**](comm-datamodem.md) est géré comme [**comm/datamodem/dialout**](comm-datamodem-dialout.md). La **valeur null** indique une classe d’appareil non valide.
-   Avant Windows 2000 :
    -   Si **null** ou [**TAPI/Line**](tapi-line.md) est spécifié dans [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), Unimodem suppose [**comm/datamodem**](comm-datamodem.md).

La classe **comm/datamodem/Dialin** utilise les structures et configurations décrites dans la classe de l’appareil [**comm/datamodem**](comm-datamodem.md) .

 

 



