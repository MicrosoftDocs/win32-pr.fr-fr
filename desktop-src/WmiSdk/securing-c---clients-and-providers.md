---
description: Les fournisseurs C++ et les applications clientes doivent effectuer la plupart des opérations pour maintenir la sécurité WMI.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Sécurisation des clients et des fournisseurs C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac93ee88f710bf17a2b6199b3a9b2e89279b4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519820"
---
# <a name="securing-c-clients-and-providers"></a><span data-ttu-id="d8fbc-103">Sécurisation des clients et des fournisseurs C++</span><span class="sxs-lookup"><span data-stu-id="d8fbc-103">Securing C++ Clients and Providers</span></span>

<span data-ttu-id="d8fbc-104">Les fournisseurs C++ et les applications clientes doivent effectuer la plupart des opérations pour maintenir la sécurité WMI.</span><span class="sxs-lookup"><span data-stu-id="d8fbc-104">Both C++ providers and client applications must perform many of the same operations to maintain WMI security.</span></span>

<span data-ttu-id="d8fbc-105">Les applications clientes doivent définir correctement l' [emprunt d’identité](setting-the-default-process-security-level-using-c-.md) DCOM et les niveaux [d’authentification](setting-authentication-in-wmi.md) lors de la connexion à WMI.</span><span class="sxs-lookup"><span data-stu-id="d8fbc-105">Client applications must set DCOM [impersonation](setting-the-default-process-security-level-using-c-.md) and [authentication](setting-authentication-in-wmi.md) levels correctly when connecting to WMI.</span></span> <span data-ttu-id="d8fbc-106">Les rappels des [appels asynchrones](setting-security-on-an-asynchronous-call.md) présentent des risques de sécurité, les applications clientes doivent donc [effectuer des vérifications d’accès](performing-access-checks.md) pour s’assurer que le rappel provient d’une source approuvée.</span><span class="sxs-lookup"><span data-stu-id="d8fbc-106">Callbacks from [asynchronous calls](setting-security-on-an-asynchronous-call.md) have security risks, so client applications must [perform access checks](performing-access-checks.md) to ensure the callback is from a trusted source.</span></span> <span data-ttu-id="d8fbc-107">Les clients doivent sécuriser les [consommateurs d’événements temporaires et permanents](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="d8fbc-107">Clients need to secure both [temporary and permanent event consumers](securing-wmi-events.md).</span></span>

<span data-ttu-id="d8fbc-108">Un fournisseur peut [effectuer des contrôles d’accès](performing-access-checks.md) pour s’assurer que les ressources qu’il crée sont accessibles uniquement par les clients appropriés.</span><span class="sxs-lookup"><span data-stu-id="d8fbc-108">A provider may [perform access checks](performing-access-checks.md) to ensure that the resources it creates are only accessed by appropriate clients.</span></span>

<span data-ttu-id="d8fbc-109">Les fournisseurs et les clients peuvent également définir la sécurité sur une connexion [proxy spécifique](setting-the-security-on-iwbemservices-and-other-proxies.md) .</span><span class="sxs-lookup"><span data-stu-id="d8fbc-109">Both providers and clients also can set the security on a [specific proxy](setting-the-security-on-iwbemservices-and-other-proxies.md) connection.</span></span> <span data-ttu-id="d8fbc-110">Les deux peuvent également activer [des privilèges](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="d8fbc-110">Both can also enable [privileges](executing-privileged-operations.md).</span></span> <span data-ttu-id="d8fbc-111">Un fournisseur d’événements doit s’assurer que le consommateur client dispose des privilèges nécessaires pour [recevoir un événement demandé](providing-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="d8fbc-111">An event provider must ensure that the client consumer has privileges to [receive a requested event](providing-events-securely.md).</span></span>

<span data-ttu-id="d8fbc-112">Un client ou un fournisseur peut avoir besoin d’établir une connexion à distance qui requiert un service d’authentification différent, NTLM au lieu de Kerberos par exemple.</span><span class="sxs-lookup"><span data-stu-id="d8fbc-112">Either a client or provider may need to make a remote connection that requires a different authentication service, NTLM instead of Kerberos for example.</span></span>

 

 



