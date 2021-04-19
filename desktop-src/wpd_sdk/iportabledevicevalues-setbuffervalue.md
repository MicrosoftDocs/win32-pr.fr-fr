---
description: La méthode SetBufferValue ajoute une nouvelle valeur d’octet \* (tapez VT \_ Vector \| VT \_ UI1) ou remplace une valeur existante.
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: 'IPortableDeviceValues :: SetBufferValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e04b41fdd397d8d03e7e0576d2ba8fb3b6ad1401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539973"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a><span data-ttu-id="67af2-103">IPortableDeviceValues :: SetBufferValue, méthode</span><span class="sxs-lookup"><span data-stu-id="67af2-103">IPortableDeviceValues::SetBufferValue method</span></span>

<span data-ttu-id="67af2-104">La méthode **SetBufferValue** ajoute une nouvelle valeur d' **octet** \* (tapez VT \_ Vector \| VT \_ UI1) ou remplace une valeur existante.</span><span class="sxs-lookup"><span data-stu-id="67af2-104">The **SetBufferValue** method adds a new **BYTE**\* value (type VT\_VECTOR \| VT\_UI1) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="67af2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67af2-105">Syntax</span></span>


```C++
HRESULT SetBufferValue(
  [in] REFPROPERTYKEY key,
  [in] BYTE           *pValue,
  [in] DWORD          cbValue
);
```



## <a name="parameters"></a><span data-ttu-id="67af2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67af2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67af2-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67af2-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67af2-108">**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.</span><span class="sxs-lookup"><span data-stu-id="67af2-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="67af2-109">*pValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67af2-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67af2-110">**Octet \*** qui contient les données à écrire dans l’élément.</span><span class="sxs-lookup"><span data-stu-id="67af2-110">A **BYTE\*** that contains the data to write to the item.</span></span> <span data-ttu-id="67af2-111">Les données de mémoire tampon envoyées sont copiées dans l’interface, de sorte que l’appelant peut libérer cette mémoire tampon après avoir effectué cet appel.</span><span class="sxs-lookup"><span data-stu-id="67af2-111">The submitted buffer data is copied to the interface, so the caller can free this buffer after making this call.</span></span>

</dd> <dt>

<span data-ttu-id="67af2-112">*cbValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67af2-112">*cbValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67af2-113">Taille de la valeur vers laquelle pointe *pValue*, en octets.</span><span class="sxs-lookup"><span data-stu-id="67af2-113">The size of the value pointed to by *pValue*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67af2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67af2-114">Return value</span></span>

<span data-ttu-id="67af2-115">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="67af2-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="67af2-116">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="67af2-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="67af2-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="67af2-117">Return code</span></span>                                                                          | <span data-ttu-id="67af2-118">Description</span><span class="sxs-lookup"><span data-stu-id="67af2-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="67af2-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="67af2-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="67af2-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="67af2-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="67af2-121">Notes</span><span class="sxs-lookup"><span data-stu-id="67af2-121">Remarks</span></span>

<span data-ttu-id="67af2-122">Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="67af2-122">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="67af2-123">La mémoire clé existante est libérée de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="67af2-123">The existing key memory is released appropriately.</span></span>

<span data-ttu-id="67af2-124">La définition d’une **valeur null** ou d’une mémoire tampon de taille zéro n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="67af2-124">Setting a **NULL** or a zero-sized buffer is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="67af2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67af2-125">Requirements</span></span>



| <span data-ttu-id="67af2-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67af2-126">Requirement</span></span> | <span data-ttu-id="67af2-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="67af2-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67af2-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="67af2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="67af2-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="67af2-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="67af2-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="67af2-130">Library</span></span><br/> | <dl> <span data-ttu-id="67af2-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67af2-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67af2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67af2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67af2-133">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="67af2-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="67af2-134">**IPortableDeviceValues::GetBufferValue**</span><span class="sxs-lookup"><span data-stu-id="67af2-134">**IPortableDeviceValues::GetBufferValue**</span></span>](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




