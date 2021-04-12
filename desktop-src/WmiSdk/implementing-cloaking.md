---
description: Le masquage est une extension de l’emprunt d’identité qui permet de mieux contrôler la façon dont COM emprunte l’identité d’un client sur un proxy. Comme de nombreuses formes de sécurité WMI, vous définissez le masquage via les interfaces CoSetProxyBlanket et CoInitializeSecurity.
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: Implémentation du masquage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac73d7aacf32a2168dc3651b82ae1ce3a977cf5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203963"
---
# <a name="implementing-cloaking"></a><span data-ttu-id="c697e-104">Implémentation du masquage</span><span class="sxs-lookup"><span data-stu-id="c697e-104">Implementing Cloaking</span></span>

<span data-ttu-id="c697e-105">Le masquage est une extension de l’emprunt d’identité qui permet de mieux contrôler la façon dont COM emprunte l’identité d’un client sur un proxy.</span><span class="sxs-lookup"><span data-stu-id="c697e-105">Cloaking is an extension to impersonation that allows for better control over how COM impersonates a client over a proxy.</span></span> <span data-ttu-id="c697e-106">Comme de nombreuses formes de sécurité WMI, vous définissez le masquage via les interfaces [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) et [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="c697e-106">Like many forms of WMI security, you set cloaking through the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) interfaces.</span></span>

<span data-ttu-id="c697e-107">COM fournit les formes de masquage suivantes :</span><span class="sxs-lookup"><span data-stu-id="c697e-107">COM provides the following forms of cloaking:</span></span>

-   <span data-ttu-id="c697e-108">statique</span><span class="sxs-lookup"><span data-stu-id="c697e-108">Static</span></span>

    <span data-ttu-id="c697e-109">COM établit l’identité du jeton par le thread ou le jeton de processus lors du premier appel au proxy.</span><span class="sxs-lookup"><span data-stu-id="c697e-109">COM establishes the token identity by the thread or process token on the first call to the proxy.</span></span> <span data-ttu-id="c697e-110">Si vous utilisez le masquage statique avec [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), vous définissez l’identité du proxy pendant la durée de vie du proxy.</span><span class="sxs-lookup"><span data-stu-id="c697e-110">If you use static cloaking with [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), you set the identity of the proxy for the life of the proxy.</span></span>

-   <span data-ttu-id="c697e-111">Dynamique</span><span class="sxs-lookup"><span data-stu-id="c697e-111">Dynamic</span></span>

    <span data-ttu-id="c697e-112">COM rétablit l’identité du jeton du thread ou du processus lors de chaque appel au proxy.</span><span class="sxs-lookup"><span data-stu-id="c697e-112">COM reestablishes the token identity from the thread or process token on each call to the proxy.</span></span> <span data-ttu-id="c697e-113">Étant donné que COM vérifie l’identité sur chaque appel, le masquage dynamique permet un contrôle plus fin de l’identité du client.</span><span class="sxs-lookup"><span data-stu-id="c697e-113">Because COM checks the identity on each call, dynamic cloaking allows for finer control over the client identity.</span></span> <span data-ttu-id="c697e-114">Toutefois, le masquage dynamique est moins efficace que le voilage statique.</span><span class="sxs-lookup"><span data-stu-id="c697e-114">However, dynamic cloaking is less efficient than static cloaking.</span></span>

<span data-ttu-id="c697e-115">Lorsque vous définissez le masquage conjointement avec le niveau de délégation d’emprunt d’identité, un serveur peut propager l’identité d’un client sur plusieurs serveurs, même si les serveurs sont distants.</span><span class="sxs-lookup"><span data-stu-id="c697e-115">When you set cloaking in conjunction with the delegation level of impersonation, a server can propagate the identity of a client across servers, even if the servers are remote.</span></span> <span data-ttu-id="c697e-116">Si vous n’activez pas le masquage, COM effectue un appel à partir d’un serveur local vers un serveur distant dans le contexte du processus serveur réel.</span><span class="sxs-lookup"><span data-stu-id="c697e-116">If you do not enable cloaking, COM makes any call from a local server to a remote server under the context of the actual server process.</span></span>

<span data-ttu-id="c697e-117">Le masquage permet à WMI d’emprunter l’identité d’un client pour accéder aux ressources réseau locales et distantes sur plusieurs limites de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c697e-117">Cloaking lets WMI impersonate a client to access both local and remote network resources across multiple computer boundaries.</span></span> <span data-ttu-id="c697e-118">WMI peut transmettre l’identité du client à des serveurs locaux et distants, comme d’autres instances distantes de WMI.</span><span class="sxs-lookup"><span data-stu-id="c697e-118">WMI can pass the identity of the client to local and remote servers, such as other remote instances of WMI.</span></span> <span data-ttu-id="c697e-119">Ces serveurs distants peuvent ensuite effectuer des opérations dans le contexte du client initial.</span><span class="sxs-lookup"><span data-stu-id="c697e-119">Those remote servers can then perform operations under the initial client context.</span></span>

<span data-ttu-id="c697e-120">La procédure suivante décrit l’utilisation conjointe du masquage et de la délégation.</span><span class="sxs-lookup"><span data-stu-id="c697e-120">The following procedure describes how to use cloaking and delegation together.</span></span>

<span data-ttu-id="c697e-121">**Pour utiliser simultanément le masquage et la délégation**</span><span class="sxs-lookup"><span data-stu-id="c697e-121">**To use cloaking and delegation together**</span></span>

1.  <span data-ttu-id="c697e-122">Définissez le service d’authentification sur Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c697e-122">Set the authentication service to Kerberos.</span></span>

    <span data-ttu-id="c697e-123">Kerberos est le seul service d’authentification qui prend en charge le masquage à distance et la délégation.</span><span class="sxs-lookup"><span data-stu-id="c697e-123">Kerberos is the only authentication service that supports remote cloaking and delegation.</span></span> <span data-ttu-id="c697e-124">Cela signifie que le masquage et la délégation ne peuvent être utilisés que sur des serveurs distants.</span><span class="sxs-lookup"><span data-stu-id="c697e-124">This means that cloaking and delegation can only be used on remote servers.</span></span>

2.  <span data-ttu-id="c697e-125">Marquez le compte de connexion du serveur comme « approuvé pour la délégation » dans les services Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c697e-125">Mark the server login account as "Trusted for Delegation" in the Active Directory services.</span></span>
3.  <span data-ttu-id="c697e-126">Marquez le compte de connexion du client en tant que « le compte est sensible et ne peut pas être délégué » dans les services Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c697e-126">Mark the client login account as "Account is sensitive and cannot be delegated" in Active Directory services.</span></span>

<span data-ttu-id="c697e-127">Par exemple, un appel au fournisseur d’affichage, qui peut retourner des objets à partir de plusieurs instances de WMI sur plusieurs ordinateurs, peut tirer parti de la délégation et du masquage.</span><span class="sxs-lookup"><span data-stu-id="c697e-127">For example, a call to the View Provider, which may return objects from multiple instances of WMI on multiple computers, can benefit from delegation and cloaking.</span></span>

 

 
