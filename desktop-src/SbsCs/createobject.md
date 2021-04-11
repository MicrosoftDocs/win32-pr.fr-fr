---
description: La méthode CreateObject de l’objet Microsoft. Windows. ActCtx crée un objet dans le contexte du manifeste actuel.
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: ActCtx. CreateObject, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.CreateObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2b4c4393d59ea5ab711dbf4bb1f4c88d906b6582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203383"
---
# <a name="actctxcreateobject-method"></a><span data-ttu-id="30ec7-103">ActCtx. CreateObject, méthode</span><span class="sxs-lookup"><span data-stu-id="30ec7-103">ActCtx.CreateObject method</span></span>

<span data-ttu-id="30ec7-104">La méthode **CreateObject** de l’objet [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) crée un objet dans le contexte du manifeste actuel.</span><span class="sxs-lookup"><span data-stu-id="30ec7-104">The **CreateObject** method of the [**Microsoft.Windows.ActCtx**](microsoft-windows-actctx-object.md) object creates an object in the context of the current manifest.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ec7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30ec7-105">Syntax</span></span>


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a><span data-ttu-id="30ec7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30ec7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30ec7-107">*objectId*</span><span class="sxs-lookup"><span data-stu-id="30ec7-107">*objectId*</span></span> 
</dt> <dd>

<span data-ttu-id="30ec7-108">Chaîne qui spécifie le type d’objet à créer.</span><span class="sxs-lookup"><span data-stu-id="30ec7-108">A string that specifies the type of object to create.</span></span> <span data-ttu-id="30ec7-109">Par exemple, un ProgID COM.</span><span class="sxs-lookup"><span data-stu-id="30ec7-109">For example, a COM ProgID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30ec7-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30ec7-110">Return value</span></span>

<span data-ttu-id="30ec7-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="30ec7-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="30ec7-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30ec7-112">Requirements</span></span>



| <span data-ttu-id="30ec7-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30ec7-113">Requirement</span></span> | <span data-ttu-id="30ec7-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="30ec7-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="30ec7-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30ec7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="30ec7-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30ec7-116">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="30ec7-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30ec7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="30ec7-118">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30ec7-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="30ec7-119">DLL</span><span class="sxs-lookup"><span data-stu-id="30ec7-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30ec7-120"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30ec7-120"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="30ec7-121">IID</span><span class="sxs-lookup"><span data-stu-id="30ec7-121">IID</span></span><br/>                      | <span data-ttu-id="30ec7-122">IID \_ IActCtx est défini en tant que 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="30ec7-122">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="30ec7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30ec7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ec7-124">**GetObject, méthode**</span><span class="sxs-lookup"><span data-stu-id="30ec7-124">**GetObject Method**</span></span>](getobject.md)
</dt> </dl>

 

 




