---
description: La propriété FeatureState est l’état d’installation de la fonctionnalité pour l’instance de ce produit. Cette propriété appelle MsiQueryFeatureStateEx, avec le ProductCode, UserSid et le contexte de l’objet. L’ID de fonctionnalité est fourni en tant que paramètre.
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: Méthode Product. FeatureState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f7e602ce5d5b0a8e524f76144c7f1eff8876bb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541278"
---
# <a name="productfeaturestate-method"></a><span data-ttu-id="e1cab-104">Méthode Product. FeatureState</span><span class="sxs-lookup"><span data-stu-id="e1cab-104">Product.FeatureState method</span></span>

<span data-ttu-id="e1cab-105">La propriété **FeatureState** est l’état d’installation de la fonctionnalité pour l’instance de ce produit.</span><span class="sxs-lookup"><span data-stu-id="e1cab-105">The **FeatureState** property is the installation state of the feature for the instance of this product.</span></span>

<span data-ttu-id="e1cab-106">Cette propriété appelle [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa), avec le *ProductCode*, *UserSid* et le *contexte* de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e1cab-106">This property calls [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa), with the *ProductCode*, *UserSid* and *Context* of the object.</span></span> <span data-ttu-id="e1cab-107">L’ID de fonctionnalité est fourni en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="e1cab-107">The feature Id is provided as a parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1cab-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1cab-108">Syntax</span></span>


```JScript
Product.FeatureState(
  FeatureId
)
```



## <a name="parameters"></a><span data-ttu-id="e1cab-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1cab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1cab-110">*FeatureId*</span><span class="sxs-lookup"><span data-stu-id="e1cab-110">*FeatureId*</span></span> 
</dt> <dd>

<span data-ttu-id="e1cab-111">ID de fonctionnalité qui apparaît dans la colonne fonctionnalité du [tableau des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="e1cab-111">Feature Id appearing in the Feature column of the [Feature Table](feature-table.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1cab-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1cab-112">Return value</span></span>

<span data-ttu-id="e1cab-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e1cab-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1cab-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e1cab-114">Remarks</span></span>

<span data-ttu-id="e1cab-115">Si l’appel est effectué, la propriété contient la valeur en tant que **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="e1cab-115">If the call succeeds, the property contains the value as a **DWORD**.</span></span>



| <span data-ttu-id="e1cab-116">State</span><span class="sxs-lookup"><span data-stu-id="e1cab-116">State</span></span>                    | <span data-ttu-id="e1cab-117">Signification</span><span class="sxs-lookup"><span data-stu-id="e1cab-117">Meaning</span></span>                                      |
|--------------------------|----------------------------------------------|
| <span data-ttu-id="e1cab-118">INSTALLSTATE \_ publié</span><span class="sxs-lookup"><span data-stu-id="e1cab-118">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="e1cab-119">Cette fonctionnalité est publiée.</span><span class="sxs-lookup"><span data-stu-id="e1cab-119">This feature is advertised.</span></span>                  |
| <span data-ttu-id="e1cab-120">INSTALLSTATE \_ local</span><span class="sxs-lookup"><span data-stu-id="e1cab-120">INSTALLSTATE\_LOCAL</span></span>      | <span data-ttu-id="e1cab-121">La fonctionnalité est installée localement.</span><span class="sxs-lookup"><span data-stu-id="e1cab-121">The feature is installed locally.</span></span>            |
| <span data-ttu-id="e1cab-122">\_source INSTALLSTATE</span><span class="sxs-lookup"><span data-stu-id="e1cab-122">INSTALLSTATE\_SOURCE</span></span>     | <span data-ttu-id="e1cab-123">La fonctionnalité est installée pour s’exécuter à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="e1cab-123">The feature is installed to run from source.</span></span> |



 

<span data-ttu-id="e1cab-124">Si l’appel échoue, la propriété contient un code d’erreur de [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).</span><span class="sxs-lookup"><span data-stu-id="e1cab-124">If the call fails, the property contains an error code from [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).</span></span>



| <span data-ttu-id="e1cab-125">Error</span><span class="sxs-lookup"><span data-stu-id="e1cab-125">Error</span></span>                     | <span data-ttu-id="e1cab-126">Signification</span><span class="sxs-lookup"><span data-stu-id="e1cab-126">Meaning</span></span>                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1cab-127">ERREUR d' \_ accès \_ refusé</span><span class="sxs-lookup"><span data-stu-id="e1cab-127">ERROR\_ACCESS\_DENIED</span></span>     | <span data-ttu-id="e1cab-128">Le processus appelant doit disposer de privilèges d’administrateur pour obtenir des informations sur un produit installé pour un utilisateur autre que l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="e1cab-128">The calling process must have administrative privileges to get information for a product installed for a user other than the current user.</span></span> |
| <span data-ttu-id="e1cab-129">ERREUR de \_ configuration incorrecte \_</span><span class="sxs-lookup"><span data-stu-id="e1cab-129">ERROR\_BAD\_CONFIGURATION</span></span> | <span data-ttu-id="e1cab-130">Les données de configuration sont endommagées.</span><span class="sxs-lookup"><span data-stu-id="e1cab-130">The configuration data is corrupt.</span></span>                                                                                                         |
| <span data-ttu-id="e1cab-131">paramètre d’erreur \_ non valide \_</span><span class="sxs-lookup"><span data-stu-id="e1cab-131">ERROR\_INVALID\_PARAMETER</span></span> | <span data-ttu-id="e1cab-132">Un paramètre non valide a été passé à la fonction.</span><span class="sxs-lookup"><span data-stu-id="e1cab-132">An invalid parameter was passed to the function.</span></span>                                                                                           |
| <span data-ttu-id="e1cab-133">ERREUR de \_ réussite</span><span class="sxs-lookup"><span data-stu-id="e1cab-133">ERROR\_SUCCESS</span></span>            | <span data-ttu-id="e1cab-134">La fonction s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e1cab-134">The function completed successfully.</span></span>                                                                                                       |
| <span data-ttu-id="e1cab-135">\_fonctionnalité inconnue d’erreur \_</span><span class="sxs-lookup"><span data-stu-id="e1cab-135">ERROR\_UNKNOWN\_FEATURE</span></span>   | <span data-ttu-id="e1cab-136">L’ID de fonctionnalité n’identifie pas une fonctionnalité connue.</span><span class="sxs-lookup"><span data-stu-id="e1cab-136">The feature ID does not identify a known feature.</span></span>                                                                                          |
| <span data-ttu-id="e1cab-137">ERREUR \_ de \_ produit inconnu</span><span class="sxs-lookup"><span data-stu-id="e1cab-137">ERROR\_UNKNOWN\_PRODUCT</span></span>   | <span data-ttu-id="e1cab-138">Le code du produit n’identifie pas un produit connu.</span><span class="sxs-lookup"><span data-stu-id="e1cab-138">The product code does not identify a known product.</span></span>                                                                                        |
| <span data-ttu-id="e1cab-139">échec de la fonction d’erreur \_ \_</span><span class="sxs-lookup"><span data-stu-id="e1cab-139">ERROR\_FUNCTION\_FAILED</span></span>   | <span data-ttu-id="e1cab-140">Une erreur interne inattendue.</span><span class="sxs-lookup"><span data-stu-id="e1cab-140">An unexpected internal failure.</span></span>                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="e1cab-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1cab-141">Requirements</span></span>



| <span data-ttu-id="e1cab-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1cab-142">Requirement</span></span> | <span data-ttu-id="e1cab-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1cab-143">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1cab-144">Version</span><span class="sxs-lookup"><span data-stu-id="e1cab-144">Version</span></span><br/> | <span data-ttu-id="e1cab-145">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e1cab-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e1cab-146">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e1cab-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e1cab-147">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e1cab-147">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="e1cab-148">DLL</span><span class="sxs-lookup"><span data-stu-id="e1cab-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="e1cab-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1cab-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="e1cab-150">IID</span><span class="sxs-lookup"><span data-stu-id="e1cab-150">IID</span></span><br/>     | <span data-ttu-id="e1cab-151">IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e1cab-151">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="e1cab-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1cab-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1cab-153">**Production**</span><span class="sxs-lookup"><span data-stu-id="e1cab-153">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="e1cab-154">**MsiQueryFeatureStateEx**</span><span class="sxs-lookup"><span data-stu-id="e1cab-154">**MsiQueryFeatureStateEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[<span data-ttu-id="e1cab-155">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="e1cab-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




