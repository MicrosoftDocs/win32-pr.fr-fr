---
title: Sécurité d’activation
description: Sécurité d’activation
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5b01b918666e911d96ed16528ba5045103f445
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463790"
---
# <a name="activation-security"></a><span data-ttu-id="c692c-103">Sécurité d’activation</span><span class="sxs-lookup"><span data-stu-id="c692c-103">Activation Security</span></span>

<span data-ttu-id="c692c-104">La sécurité d’activation (également appelée « lancement de la sécurité ») permet de contrôler qui peut lancer un serveur.</span><span class="sxs-lookup"><span data-stu-id="c692c-104">Activation security (also called launch security) helps control who can launch a server.</span></span> <span data-ttu-id="c692c-105">La sécurité d’activation est automatiquement appliquée par le gestionnaire de contrôle des services (SCM) d’un ordinateur particulier.</span><span class="sxs-lookup"><span data-stu-id="c692c-105">Activation security is automatically applied by the service control manager (SCM) of a particular computer.</span></span> <span data-ttu-id="c692c-106">À la réception d’une demande d’activation d’un objet par un client (comme décrit dans [fonctions d’assistance de création d’instance](instance-creation-helper-functions.md)), le SCM vérifie la demande par rapport aux informations de sécurité d’activation stockées dans son registre.</span><span class="sxs-lookup"><span data-stu-id="c692c-106">Upon receipt of a request from a client to activate an object (as described in [Instance Creation Helper Functions](instance-creation-helper-functions.md)), the SCM checks the request against activation-security information stored within its registry.</span></span> <span data-ttu-id="c692c-107">(La sécurité d’activation est également vérifiée pour les activations du même ordinateur.)</span><span class="sxs-lookup"><span data-stu-id="c692c-107">(Activation security is also checked for same-computer activations.)</span></span>

<span data-ttu-id="c692c-108">Lors de la détermination de l’identité du client, l’activation examine l’indicateur de masquage défini dans l’appel du client à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="c692c-108">When determining the identity of the client, activation examines the cloaking flag set in the client's call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="c692c-109">Si l’indicateur de masquage est défini (pour le masquage dynamique ou statique), le jeton de thread est utilisé, le cas échéant, pour déterminer l’identité du client.</span><span class="sxs-lookup"><span data-stu-id="c692c-109">If the cloaking flag is set (for either dynamic or static cloaking), the thread token is used, if present, to determine the identity of the client.</span></span> <span data-ttu-id="c692c-110">Si aucun voilage n’est défini, le jeton de processus est utilisé à la place du jeton de thread.</span><span class="sxs-lookup"><span data-stu-id="c692c-110">If no cloaking is set, the process token is used instead of the thread token.</span></span>

<span data-ttu-id="c692c-111">Pour plus d’informations sur la sécurité de l’activation, consultez [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) et [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).</span><span class="sxs-lookup"><span data-stu-id="c692c-111">For more information about activation security, see [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) and [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c692c-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c692c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c692c-113">Sécurité dans COM</span><span class="sxs-lookup"><span data-stu-id="c692c-113">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 