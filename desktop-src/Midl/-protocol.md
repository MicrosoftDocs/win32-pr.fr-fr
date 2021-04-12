---
title: commutateur/Protocol
description: Le commutateur/Protocol spécifie quel protocole câble est pris en charge par le stub généré.
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- MIDL du commutateur/Protocol
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9770fa94d010e21dcbd2a5574a0cffe29273a23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313024"
---
# <a name="protocol-switch"></a><span data-ttu-id="5f48d-104">commutateur/Protocol</span><span class="sxs-lookup"><span data-stu-id="5f48d-104">/protocol switch</span></span>

<span data-ttu-id="5f48d-105">Le commutateur **/Protocol** spécifie quel protocole câble est pris en charge par le stub généré.</span><span class="sxs-lookup"><span data-stu-id="5f48d-105">The **/protocol** switch specifies which wire protocol is supported by the generated stub.</span></span>

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a><span data-ttu-id="5f48d-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="5f48d-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span data-ttu-id="5f48d-107"><span id="dce"></span><span id="DCE"></span>DCE \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5f48d-107"><span id="dce"></span><span id="DCE"></span>\*\*\*\*dce\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="5f48d-108">Le stub généré prend en charge uniquement le protocole DCE.</span><span class="sxs-lookup"><span data-stu-id="5f48d-108">The generated stub supports DCE protocol only.</span></span>

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span data-ttu-id="5f48d-109"><span id="ndr64"></span><span id="NDR64"></span>ndr64\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5f48d-109"><span id="ndr64"></span><span id="NDR64"></span>\*\*\*\*ndr64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="5f48d-110">Le stub généré prend en charge uniquement le protocole Microsoft NDR64.</span><span class="sxs-lookup"><span data-stu-id="5f48d-110">The generated stub supports Microsoft NDR64 protocol only.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="5f48d-111"><span id="all"></span><span id="ALL"></span>tous les \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5f48d-111"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="5f48d-112">Le stub généré prend en charge tous les protocoles disponibles pour un environnement donné.</span><span class="sxs-lookup"><span data-stu-id="5f48d-112">The generated stub supports all available protocols for a given environment.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f48d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5f48d-113">Remarks</span></span>

<span data-ttu-id="5f48d-114">RPC marshale et démarshale les données en fonction d’un protocole strict Wire, également appelé syntaxe de transfert, qui définit la représentation de la transmission de données, telles que l’ordre dans lequel les données membres sont marshalées, l’alignement des données sur le câble, les informations supplémentaires incluses avec les données, entre autres.</span><span class="sxs-lookup"><span data-stu-id="5f48d-114">RPC marshals and unmarshals data according to a strict wire protocol, also called transfer syntax, that defines data wire representation such as the order in which data members are marshaled, the alignment of data on the wire, additional information included with the data, among others.</span></span> <span data-ttu-id="5f48d-115">Microsoft RPC est compatible avec le protocole NDR (Network Data Representation) de l’ETCD OSF.</span><span class="sxs-lookup"><span data-stu-id="5f48d-115">Microsoft RPC is compatible with OSF DCE's NDR (network data representation) protocol.</span></span> <span data-ttu-id="5f48d-116">Dans la version 64 bits de Windows XP, Microsoft introduit un NDR64 de protocole expérimental qui est optimisé pour le transfert de données 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5f48d-116">In the 64-bit release of Windows XP, Microsoft introduces an experimental protocol NDR64 that is optimized for transferring 64-bit data.</span></span> <span data-ttu-id="5f48d-117">NDR64 n’est pas à compatibilité descendante avec le protocole DCE.</span><span class="sxs-lookup"><span data-stu-id="5f48d-117">NDR64 is not backward compatible with the DCE protocol.</span></span>

<span data-ttu-id="5f48d-118">Le protocole **DCE** est compatible avec la syntaxe de transfert de NDR de l’ETCD OSF.</span><span class="sxs-lookup"><span data-stu-id="5f48d-118">The **dce** protocol is compatible with OSF DCE's NDR transfer syntax.</span></span> <span data-ttu-id="5f48d-119">Ce protocole est optimisé pour le transfert de données 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5f48d-119">This protocol is optimized for transferring 32-bit data.</span></span>

<span data-ttu-id="5f48d-120">Le protocole **ndr64** est actuellement pris en charge uniquement lorsqu’il est utilisé conjointement avec le commutateur [**/Win64**](-win64.md) .</span><span class="sxs-lookup"><span data-stu-id="5f48d-120">The **ndr64** protocol is currently supported only when used in conjunction with the [**/win64**](-win64.md) switch.</span></span> <span data-ttu-id="5f48d-121">Si un client ndr64 uniquement tente de se connecter à un serveur DCE uniquement, ou vice versa, l’appel est rejeté avec la valeur de \_ \_ trans syn non prise en charge par RPC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5f48d-121">If a ndr64 only client tries to connect to a dce-only server, or vice versa, the call is rejected with RPC\_S\_UNSUPPORTED\_TRANS\_SYN.</span></span>

<span data-ttu-id="5f48d-122">L’option **All** crée un stub qui peut utiliser n’importe quel protocole disponible.</span><span class="sxs-lookup"><span data-stu-id="5f48d-122">The **all** option creates a stub that may use any available protocol.</span></span> <span data-ttu-id="5f48d-123">Pour les stubs 32 bits, le seul protocole actuellement disponible est DCE.</span><span class="sxs-lookup"><span data-stu-id="5f48d-123">For 32-bit stubs, the only protocol currently available is DCE.</span></span> <span data-ttu-id="5f48d-124">Pour les stubs 64 bits, créés à l’aide du commutateur [**/Win64**](-win64.md) , DCE et NDR64 sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="5f48d-124">For 64-bit stubs, created using the [**/win64**](-win64.md) switch, both DCE and NDR64 are available.</span></span>

## <a name="examples"></a><span data-ttu-id="5f48d-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="5f48d-125">Examples</span></span>

<span data-ttu-id="5f48d-126">**MIDL/Protocol tous/Win64 NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="5f48d-126">**midl /protocol all /win64 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="5f48d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f48d-127">See also</span></span>

<dl> <dt>

[**/<system>**](-system-.md)
</dt> </dl>

 

 




