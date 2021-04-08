---
title: IRDVTaskPlugin PluginName, propriété (Tspubplugincom. h)
description: Contient le nom complet de l’agent de tâche.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété PluginName
- Services Bureau à distance de la propriété PluginName, interface IRDVTaskPlugin
- Services Bureau à distance de l’interface IRDVTaskPlugin, propriété PluginName
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.PluginName
- IRDVTaskPlugin.get_PluginName
api_location:
- tspubplugincom.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0262472e37a8ff3e5b9bb153d2e94f4e52029b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742076"
---
# <a name="irdvtaskpluginpluginname-property"></a><span data-ttu-id="11955-106">IRDVTaskPlugin ::P propriété luginName</span><span class="sxs-lookup"><span data-stu-id="11955-106">IRDVTaskPlugin::PluginName property</span></span>

<span data-ttu-id="11955-107">Contient le nom complet de l’agent de tâche.</span><span class="sxs-lookup"><span data-stu-id="11955-107">Contains the display name of the task agent.</span></span> <span data-ttu-id="11955-108">Ce nom est utilisé uniquement à des fins de journalisation.</span><span class="sxs-lookup"><span data-stu-id="11955-108">This name is used for logging purposes only.</span></span>

<span data-ttu-id="11955-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="11955-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="11955-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11955-110">Syntax</span></span>


```C++
HRESULT get_PluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="11955-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="11955-111">Property value</span></span>

<span data-ttu-id="11955-112">Nom complet de l’agent de tâche.</span><span class="sxs-lookup"><span data-stu-id="11955-112">The display name of the task agent.</span></span>

## <a name="requirements"></a><span data-ttu-id="11955-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11955-113">Requirements</span></span>



| <span data-ttu-id="11955-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11955-114">Requirement</span></span> | <span data-ttu-id="11955-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="11955-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="11955-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11955-116">Minimum supported client</span></span><br/> | <span data-ttu-id="11955-117">Windows 7 Entreprise</span><span class="sxs-lookup"><span data-stu-id="11955-117">Windows 7 Enterprise</span></span><br/>                                                             |
| <span data-ttu-id="11955-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11955-118">Minimum supported server</span></span><br/> | <span data-ttu-id="11955-119">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="11955-119">Windows Server 2008 R2</span></span><br/>                                                           |
| <span data-ttu-id="11955-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="11955-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="11955-121"><dt>Tspubplugincom. h</dt></span><span class="sxs-lookup"><span data-stu-id="11955-121"><dt>Tspubplugincom.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11955-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11955-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11955-123">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="11955-123">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





