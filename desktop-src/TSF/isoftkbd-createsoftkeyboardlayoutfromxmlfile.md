---
title: Méthode ISoftKbd CreateSoftKeyboardLayoutFromXMLFile (Softkbdc. h)
description: La méthode ISoftKbd CreateSoftKeyboardLayoutFromXMLFile crée une disposition de clavier programmable à partir du fichier XML spécifié.
ms.assetid: e665adab-1d75-4e41-87bf-c8ce0f7a0399
keywords:
- Infrastructure des services de texte de méthode CreateSoftKeyboardLayoutFromXMLFile
- CreateSoftKeyboardLayoutFromXMLFile méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode CreateSoftKeyboardLayoutFromXMLFile
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromXMLFile
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252db845c5e1cc732adc295e1989fee83d4ac6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513808"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromxmlfile-method"></a><span data-ttu-id="a2fcc-106">ISoftKbd :: CreateSoftKeyboardLayoutFromXMLFile, méthode</span><span class="sxs-lookup"><span data-stu-id="a2fcc-106">ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile method</span></span>

<span data-ttu-id="a2fcc-107">La méthode **ISoftKbd :: CreateSoftKeyboardLayoutFromXMLFile** crée une disposition de clavier programmable à partir du fichier XML spécifié.</span><span class="sxs-lookup"><span data-stu-id="a2fcc-107">The **ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile** method creates a soft keyboard layout from the specified XML file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2fcc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2fcc-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardLayoutFromXMLFile(
  [in]  WCHAR *lpszKeyboardDesFile,
  [in]  INT   szFileStrLen,
  [out] DWORD *pdwLayoutCookie
);
```



## <a name="parameters"></a><span data-ttu-id="a2fcc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2fcc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2fcc-110">*lpszKeyboardDesFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2fcc-110">*lpszKeyboardDesFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2fcc-111">Pointeur vers une chaîne se terminant par zéro indiquant le nom du fichier XML.</span><span class="sxs-lookup"><span data-stu-id="a2fcc-111">Pointer to a zero-terminated string indicating the name of the XML file.</span></span>

</dd> <dt>

<span data-ttu-id="a2fcc-112">*szFileStrLen* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2fcc-112">*szFileStrLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2fcc-113">Chaîne se terminant par zéro qui indique la longueur du fichier XML.</span><span class="sxs-lookup"><span data-stu-id="a2fcc-113">Zero-terminated string indicating the length of the XML file.</span></span>

</dd> <dt>

<span data-ttu-id="a2fcc-114">*pdwLayoutCookie* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a2fcc-114">*pdwLayoutCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2fcc-115">Pointeur vers la mémoire tampon dans laquelle cette méthode récupère un cookie de disposition de clavier programmable.</span><span class="sxs-lookup"><span data-stu-id="a2fcc-115">Pointer to the buffer in which this method retrieves a soft keyboard layout cookie.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2fcc-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2fcc-116">Return value</span></span>

<span data-ttu-id="a2fcc-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a2fcc-117">This method can return one of these values.</span></span>



| <span data-ttu-id="a2fcc-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2fcc-118">Value</span></span>                                                                                        | <span data-ttu-id="a2fcc-119">Description</span><span class="sxs-lookup"><span data-stu-id="a2fcc-119">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="a2fcc-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a2fcc-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a2fcc-121">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a2fcc-121">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="a2fcc-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a2fcc-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a2fcc-123">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="a2fcc-123">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a2fcc-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2fcc-124">Requirements</span></span>



| <span data-ttu-id="a2fcc-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2fcc-125">Requirement</span></span> | <span data-ttu-id="a2fcc-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2fcc-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2fcc-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2fcc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a2fcc-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2fcc-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a2fcc-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2fcc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a2fcc-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2fcc-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a2fcc-131">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a2fcc-131">Redistributable</span></span><br/>          | <span data-ttu-id="a2fcc-132">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="a2fcc-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="a2fcc-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2fcc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2fcc-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2fcc-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="a2fcc-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="a2fcc-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a2fcc-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a2fcc-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="a2fcc-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a2fcc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2fcc-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2fcc-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2fcc-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2fcc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2fcc-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="a2fcc-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="a2fcc-141">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span><span class="sxs-lookup"><span data-stu-id="a2fcc-141">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> </dl>

 

 





