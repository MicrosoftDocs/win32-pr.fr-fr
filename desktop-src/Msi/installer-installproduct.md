---
description: La méthode InstallProduct de l’objet installer ouvre un package d’installation et Initialise une session d’installation.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Installer. InstallProduct, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.InstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 08bab1081aae186b40494cff777163679847b44b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535240"
---
# <a name="installerinstallproduct-method"></a><span data-ttu-id="d1344-103">Installer. InstallProduct, méthode</span><span class="sxs-lookup"><span data-stu-id="d1344-103">Installer.InstallProduct method</span></span>

<span data-ttu-id="d1344-104">La méthode **InstallProduct** de l’objet [**installer**](installer-object.md) ouvre un package d’installation et Initialise une session d’installation.</span><span class="sxs-lookup"><span data-stu-id="d1344-104">The **InstallProduct** method of the [**Installer**](installer-object.md) object opens an installer package and initializes an install session.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1344-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1344-105">Syntax</span></span>


```JScript
Installer.InstallProduct(
  packagePath,
  propertyValues
)
```



## <a name="parameters"></a><span data-ttu-id="d1344-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1344-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1344-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="d1344-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="d1344-108">Chaîne obligatoire contenant le chemin d’accès au package d’installation.</span><span class="sxs-lookup"><span data-stu-id="d1344-108">Required string containing the path to the install package.</span></span>

</dd> <dt>

<span data-ttu-id="d1344-109">*propertyValues*</span><span class="sxs-lookup"><span data-stu-id="d1344-109">*propertyValues*</span></span> 
</dt> <dd>

<span data-ttu-id="d1344-110">Chaîne facultative contenant les paires propriété = valeur séparées par un espace blanc.</span><span class="sxs-lookup"><span data-stu-id="d1344-110">Optional string containing property=value pairs separated by white space.</span></span>

<span data-ttu-id="d1344-111">Pour effectuer une installation administrative, incluez ACTION = ADMIN dans *propertyValues*.</span><span class="sxs-lookup"><span data-stu-id="d1344-111">To perform an administrative installation, include ACTION=ADMIN in *propertyValues*.</span></span> <span data-ttu-id="d1344-112">Pour plus d’informations, consultez la propriété [**action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="d1344-112">For more information, see the [**ACTION**](action.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1344-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1344-113">Return value</span></span>

<span data-ttu-id="d1344-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d1344-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1344-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d1344-115">Remarks</span></span>

<span data-ttu-id="d1344-116">Pour supprimer complètement un produit, définissez REMOVE = ALL dans *propertyValues*.</span><span class="sxs-lookup"><span data-stu-id="d1344-116">To completely remove a product, set REMOVE=ALL in *propertyValues*.</span></span> <span data-ttu-id="d1344-117">Pour plus d’informations, consultez [**Remove**](remove.md) Property.</span><span class="sxs-lookup"><span data-stu-id="d1344-117">For more information, see [**REMOVE**](remove.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1344-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1344-118">Requirements</span></span>



| <span data-ttu-id="d1344-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1344-119">Requirement</span></span> | <span data-ttu-id="d1344-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1344-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1344-121">Version</span><span class="sxs-lookup"><span data-stu-id="d1344-121">Version</span></span><br/> | <span data-ttu-id="d1344-122">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d1344-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d1344-123">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d1344-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d1344-124">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="d1344-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d1344-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d1344-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="d1344-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1344-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d1344-127">IID</span><span class="sxs-lookup"><span data-stu-id="d1344-127">IID</span></span><br/>     | <span data-ttu-id="d1344-128">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d1344-128">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




