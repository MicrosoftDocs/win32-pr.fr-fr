---
title: Méthode ISoftKbd CreateSoftKeyboardLayoutFromResource (Softkbdc. h)
description: La méthode ISoftKbd CreateSoftKeybboardLayoutFromResource crée une disposition de clavier programmable à partir de la ressource spécifiée.
ms.assetid: c1b2f8bd-8065-426d-9c23-67fa46a33dc8
keywords:
- Infrastructure des services de texte de méthode CreateSoftKeyboardLayoutFromResource
- CreateSoftKeyboardLayoutFromResource méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode CreateSoftKeyboardLayoutFromResource
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromResource
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f454b5d8f3366517d91170d6a92d6a9dbed5764
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511163"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromresource-method"></a><span data-ttu-id="7fd2f-106">ISoftKbd :: CreateSoftKeyboardLayoutFromResource, méthode</span><span class="sxs-lookup"><span data-stu-id="7fd2f-106">ISoftKbd::CreateSoftKeyboardLayoutFromResource method</span></span>

<span data-ttu-id="7fd2f-107">La méthode **ISoftKbd :: CreateSoftKeybboardLayoutFromResource** crée une disposition de clavier logiciel à partir de la ressource spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7fd2f-107">The **ISoftKbd::CreateSoftKeybboardLayoutFromResource** method creates a soft keyboard layout from the specified resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fd2f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fd2f-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardLayoutFromResource(
  [in]  WCHAR *lpszResFile,
  [in]  WCHAR *lpszResType,
  [in]  WCHAR *lpszXMLResString,
  [out] DWORD *lpdwLayoutCookie
);
```



## <a name="parameters"></a><span data-ttu-id="7fd2f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7fd2f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fd2f-110">*lpszResFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7fd2f-110">*lpszResFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd2f-111">Pointeur vers une chaîne se terminant par zéro indiquant le nom du fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="7fd2f-111">Pointer to a zero-terminated string indicating the name of the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="7fd2f-112">*lpszResType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7fd2f-112">*lpszResType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd2f-113">Pointeur vers une chaîne se terminant par zéro indiquant le type de ressource.</span><span class="sxs-lookup"><span data-stu-id="7fd2f-113">Pointer to a zero-terminated string indicating the type of resource.</span></span>

</dd> <dt>

<span data-ttu-id="7fd2f-114">*lpszXMLResString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7fd2f-114">*lpszXMLResString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd2f-115">Pointeur vers une chaîne se terminant par zéro qui identifie la ressource.</span><span class="sxs-lookup"><span data-stu-id="7fd2f-115">Pointer to a zero-terminated string identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="7fd2f-116">*lpdwLayoutCookie* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7fd2f-116">*lpdwLayoutCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd2f-117">Pointeur vers la mémoire tampon dans laquelle cette méthode récupère un cookie de disposition de clavier programmable.</span><span class="sxs-lookup"><span data-stu-id="7fd2f-117">Pointer to the buffer in which this method retrieves a soft keyboard layout cookie.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fd2f-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7fd2f-118">Return value</span></span>

<span data-ttu-id="7fd2f-119">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="7fd2f-119">This method can return one of these values.</span></span>



| <span data-ttu-id="7fd2f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fd2f-120">Value</span></span>                                                                                        | <span data-ttu-id="7fd2f-121">Description</span><span class="sxs-lookup"><span data-stu-id="7fd2f-121">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="7fd2f-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7fd2f-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="7fd2f-123">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="7fd2f-123">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="7fd2f-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7fd2f-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="7fd2f-125">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="7fd2f-125">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7fd2f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fd2f-126">Requirements</span></span>



| <span data-ttu-id="7fd2f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fd2f-127">Requirement</span></span> | <span data-ttu-id="7fd2f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fd2f-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd2f-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fd2f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd2f-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fd2f-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7fd2f-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fd2f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd2f-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fd2f-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7fd2f-133">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7fd2f-133">Redistributable</span></span><br/>          | <span data-ttu-id="7fd2f-134">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="7fd2f-134">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="7fd2f-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="7fd2f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fd2f-136"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fd2f-136"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="7fd2f-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="7fd2f-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7fd2f-138"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7fd2f-138"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="7fd2f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7fd2f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fd2f-140"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fd2f-140"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fd2f-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fd2f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fd2f-142">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="7fd2f-142">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="7fd2f-143">**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**</span><span class="sxs-lookup"><span data-stu-id="7fd2f-143">**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**</span></span>](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)
</dt> <dt>

[<span data-ttu-id="7fd2f-144">**ISoftKbd::ShowSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="7fd2f-144">**ISoftKbd::ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)
</dt> </dl>

 

 





