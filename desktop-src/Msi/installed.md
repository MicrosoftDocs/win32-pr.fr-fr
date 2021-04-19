---
description: La propriété installed est définie uniquement si le produit est installé par ordinateur ou pour l’utilisateur actuel.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Propriété installed
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae5126107fff51f3790fb3ab9a9209490b9627a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531004"
---
# <a name="installed-property"></a><span data-ttu-id="9bc47-103">Propriété installed</span><span class="sxs-lookup"><span data-stu-id="9bc47-103">Installed property</span></span>

<span data-ttu-id="9bc47-104">La propriété **installed** est définie uniquement si le produit est installé par ordinateur ou pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="9bc47-104">The **Installed** property is set only if the product is installed per-machine or for the current user.</span></span> <span data-ttu-id="9bc47-105">Cette propriété n’est pas définie si le produit est installé pour un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9bc47-105">This property is not set if the product is installed for a different user.</span></span>

<span data-ttu-id="9bc47-106">La propriété **installed** peut être utilisée dans les expressions conditionnelles pour déterminer si un produit est installé par ordinateur ou pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="9bc47-106">The **Installed** property can be used in conditional expressions to determine whether a product is installed per-computer or for the current user.</span></span> <span data-ttu-id="9bc47-107">Par exemple, la propriété peut être utilisée dans la colonne conditionnelle d’une table de séquences ou pour faire la différence entre une installation initiale et une installation de maintenance.</span><span class="sxs-lookup"><span data-stu-id="9bc47-107">For example, the property can be used in the conditional column of a sequence table or to differentiate between a first installation and a maintenance installation.</span></span>

<span data-ttu-id="9bc47-108">Pour déterminer si le produit est installé pour un autre utilisateur, vérifiez la propriété [**ProductState**](productstate.md) .</span><span class="sxs-lookup"><span data-stu-id="9bc47-108">To determine whether the product is installed for a different user, check the [**ProductState**](productstate.md) property.</span></span>

<span data-ttu-id="9bc47-109">La valeur de la propriété [**ProductVersion**](productversion.md) est la version du produit au format de chaîne.</span><span class="sxs-lookup"><span data-stu-id="9bc47-109">The value of the [**ProductVersion**](productversion.md) property is the version of the product in string format.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bc47-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9bc47-110">Requirements</span></span>



| <span data-ttu-id="9bc47-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9bc47-111">Requirement</span></span> | <span data-ttu-id="9bc47-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bc47-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc47-113">Version</span><span class="sxs-lookup"><span data-stu-id="9bc47-113">Version</span></span><br/> | <span data-ttu-id="9bc47-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9bc47-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9bc47-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9bc47-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9bc47-116">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9bc47-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9bc47-117">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="9bc47-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9bc47-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bc47-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bc47-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9bc47-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




