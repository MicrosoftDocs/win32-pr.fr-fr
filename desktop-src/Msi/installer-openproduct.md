---
description: La méthode OpenProduct de l’objet installer ouvre un package d’installation pour un produit installé à l’aide du code de produit et retourne un objet de session.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Installer. OpenProduct, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9fd25a1f204a6d42cd4cb6e330d7d69da2cddb07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526430"
---
# <a name="installeropenproduct-method"></a><span data-ttu-id="a89e0-103">Installer. OpenProduct, méthode</span><span class="sxs-lookup"><span data-stu-id="a89e0-103">Installer.OpenProduct method</span></span>

<span data-ttu-id="a89e0-104">La méthode **OpenProduct** de l’objet [**installer**](installer-object.md) ouvre un package d’installation pour un produit installé à l’aide du code de produit et retourne un objet de [**session**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="a89e0-104">The **OpenProduct** method of the [**Installer**](installer-object.md) object opens an installer package for an installed product using the product code and returns a [**Session**](session-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a89e0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a89e0-105">Syntax</span></span>


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a><span data-ttu-id="a89e0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a89e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a89e0-107">*productCode*</span><span class="sxs-lookup"><span data-stu-id="a89e0-107">*productCode*</span></span> 
</dt> <dd>

<span data-ttu-id="a89e0-108">Chaîne obligatoire contenant le code de produit unique ( [GUID](guid.md)) ou un descripteur d’activation écrit par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="a89e0-108">Required string containing the unique product code (a [GUID](guid.md)) or an activation descriptor written by the installer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a89e0-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a89e0-109">Return value</span></span>

<span data-ttu-id="a89e0-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a89e0-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a89e0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a89e0-111">Remarks</span></span>

<span data-ttu-id="a89e0-112">Notez qu’un seul objet de [**session**](session-object.md) peut être ouvert par un processus unique.</span><span class="sxs-lookup"><span data-stu-id="a89e0-112">Note that only one [**Session**](session-object.md) object can be opened by a single process.</span></span> <span data-ttu-id="a89e0-113">**OpenProduct** ne peut pas être utilisé dans une action personnalisée, car l’installation active est la seule session autorisée.</span><span class="sxs-lookup"><span data-stu-id="a89e0-113">**OpenProduct** cannot be used in a custom action because the active installation is the only session allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a89e0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a89e0-114">Requirements</span></span>



| <span data-ttu-id="a89e0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a89e0-115">Requirement</span></span> | <span data-ttu-id="a89e0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a89e0-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a89e0-117">Version</span><span class="sxs-lookup"><span data-stu-id="a89e0-117">Version</span></span><br/> | <span data-ttu-id="a89e0-118">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a89e0-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a89e0-119">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a89e0-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a89e0-120">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="a89e0-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a89e0-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a89e0-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="a89e0-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a89e0-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a89e0-123">IID</span><span class="sxs-lookup"><span data-stu-id="a89e0-123">IID</span></span><br/>     | <span data-ttu-id="a89e0-124">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a89e0-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




