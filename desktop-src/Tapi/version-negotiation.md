---
description: Au fil du temps, différentes versions peuvent exister pour les applications TAPI, TAPI et les fournisseurs de services.
ms.assetid: 39b16328-931e-4d75-a6ec-1edc97f1a287
title: Négociation de version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beffff7ceeb90ccf419e138986562ca90f83c204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952782"
---
# <a name="version-negotiation"></a><span data-ttu-id="371cf-103">Négociation de version</span><span class="sxs-lookup"><span data-stu-id="371cf-103">Version Negotiation</span></span>

<span data-ttu-id="371cf-104">Au fil du temps, différentes versions peuvent exister pour les applications TAPI, TAPI et les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="371cf-104">Over time, different versions may exist for TAPI applications, TAPI, and the service providers.</span></span> <span data-ttu-id="371cf-105">L’interopérabilité optimale d’une application TAPI nécessite de connaître non seulement la version TAPI de l’application, mais également les versions de la DLL, TAPISVR et du fournisseur de services TAPI.</span><span class="sxs-lookup"><span data-stu-id="371cf-105">Optimal interoperability of a TAPI application requires knowledge of not just the application's TAPI version, but also of the TAPI DLL, TAPISVR, and service provider versions.</span></span>

<span data-ttu-id="371cf-106">L’échec de la négociation de version appropriée peut entraîner des problèmes sérieux.</span><span class="sxs-lookup"><span data-stu-id="371cf-106">Failure to do proper version negotiation can result in serious problems.</span></span> <span data-ttu-id="371cf-107">Par exemple, certaines structures fortement utilisées ont des membres de données ajoutés d’une version à la suivante.</span><span class="sxs-lookup"><span data-stu-id="371cf-107">For example, some heavily used structures have data members added from one version to the next.</span></span> <span data-ttu-id="371cf-108">Si la taille de la structure ne correspond pas à la valeur attendue par l’application ou l’interface TAPI, les conséquences sont comprises entre les fuites de mémoire et la synchronisation AVs intermittente.</span><span class="sxs-lookup"><span data-stu-id="371cf-108">If the structure size does not match what the application or TAPI expects, the consequences range from memory leaks to intermittent AVs.</span></span>

<span data-ttu-id="371cf-109">Pour plus d’informations, consultez contrôle de [version TAPI](./tapi-versioning.md).</span><span class="sxs-lookup"><span data-stu-id="371cf-109">For additional information, see [TAPI Versioning](./tapi-versioning.md).</span></span>

<span data-ttu-id="371cf-110">**TAPI 2. x :** Les applications négocient avec TAPI et TAPISVR pendant [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="371cf-110">**TAPI 2.x:** Applications negotiate with TAPI and TAPISVR during [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span></span> <span data-ttu-id="371cf-111">Les applications effectuent la négociation des appareils avec les fournisseurs de services en appelant [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) pour chaque ligne que l’application peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="371cf-111">Applications perform device negotiation with service providers by calling [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) for each line that the application might use.</span></span>

<span data-ttu-id="371cf-112">**TAPI 3. x :** Il n’est pas nécessaire d’effectuer une négociation de version ; Toutefois, vous pouvez utiliser [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour déterminer si une interface est disponible sur leur version.</span><span class="sxs-lookup"><span data-stu-id="371cf-112">**TAPI 3.x:** There is no need to perform version negotiation; however, you can use [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to determine if an interface is available on their version.</span></span>

 

 
