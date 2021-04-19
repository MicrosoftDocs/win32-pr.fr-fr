---
description: Windows Sockets 2 est un ensemble de fonctions qui standardise la façon dont les applications accèdent et utilisent les différents services d’attribution de noms de réseau.
ms.assetid: e245475c-26cc-491f-b335-b1b6a816dc3c
title: Inscription et résolution de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8abc778c09fa2c0cc8de00db0edaa846ed2ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524978"
---
# <a name="registration-and-name-resolution"></a><span data-ttu-id="11a52-103">Inscription et résolution de noms</span><span class="sxs-lookup"><span data-stu-id="11a52-103">Registration and Name Resolution</span></span>

<span data-ttu-id="11a52-104">Windows Sockets 2 est un ensemble de fonctions qui standardise la façon dont les applications accèdent et utilisent les différents services d’attribution de noms de réseau.</span><span class="sxs-lookup"><span data-stu-id="11a52-104">Windows Sockets 2 is a set of functions that standardizes the way applications access and use the various network naming services.</span></span> <span data-ttu-id="11a52-105">Lors de l’utilisation de ces fonctions, les applications n’ont pas besoin de distinguer les protocoles les plus différents associés aux services de noms tels que DNS, NIS, X. 500, SAP, etc. Pour assurer la compatibilité descendante complète avec Windows Sockets 1,1, les fonctions de recherche de base de données **getXbyY** et **WSAAsyncGetXbyY** asynchrone existantes continuent d’être prises en charge, mais elles sont implémentées dans l’interface du fournisseur de services Windows Sockets en termes de nouvelles capacités de résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="11a52-105">When using these functions, applications need not distinguish the widely differing protocols associated with name services such as DNS, NIS, X.500, SAP, etc. To maintain full backward compatibility with Windows Sockets 1.1, the existing **getXbyY** and asynchronous **WSAAsyncGetXbyY** database-lookup functions continue to be supported, but are implemented in the Windows Sockets service provider interface in terms of the new name resolution capabilities.</span></span> <span data-ttu-id="11a52-106">Pour plus d’informations, consultez les fonctions [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) et [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) .</span><span class="sxs-lookup"><span data-stu-id="11a52-106">For more information, see the [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) and [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) functions.</span></span> <span data-ttu-id="11a52-107">Consultez également [la résolution de noms compatible pour TCP/IP dans le SPI Windows sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).</span><span class="sxs-lookup"><span data-stu-id="11a52-107">Also, see [Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).</span></span>

<span data-ttu-id="11a52-108">Cette section décrit les fonctionnalités d’inscription et de résolution de noms disponibles pour les développeurs Winsock.</span><span class="sxs-lookup"><span data-stu-id="11a52-108">This section describes registration and name resolution capabilities available to Winsock developers.</span></span> <span data-ttu-id="11a52-109">La liste suivante décrit les rubriques de cette section :</span><span class="sxs-lookup"><span data-stu-id="11a52-109">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="11a52-110">Résolution de noms indépendante du protocole</span><span class="sxs-lookup"><span data-stu-id="11a52-110">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
-   [<span data-ttu-id="11a52-111">Résolution de noms compatible pour TCP/IP dans l’API Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="11a52-111">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)

## <a name="related-topics"></a><span data-ttu-id="11a52-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="11a52-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11a52-113">À propos de Winsock</span><span class="sxs-lookup"><span data-stu-id="11a52-113">About Winsock</span></span>](about-winsock.md)
</dt> <dt>

[<span data-ttu-id="11a52-114">Utilisation de Winsock</span><span class="sxs-lookup"><span data-stu-id="11a52-114">Using Winsock</span></span>](using-winsock.md)
</dt> </dl>

 

 



