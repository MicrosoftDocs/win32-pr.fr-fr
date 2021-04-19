---
description: L’affectation de la valeur 1 à la propriété TRANSFORMSSECURE informe le programme d’installation que les transformations doivent être mises en cache localement sur l’ordinateur de l’utilisateur dans un emplacement où l’utilisateur ne dispose pas d’un accès en écriture.
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: Propriété TRANSFORMSSECURE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b7a30ab5e94fb646e2e8960b60fd97dc35557c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523454"
---
# <a name="transformssecure-property"></a><span data-ttu-id="8aeb7-103">Propriété TRANSFORMSSECURE</span><span class="sxs-lookup"><span data-stu-id="8aeb7-103">TRANSFORMSSECURE property</span></span>

<span data-ttu-id="8aeb7-104">L’affectation de la valeur 1 à la propriété **TRANSFORMSSECURE** informe le programme d’installation que les transformations doivent être mises en cache localement sur l’ordinateur de l’utilisateur dans un emplacement où l’utilisateur ne dispose pas d’un accès en écriture.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-104">Setting the **TRANSFORMSSECURE** property to 1 informs the installer that transforms are to be cached locally on the user's computer in a location where the user does not have write access.</span></span> <span data-ttu-id="8aeb7-105">La définition de cette propriété est semblable à la définition de la [stratégie TransformsSecure](transformssecure-policy.md) , à ceci près que l’étendue est différente.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-105">Setting this property is like setting the [TransformsSecure policy](transformssecure-policy.md) except that the scope is different.</span></span> <span data-ttu-id="8aeb7-106">La définition de la stratégie TransformsSecure s’applique à tous les packages installés par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-106">Setting TransformsSecure policy applies to all packages installed by a given user.</span></span> <span data-ttu-id="8aeb7-107">La définition de la propriété **TRANSFORMSSECURE** s’applique au package, quel que soit l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-107">Setting the **TRANSFORMSSECURE** property applies to the package regardless of the user.</span></span>

<span data-ttu-id="8aeb7-108">L’objectif de cette propriété est de fournir un stockage de transformation sécurisé avec les utilisateurs itinérants de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-108">The purpose of this property is to provide for secure transform storage with traveling users of Windows 2000.</span></span> <span data-ttu-id="8aeb7-109">Lorsque cette propriété est définie, une [installation de maintenance](maintenance-installation.md) peut uniquement utiliser la transformation à partir du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-109">When this property is set, a [maintenance installation](maintenance-installation.md) can only use the transform from the specified path.</span></span> <span data-ttu-id="8aeb7-110">Si le chemin d’accès n’est pas disponible, l’installation de la maintenance échoue.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-110">If the path is not available the maintenance installation fails.</span></span> <span data-ttu-id="8aeb7-111">Une source pour chaque transformation sécurisée doit donc résider à l’emplacement de la source du package d’installation.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-111">A source for each secure transform must therefore reside at the location of the source of the installation package.</span></span> <span data-ttu-id="8aeb7-112">Puis, si le programme d’installation détecte que la transformation est manquante sur l’ordinateur local, il peut restaurer la transformation à partir de cette source.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-112">Then if the installer finds that the transform is missing on the local computer, it can restore the transform from this source.</span></span>

## <a name="remarks"></a><span data-ttu-id="8aeb7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8aeb7-113">Remarks</span></span>

<span data-ttu-id="8aeb7-114">Windows Installer interprète la propriété [**TRANSFORMSATSOURCE**](transformsatsource.md) pour qu’elle soit identique à la propriété **TRANSFORMSSECURE** .</span><span class="sxs-lookup"><span data-stu-id="8aeb7-114">Windows Installer interprets the [**TRANSFORMSATSOURCE**](transformsatsource.md) property to be the same as the **TRANSFORMSSECURE** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aeb7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8aeb7-115">Requirements</span></span>



| <span data-ttu-id="8aeb7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8aeb7-116">Requirement</span></span> | <span data-ttu-id="8aeb7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8aeb7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aeb7-118">Version</span><span class="sxs-lookup"><span data-stu-id="8aeb7-118">Version</span></span><br/> | <span data-ttu-id="8aeb7-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8aeb7-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8aeb7-121">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8aeb7-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8aeb7-122">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="8aeb7-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8aeb7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8aeb7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aeb7-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8aeb7-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="8aeb7-125">Transformations de base de données</span><span class="sxs-lookup"><span data-stu-id="8aeb7-125">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




