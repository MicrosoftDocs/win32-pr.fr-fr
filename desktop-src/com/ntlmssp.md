---
title: NTLMSSP
description: NTLMSSP
ms.assetid: ae434165-4429-4ef0-b083-60abdfc50de0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706c788f103d3d616b5a3087522b5f06b417e972
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106510711"
---
# <a name="ntlmssp"></a><span data-ttu-id="57ed1-103">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="57ed1-103">NTLMSSP</span></span>

<span data-ttu-id="57ed1-104">NTLMSSP, dont l’identificateur de service d’authentification est RPC \_ C \_ Authn \_ WinNT, est un fournisseur de support de sécurité qui est disponible sur toutes les versions de DCOM.</span><span class="sxs-lookup"><span data-stu-id="57ed1-104">NTLMSSP, whose authentication service identifier is RPC\_C\_AUTHN\_WINNT, is a security support provider that is available on all versions of DCOM.</span></span> <span data-ttu-id="57ed1-105">Elle utilise le protocole NTLM pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="57ed1-105">It uses the NTLM protocol for authentication.</span></span> <span data-ttu-id="57ed1-106">NTLM ne transmet jamais réellement le mot de passe de l’utilisateur au serveur lors de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="57ed1-106">NTLM never actually transmits the user's password to the server during authentication.</span></span> <span data-ttu-id="57ed1-107">Par conséquent, le serveur ne peut pas utiliser le mot de passe lors de l’emprunt d’identité pour accéder aux ressources réseau auxquelles l’utilisateur a accès.</span><span class="sxs-lookup"><span data-stu-id="57ed1-107">Therefore, the server cannot use the password during impersonation to access network resources that the user would have access to.</span></span> <span data-ttu-id="57ed1-108">Seules les ressources locales sont accessibles.</span><span class="sxs-lookup"><span data-stu-id="57ed1-108">Only local resources can be accessed.</span></span>

<span data-ttu-id="57ed1-109">NTLM fonctionne à la fois localement et sur plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="57ed1-109">NTLM works both locally and across computers.</span></span> <span data-ttu-id="57ed1-110">Autrement dit, si le client et le serveur se trouvent sur des ordinateurs différents, NTLM peut toujours s’assurer que le client est bien celui qu’il prétend être.</span><span class="sxs-lookup"><span data-stu-id="57ed1-110">That is, if the client and server are on different computers, NTLM can still make sure the client is who it claims to be.</span></span>

<span data-ttu-id="57ed1-111">Avec NTLM, l’identité du client est représentée par un nom de domaine, un nom d’utilisateur et un mot de passe ou un jeton.</span><span class="sxs-lookup"><span data-stu-id="57ed1-111">With NTLM, the client's identity is represented by a domain name, user name, and a password or token.</span></span> <span data-ttu-id="57ed1-112">Lorsqu’un serveur appelle [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), le nom de domaine et le nom d’utilisateur du client sont retournés.</span><span class="sxs-lookup"><span data-stu-id="57ed1-112">When a server calls [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), the client's domain name and user name are returned.</span></span> <span data-ttu-id="57ed1-113">Toutefois, lorsqu’un serveur appelle [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), le jeton du client est retourné.</span><span class="sxs-lookup"><span data-stu-id="57ed1-113">However, when a server calls [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), the client's token is returned.</span></span> <span data-ttu-id="57ed1-114">S’il n’existe aucune relation d’approbation entre le client et le serveur et si le serveur possède un compte local avec le même nom et le même mot de passe que le client, ce compte sera utilisé pour représenter le client.</span><span class="sxs-lookup"><span data-stu-id="57ed1-114">If there is no trust relationship between client and server and if the server has a local account with the same name and password as the client, that account will be used to represent the client.</span></span>

<span data-ttu-id="57ed1-115">NTLM prend en charge l’authentification mutuelle inter-threads et inter-processus (localement uniquement).</span><span class="sxs-lookup"><span data-stu-id="57ed1-115">NTLM supports mutual authentication cross-thread and cross-process (locally only).</span></span> <span data-ttu-id="57ed1-116">Si le client spécifie le nom principal du serveur sous la forme utilisateur de domaine \\ dans un appel à [**IClientSecurity :: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), l’identité du serveur doit correspondre à ce nom de principal, sans quoi l’appel échoue.</span><span class="sxs-lookup"><span data-stu-id="57ed1-116">If the client specifies the principal name of the server in the form domain\\user in a call to [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), the server's identity must match that principal name or the call will fail.</span></span> <span data-ttu-id="57ed1-117">Si le client spécifie **null**, l’identité du serveur n’est pas vérifiée.</span><span class="sxs-lookup"><span data-stu-id="57ed1-117">If the client specifies **NULL**, the server's identity will not be checked.</span></span>

<span data-ttu-id="57ed1-118">NTLM prend également en charge le niveau d’emprunt d’identité du délégué, inter-threads et inter-processus (localement uniquement).</span><span class="sxs-lookup"><span data-stu-id="57ed1-118">NTLM additionally supports the delegate impersonation level cross-thread and cross-process (locally only).</span></span>

## <a name="related-topics"></a><span data-ttu-id="57ed1-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="57ed1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57ed1-120">Packages COM et de sécurité</span><span class="sxs-lookup"><span data-stu-id="57ed1-120">COM and Security Packages</span></span>](com-and-security-packages.md)
</dt> </dl>

 

 