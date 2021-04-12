---
description: La plupart des fonctions getXbyY sont traduites par le32.dll Ws2 en \_ une séquence WSALookupServiceBegin, WSALookupServiceNext et WSALookupServiceEnd qui utilise l’un des ensembles de GUID spéciaux comme classe de service.
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: Approche de base pour GetXbyY dans l’API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4c038c87d6eb6e7ab2a4476271662d5b9567ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526206"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a><span data-ttu-id="3aff3-103">Approche de base pour GetXbyY dans l’API</span><span class="sxs-lookup"><span data-stu-id="3aff3-103">Basic Approach for GetXbyY in the API</span></span>

<span data-ttu-id="3aff3-104">La plupart des fonctions **getXbyY** sont traduites par le32.dll Ws2 en \_ une séquence [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)et [**WSALOOKUPSERVICEEND**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) qui utilise l’un des ensembles de GUID spéciaux comme classe de service.</span><span class="sxs-lookup"><span data-stu-id="3aff3-104">Most **getXbyY** functions are translated by the Ws2\_32.dll to a [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), and [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) sequence that uses one of a set of special GUIDs as the service class.</span></span> <span data-ttu-id="3aff3-105">Ces GUID identifient le type de l’opération **getXbyY** qui est émulée.</span><span class="sxs-lookup"><span data-stu-id="3aff3-105">These GUIDs identify the type of **getXbyY** operation that is being emulated.</span></span> <span data-ttu-id="3aff3-106">La requête est restreinte aux fournisseurs de services de noms qui prennent en charge AF \_ inet.</span><span class="sxs-lookup"><span data-stu-id="3aff3-106">The query is constrained to those name service providers that support AF\_INET.</span></span> <span data-ttu-id="3aff3-107">Chaque fois qu’une fonction **getXbyY** retourne une structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) ou [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) , l' \_32.dll Ws2 SPÉCIFIe l' \_ \_ indicateur d’objet BLOB lup return dans **WSALookupServiceBegin** afin que les informations souhaitées soient retournées par le fournisseur de services de noms.</span><span class="sxs-lookup"><span data-stu-id="3aff3-107">Whenever a **getXbyY** function returns a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) or [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure, the Ws2\_32.dll specifies the LUP\_RETURN\_BLOB flag in **WSALookupServiceBegin** so that the desired information is returned by the name service provider.</span></span> <span data-ttu-id="3aff3-108">Ces structures doivent être légèrement modifiées en ce sens que les pointeurs contenus dans doivent être remplacés par des décalages relatifs au début des données de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="3aff3-108">These structures must be modified slightly in that the pointers contained within must be replaced with offsets that are relative to the start of the blob's data.</span></span> <span data-ttu-id="3aff3-109">Toutes les valeurs référencées par ces paramètres de pointeur doivent, bien sûr, être entièrement contenues dans l’objet BLOB, et toutes les chaînes sont au format ASCII.</span><span class="sxs-lookup"><span data-stu-id="3aff3-109">All values referenced by these pointer parameters must, of course, be completely contained within the blob, and all strings are ASCII.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3aff3-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3aff3-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3aff3-111">Résolution de noms compatible pour TCP/IP dans l’API Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="3aff3-111">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="3aff3-112">Résolution de noms indépendante du protocole</span><span class="sxs-lookup"><span data-stu-id="3aff3-112">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="3aff3-113">Inscription et résolution de noms</span><span class="sxs-lookup"><span data-stu-id="3aff3-113">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



