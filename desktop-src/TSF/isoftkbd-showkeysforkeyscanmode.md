---
title: Méthode ISoftKbd ShowKeysForKeyScanMode (Softkbdc. h)
description: La méthode ISoftKbd ShowKeysForKeyScanMode affiche les clés utilisées pour le mode d’analyse de clé pour un clavier conditionnel.
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- Infrastructure des services de texte de méthode ShowKeysForKeyScanMode
- ShowKeysForKeyScanMode méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode ShowKeysForKeyScanMode
topic_type:
- apiref
api_name:
- ISoftKbd.ShowKeysForKeyScanMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c46fbfc103c0ba40294e4c149d5fd427296765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466299"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a><span data-ttu-id="a4fcb-106">ISoftKbd :: ShowKeysForKeyScanMode, méthode</span><span class="sxs-lookup"><span data-stu-id="a4fcb-106">ISoftKbd::ShowKeysForKeyScanMode method</span></span>

<span data-ttu-id="a4fcb-107">La méthode **ISoftKbd :: ShowKeysForKeyScanMode** affiche les clés utilisées pour le mode d’analyse de clé pour un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a4fcb-107">The **ISoftKbd::ShowKeysForKeyScanMode** method displays the keys used for the key scan mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4fcb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4fcb-108">Syntax</span></span>


```C++
HRESULT ShowKeysForKeyScanMode(
  [in] KEYID *lpKeyID,
  [in] INT   iKeyNum,
  [in] BOOL  fHighL
);
```



## <a name="parameters"></a><span data-ttu-id="a4fcb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4fcb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4fcb-110">*lpKeyID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a4fcb-110">*lpKeyID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4fcb-111">Pointeur vers un tableau d’éléments KEYID indiquant les identificateurs des clés à afficher.</span><span class="sxs-lookup"><span data-stu-id="a4fcb-111">Pointer to an array of KEYID elements indicating the identifiers of keys to display.</span></span>

</dd> <dt>

<span data-ttu-id="a4fcb-112">*iKeyNum* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a4fcb-112">*iKeyNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4fcb-113">Nombre de clés à afficher.</span><span class="sxs-lookup"><span data-stu-id="a4fcb-113">The number of keys to display.</span></span>

</dd> <dt>

<span data-ttu-id="a4fcb-114">*fHighL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a4fcb-114">*fHighL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4fcb-115">TRUE si la méthode doit mettre en surbrillance les clés et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a4fcb-115">TRUE if the method is to highlight the keys, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4fcb-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4fcb-116">Return value</span></span>

<span data-ttu-id="a4fcb-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a4fcb-117">This method can return one of these values.</span></span>



| <span data-ttu-id="a4fcb-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4fcb-118">Value</span></span>                                                                                        | <span data-ttu-id="a4fcb-119">Description</span><span class="sxs-lookup"><span data-stu-id="a4fcb-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a4fcb-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a4fcb-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a4fcb-121">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a4fcb-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="a4fcb-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a4fcb-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a4fcb-123">L’un des paramètres n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a4fcb-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a4fcb-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4fcb-124">Requirements</span></span>



| <span data-ttu-id="a4fcb-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4fcb-125">Requirement</span></span> | <span data-ttu-id="a4fcb-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4fcb-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4fcb-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4fcb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a4fcb-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4fcb-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a4fcb-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4fcb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a4fcb-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4fcb-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a4fcb-131">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a4fcb-131">Redistributable</span></span><br/>          | <span data-ttu-id="a4fcb-132">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="a4fcb-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="a4fcb-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4fcb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4fcb-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4fcb-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="a4fcb-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="a4fcb-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a4fcb-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a4fcb-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="a4fcb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a4fcb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4fcb-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4fcb-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4fcb-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4fcb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4fcb-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="a4fcb-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





