---
description: Si une application ne souhaite aucune interférence par des événements extérieurs pour une session de la part de l’interface TAPI ou du fournisseur de services, elle doit sécuriser l’appel.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Sécuriser une session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b1567303efb61f28f9c6b3e92c24287d23d4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543000"
---
# <a name="secure-a-session"></a><span data-ttu-id="65193-103">Sécuriser une session</span><span class="sxs-lookup"><span data-stu-id="65193-103">Secure a Session</span></span>

<span data-ttu-id="65193-104">Si une application ne souhaite aucune interférence par des événements extérieurs pour une session de la part de l’interface TAPI ou du fournisseur de services, elle doit sécuriser l’appel.</span><span class="sxs-lookup"><span data-stu-id="65193-104">If an application does not want any interference by outside events for a session from TAPI or the service provider, it should secure the call.</span></span> <span data-ttu-id="65193-105">Par exemple, dans un environnement analogique, l’appel de tonalités peut détruire une télécopie ou une session de modem sur l’appel d’origine.</span><span class="sxs-lookup"><span data-stu-id="65193-105">For example, in an analog environment call-waiting tones can destroy a fax or modem session on the original call.</span></span>

<span data-ttu-id="65193-106">Une application peut sécuriser un appel au moment où l’appel est effectué ou après que l’appel existe déjà.</span><span class="sxs-lookup"><span data-stu-id="65193-106">An application can secure a call at the time the call is made or after the call already exists.</span></span>

<span data-ttu-id="65193-107">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.</span><span class="sxs-lookup"><span data-stu-id="65193-107">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="65193-108">**TAPI 2. x :** Consultez [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).</span><span class="sxs-lookup"><span data-stu-id="65193-108">**TAPI 2.x:** See [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).</span></span>

<span data-ttu-id="65193-109">**TAPI 3. x :** Consultez [**ITAddress :: Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).</span><span class="sxs-lookup"><span data-stu-id="65193-109">**TAPI 3.x:** See [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).</span></span>

 

 
