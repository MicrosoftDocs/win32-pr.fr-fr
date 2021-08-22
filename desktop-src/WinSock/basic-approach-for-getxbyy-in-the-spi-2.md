---
description: La plupart des fonctions GetXbyY sont traduites par Ws2 \_32.dll à une séquence WSALookupServiceBegin, WSALookupServiceNext, WSALookupServiceEnd qui utilise l’un des ensembles de GUID spéciaux comme classe de service.
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: Approche de base pour GetXbyY dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba707747dd6082bfa6c8b3c4dd3c19e8d6ce968359745947227ee464d97f984f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560523"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a>Approche de base pour GetXbyY dans le SPI

La plupart des fonctions **GetXbyY** sont traduites par Ws2 \_32.dll à une séquence [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALOOKUPSERVICEEND**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) qui utilise l’un des ensembles de GUID spéciaux comme classe de service. Ces GUID identifient le type de l’opération **GetXbyY** qui est émulée. La requête est restreinte aux NSP qui prennent en charge les \_ inet AF. Chaque fois qu’une fonction **GetXbyY** retourne une structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) ou [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) , l' \_32.dll Ws2 SPÉCIFIe \_ l' \_ indicateur d’objet BLOB lup return dans **WSALookupServiceBegin** afin que les informations souhaitées soient retournées par la NSP. Ces structures doivent être légèrement modifiées en ce sens que les pointeurs contenus dans doivent être remplacés par des décalages relatifs au début des données de l’objet BLOB. Toutes les valeurs référencées par ces membres de pointeur doivent, bien sûr, être entièrement contenues dans l’objet BLOB, et toutes les chaînes sont au format ASCII.

 

 



