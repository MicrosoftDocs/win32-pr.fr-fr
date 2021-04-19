---
title: Résultats du traitement de la sécurité
description: Sur un canal sécurisé, seuls les messages qui réussissent les vérifications de sécurité sont remis à l’application.
ms.assetid: 891e1f91-406e-4997-9da6-59b5fe578d0d
keywords:
- Résultats du traitement de la sécurité services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf6f8964d14c8cfdca3f6bd66b2f24e9fa611d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "106509070"
---
# <a name="security-processing-results"></a><span data-ttu-id="8a087-106">Résultats du traitement de la sécurité</span><span class="sxs-lookup"><span data-stu-id="8a087-106">Security Processing Results</span></span>

<span data-ttu-id="8a087-107">Sur un canal sécurisé, seuls les messages qui réussissent les vérifications de sécurité sont remis à l’application.</span><span class="sxs-lookup"><span data-stu-id="8a087-107">On a secure channel, only those messages that successfully pass security checks are delivered to the application.</span></span> <span data-ttu-id="8a087-108">Pour ces messages, certains résultats de la vérification de sécurité sont joints en tant que propriétés de message, et l’application peut extraire et examiner ces propriétés pour effectuer des étapes supplémentaires, telles que les vérifications d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="8a087-108">For these messages, some results from security verification are attached as message properties, and the application may extract and examine these properties to perform additional steps such as authorization checks.</span></span>


<span data-ttu-id="8a087-109">La fonction [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) peut être utilisée pour récupérer les propriétés liées à la sécurité définies dans [**ID de \_ \_ propriété de \_ message WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span><span class="sxs-lookup"><span data-stu-id="8a087-109">The function [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) can be used to retrieve any of the security-related properties defined in [**WS\_MESSAGE\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span></span> <span data-ttu-id="8a087-110">**WsGetMessageProperty** retourne une erreur pour les requêtes qui demandent des propriétés de sécurité non applicables au type de sécurité utilisé sur le canal.</span><span class="sxs-lookup"><span data-stu-id="8a087-110">**WsGetMessageProperty** returns an error for queries that ask for security properties not applicable to the type of security used on the channel.</span></span> <span data-ttu-id="8a087-111">Le message continue à posséder les propriétés retournées par la fonction de requête.</span><span class="sxs-lookup"><span data-stu-id="8a087-111">The message continues to own the properties returned by the query function.</span></span>

<span data-ttu-id="8a087-112">Les éléments d’API suivants sont utilisés avec les résultats du traitement de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8a087-112">The following API elements are used with security processing results.</span></span>

| <span data-ttu-id="8a087-113">Énumération</span><span class="sxs-lookup"><span data-stu-id="8a087-113">Enumeration</span></span>                                                                | <span data-ttu-id="8a087-114">Description</span><span class="sxs-lookup"><span data-stu-id="8a087-114">Description</span></span>                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a087-115">**\_ID de \_ propriété du jeton de sécurité WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8a087-115">**WS\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | <span data-ttu-id="8a087-116">Définit les clés pour les champs et les propriétés qui peuvent être extraits à partir d’un jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8a087-116">Defines the keys for the fields and properties that can be extracted from a security token.</span></span> |



 



| <span data-ttu-id="8a087-117">Fonction</span><span class="sxs-lookup"><span data-stu-id="8a087-117">Function</span></span>                                                         | <span data-ttu-id="8a087-118">Description</span><span class="sxs-lookup"><span data-stu-id="8a087-118">Description</span></span>                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="8a087-119">**WsGetSecurityTokenProperty**</span><span class="sxs-lookup"><span data-stu-id="8a087-119">**WsGetSecurityTokenProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | <span data-ttu-id="8a087-120">Extrait un champ ou une propriété d’un jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8a087-120">Extracts a field or a property from a security token.</span></span> |



 



| <span data-ttu-id="8a087-121">Handle</span><span class="sxs-lookup"><span data-stu-id="8a087-121">Handle</span></span>                                       | <span data-ttu-id="8a087-122">Description</span><span class="sxs-lookup"><span data-stu-id="8a087-122">Description</span></span>                                     |
|----------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="8a087-123">\_jeton de sécurité WS \_</span><span class="sxs-lookup"><span data-stu-id="8a087-123">WS\_SECURITY\_TOKEN</span></span>](ws-security-token.md) | <span data-ttu-id="8a087-124">Handle opaque représentant un jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8a087-124">An opaque handle representing a security token.</span></span> |



 

 

 




