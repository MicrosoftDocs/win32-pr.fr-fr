---
title: ITsSbSession propriété InitialProgram
description: Récupère ou spécifie le programme initial pour cette session.
ms.assetid: c299c4f7-3c5f-468f-9fc7-81eac322dfa2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété InitialProgram
- Services Bureau à distance de la propriété InitialProgram, interface ITsSbSession
- Services Bureau à distance de l’interface ITsSbSession, propriété InitialProgram
topic_type:
- apiref
api_name:
- ITsSbSession.InitialProgram
- ITsSbSession.get_InitialProgram
- ITsSbSession.put_InitialProgram
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 307f8bb4330caf4b84b8650c9ccc2551c94da76d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465315"
---
# <a name="itssbsessioninitialprogram-property"></a><span data-ttu-id="3d863-106">ITsSbSession :: InitialProgram, propriété</span><span class="sxs-lookup"><span data-stu-id="3d863-106">ITsSbSession::InitialProgram property</span></span>

<span data-ttu-id="3d863-107">Récupère ou spécifie le programme initial pour cette session.</span><span class="sxs-lookup"><span data-stu-id="3d863-107">Retrieves or specifies the initial program for this session.</span></span> <span data-ttu-id="3d863-108">Le programme initial est le programme qui est lancé au démarrage de la session utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3d863-108">The initial program is the program that is launched when the user session starts.</span></span>

<span data-ttu-id="3d863-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d863-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d863-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d863-110">Syntax</span></span>


```C++
HRESULT put_InitialProgram(
  [in]          BSTR Application
);

HRESULT get_InitialProgram(
  [out, retval] BSTR *app
);
```



## <a name="property-value"></a><span data-ttu-id="3d863-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3d863-111">Property value</span></span>

<span data-ttu-id="3d863-112">Variable **BSTR** qui contient le programme initial.</span><span class="sxs-lookup"><span data-stu-id="3d863-112">A **BSTR** variable that contains the initial program.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d863-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d863-113">Requirements</span></span>



| <span data-ttu-id="3d863-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d863-114">Requirement</span></span> | <span data-ttu-id="3d863-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d863-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3d863-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d863-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3d863-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d863-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="3d863-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d863-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3d863-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3d863-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="3d863-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="3d863-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3d863-121"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3d863-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d863-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d863-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d863-123">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="3d863-123">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





