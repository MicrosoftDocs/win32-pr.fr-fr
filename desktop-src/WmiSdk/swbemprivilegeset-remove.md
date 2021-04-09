---
description: La méthode Remove de l’objet SWbemPrivilegeSet supprime un privilège de la collection.
ms.assetid: 4c0b6d49-262c-4840-955b-35b16b68f29f
ms.tgt_platform: multiple
title: SWbemPrivilegeSet. Remove, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f277e291a4296253d7c0b1b11c694952ddc17ddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865658"
---
# <a name="swbemprivilegesetremove-method"></a><span data-ttu-id="62812-103">SWbemPrivilegeSet. Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="62812-103">SWbemPrivilegeSet.Remove method</span></span>

<span data-ttu-id="62812-104">La méthode **Remove** de l’objet [**SWbemPrivilegeSet**](swbemprivilegeset.md) supprime un privilège de la collection.</span><span class="sxs-lookup"><span data-stu-id="62812-104">The **Remove** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object deletes a privilege from the collection.</span></span>

<span data-ttu-id="62812-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="62812-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="62812-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62812-106">Syntax</span></span>


```VB
SWbemPrivilegeSet.Remove( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a><span data-ttu-id="62812-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62812-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62812-108">*iPrivilege*</span><span class="sxs-lookup"><span data-stu-id="62812-108">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="62812-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="62812-109">Required.</span></span> <span data-ttu-id="62812-110">Il s’agit de l’une des constantes WMI du groupe [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="62812-110">This is one of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="62812-111">Ces constantes sont essentiellement des entiers qui représentent des privilèges spécifiques.</span><span class="sxs-lookup"><span data-stu-id="62812-111">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="62812-112">Par exemple, pour supprimer le privilège qui vous permet d’arrêter un système Windows, utilisez la constante **wbemPrivilegeShutdown** ou l’équivalent numérique de 0x17.</span><span class="sxs-lookup"><span data-stu-id="62812-112">For example, to remove the privilege that allows you to shut down a Windows system, use the **wbemPrivilegeShutdown** constant or the numeric equivalent of 0x17.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62812-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62812-113">Return value</span></span>

<span data-ttu-id="62812-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="62812-114">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="62812-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="62812-115">Error codes</span></span>

<span data-ttu-id="62812-116">À la fin de la méthode **Remove** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="62812-116">Upon completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="62812-117">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="62812-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="62812-118">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="62812-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="62812-119">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="62812-119">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="62812-120">Le privilège spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="62812-120">Specified privilege does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62812-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62812-121">Requirements</span></span>



| <span data-ttu-id="62812-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62812-122">Requirement</span></span> | <span data-ttu-id="62812-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="62812-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62812-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62812-124">Minimum supported client</span></span><br/> | <span data-ttu-id="62812-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62812-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62812-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62812-126">Minimum supported server</span></span><br/> | <span data-ttu-id="62812-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62812-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62812-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="62812-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="62812-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="62812-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="62812-130">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="62812-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="62812-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="62812-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="62812-132">DLL</span><span class="sxs-lookup"><span data-stu-id="62812-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62812-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62812-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="62812-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="62812-134">CLSID</span></span><br/>                    | <span data-ttu-id="62812-135">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="62812-135">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="62812-136">IID</span><span class="sxs-lookup"><span data-stu-id="62812-136">IID</span></span><br/>                      | <span data-ttu-id="62812-137">IID \_ ISWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="62812-137">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="62812-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62812-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62812-139">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="62812-139">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="62812-140">**SWbemPrivilegeSet. Add**</span><span class="sxs-lookup"><span data-stu-id="62812-140">**SWbemPrivilegeSet.Add**</span></span>](swbemprivilegeset-add.md)
</dt> </dl>

 

 




