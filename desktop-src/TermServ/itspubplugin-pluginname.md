---
title: ItsPubPlugin propriété pluginName
description: Récupère le nom du plug-in.
ms.assetid: c1ea46b6-fac6-4140-a278-cb04ee9af739
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété pluginName
- Services Bureau à distance de la propriété pluginName, interface ItsPubPlugin
- Services Bureau à distance de l’interface ItsPubPlugin, propriété pluginName
topic_type:
- apiref
api_name:
- ItsPubPlugin.pluginName
- ItsPubPlugin.get_pluginName
api_location:
- Cpubplugin.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f5aa6ff6659047e9be48fd7b7a41f652c5cfd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527574"
---
# <a name="itspubpluginpluginname-property"></a><span data-ttu-id="47817-106">ItsPubPlugin ::p propriété luginName</span><span class="sxs-lookup"><span data-stu-id="47817-106">ItsPubPlugin::pluginName property</span></span>

<span data-ttu-id="47817-107">Récupère le nom du plug-in.</span><span class="sxs-lookup"><span data-stu-id="47817-107">Retrieves the name of the plug-in.</span></span>

<span data-ttu-id="47817-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="47817-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="47817-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47817-109">Syntax</span></span>


```C++
HRESULT get_pluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="47817-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="47817-110">Property value</span></span>

<span data-ttu-id="47817-111">Pointeur vers une variable **BSTR** devant recevoir le nom du plug-in.</span><span class="sxs-lookup"><span data-stu-id="47817-111">A pointer to a **BSTR** variable to receive the name of the plug-in.</span></span>

## <a name="requirements"></a><span data-ttu-id="47817-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47817-112">Requirements</span></span>



| <span data-ttu-id="47817-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47817-113">Requirement</span></span> | <span data-ttu-id="47817-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="47817-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="47817-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47817-115">Minimum supported client</span></span><br/> | <span data-ttu-id="47817-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="47817-116">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="47817-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47817-117">Minimum supported server</span></span><br/> | <span data-ttu-id="47817-118">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="47817-118">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="47817-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="47817-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="47817-120"><dt>Cpubplugin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="47817-120"><dt>Cpubplugin.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47817-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47817-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47817-122">**ItsPubPlugin**</span><span class="sxs-lookup"><span data-stu-id="47817-122">**ItsPubPlugin**</span></span>](/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin)
</dt> </dl>

 

 





