---
description: Le schéma de rapport d’erreurs diffère entre les interfaces SPI et API.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Rapport d’erreurs et validation des paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291fa2ed950d916be39b1a696f5fe8ad6f07280c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519300"
---
# <a name="error-reporting-and-parameter-validation"></a><span data-ttu-id="c4048-103">Rapport d’erreurs et validation des paramètres</span><span class="sxs-lookup"><span data-stu-id="c4048-103">Error Reporting and Parameter Validation</span></span>

<span data-ttu-id="c4048-104">Le schéma de rapport d’erreurs diffère entre les interfaces SPI et API.</span><span class="sxs-lookup"><span data-stu-id="c4048-104">The scheme for error reporting differs between the SPI and API interfaces.</span></span> <span data-ttu-id="c4048-105">Les fournisseurs de services Windows Sockets signalent des erreurs, ainsi que la fonction qui retourne, par opposition à l’approche basée sur les threads utilisée dans l’API.</span><span class="sxs-lookup"><span data-stu-id="c4048-105">Windows Sockets service providers report errors along with the function returning, as opposed to the per-thread based approach utilized in the API.</span></span> <span data-ttu-id="c4048-106">Le \_32.dll Ws2 utilise le code d’erreur par fonction du fournisseur de services pour mettre à jour la valeur d’erreur par thread obtenue via la fonction de l’API [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) .</span><span class="sxs-lookup"><span data-stu-id="c4048-106">The Ws2\_32.dll uses the service provider's per-function error code to update the per-thread error value that is obtained through the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) API function.</span></span> <span data-ttu-id="c4048-107">Toutefois, les fournisseurs de services sont toujours requis pour maintenir l’erreur basée sur socket qui peut être récupérée à l’aide de l' \_ option de socket par erreur.</span><span class="sxs-lookup"><span data-stu-id="c4048-107">Service providers are still required, however, to maintain the per-socket based error which can be retrieved through the SO\_ERROR socket option.</span></span>

<span data-ttu-id="c4048-108">Le \_32.dll Ws2 effectue une validation de paramètre uniquement sur les appels de fonction qui sont entièrement implémentés dans lui-même.</span><span class="sxs-lookup"><span data-stu-id="c4048-108">The Ws2\_32.dll performs parameter validation only on function calls that are implemented entirely within itself.</span></span> <span data-ttu-id="c4048-109">Les fournisseurs de services sont responsables de l’exécution de toute leur propre validation de paramètre.</span><span class="sxs-lookup"><span data-stu-id="c4048-109">Service providers are responsible for performing all of their own parameter validation.</span></span>

 

 



