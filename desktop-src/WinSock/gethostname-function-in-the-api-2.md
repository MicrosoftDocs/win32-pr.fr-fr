---
description: La fonction GetHostName utilise la fonction WSALookupServiceBegin pour interroger le \_ nom d’hôte SVCID en tant que GUID de classe de service.
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: GetHostName fonction dans l’API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8629083c49e3915dd0ec4f1cfeb9363caabf8b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515026"
---
# <a name="gethostname-function-in-the-api"></a><span data-ttu-id="d56fa-103">GetHostName fonction dans l’API</span><span class="sxs-lookup"><span data-stu-id="d56fa-103">gethostname Function in the API</span></span>

<span data-ttu-id="d56fa-104">La fonction [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) utilise la fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) pour interroger le nom d' \_ hôte SVCID en tant que GUID de classe de service.</span><span class="sxs-lookup"><span data-stu-id="d56fa-104">The [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_HOSTNAME as the service class GUID.</span></span> <span data-ttu-id="d56fa-105">Si le membre **lpszServiceInstanceName** de la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passé à la fonction **WSALookupServiceBegin** a la **valeur null** ou fait référence à une chaîne **null** (autrement dit,.</span><span class="sxs-lookup"><span data-stu-id="d56fa-105">If the **lpszServiceInstanceName** member of the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function is **NULL** or references a **NULL** string (that is .</span></span> <span data-ttu-id="d56fa-106">«»), l’hôte local doit être résolu.</span><span class="sxs-lookup"><span data-stu-id="d56fa-106">""), the local host is to be resolved.</span></span> <span data-ttu-id="d56fa-107">Dans le cas contraire, une recherche sur un nom d’hôte spécifié se produit.</span><span class="sxs-lookup"><span data-stu-id="d56fa-107">Otherwise, a lookup on a specified host name occurs.</span></span> <span data-ttu-id="d56fa-108">Dans le cadre de l’émulation de **GetHostName** \_ , le32.dll Ws2 spécifie un pointeur **null** pour le membre **lpszServiceInstanceName** , et spécifie lup \_ nom de retour \_ afin que le nom d’hôte soit retourné dans le membre **lpszServiceInstanceName** .</span><span class="sxs-lookup"><span data-stu-id="d56fa-108">For the purposes of emulating **gethostname** the Ws2\_32.dll specifies a **NULL** pointer for the **lpszServiceInstanceName** member, and specifies LUP\_RETURN\_NAME so that the host name is returned in the **lpszServiceInstanceName** member.</span></span> <span data-ttu-id="d56fa-109">Si une application utilise cette requête et spécifie LUP \_ retour \_ addr, l’adresse de l’hôte est fournie dans une structure [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="d56fa-109">If an application uses this query and specifies LUP\_RETURN\_ADDR then the host address is provided in a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span> <span data-ttu-id="d56fa-110">L' \_ \_ action de retour d’objet BLOB lup n’est pas définie pour cette requête.</span><span class="sxs-lookup"><span data-stu-id="d56fa-110">The LUP\_RETURN\_BLOB action is undefined for this query.</span></span> <span data-ttu-id="d56fa-111">Les informations de port sont par défaut égales à zéro, sauf si le membre **lpszQueryString** de la structure **WSAQUERYSET** transmis à la fonction **WSALookupServiceBegin** fait référence à un service tel que FTP. dans ce cas, l’adresse de transport complète du service indiqué est fournie.</span><span class="sxs-lookup"><span data-stu-id="d56fa-111">Port information is defaulted to zero unless the **lpszQueryString** member of the **WSAQUERYSET** structure passed to the **WSALookupServiceBegin** function references a service such as FTP, in which case the complete transport address of the indicated service is supplied.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d56fa-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d56fa-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d56fa-113">Résolution de noms compatible pour TCP/IP dans l’API Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="d56fa-113">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="d56fa-114">Résolution de noms indépendante du protocole</span><span class="sxs-lookup"><span data-stu-id="d56fa-114">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="d56fa-115">Inscription et résolution de noms</span><span class="sxs-lookup"><span data-stu-id="d56fa-115">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
