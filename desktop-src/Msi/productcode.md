---
description: La propriété ProductCode est un identificateur unique pour la version particulière du produit, représenté sous la forme d’un GUID de chaîne, par exemple &\# 0034 ; {12345678-1234-1234-1234-123456789012}&\# 0034 ;.
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: Propriété ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a714687ab49bca07d1137b3395cb19ddba0944
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541295"
---
# <a name="productcode-property"></a><span data-ttu-id="14866-103">Propriété ProductCode</span><span class="sxs-lookup"><span data-stu-id="14866-103">ProductCode property</span></span>

<span data-ttu-id="14866-104">La propriété **ProductCode** est un identificateur unique pour la version particulière du produit, représenté sous la forme d’un [GUID](guid.md)de chaîne, par exemple « {12345678-1234-1234-1234-123456789012} ».</span><span class="sxs-lookup"><span data-stu-id="14866-104">The **ProductCode** property is a unique identifier for the particular product release, represented as a string [GUID](guid.md), for example "{12345678-1234-1234-1234-123456789012}".</span></span> <span data-ttu-id="14866-105">Les lettres utilisées dans ce GUID doivent être en majuscules.</span><span class="sxs-lookup"><span data-stu-id="14866-105">Letters used in this GUID must be uppercase.</span></span> <span data-ttu-id="14866-106">Cet ID doit varier en fonction des versions et des langues.</span><span class="sxs-lookup"><span data-stu-id="14866-106">This ID must vary for different versions and languages.</span></span>

<span data-ttu-id="14866-107">Une mise à niveau de produit qui met à jour un produit dans un produit entièrement nouveau doit également modifier le code du produit.</span><span class="sxs-lookup"><span data-stu-id="14866-107">A product upgrade that updates a product into an entirely new product must also change the product code.</span></span> <span data-ttu-id="14866-108">Les versions 32 bits et 64 bits du package d’une application doivent se voir assigner des codes de produit différents.</span><span class="sxs-lookup"><span data-stu-id="14866-108">The 32-bit and 64-bit versions of an application's package must be assigned different product codes.</span></span>

<span data-ttu-id="14866-109">Le **ProductCode** est publié en tant que propriété de produit et constitue la principale méthode de spécification du produit.</span><span class="sxs-lookup"><span data-stu-id="14866-109">The **ProductCode** is advertised as a product property, and is the primary method of specifying the product.</span></span> <span data-ttu-id="14866-110">Cette propriété est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="14866-110">This property is REQUIRED.</span></span>

## <a name="requirements"></a><span data-ttu-id="14866-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14866-111">Requirements</span></span>



| <span data-ttu-id="14866-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14866-112">Requirement</span></span> | <span data-ttu-id="14866-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="14866-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14866-114">Version</span><span class="sxs-lookup"><span data-stu-id="14866-114">Version</span></span><br/> | <span data-ttu-id="14866-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="14866-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="14866-116">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="14866-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="14866-117">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="14866-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="14866-118">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="14866-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14866-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14866-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14866-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="14866-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




