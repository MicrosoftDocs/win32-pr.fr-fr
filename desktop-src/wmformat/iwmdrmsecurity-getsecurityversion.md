---
title: Méthode IWMDRMSecurity GetSecurityVersion (wmdrmsdk. h)
description: La méthode GetSecurityVersion récupère la version du sous-système DRM sur l’ordinateur client.
ms.assetid: ec97dec8-61ba-4424-b5eb-2e6885cc1f48
keywords:
- Méthode GetSecurityVersion format Windows Media
- Méthode GetSecurityVersion format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode GetSecurityVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetSecurityVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33be994383a7e16d136aac340a77deef8256d62f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539634"
---
# <a name="iwmdrmsecuritygetsecurityversion-method"></a><span data-ttu-id="96726-106">IWMDRMSecurity :: GetSecurityVersion, méthode</span><span class="sxs-lookup"><span data-stu-id="96726-106">IWMDRMSecurity::GetSecurityVersion method</span></span>

<span data-ttu-id="96726-107">La méthode **GetSecurityVersion** récupère la version du sous-système DRM sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="96726-107">The **GetSecurityVersion** method retrieves the version of the DRM subsystem on the client computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="96726-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96726-108">Syntax</span></span>


```C++
HRESULT GetSecurityVersion(
  [out] BSTR *pbstrVersion
);
```



## <a name="parameters"></a><span data-ttu-id="96726-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96726-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96726-110">*pbstrVersion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="96726-110">*pbstrVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96726-111">Adresse d’une variable qui reçoit le numéro de version du sous-système DRM.</span><span class="sxs-lookup"><span data-stu-id="96726-111">Address of a variable that receives the DRM subsystem version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96726-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="96726-112">Return value</span></span>

<span data-ttu-id="96726-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="96726-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="96726-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="96726-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="96726-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="96726-115">Return code</span></span>                                                                          | <span data-ttu-id="96726-116">Description</span><span class="sxs-lookup"><span data-stu-id="96726-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="96726-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="96726-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="96726-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="96726-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="96726-119">Notes</span><span class="sxs-lookup"><span data-stu-id="96726-119">Remarks</span></span>

<span data-ttu-id="96726-120">Le numéro de version est exprimé sous la forme d’une chaîne composée de quatre nombres séparés par des points.</span><span class="sxs-lookup"><span data-stu-id="96726-120">The version number is expressed as a string consisting of four numbers separated by periods.</span></span> <span data-ttu-id="96726-121">Le premier numéro est le numéro de version principale, qui est généralement défini sur 2.</span><span class="sxs-lookup"><span data-stu-id="96726-121">The first number is the major version number, which is usually set to 2.</span></span> <span data-ttu-id="96726-122">Le deuxième nombre est le numéro de version secondaire, compris entre 2 et 10.</span><span class="sxs-lookup"><span data-stu-id="96726-122">The second number is the minor version number, ranging from 2 to 10.</span></span> <span data-ttu-id="96726-123">Le troisième nombre a toujours la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="96726-123">The third number is always set to 0.</span></span> <span data-ttu-id="96726-124">Le quatrième nombre a la valeur 0 ou 1, et est une valeur booléenne indiquant si le sous-système a été individualisé.</span><span class="sxs-lookup"><span data-stu-id="96726-124">The fourth number is set to 0 or 1, and is a Boolean value indicating whether the subsystem has been individualized.</span></span> <span data-ttu-id="96726-125">Par exemple, le numéro de version « 2.4.0.1 » indique la quatrième version mineure de la deuxième version principale.</span><span class="sxs-lookup"><span data-stu-id="96726-125">For example, a version number of "2.4.0.1" indicates the individualized fourth minor version of the second major version.</span></span>

## <a name="requirements"></a><span data-ttu-id="96726-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96726-126">Requirements</span></span>



| <span data-ttu-id="96726-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96726-127">Requirement</span></span> | <span data-ttu-id="96726-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="96726-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96726-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="96726-129">Header</span></span><br/>  | <dl> <span data-ttu-id="96726-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="96726-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="96726-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="96726-131">Library</span></span><br/> | <dl> <span data-ttu-id="96726-132"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96726-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96726-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96726-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96726-134">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="96726-134">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





