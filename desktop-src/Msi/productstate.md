---
description: Le programme d’installation définit la propriété ProductState sur l’état d’installation du produit lors de l’initialisation.
ms.assetid: 833e9a15-10f8-4b1c-945f-bc02b506f627
title: Propriété ProductState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51ea88058aa8bae6b67acaea96b506a7560c7a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541793"
---
# <a name="productstate-property"></a><span data-ttu-id="4df0e-103">Propriété ProductState</span><span class="sxs-lookup"><span data-stu-id="4df0e-103">ProductState property</span></span>

<span data-ttu-id="4df0e-104">Le programme d’installation définit la propriété **ProductState** sur l’état d’installation du produit lors de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="4df0e-104">The installer sets the **ProductState** property to the installation state for the product at initialization.</span></span> <span data-ttu-id="4df0e-105">Cette propriété est définie sur l’un des types de données INSTALLSTATE suivants retournés par [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).</span><span class="sxs-lookup"><span data-stu-id="4df0e-105">This property is set to one of the following INSTALLSTATE data types returned by [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).</span></span>



| <span data-ttu-id="4df0e-106">INSTALLSTATE</span><span class="sxs-lookup"><span data-stu-id="4df0e-106">INSTALLSTATE</span></span>             | <span data-ttu-id="4df0e-107">Valeur numérique</span><span class="sxs-lookup"><span data-stu-id="4df0e-107">Numeric value</span></span> | <span data-ttu-id="4df0e-108">État d’installation du produit</span><span class="sxs-lookup"><span data-stu-id="4df0e-108">Installation state of product</span></span>                   |
|--------------------------|---------------|-------------------------------------------------|
| <span data-ttu-id="4df0e-109">INSTALLSTATE \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="4df0e-109">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="4df0e-110">-1</span><span class="sxs-lookup"><span data-stu-id="4df0e-110">-1</span></span>            | <span data-ttu-id="4df0e-111">Le produit n’est ni publié ni installé.</span><span class="sxs-lookup"><span data-stu-id="4df0e-111">The product is neither advertised or installed.</span></span> |
| <span data-ttu-id="4df0e-112">INSTALLSTATE \_ publié</span><span class="sxs-lookup"><span data-stu-id="4df0e-112">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="4df0e-113">1</span><span class="sxs-lookup"><span data-stu-id="4df0e-113">1</span></span>             | <span data-ttu-id="4df0e-114">Le produit est publié, mais n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="4df0e-114">The product is advertised but not installed.</span></span>    |
| <span data-ttu-id="4df0e-115">INSTALLSTATE \_ absent</span><span class="sxs-lookup"><span data-stu-id="4df0e-115">INSTALLSTATE\_ABSENT</span></span>     | <span data-ttu-id="4df0e-116">2</span><span class="sxs-lookup"><span data-stu-id="4df0e-116">2</span></span>             | <span data-ttu-id="4df0e-117">Le produit est installé pour un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4df0e-117">The product is installed for a different user.</span></span>  |
| <span data-ttu-id="4df0e-118">INSTALLSTATE \_ par défaut</span><span class="sxs-lookup"><span data-stu-id="4df0e-118">INSTALLSTATE\_DEFAULT</span></span>    | <span data-ttu-id="4df0e-119">5</span><span class="sxs-lookup"><span data-stu-id="4df0e-119">5</span></span>             | <span data-ttu-id="4df0e-120">Le produit est installé pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="4df0e-120">The product is installed for the current user.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="4df0e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4df0e-121">Requirements</span></span>



| <span data-ttu-id="4df0e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4df0e-122">Requirement</span></span> | <span data-ttu-id="4df0e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4df0e-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4df0e-124">Version</span><span class="sxs-lookup"><span data-stu-id="4df0e-124">Version</span></span><br/> | <span data-ttu-id="4df0e-125">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4df0e-125">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4df0e-126">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4df0e-126">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4df0e-127">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4df0e-127">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="4df0e-128">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="4df0e-128">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4df0e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4df0e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df0e-130">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4df0e-130">Properties</span></span>](properties.md)
</dt> </dl>

 

 




