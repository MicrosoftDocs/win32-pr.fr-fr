---
description: Ferme un handle vers un fournisseur de tickets d’impression.
ms.assetid: ce979c89-9f9d-4e89-b142-beed414caa3f
title: UnbindPTProviderThunk fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnbindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: dd87f528603624e9957d8c5f3fb12cc857ec4f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520553"
---
# <a name="unbindptproviderthunk-function"></a><span data-ttu-id="90b4a-103">UnbindPTProviderThunk fonction)</span><span class="sxs-lookup"><span data-stu-id="90b4a-103">UnbindPTProviderThunk function</span></span>

<span data-ttu-id="90b4a-104">\[Cette fonction n’est pas prise en charge et peut être désactivée ou supprimée dans les versions futures de Windows.</span><span class="sxs-lookup"><span data-stu-id="90b4a-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="90b4a-105">[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) fournit des fonctionnalités équivalentes et doit être utilisé à la place.\]</span><span class="sxs-lookup"><span data-stu-id="90b4a-105">[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="90b4a-106">Ferme un handle vers un fournisseur de tickets d’impression.</span><span class="sxs-lookup"><span data-stu-id="90b4a-106">Closes a handle to a print ticket provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="90b4a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90b4a-107">Syntax</span></span>


```C++
HRESULT UnbindPTProviderThunk(
  _In_ HPTPROVIDER hProvider
);
```



## <a name="parameters"></a><span data-ttu-id="90b4a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90b4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90b4a-109">*hProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="90b4a-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90b4a-110">Handle d’un fournisseur de tickets d’impression ouvert.</span><span class="sxs-lookup"><span data-stu-id="90b4a-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="90b4a-111">Ce descripteur est retourné par la fonction [**BindPTProviderThunk**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="90b4a-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90b4a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="90b4a-112">Return value</span></span>

<span data-ttu-id="90b4a-113">Si la méthode est réussie, elle retourne **S \_ OK**; sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="90b4a-113">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="90b4a-114">Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="90b4a-114">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90b4a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90b4a-115">Requirements</span></span>



| <span data-ttu-id="90b4a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90b4a-116">Requirement</span></span> | <span data-ttu-id="90b4a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="90b4a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90b4a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90b4a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="90b4a-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90b4a-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="90b4a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90b4a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="90b4a-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90b4a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="90b4a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="90b4a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90b4a-123"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90b4a-123"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90b4a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90b4a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90b4a-125">Schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="90b4a-125">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="90b4a-126">**PTCloseProvider**</span><span class="sxs-lookup"><span data-stu-id="90b4a-126">**PTCloseProvider**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)
</dt> <dt>

[<span data-ttu-id="90b4a-127">Impression</span><span class="sxs-lookup"><span data-stu-id="90b4a-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="90b4a-128">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="90b4a-128">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

