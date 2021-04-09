---
description: Les protocoles Schannel requièrent des informations d’identification pour authentifier les serveurs et, éventuellement, les clients.
ms.assetid: 8295b1bd-6ae1-4f7e-926d-a9da7ec6a524
title: Informations d’identification Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91556a7e3bfca67aa386f0264e78ae67052f02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951884"
---
# <a name="schannel-credentials"></a><span data-ttu-id="65c34-103">Informations d’identification Schannel</span><span class="sxs-lookup"><span data-stu-id="65c34-103">Schannel Credentials</span></span>

<span data-ttu-id="65c34-104">Les protocoles Schannel requièrent des informations d’identification pour authentifier les serveurs et, éventuellement, les clients.</span><span class="sxs-lookup"><span data-stu-id="65c34-104">Schannel protocols require credentials to authenticate servers and optionally, clients.</span></span> <span data-ttu-id="65c34-105">L’authentification du serveur, où le serveur fournit la preuve de son identité au client, est requise par les [*protocoles de sécurité*](../secgloss/s-gly.md)Schannel.</span><span class="sxs-lookup"><span data-stu-id="65c34-105">Server authentication, where the server provides proof of its identity to the client, is required by the Schannel [*security protocols*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="65c34-106">L’authentification du client peut être demandée par le serveur à tout moment.</span><span class="sxs-lookup"><span data-stu-id="65c34-106">Client authentication may be requested by the server at any time.</span></span>

<span data-ttu-id="65c34-107">Les informations d’identification Schannel sont des certificats [*X. 509*](../secgloss/x-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="65c34-107">Schannel credentials are [*X.509*](../secgloss/x-gly.md) certificates.</span></span> <span data-ttu-id="65c34-108">Les informations de clés [*publiques*](../secgloss/p-gly.md) et [*privées*](../secgloss/p-gly.md) des certificats sont utilisées pour authentifier le serveur et éventuellement le client.</span><span class="sxs-lookup"><span data-stu-id="65c34-108">[*Public*](../secgloss/p-gly.md) and [*private key*](../secgloss/p-gly.md) information from certificates is used to authenticate the server and optionally, the client.</span></span> <span data-ttu-id="65c34-109">Ces clés sont également utilisées pour assurer [*l’intégrité*](../secgloss/i-gly.md) des messages lorsque le client et le serveur échangent les informations requises pour générer et échanger des [*clés de session*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="65c34-109">These keys are also used to provide message [*integrity*](../secgloss/i-gly.md) while client and server exchange the information required to generate and exchange [*session keys*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="65c34-110">Pour plus d’informations sur la programmation, consultez [obtention d’informations d’identification Schannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="65c34-110">For programming information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

 

 
