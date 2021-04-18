---
description: La méthode SaveToBlob enregistre les données de propriété dans un format de persistance.
ms.assetid: 48201192-abda-484e-bdb3-442aca52b2bf
title: 'IPropertySetter :: SaveToBlob, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SaveToBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 97e248ebf741b45e73c82b17eee4181b1f19ac35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540537"
---
# <a name="ipropertysettersavetoblob-method"></a><span data-ttu-id="af7c7-103">IPropertySetter :: SaveToBlob, méthode</span><span class="sxs-lookup"><span data-stu-id="af7c7-103">IPropertySetter::SaveToBlob method</span></span>

> [!Note]  
> <span data-ttu-id="af7c7-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="af7c7-104">\[Deprecated.</span></span> <span data-ttu-id="af7c7-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="af7c7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="af7c7-106">La `SaveToBlob` méthode enregistre les données de propriété dans un format de persistance.</span><span class="sxs-lookup"><span data-stu-id="af7c7-106">The `SaveToBlob` method saves the property data to a persistence format.</span></span>

## <a name="syntax"></a><span data-ttu-id="af7c7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af7c7-107">Syntax</span></span>


```C++
HRESULT SaveToBlob(
  [out] LONG *pcSize,
  [out] BYTE **ppb
);
```



## <a name="parameters"></a><span data-ttu-id="af7c7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af7c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af7c7-109">*pcSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="af7c7-109">*pcSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af7c7-110">Reçoit la taille des données, en octets.</span><span class="sxs-lookup"><span data-stu-id="af7c7-110">Receives the size of the data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="af7c7-111">*ppb* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="af7c7-111">*ppb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af7c7-112">Reçoit un pointeur vers un tableau d’octets qui reçoit les données.</span><span class="sxs-lookup"><span data-stu-id="af7c7-112">Receives a pointer to an array of bytes that receives the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af7c7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af7c7-113">Return value</span></span>

<span data-ttu-id="af7c7-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="af7c7-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="af7c7-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="af7c7-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="af7c7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="af7c7-116">Remarks</span></span>

<span data-ttu-id="af7c7-117">La méthode alloue de la mémoire pour le tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="af7c7-117">The method allocates memory for the byte array.</span></span> <span data-ttu-id="af7c7-118">L’appelant doit le libérer, à l’aide de la fonction **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="af7c7-118">The caller must free it, using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="af7c7-119">La longueur de tous les noms et valeurs de propriétés est tronquée à 40 caractères.</span><span class="sxs-lookup"><span data-stu-id="af7c7-119">All property names and values are truncated to 40 characters in length.</span></span> <span data-ttu-id="af7c7-120">C’est la raison pour laquelle XML est le format de persistance par défaut.</span><span class="sxs-lookup"><span data-stu-id="af7c7-120">For this reason, XML is the preferred persistence format.</span></span> <span data-ttu-id="af7c7-121">Voir [**interface IXml2Dex**](ixml2dex.md).</span><span class="sxs-lookup"><span data-stu-id="af7c7-121">See [**IXml2Dex Interface**](ixml2dex.md).</span></span>

> [!Note]  
> <span data-ttu-id="af7c7-122">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="af7c7-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="af7c7-123">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="af7c7-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="af7c7-124">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="af7c7-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="af7c7-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af7c7-125">Requirements</span></span>



| <span data-ttu-id="af7c7-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af7c7-126">Requirement</span></span> | <span data-ttu-id="af7c7-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="af7c7-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af7c7-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="af7c7-128">Header</span></span><br/>  | <dl> <span data-ttu-id="af7c7-129"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="af7c7-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="af7c7-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="af7c7-130">Library</span></span><br/> | <dl> <span data-ttu-id="af7c7-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af7c7-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af7c7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af7c7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af7c7-133">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="af7c7-133">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="af7c7-134">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="af7c7-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




