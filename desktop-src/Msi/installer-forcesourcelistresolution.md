---
description: La méthode ForceSourceListResolution de l’objet installer force l’Windows Installer à rechercher dans la liste source une source de produit valide.
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: Installer. ForceSourceListResolution, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ForceSourceListResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cadc27f3eaa90cd6fb2729f73d07cbcfa1f96b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539548"
---
# <a name="installerforcesourcelistresolution-method"></a><span data-ttu-id="dbebc-103">Installer. ForceSourceListResolution, méthode</span><span class="sxs-lookup"><span data-stu-id="dbebc-103">Installer.ForceSourceListResolution method</span></span>

<span data-ttu-id="dbebc-104">La méthode **ForceSourceListResolution** de l’objet [**installer**](installer-object.md) oblige le programme d’installation à rechercher dans la liste source une source de produit valide la prochaine fois qu’une source est nécessaire, par exemple quand le programme d’installation effectue une installation ou une réinstallation, ou lorsqu’il a besoin du chemin d’accès d’un jeu de composants à exécuter à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="dbebc-104">The **ForceSourceListResolution** method of the [**Installer**](installer-object.md) object forces the installer to search the source list for a valid product source the next time a source is needed, such as when the installer performs an installation or a reinstallation, or when it needs the path for a component set to run from source.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbebc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbebc-105">Syntax</span></span>


```JScript
Installer.ForceSourceListResolution(
  Product,
  User
)
```



## <a name="parameters"></a><span data-ttu-id="dbebc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbebc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbebc-107">*Produit*</span><span class="sxs-lookup"><span data-stu-id="dbebc-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="dbebc-108">Spécifie le code du produit.</span><span class="sxs-lookup"><span data-stu-id="dbebc-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="dbebc-109">*Utilisateur*</span><span class="sxs-lookup"><span data-stu-id="dbebc-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="dbebc-110">Nom d’utilisateur pour l’installation par utilisateur ; chaîne null ou vide pour une installation par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dbebc-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbebc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dbebc-111">Return value</span></span>

<span data-ttu-id="dbebc-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="dbebc-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbebc-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbebc-113">Requirements</span></span>



| <span data-ttu-id="dbebc-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbebc-114">Requirement</span></span> | <span data-ttu-id="dbebc-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbebc-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbebc-116">Version</span><span class="sxs-lookup"><span data-stu-id="dbebc-116">Version</span></span><br/> | <span data-ttu-id="dbebc-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dbebc-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dbebc-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dbebc-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dbebc-119">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="dbebc-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="dbebc-120">DLL</span><span class="sxs-lookup"><span data-stu-id="dbebc-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="dbebc-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbebc-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="dbebc-122">IID</span><span class="sxs-lookup"><span data-stu-id="dbebc-122">IID</span></span><br/>     | <span data-ttu-id="dbebc-123">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="dbebc-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="dbebc-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbebc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbebc-125">**MsiSourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="dbebc-125">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="dbebc-126">Résilience source</span><span class="sxs-lookup"><span data-stu-id="dbebc-126">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




