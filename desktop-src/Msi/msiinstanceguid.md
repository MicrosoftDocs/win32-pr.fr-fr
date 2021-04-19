---
description: La présence de la propriété MSIINSTANCEGUID indique qu’un code produit&\# 8211 ; la modification de la transformation est enregistrée dans le produit.
ms.assetid: c39be15d-e10a-4055-bd81-aa7510a19fe4
title: Propriété MSIINSTANCEGUID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c798d56cf3ede6a75a133dd7e0ec7f42c32e84f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543786"
---
# <a name="msiinstanceguid-property"></a><span data-ttu-id="5435e-103">Propriété MSIINSTANCEGUID</span><span class="sxs-lookup"><span data-stu-id="5435e-103">MSIINSTANCEGUID property</span></span>

<span data-ttu-id="5435e-104">La présence de la propriété **MSIINSTANCEGUID** indique qu’un code de produit-modification de la transformation est enregistré dans le produit.</span><span class="sxs-lookup"><span data-stu-id="5435e-104">The presence of the **MSIINSTANCEGUID** property indicates that a product code–changing transform is registered to the product.</span></span> <span data-ttu-id="5435e-105">La valeur de la propriété **MSIINSTANCEGUID** spécifie l’instance d’un produit à utiliser pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="5435e-105">The value of the **MSIINSTANCEGUID** property specifies which instance of a product is to be used for installation.</span></span> <span data-ttu-id="5435e-106">La propriété **MSIINSTANCEGUID** peut uniquement faire référence à un produit qui a déjà été installé avec une transformation d’instance.</span><span class="sxs-lookup"><span data-stu-id="5435e-106">The **MSIINSTANCEGUID** property can only reference a product that has already been installed with an instance transform.</span></span>

<span data-ttu-id="5435e-107">Les transformations d’instance sont du code de produit : modification des transformations disponibles avec le programme d’installation qui s’exécute sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5435e-107">Instance transforms are product code–changing transforms available with the installer running on either Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5435e-108">Pour plus d’informations, consultez [installation de plusieurs instances de produits et de correctifs](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="5435e-108">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5435e-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5435e-109">Requirements</span></span>



| <span data-ttu-id="5435e-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5435e-110">Requirement</span></span> | <span data-ttu-id="5435e-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="5435e-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5435e-112">Version</span><span class="sxs-lookup"><span data-stu-id="5435e-112">Version</span></span><br/> | <span data-ttu-id="5435e-113">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5435e-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5435e-114">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5435e-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5435e-115">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5435e-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5435e-116">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5435e-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5435e-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5435e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5435e-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5435e-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="5435e-119">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="5435e-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




