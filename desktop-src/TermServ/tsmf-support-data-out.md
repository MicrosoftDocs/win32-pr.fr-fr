---
title: Structure TSMF_SUPPORT_DATA_OUT
description: Contient des informations sur les formats multimédias. | Structure TSMF_SUPPORT_DATA_OUT
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_OUT structure Services Bureau à distance
- Pointeur de structure PTSMF_SUPPORT_DATA_OUT Services Bureau à distance
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9705c4c2c27eaff904e09364b029bd74ebd05d6c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953570"
---
# <a name="tsmf_support_data_out-structure"></a><span data-ttu-id="7a8de-106">TSMF \_ prendre en charge la \_ \_ structure Data Out</span><span class="sxs-lookup"><span data-stu-id="7a8de-106">TSMF\_SUPPORT\_DATA\_OUT structure</span></span>

<span data-ttu-id="7a8de-107">Contient des informations sur les formats multimédias.</span><span class="sxs-lookup"><span data-stu-id="7a8de-107">Contains information about media formats.</span></span> <span data-ttu-id="7a8de-108">Cette structure est utilisée par la méthode [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) lors des requêtes de **\_ \_ \_ \_ prise en charge du format de requête MF Wrds** .</span><span class="sxs-lookup"><span data-stu-id="7a8de-108">This structure is used by the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) method during **WRDS\_QUERY\_MF\_FORMAT\_SUPPORT** queries.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a8de-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a8de-109">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_DATA_OUT {
  GUID                      guidMfSession;
  UINT32                    numEntries;
  TSMF_SUPPORT_NODEDATA_OUT ...;
} TSMF_SUPPORT_DATA_OUT, *PTSMF_SUPPORT_DATA_OUT;
```



## <a name="members"></a><span data-ttu-id="7a8de-110">Membres</span><span class="sxs-lookup"><span data-stu-id="7a8de-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a8de-111">**guidMfSession**</span><span class="sxs-lookup"><span data-stu-id="7a8de-111">**guidMfSession**</span></span>
</dt> <dd>

<span data-ttu-id="7a8de-112">Cela doit correspondre à la propriété **guidMfSession** dans les [**\_ données de prise en charge TSMF correspondantes \_ \_ dans**](tsmf-support-data-in.md) la structure.</span><span class="sxs-lookup"><span data-stu-id="7a8de-112">This must match the **guidMfSession** property in the corresponding [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7a8de-113">**numEntries**</span><span class="sxs-lookup"><span data-stu-id="7a8de-113">**numEntries**</span></span>
</dt> <dd>

<span data-ttu-id="7a8de-114">Nombre de structures dans les données de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="7a8de-114">The number of structures in the variable length data.</span></span>

</dd> <dt>

<span data-ttu-id="7a8de-115">**...**</span><span class="sxs-lookup"><span data-stu-id="7a8de-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="7a8de-116">Nombre variable de structures contenant des données au format de média.</span><span class="sxs-lookup"><span data-stu-id="7a8de-116">A variable number of structures containing media format data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a8de-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a8de-117">Requirements</span></span>



| <span data-ttu-id="7a8de-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a8de-118">Requirement</span></span> | <span data-ttu-id="7a8de-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a8de-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="7a8de-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a8de-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7a8de-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a8de-121">None supported</span></span><br/>         |
| <span data-ttu-id="7a8de-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a8de-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7a8de-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7a8de-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a8de-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a8de-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a8de-125">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="7a8de-125">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="7a8de-126">**TSMF \_ support \_ NODEDATA \_ out**</span><span class="sxs-lookup"><span data-stu-id="7a8de-126">**TSMF\_SUPPORT\_NODEDATA\_OUT**</span></span>](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





