---
description: La plupart des fonctions getXbyY sont traduites par le32.dll Ws2 en \_ une séquence WSALookupServiceBegin, WSALookupServiceNext et WSALookupServiceEnd qui utilise l’un des ensembles de GUID spéciaux comme classe de service.
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: Approche de base pour GetXbyY dans l’API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9e6dd0e5569bd11de813e28eaec1ee04f6b5f206277f695cdb9aaab05ec4a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322623"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a>Approche de base pour GetXbyY dans l’API

La plupart des fonctions **getXbyY** sont traduites par le32.dll Ws2 en \_ une séquence [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)et [**WSALOOKUPSERVICEEND**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) qui utilise l’un des ensembles de GUID spéciaux comme classe de service. Ces GUID identifient le type de l’opération **getXbyY** qui est émulée. La requête est restreinte aux fournisseurs de services de noms qui prennent en charge AF \_ inet. Chaque fois qu’une fonction **getXbyY** retourne une structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) ou [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) , l' \_32.dll Ws2 SPÉCIFIe l' \_ \_ indicateur d’objet BLOB lup return dans **WSALookupServiceBegin** afin que les informations souhaitées soient retournées par le fournisseur de services de noms. Ces structures doivent être légèrement modifiées en ce sens que les pointeurs contenus dans doivent être remplacés par des décalages relatifs au début des données de l’objet BLOB. Toutes les valeurs référencées par ces paramètres de pointeur doivent, bien sûr, être entièrement contenues dans l’objet BLOB, et toutes les chaînes sont au format ASCII.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[résolution de noms Compatible pour TCP/IP dans l’API Windows sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Résolution de noms indépendante du protocole](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Inscription et résolution de noms](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



