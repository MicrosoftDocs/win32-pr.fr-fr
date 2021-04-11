---
title: Utilisation de RPC avec le proxy Winsock
description: Utilisation de RPC avec le proxy Winsock
ms.assetid: d36e2737-f6a0-40ce-92e0-058976c08eb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5f658cf60d7e530da99ee139dbcdcbb2c89685
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031813"
---
# <a name="using-rpc-with-winsock-proxy"></a><span data-ttu-id="d1c4e-103">Utilisation de RPC avec le proxy Winsock</span><span class="sxs-lookup"><span data-stu-id="d1c4e-103">Using RPC with Winsock Proxy</span></span>

<span data-ttu-id="d1c4e-104">La version de Microsoft Internet Access Server comprenait le proxy Winsock, version améliorée de l’API Windows Sockets version 1,1.</span><span class="sxs-lookup"><span data-stu-id="d1c4e-104">The release of Microsoft Internet Access Server included Winsock Proxy, an enhanced version of Windows Sockets API version 1.1.</span></span> <span data-ttu-id="d1c4e-105">Le proxy Winsock permet à une application Windows Sockets exécutée sur un client réseau privé de se comporter comme si elle était connectée directement à une application de serveur Internet distant.</span><span class="sxs-lookup"><span data-stu-id="d1c4e-105">Winsock Proxy lets a Windows Sockets application, running on a private network client, behave as if it were directly connected to a remote Internet server application.</span></span> <span data-ttu-id="d1c4e-106">Le serveur proxy Microsoft joue le rôle d’hôte pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="d1c4e-106">The Microsoft Proxy Server acts as the host for this connection.</span></span> <span data-ttu-id="d1c4e-107">Cela signifie que toutes les communications au niveau de l’application sont représentées par un seul ordinateur sécurisé : l’ordinateur de passerelle exécutant Microsoft Proxy Server.</span><span class="sxs-lookup"><span data-stu-id="d1c4e-107">This means that all application-level communications are channeled through a single secured computer—the gateway computer running Microsoft Proxy Server.</span></span>

<span data-ttu-id="d1c4e-108">Habituellement, pour les transferts de paquets de datagrammes, la DLL de transport RPC ignore les fonctions [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) et [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) fournies dans Wsock32.dll, et communique directement avec le pilote de périphérique sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="d1c4e-108">Ordinarily, for datagram-packet transfers, the RPC transport DLL bypasses the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) and [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) functions provided in Wsock32.dll, and communicates directly with the underlying device driver.</span></span> <span data-ttu-id="d1c4e-109">Cela améliore la vitesse des transferts de paquets, mais rend les fonctionnalités du proxy Winsock indisponibles pour l’application.</span><span class="sxs-lookup"><span data-stu-id="d1c4e-109">This improves the speed of packet transfers but makes Winsock Proxy features unavailable to the application.</span></span>

<span data-ttu-id="d1c4e-110">Chaque fournisseur de protocole réseau doit avoir un GUID associé.</span><span class="sxs-lookup"><span data-stu-id="d1c4e-110">Each network protocol provider to have an associated GUID.</span></span> <span data-ttu-id="d1c4e-111">La bibliothèque Runtime RPC compare les GUID UDP et IPX aux identificateurs Microsoft connus.</span><span class="sxs-lookup"><span data-stu-id="d1c4e-111">The RPC run-time library compares the UDP and IPX GUIDs to the well known Microsoft identifiers.</span></span> <span data-ttu-id="d1c4e-112">S’ils ne correspondent pas, RPC utilise automatiquement Winsock.</span><span class="sxs-lookup"><span data-stu-id="d1c4e-112">If they don't match, RPC automatically uses Winsock.</span></span>

<span data-ttu-id="d1c4e-113">Une autre fonctionnalité du proxy Winsock est sa capacité à émuler le protocole de transport TCP sur le transport Novell SPX lorsque TCP n’est pas installé sur l’ordinateur client SPX.</span><span class="sxs-lookup"><span data-stu-id="d1c4e-113">Another feature of Winsock Proxy is its ability to emulate the TCP transport protocol over the Novell SPX transport when the SPX client computer does not have TCP installed.</span></span> <span data-ttu-id="d1c4e-114">Pour utiliser cette fonctionnalité avec les applications RPC, modifiez le registre système sur chaque ordinateur client pour ajouter cette entrée :</span><span class="sxs-lookup"><span data-stu-id="d1c4e-114">To use this feature with RPC applications, edit the system registry on each client computer to add this entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ClientProtocols
   ncacn_ip_tcp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

<span data-ttu-id="d1c4e-115">Modifiez le registre sur chaque ordinateur serveur pour ajouter cette entrée :</span><span class="sxs-lookup"><span data-stu-id="d1c4e-115">Edit the registry on each server computer to add this entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ServerProtocols
   ncacn_ip_tcp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

<span data-ttu-id="d1c4e-116">Pour plus d’informations sur les protocoles de transport RPC, consultez [spécification de séquences de protocole](specifying-protocol-sequences.md).</span><span class="sxs-lookup"><span data-stu-id="d1c4e-116">For more information about RPC transport protocols see [Specifying Protocol Sequences](specifying-protocol-sequences.md).</span></span> <span data-ttu-id="d1c4e-117">Pour plus d’informations sur le proxy Winsock, consultez la documentation produit de Microsoft Internet Access Server (en anglais).</span><span class="sxs-lookup"><span data-stu-id="d1c4e-117">For more information about Winsock Proxy, see the product documentation for Microsoft Internet Access Server.</span></span>

<span data-ttu-id="d1c4e-118">Windows 2000 n’implémente pas les entrées de Registre **ClientProtocols** et **ServerProtocols** .</span><span class="sxs-lookup"><span data-stu-id="d1c4e-118">Windows 2000 does not implement the **ClientProtocols** and **ServerProtocols** registry entries.</span></span> <span data-ttu-id="d1c4e-119">Microsoft fournit tous les transports bien connus dans le cadre de la bibliothèque Runtime.</span><span class="sxs-lookup"><span data-stu-id="d1c4e-119">Microsoft provides all well known transports as part of the run-time library.</span></span> <span data-ttu-id="d1c4e-120">Par conséquent, ces entrées ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="d1c4e-120">Therefore, these entries are not necessary.</span></span>

 

 