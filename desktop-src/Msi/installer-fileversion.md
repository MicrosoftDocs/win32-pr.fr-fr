---
description: La méthode FileVersion de l’objet installer retourne la chaîne de version ou la chaîne de langue du chemin d’accès spécifié dans le chemin d’accès à l’aide du format dans lequel le programme d’installation s’attend à les trouver dans la base de données.
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Installer. FileVersion, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileVersion
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a36a92b42815a1b2df913ba6bd9f687cdd1b609b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540161"
---
# <a name="installerfileversion-method"></a><span data-ttu-id="dd67b-103">Installer. FileVersion, méthode</span><span class="sxs-lookup"><span data-stu-id="dd67b-103">Installer.FileVersion method</span></span>

<span data-ttu-id="dd67b-104">La méthode **FileVersion** de l’objet [**installer**](installer-object.md) retourne la chaîne de version ou la chaîne de langue du chemin d’accès spécifié dans le *chemin d’accès* à l’aide du format dans lequel le programme d’installation s’attend à les trouver dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="dd67b-104">The **FileVersion** method of the [**Installer**](installer-object.md) object returns the version string or language string of the path specified in *Path* using the format in which the installer expects to find them in the database.</span></span> <span data-ttu-id="dd67b-105">Pour les versions, il s’agit d’une chaîne au \# format « . \# . \# . \# ».</span><span class="sxs-lookup"><span data-stu-id="dd67b-105">For versions, this is a string in "\#.\#.\#.\#" format.</span></span> <span data-ttu-id="dd67b-106">Pour la langue, il s’agit de l’ID de langue décimale.</span><span class="sxs-lookup"><span data-stu-id="dd67b-106">For language, this is the decimal language ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd67b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd67b-107">Syntax</span></span>


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a><span data-ttu-id="dd67b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd67b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd67b-109">*Chemin d’accès*</span><span class="sxs-lookup"><span data-stu-id="dd67b-109">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="dd67b-110">Chaîne obligatoire contenant le chemin d’accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="dd67b-110">Required string containing the path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="dd67b-111">*Langage*</span><span class="sxs-lookup"><span data-stu-id="dd67b-111">*Language*</span></span> 
</dt> <dd>

<span data-ttu-id="dd67b-112">Indicateur de désignation indiquant si la valeur retournée est un ID de langue ou une chaîne de version.</span><span class="sxs-lookup"><span data-stu-id="dd67b-112">Flag for designating whether the returned value is a language ID or version string.</span></span> <span data-ttu-id="dd67b-113">TRUE retourne la langue, FALSe retourne la version.</span><span class="sxs-lookup"><span data-stu-id="dd67b-113">TRUE returns the language, FALSE returns the version.</span></span> <span data-ttu-id="dd67b-114">Ce paramètre est facultatif, avec FALSe comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="dd67b-114">This parameter is optional, with a default value of FALSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd67b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd67b-115">Return value</span></span>

<span data-ttu-id="dd67b-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="dd67b-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd67b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd67b-117">Requirements</span></span>



| <span data-ttu-id="dd67b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd67b-118">Requirement</span></span> | <span data-ttu-id="dd67b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd67b-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd67b-120">Version</span><span class="sxs-lookup"><span data-stu-id="dd67b-120">Version</span></span><br/> | <span data-ttu-id="dd67b-121">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dd67b-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dd67b-122">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dd67b-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dd67b-123">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="dd67b-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="dd67b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="dd67b-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="dd67b-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd67b-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="dd67b-126">IID</span><span class="sxs-lookup"><span data-stu-id="dd67b-126">IID</span></span><br/>     | <span data-ttu-id="dd67b-127">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="dd67b-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




