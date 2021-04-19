---
description: La méthode AddSource de l’objet installer ajoute une source à la liste des sources réseau valides dans la liste de ressources réseau.
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: Installer. AddSource, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3067ae287311c6ed26b509545523db75a3fed4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541115"
---
# <a name="installeraddsource-method"></a><span data-ttu-id="f1dc3-103">Installer. AddSource, méthode</span><span class="sxs-lookup"><span data-stu-id="f1dc3-103">Installer.AddSource method</span></span>

<span data-ttu-id="f1dc3-104">La méthode **addsource** de l’objet [**installer**](installer-object.md) ajoute une source à la liste des sources réseau valides dans la liste de ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-104">The **AddSource** method of the [**Installer**](installer-object.md) object adds a source to the list of valid network sources in the sourcelist.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1dc3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1dc3-105">Syntax</span></span>


```JScript
Installer.AddSource(
  Product,
  User,
  Source
)
```



## <a name="parameters"></a><span data-ttu-id="f1dc3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1dc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1dc3-107">*Produit*</span><span class="sxs-lookup"><span data-stu-id="f1dc3-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="f1dc3-108">Spécifie le code du produit.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="f1dc3-109">*Utilisateur*</span><span class="sxs-lookup"><span data-stu-id="f1dc3-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="f1dc3-110">Nom d’utilisateur pour l’installation par utilisateur ; chaîne null ou vide pour une installation par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> <dt>

<span data-ttu-id="f1dc3-111">*Source*</span><span class="sxs-lookup"><span data-stu-id="f1dc3-111">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="f1dc3-112">Pointeur vers la chaîne spécifiant la source.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-112">Pointer to the string specifying the source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1dc3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f1dc3-113">Return value</span></span>

<span data-ttu-id="f1dc3-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1dc3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1dc3-115">Requirements</span></span>



| <span data-ttu-id="f1dc3-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1dc3-116">Requirement</span></span> | <span data-ttu-id="f1dc3-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1dc3-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1dc3-118">Version</span><span class="sxs-lookup"><span data-stu-id="f1dc3-118">Version</span></span><br/> | <span data-ttu-id="f1dc3-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f1dc3-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f1dc3-121">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1dc3-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f1dc3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f1dc3-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="f1dc3-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1dc3-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f1dc3-124">IID</span><span class="sxs-lookup"><span data-stu-id="f1dc3-124">IID</span></span><br/>     | <span data-ttu-id="f1dc3-125">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f1dc3-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="f1dc3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1dc3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1dc3-127">**MsiSourceListAddSource**</span><span class="sxs-lookup"><span data-stu-id="f1dc3-127">**MsiSourceListAddSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[<span data-ttu-id="f1dc3-128">résilience source</span><span class="sxs-lookup"><span data-stu-id="f1dc3-128">source resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




