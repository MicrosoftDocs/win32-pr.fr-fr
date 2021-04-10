---
title: Description de la sécurité
description: Une description de la sécurité est représentée par une \_ \_ structure de description de la sécurité WS et une instance d’une description de sécurité est fournie quand vous appelez la fonction WsCreateChannel pour créer un canal sécurisé ou la fonction WsCreateListener pour créer un écouteur.
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- Services Web de la description de la sécurité pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c06e8553441b7eb813106213dbfa089810aad74c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104116018"
---
# <a name="security-description"></a><span data-ttu-id="35d8c-106">Description de la sécurité</span><span class="sxs-lookup"><span data-stu-id="35d8c-106">Security Description</span></span>

<span data-ttu-id="35d8c-107">Une description de la sécurité est représentée par une structure de [**\_ \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) de la sécurité WS et une instance d’une description de sécurité est fournie quand vous appelez la fonction [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) pour créer un canal sécurisé ou la fonction [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) pour créer un écouteur.</span><span class="sxs-lookup"><span data-stu-id="35d8c-107">A security desciption is represented by a [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure, and an instance of a security description is supplied when you call the [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) function to create a secure channel or the [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) function to create a listener.</span></span>


## <a name="structure-of-a-security-description"></a><span data-ttu-id="35d8c-108">Structure d’une description de sécurité</span><span class="sxs-lookup"><span data-stu-id="35d8c-108">Structure of a Security Description</span></span>

<span data-ttu-id="35d8c-109">Le modèle de base de sécurité de canal est qu’un canal est sécurisé avec un ou plusieurs jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="35d8c-109">The basic model of channel security is that a channel is secured with one or more security tokens.</span></span> <span data-ttu-id="35d8c-110">Reflétant ce modèle, la structure de [**\_ \_ Description de la sécurité WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) contient une liste de liaisons de sécurité, représentées par les structures de [**\_ \_ liaison WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) , et chaque liaison de sécurité décrit comment un jeton de sécurité est obtenu et utilisé sur le canal.</span><span class="sxs-lookup"><span data-stu-id="35d8c-110">Reflecting this model, the [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure contains a list of security bindings, represented by [**WS\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) structures, and each security binding describes how one security token is obtained and used on the channel.</span></span> <span data-ttu-id="35d8c-111">Le type de sécurité utilisé sur un canal est déterminé par la sélection des sous-types de liaison de sécurité inclus dans la description de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="35d8c-111">The kind of security used on a channel is decided by the selection of security binding subtypes that are included in the security description.</span></span>

<span data-ttu-id="35d8c-112">Les paramètres de sécurité facultatifs spécifiques à une liaison de sécurité sont spécifiés en tant que [paramètres de liaison](security-binding-settings.md) de sécurité dans la structure de liaison de sécurité. Toutefois, les paramètres au niveau du canal indépendamment des liaisons de sécurité sont directement spécifiés en tant que [paramètres de canal de sécurité](security-channel-settings.md) dans le champ des **Propriétés** de la description de sécurité proprement dite.</span><span class="sxs-lookup"><span data-stu-id="35d8c-112">Optional security settings that are specific to a security binding are specified as [security binding settings](security-binding-settings.md) in the security binding structure; however, channel-wide settings independent of security bindings are directly specified as [security channel settings](security-channel-settings.md) in the **properties** field of the security description itself.</span></span>

![Diagramme montrant la structure d’une description de sécurité.](images/securitydescription.png)

<span data-ttu-id="35d8c-114">Les éléments d’API suivants sont utilisés avec les descriptions de sécurité.</span><span class="sxs-lookup"><span data-stu-id="35d8c-114">The following API elements are used with security descriptions.</span></span>

| <span data-ttu-id="35d8c-115">Structure</span><span class="sxs-lookup"><span data-stu-id="35d8c-115">Structure</span></span>                                                    | <span data-ttu-id="35d8c-116">Description</span><span class="sxs-lookup"><span data-stu-id="35d8c-116">Description</span></span>                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35d8c-117">**Description de la sécurité de WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="35d8c-117">**WS\_SECURITY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | <span data-ttu-id="35d8c-118">Structure de niveau supérieur utilisée pour spécifier les exigences de sécurité pour un canal (côté client) ou un écouteur (côté serveur).</span><span class="sxs-lookup"><span data-stu-id="35d8c-118">The top-level structure used to specify the security requirements for a channel (on the client side) or a listener (on the server side).</span></span> |



 

 

 




