---
title: Session. Delete, méthode (WSManDisp. h)
description: Supprime la ressource spécifiée dans l’URI de ressource.
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- Supprimer la méthode Windows Remote Management
- Delete, méthode Windows Remote Management, objet session
- Windows Remote Management d’objet de session, méthode Delete
topic_type:
- apiref
api_name:
- Session.Delete
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf4b46997a7e3cf50dbf50c2828de78a814a513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941859"
---
# <a name="sessiondelete-method"></a><span data-ttu-id="81e66-106">Session. Delete, méthode</span><span class="sxs-lookup"><span data-stu-id="81e66-106">Session.Delete method</span></span>

<span data-ttu-id="81e66-107">Supprime la ressource spécifiée dans l’URI de ressource.</span><span class="sxs-lookup"><span data-stu-id="81e66-107">Deletes the resource specified in the resource URI.</span></span>

## <a name="syntax"></a><span data-ttu-id="81e66-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81e66-108">Syntax</span></span>


```VB
Session.Delete( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="81e66-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81e66-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81e66-110">*resourceuri* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81e66-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81e66-111">URI de la ressource à supprimer.</span><span class="sxs-lookup"><span data-stu-id="81e66-111">The URI of the resource to be deleted.</span></span> <span data-ttu-id="81e66-112">Vous pouvez également utiliser un objet [**ResourceLocator**](resourcelocator.md) pour spécifier la ressource.</span><span class="sxs-lookup"><span data-stu-id="81e66-112">You can also use a [**ResourceLocator**](resourcelocator.md) object to specify the resource.</span></span>

</dd> <dt>

<span data-ttu-id="81e66-113">*indicateurs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="81e66-113">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="81e66-114">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="81e66-114">Reserved for future use.</span></span> <span data-ttu-id="81e66-115">Doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="81e66-115">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81e66-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81e66-116">Return value</span></span>

<span data-ttu-id="81e66-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="81e66-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81e66-118">Notes</span><span class="sxs-lookup"><span data-stu-id="81e66-118">Remarks</span></span>

<span data-ttu-id="81e66-119">La syntaxe suivante est utilisée pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="81e66-119">The following syntax is used to call this method.</span></span>


```VB
session.Delete("<resourceUri>")
```



## <a name="examples"></a><span data-ttu-id="81e66-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="81e66-120">Examples</span></span>

<span data-ttu-id="81e66-121">L’exemple de code VBScript suivant supprime les écouteurs configurés pour le transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="81e66-121">The following VBScript code example deletes the listeners configured for HTTP transport.</span></span>


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
  "config/Listener?Address=*+Transport=HTTP"
objSession.Delete(strResource)
```



## <a name="requirements"></a><span data-ttu-id="81e66-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81e66-122">Requirements</span></span>



| <span data-ttu-id="81e66-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81e66-123">Requirement</span></span> | <span data-ttu-id="81e66-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="81e66-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="81e66-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81e66-125">Minimum supported client</span></span><br/> | <span data-ttu-id="81e66-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81e66-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="81e66-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81e66-127">Minimum supported server</span></span><br/> | <span data-ttu-id="81e66-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81e66-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="81e66-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="81e66-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="81e66-130"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="81e66-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="81e66-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="81e66-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="81e66-132"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="81e66-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="81e66-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="81e66-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="81e66-134"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="81e66-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="81e66-135">DLL</span><span class="sxs-lookup"><span data-stu-id="81e66-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81e66-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81e66-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="81e66-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81e66-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81e66-138">**session**</span><span class="sxs-lookup"><span data-stu-id="81e66-138">**Session**</span></span>](session.md)
</dt> </dl>

 

 





