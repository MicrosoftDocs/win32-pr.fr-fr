---
description: La requête WSALookupServiceBegin utilise \_ le nom d’hôte SVCID en tant que GUID de classe de service.
ms.assetid: 6f073e1a-2985-4e94-8174-94b1fcaf13d1
title: GetHostName fonction dans l’index SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9aef10be48b264eb607184caf38bd687a5fe307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516245"
---
# <a name="gethostname-function-in-the-spi"></a>GetHostName fonction dans l’index SPI

La requête [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) utilise \_ le nom d’hôte SVCID en tant que GUID de classe de service. Si *lpszServiceInstanceName* a la valeur null ou fait référence à une chaîne null (autrement dit,. «»), l’hôte local doit être résolu. Dans le cas contraire, une recherche sur un nom d’hôte spécifié doit se produire. Dans le cadre de l’émulation de [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) \_ , le32.dll Ws2 spécifie un pointeur null pour *lpszServiceInstanceName* et spécifie le nom de \_ retour lup \_ afin que le nom d’hôte soit retourné dans le paramètre *lpszServiceInstanceName* . Si une application utilise cette requête et spécifie LUP \_ retour \_ addr, l’adresse de l’hôte sera fournie dans une structure **CSADDR \_ info** . L' \_ \_ action de retour d’objet BLOB lup n’est pas définie pour cette requête. Les informations de port sont par défaut égales à zéro, sauf si le *lpszQueryString* fait référence à un service tel que FTP. dans ce cas, l’adresse de transport complète du service indiqué est fournie.

 

 



