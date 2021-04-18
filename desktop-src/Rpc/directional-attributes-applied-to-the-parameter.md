---
title: Attributs directionnels appliqués au paramètre
description: Les attributs directionnels \ dans \ et \ out \ déterminent la façon dont le client et le serveur allouent et libèrent de la mémoire. Le tableau suivant résume l’effet des attributs directionnels sur l’allocation de mémoire.
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752432836075b319483e3a17421f691a111689b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512119"
---
# <a name="directional-attributes-applied-to-the-parameter"></a><span data-ttu-id="de815-104">Attributs directionnels appliqués au paramètre</span><span class="sxs-lookup"><span data-stu-id="de815-104">Directional Attributes Applied to the Parameter</span></span>

<span data-ttu-id="de815-105">Les attributs directionnels \[ [dans](/windows/desktop/Midl/in) \] et \[ [out](/windows/desktop/Midl/out-idl) \] déterminent la façon dont le client et le serveur allouent et libèrent de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="de815-105">The directional attributes \[ [in](/windows/desktop/Midl/in)\] and \[ [out](/windows/desktop/Midl/out-idl)\] determine how the client and server allocate and free memory.</span></span> <span data-ttu-id="de815-106">Le tableau suivant résume l’effet des attributs directionnels sur l’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="de815-106">The following table summarizes the effect of directional attributes on memory allocation.</span></span>



| <span data-ttu-id="de815-107">Attribut directionnel</span><span class="sxs-lookup"><span data-stu-id="de815-107">Directional attribute</span></span>    | <span data-ttu-id="de815-108">Mémoire sur le client</span><span class="sxs-lookup"><span data-stu-id="de815-108">Memory on client</span></span>                                                                                            | <span data-ttu-id="de815-109">Mémoire sur le serveur</span><span class="sxs-lookup"><span data-stu-id="de815-109">Memory on server</span></span>                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de815-110">\[[dans](/windows/desktop/Midl/in)\]</span><span class="sxs-lookup"><span data-stu-id="de815-110">\[ [in](/windows/desktop/Midl/in)\]</span></span>       | <span data-ttu-id="de815-111">L’application cliente doit allouer avant l’appel.</span><span class="sxs-lookup"><span data-stu-id="de815-111">Client application must allocate before the call.</span></span>                                                           | <span data-ttu-id="de815-112">Le stub serveur est alloué.</span><span class="sxs-lookup"><span data-stu-id="de815-112">Server stub allocates.</span></span>                                                                                                                                  |
| <span data-ttu-id="de815-113">\[en [sortie](/windows/desktop/Midl/out-idl)\]</span><span class="sxs-lookup"><span data-stu-id="de815-113">\[ [out](/windows/desktop/Midl/out-idl)\]</span></span> | <span data-ttu-id="de815-114">Le stub client est alloué lors du retour.</span><span class="sxs-lookup"><span data-stu-id="de815-114">Client stub allocates on return.</span></span>                                                                            | <span data-ttu-id="de815-115">Le stub serveur alloue le pointeur de niveau supérieur uniquement. l’application serveur doit allouer tous les pointeurs incorporés.</span><span class="sxs-lookup"><span data-stu-id="de815-115">Server stub allocates top-level pointer only; the server application must allocate all embedded pointers.</span></span> <span data-ttu-id="de815-116">Le serveur alloue également de nouvelles données en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="de815-116">The server also allocates new data as needed.</span></span> |
| <span data-ttu-id="de815-117">\[**in**, **out**\]</span><span class="sxs-lookup"><span data-stu-id="de815-117">\[**in**, **out**\]</span></span>      | <span data-ttu-id="de815-118">L’application cliente doit allouer les données initiales transmises au serveur. le stub client alloue des données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="de815-118">Client application must allocate initial data transmitted to server; client stub allocates additional data.</span></span> | <span data-ttu-id="de815-119">Le stub serveur alloue les données initiales transmises à partir du client ; l’application serveur alloue les nouvelles données en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="de815-119">Server stub allocates initial data transmitted from client; the server application allocates new data as needed.</span></span>                                        |



 

<span data-ttu-id="de815-120">Dans tous les cas, le stub client ne libère pas la mémoire.</span><span class="sxs-lookup"><span data-stu-id="de815-120">In all of these cases the client stub does not free memory.</span></span> <span data-ttu-id="de815-121">L’application cliente doit libérer la mémoire avant qu’elle ne se termine.</span><span class="sxs-lookup"><span data-stu-id="de815-121">The client application must free the memory before it terminates.</span></span> <span data-ttu-id="de815-122">Le stub serveur libère de la mémoire lorsque l’appel de procédure distante retourne (sous réserve de l' \[ attribut [allocate](/windows/desktop/Midl/allocate) \] ACF).</span><span class="sxs-lookup"><span data-stu-id="de815-122">The server stub frees memory when the remote procedure call returns (subject to the \[ [allocate](/windows/desktop/Midl/allocate)\] ACF attribute).</span></span>

 

 