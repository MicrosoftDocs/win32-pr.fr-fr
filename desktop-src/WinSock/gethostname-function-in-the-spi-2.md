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
# <a name="gethostname-function-in-the-spi"></a><span data-ttu-id="5501c-103">GetHostName fonction dans l’index SPI</span><span class="sxs-lookup"><span data-stu-id="5501c-103">gethostname Function in the SPI</span></span>

<span data-ttu-id="5501c-104">La requête [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) utilise \_ le nom d’hôte SVCID en tant que GUID de classe de service.</span><span class="sxs-lookup"><span data-stu-id="5501c-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_HOSTNAME as the service class GUID.</span></span> <span data-ttu-id="5501c-105">Si *lpszServiceInstanceName* a la valeur null ou fait référence à une chaîne null (autrement dit,.</span><span class="sxs-lookup"><span data-stu-id="5501c-105">If *lpszServiceInstanceName* is null or references a null string (that is .</span></span> <span data-ttu-id="5501c-106">«»), l’hôte local doit être résolu.</span><span class="sxs-lookup"><span data-stu-id="5501c-106">""), the local host is to be resolved.</span></span> <span data-ttu-id="5501c-107">Dans le cas contraire, une recherche sur un nom d’hôte spécifié doit se produire.</span><span class="sxs-lookup"><span data-stu-id="5501c-107">Otherwise, a lookup on a specified host name shall occur.</span></span> <span data-ttu-id="5501c-108">Dans le cadre de l’émulation de [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) \_ , le32.dll Ws2 spécifie un pointeur null pour *lpszServiceInstanceName* et spécifie le nom de \_ retour lup \_ afin que le nom d’hôte soit retourné dans le paramètre *lpszServiceInstanceName* .</span><span class="sxs-lookup"><span data-stu-id="5501c-108">For the purposes of emulating [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) the Ws2\_32.dll will specify a null pointer for *lpszServiceInstanceName*, and specify LUP\_RETURN\_NAME so that the host name is returned in the *lpszServiceInstanceName* parameter.</span></span> <span data-ttu-id="5501c-109">Si une application utilise cette requête et spécifie LUP \_ retour \_ addr, l’adresse de l’hôte sera fournie dans une structure **CSADDR \_ info** .</span><span class="sxs-lookup"><span data-stu-id="5501c-109">If an application uses this query and specifies LUP\_RETURN\_ADDR then the host address will be provided in a **CSADDR\_INFO** structure.</span></span> <span data-ttu-id="5501c-110">L' \_ \_ action de retour d’objet BLOB lup n’est pas définie pour cette requête.</span><span class="sxs-lookup"><span data-stu-id="5501c-110">The LUP\_RETURN\_BLOB action is undefined for this query.</span></span> <span data-ttu-id="5501c-111">Les informations de port sont par défaut égales à zéro, sauf si le *lpszQueryString* fait référence à un service tel que FTP. dans ce cas, l’adresse de transport complète du service indiqué est fournie.</span><span class="sxs-lookup"><span data-stu-id="5501c-111">Port information will be defaulted to zero unless the *lpszQueryString* references a service such as ftp, in which case the complete transport address of the indicated service will be supplied.</span></span>

 

 



