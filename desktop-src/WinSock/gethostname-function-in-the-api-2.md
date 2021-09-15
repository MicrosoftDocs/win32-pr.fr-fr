---
description: La fonction GetHostName utilise la fonction WSALookupServiceBegin pour interroger le \_ nom d’hôte SVCID en tant que GUID de classe de service.
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: GetHostName fonction dans l’API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8629083c49e3915dd0ec4f1cfeb9363caabf8b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517696"
---
# <a name="gethostname-function-in-the-api"></a>GetHostName fonction dans l’API

La fonction [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) utilise la fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) pour interroger le nom d' \_ hôte SVCID en tant que GUID de classe de service. Si le membre **lpszServiceInstanceName** de la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passé à la fonction **WSALookupServiceBegin** a la **valeur null** ou fait référence à une chaîne **null** (autrement dit,. «»), l’hôte local doit être résolu. Dans le cas contraire, une recherche sur un nom d’hôte spécifié se produit. Dans le cadre de l’émulation de **GetHostName** \_ , le32.dll Ws2 spécifie un pointeur **null** pour le membre **lpszServiceInstanceName** , et spécifie lup \_ nom de retour \_ afin que le nom d’hôte soit retourné dans le membre **lpszServiceInstanceName** . Si une application utilise cette requête et spécifie LUP \_ retour \_ addr, l’adresse de l’hôte est fournie dans une structure [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . L' \_ \_ action de retour d’objet BLOB lup n’est pas définie pour cette requête. Les informations de port sont par défaut égales à zéro, sauf si le membre **lpszQueryString** de la structure **WSAQUERYSET** transmis à la fonction **WSALookupServiceBegin** fait référence à un service tel que FTP. dans ce cas, l’adresse de transport complète du service indiqué est fournie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[résolution de noms Compatible pour TCP/IP dans l’API Windows sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Résolution de noms indépendante du protocole](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Inscription et résolution de noms](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
