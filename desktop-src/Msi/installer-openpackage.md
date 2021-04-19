---
description: La méthode OpenPackage de l’objet installer ouvre un package d’installation à utiliser avec les fonctions qui accèdent à la base de données du produit et au moteur d’installation, en retournant un objet de session.
ms.assetid: 22b03bde-29ae-4dd4-a41c-d55b3a4f424c
title: Installer. OpenPackage, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenPackage
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 621fac51155b2ac89eba40d39da6d5af6c305e67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523478"
---
# <a name="installeropenpackage-method"></a><span data-ttu-id="61e93-103">Installer. OpenPackage, méthode</span><span class="sxs-lookup"><span data-stu-id="61e93-103">Installer.OpenPackage method</span></span>

<span data-ttu-id="61e93-104">La méthode **OpenPackage** de l’objet [**installer**](installer-object.md) ouvre un package d’installation à utiliser avec les fonctions qui accèdent à la base de données du produit et au moteur d’installation, en retournant un objet de [**session**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="61e93-104">The **OpenPackage** method of the [**Installer**](installer-object.md) object opens an installer package for use with functions that access the product database and install engine, returning an [**Session**](session-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="61e93-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61e93-105">Syntax</span></span>


```JScript
Installer.OpenPackage(
  packagePath,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="61e93-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61e93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61e93-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="61e93-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="61e93-108">Chaîne obligatoire contenant le nom du chemin d’accès du package.</span><span class="sxs-lookup"><span data-stu-id="61e93-108">Required string containing the path name of the package.</span></span>

</dd> <dt>

<span data-ttu-id="61e93-109">*options*</span><span class="sxs-lookup"><span data-stu-id="61e93-109">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="61e93-110">Valeur entière facultative qui spécifie si **OpenPackage** doit ignorer l’état actuel de l’ordinateur lors de la création de l’objet de session.</span><span class="sxs-lookup"><span data-stu-id="61e93-110">An optional integer value that specifies whether or not **OpenPackage** should ignore the current computer state when creating the Session object.</span></span> <span data-ttu-id="61e93-111">Aucune valeur ou valeur de 0 pour les options par défaut est le comportement d’origine.</span><span class="sxs-lookup"><span data-stu-id="61e93-111">No value or a value of 0 for options defaults to the original behavior.</span></span> <span data-ttu-id="61e93-112">Lorsque l’option Options est 1, la méthode **OpenPackage** ignore l’état actuel de l’ordinateur lors de l’ouverture du package.</span><span class="sxs-lookup"><span data-stu-id="61e93-112">When options is 1, the **OpenPackage** Method ignores the current computer state when opening the package.</span></span> <span data-ttu-id="61e93-113">La valeur 1 empêche toute modification de l’état actuel de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="61e93-113">A value of 1 prevents changes to the current computer state.</span></span> <span data-ttu-id="61e93-114">Pour plus d’informations, consultez [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span><span class="sxs-lookup"><span data-stu-id="61e93-114">For more information, see [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61e93-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61e93-115">Return value</span></span>

<span data-ttu-id="61e93-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="61e93-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61e93-117">Notes</span><span class="sxs-lookup"><span data-stu-id="61e93-117">Remarks</span></span>

<span data-ttu-id="61e93-118">La méthode **OpenPackage** peut accepter directement le handle de base de données au lieu de la chaîne pour le chemin d’accès au package.</span><span class="sxs-lookup"><span data-stu-id="61e93-118">The **OpenPackage** method can accept the database handle directly instead of the string for the package path.</span></span>

<span data-ttu-id="61e93-119">Notez qu’un seul objet de [**session**](session-object.md) peut être ouvert par un processus unique.</span><span class="sxs-lookup"><span data-stu-id="61e93-119">Note that only one [**Session**](session-object.md) object can be opened by a single process.</span></span> <span data-ttu-id="61e93-120">**OpenPackage** ne peut pas être utilisé dans une action personnalisée, car l’installation active est la seule session autorisée.</span><span class="sxs-lookup"><span data-stu-id="61e93-120">**OpenPackage** cannot be used in a custom action because the active installation is the only session allowed.</span></span>

<span data-ttu-id="61e93-121">Un objet de [**session**](session-object.md) sécurisé ignore l’état actuel de l’ordinateur lors de l’ouverture du package et empêche toute modification de l’état actuel de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="61e93-121">A safe [**Session**](session-object.md) object ignores the current computer state when opening the package and prevents changes to the current computer state.</span></span> <span data-ttu-id="61e93-122">Pour plus d’informations, consultez [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span><span class="sxs-lookup"><span data-stu-id="61e93-122">For more information, see [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="61e93-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61e93-123">Requirements</span></span>



| <span data-ttu-id="61e93-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61e93-124">Requirement</span></span> | <span data-ttu-id="61e93-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="61e93-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61e93-126">Version</span><span class="sxs-lookup"><span data-stu-id="61e93-126">Version</span></span><br/> | <span data-ttu-id="61e93-127">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="61e93-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="61e93-128">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="61e93-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="61e93-129">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="61e93-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="61e93-130">DLL</span><span class="sxs-lookup"><span data-stu-id="61e93-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="61e93-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61e93-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="61e93-132">IID</span><span class="sxs-lookup"><span data-stu-id="61e93-132">IID</span></span><br/>     | <span data-ttu-id="61e93-133">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="61e93-133">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




