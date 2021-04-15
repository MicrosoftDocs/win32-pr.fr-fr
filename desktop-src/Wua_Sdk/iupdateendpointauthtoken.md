---
description: Fournit les méthodes que WUA peut utiliser pour collecter des informations sur le jeton de point de terminaison.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: Interface IUpdateEndpointAuthToken (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a5902b3c91b3ab12b311121bd7dcd8c415a68d6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485137"
---
# <a name="iupdateendpointauthtoken-interface"></a><span data-ttu-id="14b1a-103">Interface IUpdateEndpointAuthToken</span><span class="sxs-lookup"><span data-stu-id="14b1a-103">IUpdateEndpointAuthToken interface</span></span>

<span data-ttu-id="14b1a-104">Fournit les méthodes que WUA peut utiliser pour collecter des informations sur le jeton de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="14b1a-104">Provides the methods that WUA can use to gather information about the endpoint token.</span></span>

## <a name="members"></a><span data-ttu-id="14b1a-105">Membres</span><span class="sxs-lookup"><span data-stu-id="14b1a-105">Members</span></span>

<span data-ttu-id="14b1a-106">L’interface **IUpdateEndpointAuthToken** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="14b1a-106">The **IUpdateEndpointAuthToken** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="14b1a-107">**IUpdateEndpointAuthToken** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="14b1a-107">**IUpdateEndpointAuthToken** also has these types of members:</span></span>

-   [<span data-ttu-id="14b1a-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="14b1a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="14b1a-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="14b1a-109">Methods</span></span>

<span data-ttu-id="14b1a-110">L’interface **IUpdateEndpointAuthToken** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="14b1a-110">The **IUpdateEndpointAuthToken** interface has these methods.</span></span>



| <span data-ttu-id="14b1a-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="14b1a-111">Method</span></span>                                                                                | <span data-ttu-id="14b1a-112">Description</span><span class="sxs-lookup"><span data-stu-id="14b1a-112">Description</span></span>                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14b1a-113">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="14b1a-113">**ServiceID**</span></span>](iupdateendpointauthtoken-serviceid.md)                               | <span data-ttu-id="14b1a-114">Obtient l’identificateur du service à authentifier.</span><span class="sxs-lookup"><span data-stu-id="14b1a-114">Gets the identifier of the service to be authenticated.</span></span><br/>                                                          |
| [<span data-ttu-id="14b1a-115">**SigningKey**</span><span class="sxs-lookup"><span data-stu-id="14b1a-115">**SigningKey**</span></span>](iupdateendpointauthtoken-signingkey.md)                             | <span data-ttu-id="14b1a-116">Obtient la clé utilisée pour signer les messages sortants entre l’ordinateur client et le Sercvice.</span><span class="sxs-lookup"><span data-stu-id="14b1a-116">Gets the key used to sign outgoing messages between the client computer and the sercvice.</span></span><br/>                        |
| [<span data-ttu-id="14b1a-117">**TokenData**</span><span class="sxs-lookup"><span data-stu-id="14b1a-117">**TokenData**</span></span>](iupdateendpointauthtoken-tokendata.md)                               | <span data-ttu-id="14b1a-118">Obtient les données XML (envoyées sur le réseau) qui représentent le jeton.</span><span class="sxs-lookup"><span data-stu-id="14b1a-118">Gets the XML data (sent over the wire) that represents the token.</span></span> <br/>                                               |
| [<span data-ttu-id="14b1a-119">**TokenReferenceAttached**</span><span class="sxs-lookup"><span data-stu-id="14b1a-119">**TokenReferenceAttached**</span></span>](iupdateendpointauthtoken-tokenreferenceattached.md)     | <span data-ttu-id="14b1a-120">Obtient le format XML d’une référence jointe au jeton.</span><span class="sxs-lookup"><span data-stu-id="14b1a-120">Gets the XML format of an attached reference to the token.</span></span><br/>                                                       |
| [<span data-ttu-id="14b1a-121">**TokenReferenceUnattached**</span><span class="sxs-lookup"><span data-stu-id="14b1a-121">**TokenReferenceUnattached**</span></span>](iupdateendpointauthtoken-tokenreferenceunattached.md) | <span data-ttu-id="14b1a-122">Obtient le format XML d’une référence non attachée au jeton.</span><span class="sxs-lookup"><span data-stu-id="14b1a-122">Gets the XML format of an unattached reference to the token.</span></span><br/>                                                     |
| [<span data-ttu-id="14b1a-123">**TokenType**</span><span class="sxs-lookup"><span data-stu-id="14b1a-123">**TokenType**</span></span>](iupdateendpointauthtoken-tokentype.md)                               | <span data-ttu-id="14b1a-124">Obtient le type du jeton de point de terminaison, tel qu’un jeton WS-Security SAML (Security Assertion Markup Language) 1,1.</span><span class="sxs-lookup"><span data-stu-id="14b1a-124">Gets the type of the endpoint token, such as a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="14b1a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14b1a-125">Requirements</span></span>



| <span data-ttu-id="14b1a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14b1a-126">Requirement</span></span> | <span data-ttu-id="14b1a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="14b1a-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14b1a-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14b1a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="14b1a-129">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14b1a-129">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="14b1a-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14b1a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="14b1a-131">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14b1a-131">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="14b1a-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="14b1a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="14b1a-133"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="14b1a-133"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="14b1a-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="14b1a-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14b1a-135"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14b1a-135"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="14b1a-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14b1a-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="14b1a-137"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14b1a-137"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="14b1a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="14b1a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14b1a-139"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14b1a-139"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



 

 
