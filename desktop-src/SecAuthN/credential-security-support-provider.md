---
description: CredSSP (Credential Security Support Provider Protocol) est un fournisseur de support de sécurité implémenté à l’aide de l’interface SSPI (Security Support Provider Interface).
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: Fournisseur de support de sécurité des informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9aa961f37043d84dc21280ea7d5ecb9c27c075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201829"
---
# <a name="credential-security-support-provider"></a><span data-ttu-id="d7263-103">Fournisseur de support de sécurité des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="d7263-103">Credential Security Support Provider</span></span>

<span data-ttu-id="d7263-104">CredSSP (Credential Security Support Provider Protocol) est un fournisseur de support de sécurité implémenté à l’aide de l’interface[SSPI](sspi.md)(Security Support Provider Interface).</span><span class="sxs-lookup"><span data-stu-id="d7263-104">The Credential Security Support Provider protocol (CredSSP) is a Security Support Provider that is implemented by using the Security Support Provider Interface ([SSPI](sspi.md)).</span></span> <span data-ttu-id="d7263-105">CredSSP permet à une application de déléguer les informations d’identification de l’utilisateur du client au serveur cible pour l’authentification distante.</span><span class="sxs-lookup"><span data-stu-id="d7263-105">CredSSP lets an application delegate the user's credentials from the client to the target server for remote authentication.</span></span> <span data-ttu-id="d7263-106">CredSSP fournit un canal de [protocole TLS (Transport Layer Security](transport-layer-security-protocol.md) ) chiffré.</span><span class="sxs-lookup"><span data-stu-id="d7263-106">CredSSP provides an encrypted [Transport Layer Security Protocol](transport-layer-security-protocol.md) channel.</span></span> <span data-ttu-id="d7263-107">Le client est authentifié sur le canal chiffré à l’aide du protocole SPNEGO (simple and Protected Negotiate) avec [Microsoft Kerberos](microsoft-kerberos.md) ou [Microsoft NTLM](microsoft-ntlm.md).</span><span class="sxs-lookup"><span data-stu-id="d7263-107">The client is authenticated over the encrypted channel by using the Simple and Protected Negotiate (SPNEGO) protocol with either [Microsoft Kerberos](microsoft-kerberos.md) or [Microsoft NTLM](microsoft-ntlm.md).</span></span>

> [!Caution]  
> <span data-ttu-id="d7263-108">Il ne s’agit pas d’une délégation restreinte.</span><span class="sxs-lookup"><span data-stu-id="d7263-108">This is not constrained delegation.</span></span> <span data-ttu-id="d7263-109">CredSSP transmet les informations d’identification complètes de l’utilisateur au serveur sans aucune contrainte.</span><span class="sxs-lookup"><span data-stu-id="d7263-109">CredSSP passes the user's full credentials to the server without any constraint.</span></span>

 

<span data-ttu-id="d7263-110">Pour plus d’informations sur SPNEGO, consultez [Microsoft Negotiate](microsoft-negotiate.md).</span><span class="sxs-lookup"><span data-stu-id="d7263-110">For information about SPNEGO, see [Microsoft Negotiate](microsoft-negotiate.md).</span></span>

<span data-ttu-id="d7263-111">Une fois que le client et le serveur sont authentifiés, le client transmet les informations d’identification de l’utilisateur au serveur.</span><span class="sxs-lookup"><span data-stu-id="d7263-111">After the client and server are authenticated, the client passes the user's credentials to the server.</span></span> <span data-ttu-id="d7263-112">Les informations d’identification sont chiffrées doublement sous les clés de session SPNEGO et TLS.</span><span class="sxs-lookup"><span data-stu-id="d7263-112">The credentials are doubly encrypted under the SPNEGO and TLS session keys.</span></span> <span data-ttu-id="d7263-113">CredSSP prend en charge l’ouverture de session par mot de passe, ainsi que l’ouverture de session par carte à puce basée sur [*X. 509*](/windows/desktop/SecGloss/x-gly) et PKINIT.</span><span class="sxs-lookup"><span data-stu-id="d7263-113">CredSSP supports password-based logon as well as smart card logon based on both [*X.509*](/windows/desktop/SecGloss/x-gly) and PKINIT.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7263-114">CredSSP ne prend pas en charge les clients WOW64.</span><span class="sxs-lookup"><span data-stu-id="d7263-114">CredSSP does not support Wow64 clients.</span></span>

 

<span data-ttu-id="d7263-115">Pour plus d’informations sur CredSSP, consultez les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7263-115">For more information about CredSSP, see the following topics.</span></span>



| <span data-ttu-id="d7263-116">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d7263-116">Topic</span></span>                                                                         | <span data-ttu-id="d7263-117">Description</span><span class="sxs-lookup"><span data-stu-id="d7263-117">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7263-118">Paramètres stratégie de groupe CredSSP</span><span class="sxs-lookup"><span data-stu-id="d7263-118">CredSSP Group Policy Settings</span></span>](credssp-group-policy-settings.md)<br/> | <span data-ttu-id="d7263-119">La délégation des informations d’identification par CredSSP peut être contrôlée à l’aide des paramètres de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d7263-119">Delegation of credentials by CredSSP can be controlled by using group policy settings.</span></span><br/> |



 

 

