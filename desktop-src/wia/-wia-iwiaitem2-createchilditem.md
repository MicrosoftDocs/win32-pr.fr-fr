---
description: Créez un nouvel élément enfant. Ajoute des objets IWiaItem2 à l’arborescence IWiaItem2 d’un appareil.
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: 'IWiaItem2 :: CreateChildItem, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CreateChildItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0002a6110894491a8d6efabb5a142b7c81adc820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517718"
---
# <a name="iwiaitem2createchilditem-method"></a><span data-ttu-id="56ef9-104">IWiaItem2 :: CreateChildItem, méthode</span><span class="sxs-lookup"><span data-stu-id="56ef9-104">IWiaItem2::CreateChildItem method</span></span>

<span data-ttu-id="56ef9-105">Créez un nouvel élément enfant.</span><span class="sxs-lookup"><span data-stu-id="56ef9-105">Create a new child item.</span></span> <span data-ttu-id="56ef9-106">Ajoute des objets [**IWiaItem2**](-wia-iwiaitem2.md) à l’arborescence **IWiaItem2** d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="56ef9-106">Adds [**IWiaItem2**](-wia-iwiaitem2.md) objects to a device's **IWiaItem2** tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="56ef9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56ef9-107">Syntax</span></span>


```C++
HRESULT CreateChildItem(
  [in]  LONG      lItemFlags,
  [in]  LONG      lCreationFlags,
  [in]  BSTR      bstrItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="56ef9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56ef9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56ef9-109">*lItemFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56ef9-109">*lItemFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56ef9-110">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="56ef9-110">Type: **LONG**</span></span>

<span data-ttu-id="56ef9-111">Spécifie le type d’élément WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="56ef9-111">Specifies the WIA 2.0 item type.</span></span> <span data-ttu-id="56ef9-112">Consultez [**indicateurs de type d’élément WIA**](-wia-wia-item-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="56ef9-112">See [**WIA Item Type Flags**](-wia-wia-item-type-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="56ef9-113">*lCreationFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56ef9-113">*lCreationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56ef9-114">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="56ef9-114">Type: **LONG**</span></span>

<span data-ttu-id="56ef9-115">Spécifie comment créer le nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="56ef9-115">Specifies how to create the new item.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="56ef9-116"><span id="0"></span>**0** (0)</span><span class="sxs-lookup"><span data-stu-id="56ef9-116"><span id="0"></span>**0** (0)</span></span>


</dt> <dd>

<span data-ttu-id="56ef9-117">Définissez les valeurs par défaut des propriétés de l’enfant.</span><span class="sxs-lookup"><span data-stu-id="56ef9-117">Set the default values for the properties of the child.</span></span>

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span data-ttu-id="56ef9-118"><span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**Copier \_ \_ \_ Valeurs de propriété Parent** (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="56ef9-118"><span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**COPY\_PARENT\_PROPERTY\_VALUES** (0x40000000)</span></span>


</dt> <dd>

<span data-ttu-id="56ef9-119">Copiez les valeurs de toutes les propriétés en lecture/écriture à partir du parent.</span><span class="sxs-lookup"><span data-stu-id="56ef9-119">Copy the values of all Read/Write properties from the parent.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="56ef9-120">*bstrItemName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56ef9-120">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56ef9-121">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="56ef9-121">Type: **BSTR**</span></span>

<span data-ttu-id="56ef9-122">Spécifie le nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="56ef9-122">Specifies the item name.</span></span> <span data-ttu-id="56ef9-123">Ce nom est ajouté à la fin du nom de l’élément parent pour générer le nom complet de l’élément.</span><span class="sxs-lookup"><span data-stu-id="56ef9-123">This name is appended to the end of the parent item's name to generate the full item name.</span></span>

</dd> <dt>

<span data-ttu-id="56ef9-124">*ppIWiaItem2* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="56ef9-124">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56ef9-125">Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="56ef9-125">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="56ef9-126">Reçoit l’adresse d’un pointeur vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) qui définit la méthode **IWiaItem2 :: CreateChildItem** .</span><span class="sxs-lookup"><span data-stu-id="56ef9-126">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface that sets the **IWiaItem2::CreateChildItem** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56ef9-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56ef9-127">Return value</span></span>

<span data-ttu-id="56ef9-128">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="56ef9-128">Type: **HRESULT**</span></span>

<span data-ttu-id="56ef9-129">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="56ef9-129">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="56ef9-130">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="56ef9-130">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="56ef9-131">Notes</span><span class="sxs-lookup"><span data-stu-id="56ef9-131">Remarks</span></span>

<span data-ttu-id="56ef9-132">Certains périphériques matériels WIA 2,0 permettent aux applications de créer des éléments dans l’arborescence [**IWiaItem2**](-wia-iwiaitem2.md) qui représente l’appareil.</span><span class="sxs-lookup"><span data-stu-id="56ef9-132">Some WIA 2.0 hardware devices allow applications to create new items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree that represents the device.</span></span> <span data-ttu-id="56ef9-133">Les applications doivent tester les périphériques pour voir s’ils prennent en charge cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="56ef9-133">Applications must test the devices to see if they support this capability.</span></span> <span data-ttu-id="56ef9-134">Utilisez l' \_ interface IEnumWIA dev \_ Caps pour énumérer les fonctionnalités actuelles de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="56ef9-134">Use the IEnumWIA\_DEV\_CAPS interface to enumerate the current device's capabilities.</span></span>

<span data-ttu-id="56ef9-135">Si l’appareil autorise la création de nouveaux éléments dans l’arborescence [**IWiaItem2**](-wia-iwiaitem2.md) , l’appel de **IWiaItem2 :: CreateChildItem** crée un nouvel objet **IWiaItem2** qui est un enfant du nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="56ef9-135">If the device allows the creation of new items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree, invoking **IWiaItem2::CreateChildItem** creates a new **IWiaItem2** object that is a child of the current node.</span></span> <span data-ttu-id="56ef9-136">Il passe un pointeur vers le nouveau nœud à l’application via le paramètre *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="56ef9-136">It passes a pointer to the new node to the application through the *ppIWiaItem2* parameter.</span></span> <span data-ttu-id="56ef9-137">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="56ef9-137">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="56ef9-138">Si *lCreationFlags* est une \_ copie \_ \_ des valeurs de propriété parent et *lItemFlags* est égal à zéro, la fonction retourne E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="56ef9-138">If *lCreationFlags* is COPY\_PARENT\_PROPERTY\_VALUES and *lItemFlags* is zero, the function returns E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="56ef9-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56ef9-139">Requirements</span></span>



| <span data-ttu-id="56ef9-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56ef9-140">Requirement</span></span> | <span data-ttu-id="56ef9-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="56ef9-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="56ef9-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56ef9-142">Minimum supported client</span></span><br/> | <span data-ttu-id="56ef9-143">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56ef9-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="56ef9-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56ef9-144">Minimum supported server</span></span><br/> | <span data-ttu-id="56ef9-145">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56ef9-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="56ef9-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="56ef9-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="56ef9-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="56ef9-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="56ef9-148">MIDL</span><span class="sxs-lookup"><span data-stu-id="56ef9-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="56ef9-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56ef9-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 
