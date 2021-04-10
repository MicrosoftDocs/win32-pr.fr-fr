---
description: Le package d’authentification Kerberos est utilisé lors de la connexion à un réseau. les ouvertures de session locales sont gérées par MSV1 \_ 0.
ms.assetid: 43970c99-53f1-43c1-9d9f-65573572f731
title: SSP Kerberos/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d14565c8c6526d9cab34d7b9ddec9a0a04ff8de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034635"
---
# <a name="kerberos-sspap"></a><span data-ttu-id="e4df4-103">SSP Kerberos/AP</span><span class="sxs-lookup"><span data-stu-id="e4df4-103">Kerberos SSP/AP</span></span>

<span data-ttu-id="e4df4-104">Le package d’authentification [*Kerberos*](../secgloss/k-gly.md) est utilisé lors de la connexion à un réseau. les ouvertures de session locales sont gérées par MSV1 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="e4df4-104">The [*Kerberos*](../secgloss/k-gly.md) authentication package is used when logging on to a network; local logons are handled by MSV1\_0.</span></span>

<span data-ttu-id="e4df4-105">Lorsqu’un utilisateur se connecte à l’aide d’un compte réseau, par défaut, Kerberos tente de se connecter au [*Centre de distribution de clés*](../secgloss/k-gly.md) Kerberos sur le contrôleur de domaine et d’obtenir un ticket TGT (Ticket Granting Ticket) à l’aide des données de connexion fournies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e4df4-105">When a user logs on using a network account, by default, Kerberos attempts to connect to the Kerberos [*Key Distribution Center*](../secgloss/k-gly.md) (KDC) on the domain controller and obtain a ticket granting ticket (TGT) by using the logon data supplied by the user.</span></span>

<span data-ttu-id="e4df4-106">Si aucun KDC Kerberos n’est disponible, Windows utilise MSV1 \_ 0 et l’authentification directe comme décrit dans [ \_ package d’authentification MSV1 0](msv1-0-authentication-package.md).</span><span class="sxs-lookup"><span data-stu-id="e4df4-106">If a Kerberos KDC is not available, Windows uses MSV1\_0 and pass-through authentication as described in [MSV1\_0 Authentication Package](msv1-0-authentication-package.md).</span></span>

<span data-ttu-id="e4df4-107">Le package d’authentification Kerberos prend en charge la version 5, révision 6 du protocole Kerberos.</span><span class="sxs-lookup"><span data-stu-id="e4df4-107">The Kerberos authentication package supports version 5, revision 6 of the Kerberos protocol.</span></span> <span data-ttu-id="e4df4-108">Ce protocole est basé sur Internet [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).</span><span class="sxs-lookup"><span data-stu-id="e4df4-108">This protocol is based on Internet [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).</span></span> <span data-ttu-id="e4df4-109">Pour plus d’informations, consultez le site Web IETF :</span><span class="sxs-lookup"><span data-stu-id="e4df4-109">For more information, see the IETF website:</span></span>

[https://www.ietf.org](https://www.ietf.org/)

<span data-ttu-id="e4df4-110">Pour plus d’informations sur Kerberos, consultez [Microsoft Kerberos](microsoft-kerberos.md).</span><span class="sxs-lookup"><span data-stu-id="e4df4-110">For more information about Kerberos, see [Microsoft Kerberos](microsoft-kerberos.md).</span></span>

## <a name="kerberos-credential-formats"></a><span data-ttu-id="e4df4-111">Formats d’informations d’identification Kerberos</span><span class="sxs-lookup"><span data-stu-id="e4df4-111">Kerberos Credential Formats</span></span>

<span data-ttu-id="e4df4-112">Les [*informations d’identification*](../secgloss/c-gly.md) de l’utilisateur affectées par le package d’authentification Kerberos après une tentative de connexion réussie sont un ticket et une clé de chiffrement temporaire, souvent appelée [*clé de session*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e4df4-112">The user [*credentials*](../secgloss/c-gly.md) assigned by the Kerberos authentication package after a successful logon attempt are a ticket and a temporary encryption key, often called a [*session key*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="e4df4-113">Le ticket contient à la fois une copie chiffrée des informations d’identification du client et la clé de session.</span><span class="sxs-lookup"><span data-stu-id="e4df4-113">The ticket contains both an encrypted copy of the client's credentials and the session key.</span></span>

 

 
