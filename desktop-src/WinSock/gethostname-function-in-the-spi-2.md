---
description: La requête WSALookupServiceBegin utilise \_ le nom d’hôte SVCID en tant que GUID de classe de service.
ms.assetid: 6f073e1a-2985-4e94-8174-94b1fcaf13d1
title: GetHostName fonction dans l’index SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b610016222ab8a06ed874377be9ae447ad1d194ab9605a6e07b3cf829f520093
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132262"
---
# <a name="gethostname-function-in-the-spi"></a>GetHostName fonction dans l’index SPI

La requête [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) utilise \_ le nom d’hôte SVCID en tant que GUID de classe de service. Si *lpszServiceInstanceName* a la valeur null ou fait référence à une chaîne null (autrement dit,. «»), l’hôte local doit être résolu. Dans le cas contraire, une recherche sur un nom d’hôte spécifié doit se produire. Dans le cadre de l’émulation de [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) \_ , le32.dll Ws2 spécifie un pointeur null pour *lpszServiceInstanceName* et spécifie le nom de \_ retour lup \_ afin que le nom d’hôte soit retourné dans le paramètre *lpszServiceInstanceName* . Si une application utilise cette requête et spécifie LUP \_ retour \_ addr, l’adresse de l’hôte sera fournie dans une structure **CSADDR \_ info** . L' \_ \_ action de retour d’objet BLOB lup n’est pas définie pour cette requête. Les informations de port sont par défaut égales à zéro, sauf si le *lpszQueryString* fait référence à un service tel que FTP. dans ce cas, l’adresse de transport complète du service indiqué est fournie.

 

 



