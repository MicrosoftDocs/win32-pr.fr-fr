---
title: attribut de point de terminaison
description: L’attribut \ Endpoint \ spécifie un ou des ports connus (points de terminaison de communication) sur lesquels les serveurs de l’interface écoutent les appels.
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- MIDL, attribut de point de terminaison
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4383df496a791859f7249766f0dbb59266d28e93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842134"
---
# <a name="endpoint-attribute"></a><span data-ttu-id="57039-104">attribut de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="57039-104">endpoint attribute</span></span>

<span data-ttu-id="57039-105">L’attribut **\[ point de terminaison \]** spécifie un ou des ports bien connus (points de terminaison de communication) sur lesquels les serveurs de l’interface écoutent les appels.</span><span class="sxs-lookup"><span data-stu-id="57039-105">The **\[endpoint\]** attribute specifies a well-known port or ports (communication endpoints) on which servers of the interface listen for calls.</span></span>

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a><span data-ttu-id="57039-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57039-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57039-107">*Protocole-séquence*</span><span class="sxs-lookup"><span data-stu-id="57039-107">*protocol-sequence*</span></span> 
</dt> <dd>

<span data-ttu-id="57039-108">Spécifie une chaîne de caractères qui représente une combinaison valide d’un protocole RPC (tel que « ncacn »), un protocole de transport (tel que « TCP ») et un protocole réseau (tel que « IP »).</span><span class="sxs-lookup"><span data-stu-id="57039-108">Specifies a character string that represents a valid combination of an RPC protocol (such as "ncacn"), a transport protocol (such as "tcp"), and a network protocol (such as "ip").</span></span> <span data-ttu-id="57039-109">Pour obtenir la liste des séquences de protocole valides, consultez [constantes de séquence de protocole](/windows/desktop/Rpc/protocol-sequence-constants).</span><span class="sxs-lookup"><span data-stu-id="57039-109">For a list of valid protocol sequences, see [Protocol Sequence Constants](/windows/desktop/Rpc/protocol-sequence-constants).</span></span>

</dd> <dt>

<span data-ttu-id="57039-110">*port de point de terminaison*</span><span class="sxs-lookup"><span data-stu-id="57039-110">*endpoint-port*</span></span> 
</dt> <dd>

<span data-ttu-id="57039-111">Spécifie une chaîne qui représente la désignation du point de terminaison pour la famille de protocoles spécifiée.</span><span class="sxs-lookup"><span data-stu-id="57039-111">Specifies a string that represents the endpoint designation for the specified protocol family.</span></span> <span data-ttu-id="57039-112">La syntaxe de la chaîne de port est spécifique à chaque séquence de protocole.</span><span class="sxs-lookup"><span data-stu-id="57039-112">The syntax of the port string is specific to each protocol sequence.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57039-113">Notes</span><span class="sxs-lookup"><span data-stu-id="57039-113">Remarks</span></span>

<span data-ttu-id="57039-114">L’attribut **\[ point de terminaison \]** spécifie une famille de transport telle que le protocole orienté connexion TCP/IP, un protocole orienté connexion NetBIOS ou le protocole orienté connexion de canal nommé.</span><span class="sxs-lookup"><span data-stu-id="57039-114">The **\[endpoint\]** attribute specifies a transport family such as the TCP/IP connection-oriented protocol, a NetBIOS connection-oriented protocol, or the named-pipe connection-oriented protocol.</span></span> <span data-ttu-id="57039-115">L’utilisation de l’attribut de **\[ point de terminaison \]** est cohérente avec d’autres méthodes pour ajouter un point de terminaison, et ne fournit pas de services supplémentaires ou spéciaux pour le point de terminaison ; il fournit simplement un raccourci pour appeler l’API.</span><span class="sxs-lookup"><span data-stu-id="57039-115">Use of the **\[endpoint\]** attribute is consistent with other methods for adding an endpoint, and does not provide additional or special services for the endpoint; it simply provides a shortcut for calling the API.</span></span>

> [!Note]  
> <span data-ttu-id="57039-116">Spécification d’un point de terminaison dans le. La définition de l’interface IDL ne restreint pas l’accès à l’interface au point de terminaison spécifié.</span><span class="sxs-lookup"><span data-stu-id="57039-116">Specifying an endpoint in the .IDL interface definition does not restrict access to the interface to the specified endpoint.</span></span> <span data-ttu-id="57039-117">Ajout d’un point de terminaison à. La définition de l’interface IDL permet à l’interface d’être appelée par n’importe quel point de terminaison de ce processus, et permet d’utiliser le point de terminaison pour appeler d’autres interfaces dans ce processus.</span><span class="sxs-lookup"><span data-stu-id="57039-117">Adding an endpoint to the .IDL interface definition allows the interface to be called through any endpoint in that process, and allows the endpoint to be used to call other interfaces in that process.</span></span>

 

<span data-ttu-id="57039-118">La valeur de *séquence de protocole* détermine les valeurs valides pour le port de *point de terminaison*.</span><span class="sxs-lookup"><span data-stu-id="57039-118">The *protocol-sequence* value determines the valid values for the *endpoint-port*.</span></span> <span data-ttu-id="57039-119">Le compilateur MIDL vérifie uniquement la syntaxe générale de l’entrée *Endpoint-port* .</span><span class="sxs-lookup"><span data-stu-id="57039-119">The MIDL compiler checks only general syntax for the *endpoint-port* entry.</span></span> <span data-ttu-id="57039-120">Les erreurs de spécification de port sont signalées par les bibliothèques Runtime.</span><span class="sxs-lookup"><span data-stu-id="57039-120">Port specification errors are reported by the run-time libraries.</span></span> <span data-ttu-id="57039-121">Pour plus d’informations sur les valeurs autorisées pour chaque séquence de protocole, consultez les [constantes de séquence de protocole](/windows/desktop/Rpc/protocol-sequence-constants).</span><span class="sxs-lookup"><span data-stu-id="57039-121">For information about the allowed values for each protocol sequence, see the [Protocol Sequence Constants](/windows/desktop/Rpc/protocol-sequence-constants).</span></span>

<span data-ttu-id="57039-122">Les séquences de protocole suivantes spécifiées par DCE ne sont pas prises en charge par le compilateur MIDL fourni avec Microsoft RPC : **ncacn \_ OSI \_ DNA** et **ncadg \_ DDS**.</span><span class="sxs-lookup"><span data-stu-id="57039-122">The following protocol sequences specified by DCE are not supported by the MIDL compiler provided with Microsoft RPC: **ncacn\_osi\_dna** and **ncadg\_dds**.</span></span>

<span data-ttu-id="57039-123">Veillez à bien citer les barres obliques inverses dans les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="57039-123">Make sure that you correctly quote backslash characters in endpoints.</span></span> <span data-ttu-id="57039-124">Cette erreur se produit généralement lorsque le point de terminaison est un canal nommé.</span><span class="sxs-lookup"><span data-stu-id="57039-124">This error commonly occurs when the endpoint is a named pipe.</span></span>

<span data-ttu-id="57039-125">Les informations de point de terminaison spécifiées dans le fichier IDL sont utilisées par les fonctions d’exécution RPC [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) et [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).</span><span class="sxs-lookup"><span data-stu-id="57039-125">Endpoint information specified in the IDL file is used by the RPC run-time functions [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) and [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).</span></span>

## <a name="examples"></a><span data-ttu-id="57039-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="57039-126">Examples</span></span>

``` syntax
endpoint("ncacn_np:[\\pipe\\rainier]") 

endpoint("ncacn_ip_tcp:[1044]", "ncacn_np:[\\pipe\\shasta]")
```

## <a name="see-also"></a><span data-ttu-id="57039-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57039-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57039-128">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="57039-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="57039-129">**RpcServerUseAllProtseqsIf**</span><span class="sxs-lookup"><span data-stu-id="57039-129">**RpcServerUseAllProtseqsIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)
</dt> <dt>

[<span data-ttu-id="57039-130">**RpcServerUseProtseqIf**</span><span class="sxs-lookup"><span data-stu-id="57039-130">**RpcServerUseProtseqIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif)
</dt> </dl>

 

 