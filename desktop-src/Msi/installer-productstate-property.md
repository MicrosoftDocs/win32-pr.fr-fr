---
description: La propriété ProductState est une propriété en lecture seule qui retourne les informations d’état d’installation d’un produit.
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: Méthode de propriété installer. ProductState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cdd1397def1cd25405d0a80a6d5cfde2ee6ef77e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528763"
---
# <a name="installerproductstate-property-method"></a><span data-ttu-id="dac69-103">Méthode de propriété installer. ProductState</span><span class="sxs-lookup"><span data-stu-id="dac69-103">Installer.ProductState Property method</span></span>

<span data-ttu-id="dac69-104">La **propriété ProductState** est une propriété en lecture seule qui retourne les informations d’état d’installation d’un produit.</span><span class="sxs-lookup"><span data-stu-id="dac69-104">The **ProductState property** is a read-only property that returns the install state information for a product.</span></span>

## <a name="syntax"></a><span data-ttu-id="dac69-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dac69-105">Syntax</span></span>


```JScript
Installer.ProductState Property(
  Product
)
```



## <a name="parameters"></a><span data-ttu-id="dac69-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dac69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dac69-107">*Produit*</span><span class="sxs-lookup"><span data-stu-id="dac69-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="dac69-108">Spécifie le code de produit du produit.</span><span class="sxs-lookup"><span data-stu-id="dac69-108">Specifies the product code of the product.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dac69-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dac69-109">Return value</span></span>

<span data-ttu-id="dac69-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="dac69-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dac69-111">Notes</span><span class="sxs-lookup"><span data-stu-id="dac69-111">Remarks</span></span>

<span data-ttu-id="dac69-112">Retourne l’une des valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dac69-112">Returns one of the values shown in the following table.</span></span>



| <span data-ttu-id="dac69-113">État de l'installation</span><span class="sxs-lookup"><span data-stu-id="dac69-113">Installation state</span></span>        | <span data-ttu-id="dac69-114">Description</span><span class="sxs-lookup"><span data-stu-id="dac69-114">Description</span></span>                                      |
|---------------------------|--------------------------------------------------|
| <span data-ttu-id="dac69-115">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="dac69-115">msiInstallStateAbsent</span></span>     | <span data-ttu-id="dac69-116">Le produit est installé pour un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dac69-116">The product is installed for a different user.</span></span>   |
| <span data-ttu-id="dac69-117">msiInstallStateDefault</span><span class="sxs-lookup"><span data-stu-id="dac69-117">msiInstallStateDefault</span></span>    | <span data-ttu-id="dac69-118">Le produit est installé pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="dac69-118">The product is installed for the current user.</span></span>   |
| <span data-ttu-id="dac69-119">msiInstallStateAdvertised</span><span class="sxs-lookup"><span data-stu-id="dac69-119">msiInstallStateAdvertised</span></span> | <span data-ttu-id="dac69-120">Le produit est publié, mais n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="dac69-120">The product is advertised but not installed.</span></span>     |
| <span data-ttu-id="dac69-121">msiInstallStateInvalidArg</span><span class="sxs-lookup"><span data-stu-id="dac69-121">msiInstallStateInvalidArg</span></span> | <span data-ttu-id="dac69-122">Un paramètre non valide a été passé à la fonction.</span><span class="sxs-lookup"><span data-stu-id="dac69-122">An invalid parameter was passed to the function.</span></span> |
| <span data-ttu-id="dac69-123">msiInstallStateUnknown</span><span class="sxs-lookup"><span data-stu-id="dac69-123">msiInstallStateUnknown</span></span>    | <span data-ttu-id="dac69-124">Le produit n’est ni publié ni installé.</span><span class="sxs-lookup"><span data-stu-id="dac69-124">The product is neither advertised nor installed.</span></span> |
| <span data-ttu-id="dac69-125">msiInstallStateBadConfig</span><span class="sxs-lookup"><span data-stu-id="dac69-125">msiInstallStateBadConfig</span></span>  | <span data-ttu-id="dac69-126">Les données de configuration sont endommagées.</span><span class="sxs-lookup"><span data-stu-id="dac69-126">The configuration data is corrupt.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="dac69-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dac69-127">Requirements</span></span>



| <span data-ttu-id="dac69-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dac69-128">Requirement</span></span> | <span data-ttu-id="dac69-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="dac69-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dac69-130">Version</span><span class="sxs-lookup"><span data-stu-id="dac69-130">Version</span></span><br/> | <span data-ttu-id="dac69-131">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dac69-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dac69-132">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dac69-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dac69-133">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="dac69-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="dac69-134">DLL</span><span class="sxs-lookup"><span data-stu-id="dac69-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="dac69-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dac69-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="dac69-136">IID</span><span class="sxs-lookup"><span data-stu-id="dac69-136">IID</span></span><br/>     | <span data-ttu-id="dac69-137">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="dac69-137">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="dac69-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dac69-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac69-139">**MsiQueryProductState**</span><span class="sxs-lookup"><span data-stu-id="dac69-139">**MsiQueryProductState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




