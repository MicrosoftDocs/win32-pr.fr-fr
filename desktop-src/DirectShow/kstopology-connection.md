---
description: Cette rubrique s’applique à Windows XP Service Pack 2 ou version ultérieure. La \_ structure de connexion KSTOPOLOGY décrit une connexion de nœud dans un filtre de diffusion en continu de noyau (KS). Un nœud peut être connecté à un autre nœud dans le filtre ou à un code confidentiel sur le filtre.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: KSTOPOLOGY_CONNECTION, structure (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSTOPOLOGY_CONNECTION
api_type:
- HeaderDef
api_location:
- Ks.h
ms.openlocfilehash: f523d378a54311845781c144b33e131d5875e41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533143"
---
# <a name="kstopology_connection-structure"></a><span data-ttu-id="65ac1-105">\_Structure de connexion KSTOPOLOGY</span><span class="sxs-lookup"><span data-stu-id="65ac1-105">KSTOPOLOGY\_CONNECTION structure</span></span>

<span data-ttu-id="65ac1-106">Cette rubrique s’applique à Windows XP Service Pack 2 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="65ac1-106">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="65ac1-107">La structure de **\_ connexion KSTOPOLOGY** décrit une connexion de nœud dans un filtre de diffusion en continu de noyau (KS).</span><span class="sxs-lookup"><span data-stu-id="65ac1-107">The **KSTOPOLOGY\_CONNECTION** structure describes a node connection within a kernel-streaming (KS) filter.</span></span> <span data-ttu-id="65ac1-108">Un nœud peut être connecté à un autre nœud dans le filtre ou à un code confidentiel sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="65ac1-108">A node can be connected to another node within the filter, or to a pin on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="65ac1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65ac1-109">Syntax</span></span>


```C++
typedef struct {
  ULONG FromNode;
  ULONG FromNodePin;
  ULONG ToNode;
  ULONG ToNodePin;
} KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION;
```



## <a name="members"></a><span data-ttu-id="65ac1-110">Membres</span><span class="sxs-lookup"><span data-stu-id="65ac1-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="65ac1-111">**FromNode**</span><span class="sxs-lookup"><span data-stu-id="65ac1-111">**FromNode**</span></span>
</dt> <dd>

<span data-ttu-id="65ac1-112">Index du nœud amont dans la connexion.</span><span class="sxs-lookup"><span data-stu-id="65ac1-112">Index of the upstream node in the connection.</span></span> <span data-ttu-id="65ac1-113">Si la connexion amont est un code confidentiel, et non un nœud, la valeur est KSFILTER \_ node.</span><span class="sxs-lookup"><span data-stu-id="65ac1-113">If the upstream connection is a pin, rather than a node, the value is KSFILTER\_NODE.</span></span>

</dd> <dt>

<span data-ttu-id="65ac1-114">**FromNodePin**</span><span class="sxs-lookup"><span data-stu-id="65ac1-114">**FromNodePin**</span></span>
</dt> <dd>

<span data-ttu-id="65ac1-115">Si la valeur du champ **FromNode** est KSFILTER \_ nœud, ce champ spécifie l’index de la broche amont.</span><span class="sxs-lookup"><span data-stu-id="65ac1-115">If the value of the **FromNode** field is KSFILTER\_NODE, this field specifies the index of the upstream pin.</span></span> <span data-ttu-id="65ac1-116">Dans le cas contraire, ce champ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="65ac1-116">Otherwise, this field is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="65ac1-117">**ToNode**</span><span class="sxs-lookup"><span data-stu-id="65ac1-117">**ToNode**</span></span>
</dt> <dd>

<span data-ttu-id="65ac1-118">Index du nœud en aval dans la connexion.</span><span class="sxs-lookup"><span data-stu-id="65ac1-118">Index of the downstream node in the connection.</span></span> <span data-ttu-id="65ac1-119">Si la connexion en aval est un code confidentiel, et non un nœud, la valeur est KSFILTER \_ node.</span><span class="sxs-lookup"><span data-stu-id="65ac1-119">If the downstream connection is a pin, rather than a node, the value is KSFILTER\_NODE.</span></span>

</dd> <dt>

<span data-ttu-id="65ac1-120">**ToNodePin**</span><span class="sxs-lookup"><span data-stu-id="65ac1-120">**ToNodePin**</span></span>
</dt> <dd>

<span data-ttu-id="65ac1-121">Si la valeur du champ **ToNode** est KSFILTER \_ nœud, ce champ spécifie l’index du code confidentiel en aval.</span><span class="sxs-lookup"><span data-stu-id="65ac1-121">If the value of the **ToNode** field is KSFILTER\_NODE, this field specifies the index of the downstream pin.</span></span> <span data-ttu-id="65ac1-122">Dans le cas contraire, ce champ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="65ac1-122">Otherwise, this field is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65ac1-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65ac1-123">Requirements</span></span>



| <span data-ttu-id="65ac1-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65ac1-124">Requirement</span></span> | <span data-ttu-id="65ac1-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="65ac1-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="65ac1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="65ac1-126">Header</span></span><br/> | <dl> <span data-ttu-id="65ac1-127"><dt>KS. h</dt></span><span class="sxs-lookup"><span data-stu-id="65ac1-127"><dt>Ks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65ac1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65ac1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ac1-129">Structures DirectShow</span><span class="sxs-lookup"><span data-stu-id="65ac1-129">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="65ac1-130">**IKsTopologyInfo :: obtient \_ ConnectionInfo**</span><span class="sxs-lookup"><span data-stu-id="65ac1-130">**IKsTopologyInfo::get\_ConnectionInfo**</span></span>](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




