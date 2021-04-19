---
description: L’interface IDxtKey définit les propriétés de la transition de clé. Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de la transition de clé.
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: Interface IDxtKey (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f4f1bc6a5dd0e89789e098fc4180bfc826f10c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538774"
---
# <a name="idxtkey-interface"></a><span data-ttu-id="4a460-103">Interface IDxtKey</span><span class="sxs-lookup"><span data-stu-id="4a460-103">IDxtKey interface</span></span>

> [!Note]  
> <span data-ttu-id="4a460-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="4a460-104">\[Deprecated.</span></span> <span data-ttu-id="4a460-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4a460-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4a460-106">L' `IDxtKey` interface définit les propriétés de la transition de [clé](key-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="4a460-106">The `IDxtKey` interface sets properties on the [Key](key-transition.md) transition.</span></span>

<span data-ttu-id="4a460-107">Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de la transition de clé.</span><span class="sxs-lookup"><span data-stu-id="4a460-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Key transition.</span></span> <span data-ttu-id="4a460-108">Les applications DES n’ont pas besoin d’utiliser cette interface.</span><span class="sxs-lookup"><span data-stu-id="4a460-108">DES applications do not need to use this interface.</span></span> <span data-ttu-id="4a460-109">Pour définir les propriétés d’une transition dans DES, utilisez l’interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="4a460-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="4a460-110">Membres</span><span class="sxs-lookup"><span data-stu-id="4a460-110">Members</span></span>

<span data-ttu-id="4a460-111">L’interface **IDxtKey** hérite de **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="4a460-111">The **IDxtKey** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="4a460-112">**IDxtKey** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4a460-112">**IDxtKey** also has these types of members:</span></span>

-   [<span data-ttu-id="4a460-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4a460-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4a460-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4a460-114">Methods</span></span>

<span data-ttu-id="4a460-115">L’interface **IDxtKey** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4a460-115">The **IDxtKey** interface has these methods.</span></span>



| <span data-ttu-id="4a460-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="4a460-116">Method</span></span>                                            | <span data-ttu-id="4a460-117">Description</span><span class="sxs-lookup"><span data-stu-id="4a460-117">Description</span></span>                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a460-118">**Obtient la \_ teinte**</span><span class="sxs-lookup"><span data-stu-id="4a460-118">**get\_Hue**</span></span>](idxtkey-get-hue.md)               | <span data-ttu-id="4a460-119">Récupère la valeur de teinte sur laquelle la clé doit être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="4a460-119">Retrieves the hue value on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="4a460-120">**être \_ inversée**</span><span class="sxs-lookup"><span data-stu-id="4a460-120">**get\_Invert**</span></span>](idxtkey-get-invert.md)         | <span data-ttu-id="4a460-121">Récupère une valeur booléenne indiquant si l’opération de clé est inversée.</span><span class="sxs-lookup"><span data-stu-id="4a460-121">Retrieves a Boolean value indicating whether the key operation is inverted.</span></span><br/> |
| [<span data-ttu-id="4a460-122">**Obtient le \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="4a460-122">**get\_KeyType**</span></span>](idxtkey-get-keytype.md)       | <span data-ttu-id="4a460-123">Récupère le type de clé.</span><span class="sxs-lookup"><span data-stu-id="4a460-123">Retrieves the type of key.</span></span><br/>                                                  |
| [<span data-ttu-id="4a460-124">**récupérer de la \_ luminance**</span><span class="sxs-lookup"><span data-stu-id="4a460-124">**get\_Luminance**</span></span>](idxtkey-get-luminance.md)   | <span data-ttu-id="4a460-125">Récupère la valeur de luminance sur laquelle la clé doit être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="4a460-125">Retrieves the luminance value on which to key.</span></span><br/>                              |
| [<span data-ttu-id="4a460-126">**recevoir des \_ couleurs RVB**</span><span class="sxs-lookup"><span data-stu-id="4a460-126">**get\_RGB**</span></span>](idxtkey-get-rgb.md)               | <span data-ttu-id="4a460-127">Récupère la couleur RVB sur laquelle la touche est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="4a460-127">Retrieves the RGB color on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="4a460-128">**faire \_ la similarité**</span><span class="sxs-lookup"><span data-stu-id="4a460-128">**get\_Similarity**</span></span>](idxtkey-get-similarity.md) | <span data-ttu-id="4a460-129">Récupère la plage de données de couleur qui devient transparente.</span><span class="sxs-lookup"><span data-stu-id="4a460-129">Retrieves the range of color data that becomes transparent.</span></span><br/>                 |
| [<span data-ttu-id="4a460-130">**mettre la \_ teinte**</span><span class="sxs-lookup"><span data-stu-id="4a460-130">**put\_Hue**</span></span>](idxtkey-put-hue.md)               | <span data-ttu-id="4a460-131">Spécifie la valeur de teinte sur laquelle la clé doit être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="4a460-131">Specifies the hue value on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="4a460-132">**mettre en \_ inverse**</span><span class="sxs-lookup"><span data-stu-id="4a460-132">**put\_Invert**</span></span>](idxtkey-put-invert.md)         | <span data-ttu-id="4a460-133">Spécifie si l’opération de clé est inversée.</span><span class="sxs-lookup"><span data-stu-id="4a460-133">Specifies whether the key operation is inverted.</span></span><br/>                            |
| [<span data-ttu-id="4a460-134">**Placer le \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="4a460-134">**put\_KeyType**</span></span>](idxtkey-put-keytype.md)       | <span data-ttu-id="4a460-135">Spécifie le type de clé.</span><span class="sxs-lookup"><span data-stu-id="4a460-135">Specifies the type of key.</span></span><br/>                                                  |
| [<span data-ttu-id="4a460-136">**Placer la \_ luminance**</span><span class="sxs-lookup"><span data-stu-id="4a460-136">**put\_Luminance**</span></span>](idxtkey-put-luminance.md)   | <span data-ttu-id="4a460-137">Spécifie la valeur de luminance sur laquelle la clé doit être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="4a460-137">Specifies the luminance value on which to key.</span></span><br/>                              |
| [<span data-ttu-id="4a460-138">**mettre en \_ RVB**</span><span class="sxs-lookup"><span data-stu-id="4a460-138">**put\_RGB**</span></span>](idxtkey-put-rgb.md)               | <span data-ttu-id="4a460-139">Spécifie la couleur RVB sur laquelle la clé doit être représentée.</span><span class="sxs-lookup"><span data-stu-id="4a460-139">Specifies the RGB color on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="4a460-140">**similarité des mises en place \_**</span><span class="sxs-lookup"><span data-stu-id="4a460-140">**put\_Similarity**</span></span>](idxtkey-put-similarity.md) | <span data-ttu-id="4a460-141">Spécifie la plage de données de couleur qui devient transparente.</span><span class="sxs-lookup"><span data-stu-id="4a460-141">Specifies the range of color data that becomes transparent.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="4a460-142">Notes</span><span class="sxs-lookup"><span data-stu-id="4a460-142">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4a460-143">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="4a460-143">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4a460-144">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a460-144">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4a460-145">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4a460-145">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a460-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a460-146">Requirements</span></span>



| <span data-ttu-id="4a460-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a460-147">Requirement</span></span> | <span data-ttu-id="4a460-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a460-148">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a460-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a460-149">Header</span></span><br/>  | <dl> <span data-ttu-id="4a460-150"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a460-150"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4a460-151">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4a460-151">Library</span></span><br/> | <dl> <span data-ttu-id="4a460-152"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a460-152"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




