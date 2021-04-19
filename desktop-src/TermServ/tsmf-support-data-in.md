---
title: Structure TSMF_SUPPORT_DATA_IN
description: Contient des informations sur les formats multimédias. | Structure TSMF_SUPPORT_DATA_IN
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_IN structure Services Bureau à distance
- Pointeur de structure PTSMF_SUPPORT_DATA_IN Services Bureau à distance
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2072363978cb0e70d64a09d855ed2861341e9cf0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106537213"
---
# <a name="tsmf_support_data_in-structure"></a><span data-ttu-id="9677a-106">\_Données de prise en charge TSMF \_ \_ dans la structure</span><span class="sxs-lookup"><span data-stu-id="9677a-106">TSMF\_SUPPORT\_DATA\_IN structure</span></span>

<span data-ttu-id="9677a-107">Contient des informations sur les formats multimédias.</span><span class="sxs-lookup"><span data-stu-id="9677a-107">Contains information about media formats.</span></span> <span data-ttu-id="9677a-108">Cette structure est utilisée par la méthode [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) lors des requêtes de **\_ \_ \_ \_ prise en charge du format de requête MF Wrds** .</span><span class="sxs-lookup"><span data-stu-id="9677a-108">This structure is used by the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) method during **WRDS\_QUERY\_MF\_FORMAT\_SUPPORT** queries.</span></span>

## <a name="syntax"></a><span data-ttu-id="9677a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9677a-109">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_DATA_IN {
  GUID                     guidMfSession;
  UINT32                   numEntries;
  TSMF_SUPPORT_NODEDATA_IN ...;
} TSMF_SUPPORT_DATA_IN, *PTSMF_SUPPORT_DATA_IN;
```



## <a name="members"></a><span data-ttu-id="9677a-110">Membres</span><span class="sxs-lookup"><span data-stu-id="9677a-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="9677a-111">**guidMfSession**</span><span class="sxs-lookup"><span data-stu-id="9677a-111">**guidMfSession**</span></span>
</dt> <dd>

<span data-ttu-id="9677a-112">Session.</span><span class="sxs-lookup"><span data-stu-id="9677a-112">The session.</span></span>

</dd> <dt>

<span data-ttu-id="9677a-113">**numEntries**</span><span class="sxs-lookup"><span data-stu-id="9677a-113">**numEntries**</span></span>
</dt> <dd>

<span data-ttu-id="9677a-114">Nombre de structures dans les données de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="9677a-114">The number of structures in the variable length data.</span></span>

</dd> <dt>

<span data-ttu-id="9677a-115">**...**</span><span class="sxs-lookup"><span data-stu-id="9677a-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="9677a-116">Nombre variable de structures contenant des données au format de média.</span><span class="sxs-lookup"><span data-stu-id="9677a-116">A variable number of structures containing media format data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9677a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9677a-117">Requirements</span></span>



| <span data-ttu-id="9677a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9677a-118">Requirement</span></span> | <span data-ttu-id="9677a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9677a-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="9677a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9677a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9677a-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9677a-121">None supported</span></span><br/>         |
| <span data-ttu-id="9677a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9677a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9677a-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9677a-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9677a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9677a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9677a-125">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="9677a-125">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="9677a-126">**TSMF \_ prend en charge \_ NODEDATA \_ dans**</span><span class="sxs-lookup"><span data-stu-id="9677a-126">**TSMF\_SUPPORT\_NODEDATA\_IN**</span></span>](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





