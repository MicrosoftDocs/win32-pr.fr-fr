---
description: La propriété ComponentState est l’état d’installation du composant pour l’instance de ce produit. Cette propriété appelle MsiQueryComponentState, avec le ProductCode, UserSid et le contexte de l’objet.
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: Méthode Product. ComponentState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.ComponentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 240a854a899f46bf80703bbd6cfb6b1529848586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530979"
---
# <a name="productcomponentstate-method"></a><span data-ttu-id="ea9ab-103">Méthode Product. ComponentState</span><span class="sxs-lookup"><span data-stu-id="ea9ab-103">Product.ComponentState method</span></span>

<span data-ttu-id="ea9ab-104">La propriété **ComponentState** est l’état d’installation du composant pour l’instance de ce produit.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-104">The **ComponentState** property is the installation state of the component for the instance of this product.</span></span>

<span data-ttu-id="ea9ab-105">Cette propriété appelle [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea), avec le ProductCode, UserSid et le contexte de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-105">This property calls [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea), with the ProductCode, UserSid, and Context of the object.</span></span> <span data-ttu-id="ea9ab-106">Le GUID de l’ID du composant est fourni en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-106">The component Id GUID is provided as a parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea9ab-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea9ab-107">Syntax</span></span>


```JScript
Product.ComponentState(
  ID
)
```



## <a name="parameters"></a><span data-ttu-id="ea9ab-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea9ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea9ab-109">*Identifiant*</span><span class="sxs-lookup"><span data-stu-id="ea9ab-109">*ID*</span></span> 
</dt> <dd>

<span data-ttu-id="ea9ab-110">GUID du code du composant, tel qu’il figure dans la colonne ComponentID de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="ea9ab-110">Component code GUID of the component as found in the ComponentID column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea9ab-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea9ab-111">Return value</span></span>

<span data-ttu-id="ea9ab-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea9ab-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ea9ab-113">Remarks</span></span>

<span data-ttu-id="ea9ab-114">Si l’appel est effectué, la propriété contient la valeur en tant que **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-114">If the call succeeds, the property contains the value as a **DWORD**.</span></span>



| <span data-ttu-id="ea9ab-115">State</span><span class="sxs-lookup"><span data-stu-id="ea9ab-115">State</span></span>                | <span data-ttu-id="ea9ab-116">Signification</span><span class="sxs-lookup"><span data-stu-id="ea9ab-116">Meaning</span></span>                                            |
|----------------------|----------------------------------------------------|
| <span data-ttu-id="ea9ab-117">INSTALLSTATE \_ local</span><span class="sxs-lookup"><span data-stu-id="ea9ab-117">INSTALLSTATE\_LOCAL</span></span>  | <span data-ttu-id="ea9ab-118">Le composant est installé localement.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-118">The component is installed locally.</span></span>                |
| <span data-ttu-id="ea9ab-119">\_source INSTALLSTATE</span><span class="sxs-lookup"><span data-stu-id="ea9ab-119">INSTALLSTATE\_SOURCE</span></span> | <span data-ttu-id="ea9ab-120">Le composant est installé pour s’exécuter à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-120">The component is installed to run from the source.</span></span> |



 

<span data-ttu-id="ea9ab-121">Si l’appel échoue, la propriété contient un code d’erreur de [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).</span><span class="sxs-lookup"><span data-stu-id="ea9ab-121">If the call fails, the property contains an error code from [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).</span></span>



| <span data-ttu-id="ea9ab-122">Error</span><span class="sxs-lookup"><span data-stu-id="ea9ab-122">Error</span></span>                     | <span data-ttu-id="ea9ab-123">Signification</span><span class="sxs-lookup"><span data-stu-id="ea9ab-123">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9ab-124">ERREUR d' \_ accès \_ refusé</span><span class="sxs-lookup"><span data-stu-id="ea9ab-124">ERROR\_ACCESS\_DENIED</span></span>     | <span data-ttu-id="ea9ab-125">Le processus appelant doit disposer de privilèges d’administrateur pour obtenir des informations pour un utilisateur autre que l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-125">The calling process must have administrative privileges to get information for a user other than the current user.</span></span> |
| <span data-ttu-id="ea9ab-126">ERREUR de \_ configuration incorrecte \_</span><span class="sxs-lookup"><span data-stu-id="ea9ab-126">ERROR\_BAD\_CONFIGURATION</span></span> | <span data-ttu-id="ea9ab-127">Les données de configuration sont endommagées.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-127">The configuration data is corrupt.</span></span>                                                                                 |
| <span data-ttu-id="ea9ab-128">paramètre d’erreur \_ non valide \_</span><span class="sxs-lookup"><span data-stu-id="ea9ab-128">ERROR\_INVALID\_PARAMETER</span></span> | <span data-ttu-id="ea9ab-129">Un paramètre non valide a été passé à la fonction.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-129">An invalid parameter was passed to the function.</span></span>                                                                   |
| <span data-ttu-id="ea9ab-130">ERREUR de \_ réussite</span><span class="sxs-lookup"><span data-stu-id="ea9ab-130">ERROR\_SUCCESS</span></span>            | <span data-ttu-id="ea9ab-131">La fonction s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-131">The function completed successfully.</span></span>                                                                               |
| <span data-ttu-id="ea9ab-132">ERREUR \_ de \_ composant inconnu</span><span class="sxs-lookup"><span data-stu-id="ea9ab-132">ERROR\_UNKNOWN\_COMPONENT</span></span> | <span data-ttu-id="ea9ab-133">L’ID de composant n’identifie pas un composant connu.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-133">The component ID does not identify a known component.</span></span>                                                              |
| <span data-ttu-id="ea9ab-134">ERREUR \_ de \_ produit inconnu</span><span class="sxs-lookup"><span data-stu-id="ea9ab-134">ERROR\_UNKNOWN\_PRODUCT</span></span>   | <span data-ttu-id="ea9ab-135">Le code du produit n’identifie pas un produit connu.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-135">The product code does not identify a known product.</span></span>                                                                |
| <span data-ttu-id="ea9ab-136">échec de la fonction d’erreur \_ \_</span><span class="sxs-lookup"><span data-stu-id="ea9ab-136">ERROR\_FUNCTION\_FAILED</span></span>   | <span data-ttu-id="ea9ab-137">Une erreur interne inattendue.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-137">An unexpected internal failure.</span></span>                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="ea9ab-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea9ab-138">Requirements</span></span>



| <span data-ttu-id="ea9ab-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea9ab-139">Requirement</span></span> | <span data-ttu-id="ea9ab-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea9ab-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9ab-141">Version</span><span class="sxs-lookup"><span data-stu-id="ea9ab-141">Version</span></span><br/> | <span data-ttu-id="ea9ab-142">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-142">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ea9ab-143">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-143">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ea9ab-144">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ea9ab-144">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="ea9ab-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ea9ab-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="ea9ab-146"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea9ab-146"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="ea9ab-147">IID</span><span class="sxs-lookup"><span data-stu-id="ea9ab-147">IID</span></span><br/>     | <span data-ttu-id="ea9ab-148">IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ea9ab-148">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="ea9ab-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea9ab-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea9ab-150">**Production**</span><span class="sxs-lookup"><span data-stu-id="ea9ab-150">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="ea9ab-151">**MsiQueryComponentState**</span><span class="sxs-lookup"><span data-stu-id="ea9ab-151">**MsiQueryComponentState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[<span data-ttu-id="ea9ab-152">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="ea9ab-152">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




