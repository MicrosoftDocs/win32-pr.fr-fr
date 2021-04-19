---
description: La méthode ClearSourceList de l’objet installer supprime toutes les sources réseau de la liste source.
ms.assetid: a4e4beb2-a4d7-48e7-9c8d-dd1ae19fe92a
title: Installer. ClearSourceList, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClearSourceList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f9468775c75533b766a160a390410908d04bf6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542536"
---
# <a name="installerclearsourcelist-method"></a><span data-ttu-id="82e3e-103">Installer. ClearSourceList, méthode</span><span class="sxs-lookup"><span data-stu-id="82e3e-103">Installer.ClearSourceList method</span></span>

<span data-ttu-id="82e3e-104">La méthode **ClearSourceList** de l’objet [**installer**](installer-object.md) supprime toutes les sources réseau de la liste source.</span><span class="sxs-lookup"><span data-stu-id="82e3e-104">The **ClearSourceList** method of the [**Installer**](installer-object.md) object removes all network sources from the source list.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e3e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82e3e-105">Syntax</span></span>


```JScript
Installer.ClearSourceList(
  Product,
  User
)
```



## <a name="parameters"></a><span data-ttu-id="82e3e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82e3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82e3e-107">*Produit*</span><span class="sxs-lookup"><span data-stu-id="82e3e-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="82e3e-108">Spécifie le code du produit.</span><span class="sxs-lookup"><span data-stu-id="82e3e-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="82e3e-109">*Utilisateur*</span><span class="sxs-lookup"><span data-stu-id="82e3e-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="82e3e-110">Nom d’utilisateur pour l’installation par utilisateur ; chaîne null ou vide pour une installation par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="82e3e-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82e3e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82e3e-111">Return value</span></span>

<span data-ttu-id="82e3e-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="82e3e-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="82e3e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82e3e-113">Requirements</span></span>



| <span data-ttu-id="82e3e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82e3e-114">Requirement</span></span> | <span data-ttu-id="82e3e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="82e3e-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82e3e-116">Version</span><span class="sxs-lookup"><span data-stu-id="82e3e-116">Version</span></span><br/> | <span data-ttu-id="82e3e-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="82e3e-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="82e3e-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="82e3e-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="82e3e-119">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="82e3e-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="82e3e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="82e3e-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="82e3e-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82e3e-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="82e3e-122">IID</span><span class="sxs-lookup"><span data-stu-id="82e3e-122">IID</span></span><br/>     | <span data-ttu-id="82e3e-123">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="82e3e-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="82e3e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82e3e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e3e-125">**MsiSourceListClearAll**</span><span class="sxs-lookup"><span data-stu-id="82e3e-125">**MsiSourceListClearAll**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)
</dt> <dt>

[<span data-ttu-id="82e3e-126">Résilience source</span><span class="sxs-lookup"><span data-stu-id="82e3e-126">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




