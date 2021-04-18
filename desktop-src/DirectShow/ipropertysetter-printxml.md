---
description: La méthode PrintXML convertit les données de propriété en une chaîne XML.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: IPropertySetter ::P méthode rintXML (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f31d36e8642cb669f5e365d6ffe25b538268bd1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540338"
---
# <a name="ipropertysetterprintxml-method"></a><span data-ttu-id="5e853-103">IPropertySetter ::P méthode rintXML</span><span class="sxs-lookup"><span data-stu-id="5e853-103">IPropertySetter::PrintXML method</span></span>

> [!Note]  
> <span data-ttu-id="5e853-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="5e853-104">\[Deprecated.</span></span> <span data-ttu-id="5e853-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5e853-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5e853-106">La `PrintXML` méthode convertit les données de propriété en une chaîne XML.</span><span class="sxs-lookup"><span data-stu-id="5e853-106">The `PrintXML` method converts property data into an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e853-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e853-107">Syntax</span></span>


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a><span data-ttu-id="5e853-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e853-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e853-109">*pszXML* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5e853-109">*pszXML* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e853-110">Pointeur vers une mémoire tampon qui reçoit la chaîne XML.</span><span class="sxs-lookup"><span data-stu-id="5e853-110">Pointer to a buffer that receives the XML string.</span></span>

</dd> <dt>

<span data-ttu-id="5e853-111">*cbXML* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e853-111">*cbXML* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e853-112">Taille de la mémoire tampon vers laquelle pointe *pszXML*, en octets.</span><span class="sxs-lookup"><span data-stu-id="5e853-112">Size of the buffer pointed to by *pszXML*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5e853-113">*pcbPrinted* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5e853-113">*pcbPrinted* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e853-114">Pointeur vers une variable qui reçoit la longueur de la chaîne XML.</span><span class="sxs-lookup"><span data-stu-id="5e853-114">Pointer to a variable that receives the length of the XML string.</span></span> <span data-ttu-id="5e853-115">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5e853-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5e853-116">*mettre en retrait* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e853-116">*indent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e853-117">Nombre de niveaux de mise en retrait pour la balise la plus à l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="5e853-117">Number of indent levels for the outermost tag.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e853-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e853-118">Return value</span></span>

<span data-ttu-id="5e853-119">Retourne S \_ OK en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="5e853-119">Returns S\_OK if successful.</span></span> <span data-ttu-id="5e853-120">Sinon, retourne une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="5e853-120">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span> <span data-ttu-id="5e853-121">Si la chaîne XML est plus longue que la mémoire tampon, la méthode retourne E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5e853-121">If the XML string is longer than the buffer, the method returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e853-122">Notes</span><span class="sxs-lookup"><span data-stu-id="5e853-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5e853-123">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="5e853-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5e853-124">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5e853-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5e853-125">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5e853-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5e853-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e853-126">Requirements</span></span>



| <span data-ttu-id="5e853-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e853-127">Requirement</span></span> | <span data-ttu-id="5e853-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e853-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e853-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e853-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5e853-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e853-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5e853-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5e853-131">Library</span></span><br/> | <dl> <span data-ttu-id="5e853-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e853-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e853-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e853-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e853-134">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="5e853-134">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="5e853-135">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="5e853-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




