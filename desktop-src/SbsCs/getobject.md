---
description: La méthode GetObject obtient une instance d’un objet Microsoft. Windows. ActCtx existant.
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: ActCtx. GetObject, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.GetObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 11b71d8d40d947472612c91f70e9956aa7798806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750964"
---
# <a name="actctxgetobject-method"></a><span data-ttu-id="e7fff-103">ActCtx. GetObject, méthode</span><span class="sxs-lookup"><span data-stu-id="e7fff-103">ActCtx.GetObject method</span></span>

<span data-ttu-id="e7fff-104">La méthode **GetObject** obtient une instance d’un objet [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) existant.</span><span class="sxs-lookup"><span data-stu-id="e7fff-104">The **GetObject** method gets an instance of an existing [**Microsoft.Windows.ActCtx**](microsoft-windows-actctx-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7fff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7fff-105">Syntax</span></span>


```JScript
ActCtx.GetObject(
  bstrName
)
```



## <a name="parameters"></a><span data-ttu-id="e7fff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7fff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7fff-107">*bstrName,*</span><span class="sxs-lookup"><span data-stu-id="e7fff-107">*bstrName*</span></span> 
</dt> <dd>

<span data-ttu-id="e7fff-108">Chaîne obligatoire qui indique l’objet.</span><span class="sxs-lookup"><span data-stu-id="e7fff-108">Required string that indicates the object.</span></span> <span data-ttu-id="e7fff-109">Le nom doit figurer dans le Registre sous **HKEY \_ local \_ machine** \\ **Microsoft** \\ **Visual Studio** \\ **6,0** \\ **<package>** \\ **Automation**.</span><span class="sxs-lookup"><span data-stu-id="e7fff-109">The name must be in the registry under **HKEY\_LOCAL\_MACHINE**\\**Microsoft**\\**Visual Studio**\\**6.0**\\**<package>**\\**Automation**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7fff-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7fff-110">Return value</span></span>

<span data-ttu-id="e7fff-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e7fff-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7fff-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7fff-112">Requirements</span></span>



| <span data-ttu-id="e7fff-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7fff-113">Requirement</span></span> | <span data-ttu-id="e7fff-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7fff-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e7fff-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7fff-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e7fff-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7fff-116">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e7fff-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7fff-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e7fff-118">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7fff-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e7fff-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e7fff-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7fff-120"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7fff-120"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="e7fff-121">IID</span><span class="sxs-lookup"><span data-stu-id="e7fff-121">IID</span></span><br/>                      | <span data-ttu-id="e7fff-122">IID \_ IActCtx est défini en tant que 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="e7fff-122">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="e7fff-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7fff-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7fff-124">**CreateObject, méthode**</span><span class="sxs-lookup"><span data-stu-id="e7fff-124">**CreateObject Method**</span></span>](createobject.md)
</dt> </dl>

 

 




