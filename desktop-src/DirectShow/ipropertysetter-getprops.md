---
description: La méthode GetProps récupère les propriétés définies sur cet objet, avec leurs valeurs correspondantes.
ms.assetid: 2a2ac262-f5a4-4bbe-9cd2-aa7c7d359917
title: 'IPropertySetter :: GetProps, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.GetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f512ce672cbbaca6556ad644f21c684130eb28e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520821"
---
# <a name="ipropertysettergetprops-method"></a><span data-ttu-id="d8bc6-103">IPropertySetter :: GetProps, méthode</span><span class="sxs-lookup"><span data-stu-id="d8bc6-103">IPropertySetter::GetProps method</span></span>

> [!Note]  
> <span data-ttu-id="d8bc6-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d8bc6-104">\[Deprecated.</span></span> <span data-ttu-id="d8bc6-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d8bc6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d8bc6-106">La `GetProps` méthode récupère les propriétés définies sur cet objet, avec leurs valeurs correspondantes.</span><span class="sxs-lookup"><span data-stu-id="d8bc6-106">The `GetProps` method retrieves the properties set on this object, with their corresponding values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8bc6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8bc6-107">Syntax</span></span>


```C++
HRESULT GetProps(
  [out] LONG         *pcParams,
  [out] DEXTER_PARAM **paParam,
  [out] DEXTER_VALUE **paValue
);
```



## <a name="parameters"></a><span data-ttu-id="d8bc6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8bc6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8bc6-109">*pcParams* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d8bc6-109">*pcParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bc6-110">Reçoit le nombre de structures retournées dans *paParam*.</span><span class="sxs-lookup"><span data-stu-id="d8bc6-110">Receives the number of structures returned in *paParam*.</span></span>

</dd> <dt>

<span data-ttu-id="d8bc6-111">*paParam* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d8bc6-111">*paParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bc6-112">Adresse d’un pointeur vers un tableau de structures de [**\_ paramètres Dexter**](dexter-param.md) .</span><span class="sxs-lookup"><span data-stu-id="d8bc6-112">Address of a pointer to an array of [**DEXTER\_PARAM**](dexter-param.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="d8bc6-113">*paValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d8bc6-113">*paValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bc6-114">Adresse d’un pointeur vers un tableau de structures de [**\_ valeur Dexterity**](dexter-value.md) .</span><span class="sxs-lookup"><span data-stu-id="d8bc6-114">Address of a pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8bc6-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8bc6-115">Return value</span></span>

<span data-ttu-id="d8bc6-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d8bc6-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d8bc6-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d8bc6-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8bc6-118">Notes</span><span class="sxs-lookup"><span data-stu-id="d8bc6-118">Remarks</span></span>

<span data-ttu-id="d8bc6-119">Pour chaque propriété retournée dans *paParam*, le membre **nvaleurs** indique le nombre de structures de [**\_ valeur dexterisation**](dexter-value.md) associées à la propriété.</span><span class="sxs-lookup"><span data-stu-id="d8bc6-119">For each property returned in *paParam*, the **nValues** member indicates the number of [**DEXTER\_VALUE**](dexter-value.md) structures associated with the property.</span></span> <span data-ttu-id="d8bc6-120">Les paires sont retournées dans l’ordre chronologique croissant de chaque propriété.</span><span class="sxs-lookup"><span data-stu-id="d8bc6-120">The pairs are returned in ascending time order for each property.</span></span>

<span data-ttu-id="d8bc6-121">Lorsque vous avez terminé d’utiliser les structures retournées, appelez [**IPropertySetter :: FreeProps**](ipropertysetter-freeprops.md) pour libérer les ressources allouées par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d8bc6-121">When you are finished using the returned structures, call [**IPropertySetter::FreeProps**](ipropertysetter-freeprops.md) to free the resources allocated by this method.</span></span>

> [!Note]  
> <span data-ttu-id="d8bc6-122">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="d8bc6-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d8bc6-123">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d8bc6-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d8bc6-124">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d8bc6-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d8bc6-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="d8bc6-125">Examples</span></span>

<span data-ttu-id="d8bc6-126">L’exemple de code suivant montre comment itérer au sein de toutes les valeurs sur une instance de l’accesseur Set de propriété :</span><span class="sxs-lookup"><span data-stu-id="d8bc6-126">The following code example shows how to iterate through all the values on an instance of the property setter:</span></span>


```C++
IPropertySetter *pSetter = NULL;
// Get a valid IPropertySetter pointer (not shown).

DEXTER_PARAM *pParam;
DEXTER_VALUE *pValue;
LONG count;

hr = pSetter->GetProps(&count, &pParam, &pValue);

LONG num = 0;
for (LONG i = 0; i < count; i++)
{
    for (LONG j = 0; j < pParam[i].nValues; j++)
    {
        // pValue[num] is the next value in the sequence for pParam[i]
    }
    num += pParam[i].nValues;
}
```



## <a name="requirements"></a><span data-ttu-id="d8bc6-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8bc6-127">Requirements</span></span>



| <span data-ttu-id="d8bc6-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8bc6-128">Requirement</span></span> | <span data-ttu-id="d8bc6-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8bc6-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8bc6-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8bc6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d8bc6-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8bc6-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d8bc6-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8bc6-132">Library</span></span><br/> | <dl> <span data-ttu-id="d8bc6-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8bc6-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8bc6-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8bc6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8bc6-135">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="d8bc6-135">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="d8bc6-136">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="d8bc6-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




