---
description: La définition de la stratégie TransformsSecure sur 1 informe le programme d’installation que les transformations doivent être mises en cache localement sur l’ordinateur de l’utilisateur dans un emplacement où l’utilisateur ne dispose pas d’un accès en écriture.
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: Stratégie TransformsSecure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69180c797008f34755cfa415c7a76fb5f7721f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861902"
---
# <a name="transformssecure-policy"></a><span data-ttu-id="55475-103">Stratégie TransformsSecure</span><span class="sxs-lookup"><span data-stu-id="55475-103">TransformsSecure Policy</span></span>

<span data-ttu-id="55475-104">La définition de la stratégie TransformsSecure sur 1 informe le programme d’installation que les transformations doivent être mises en cache localement sur l’ordinateur de l’utilisateur dans un emplacement où l’utilisateur ne dispose pas d’un accès en écriture.</span><span class="sxs-lookup"><span data-stu-id="55475-104">Setting the TransformsSecure policy to 1 informs the installer that transforms are to be cached locally on the user's computer in a location where the user does not have write access.</span></span> <span data-ttu-id="55475-105">La définition de cette stratégie est identique à la définition de la [propriété TRANSFORMSSECURE](transformssecure.md) , sauf que l’étendue est différente.</span><span class="sxs-lookup"><span data-stu-id="55475-105">Setting this policy is the same as setting the [TRANSFORMSSECURE property](transformssecure.md) except the scope is different.</span></span> <span data-ttu-id="55475-106">La définition de la stratégie TransformsSecure s’applique à tous les packages installés sur un ordinateur donné.</span><span class="sxs-lookup"><span data-stu-id="55475-106">Setting TransformsSecure policy applies to all packages installed to a given computer.</span></span> <span data-ttu-id="55475-107">La définition de la propriété TRANSFORMSSECURE s’applique au package, quel que soit l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="55475-107">Setting the TRANSFORMSSECURE property applies to the package regardless of the computer.</span></span>

<span data-ttu-id="55475-108">L’objectif de cette stratégie est de fournir un stockage de transformation sécurisé avec les utilisateurs itinérants de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="55475-108">The purpose of this policy is to provide for secure transform storage with traveling users of Windows 2000.</span></span> <span data-ttu-id="55475-109">À partir de Windows Server 2003, la valeur par défaut de cette stratégie est 1.</span><span class="sxs-lookup"><span data-stu-id="55475-109">Beginning with Windows Server 2003, the default value of this policy is 1.</span></span>

<span data-ttu-id="55475-110">Lorsque cette stratégie est définie, une [installation de maintenance](maintenance-installation.md) peut uniquement utiliser la transformation à partir du cache sécurisé.</span><span class="sxs-lookup"><span data-stu-id="55475-110">When this policy is set, a [maintenance installation](maintenance-installation.md) can only use the transform from the secured cache.</span></span> <span data-ttu-id="55475-111">Dans le cas où le programme d’installation détecte que la transformation est manquante sur l’ordinateur local, le programme d’installation tente de restaurer la transformation.</span><span class="sxs-lookup"><span data-stu-id="55475-111">In the event that the installer finds that the transform is missing on the local computer, the installer attempts to restore the transform.</span></span> <span data-ttu-id="55475-112">Pour que le programme d’installation puisse restaurer la transformation, la transformation sécurisée doit résider sur une source autorisée dans la liste source du package d’installation.</span><span class="sxs-lookup"><span data-stu-id="55475-112">In order for the installer to restore the transform, the secure transform must reside at an authorized source in the installation package's source list.</span></span> <span data-ttu-id="55475-113">Pour plus d’informations, consultez [résilience source](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="55475-113">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="55475-114">L’installation de la maintenance échoue si la transformation n’est pas disponible ou ne peut pas être chargée.</span><span class="sxs-lookup"><span data-stu-id="55475-114">The maintenance installation fails if the transform is unavailable or cannot be loaded.</span></span>

<span data-ttu-id="55475-115">Sur Windows Server 2003, si cette stratégie n’est pas définie, le comportement par défaut consiste à stocker les transformations dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="55475-115">On Windows Server 2003, if this policy is not set, the default behavior is to store the transforms in a secure location.</span></span> <span data-ttu-id="55475-116">Sur toutes les versions antérieures à Windows Server 2003, si la stratégie n’est pas définie, le comportement par défaut consiste à stocker les transformations dans le profil utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="55475-116">On all versions prior to Windows Server 2003, if the policy is not set, the default behavior is to store the transforms in the users profile.</span></span>

<span data-ttu-id="55475-117">Pour plus d’informations, consultez également la section [transformations sécurisées](secured-transforms.md) .</span><span class="sxs-lookup"><span data-stu-id="55475-117">See also [Secured Transforms](secured-transforms.md) for more information.</span></span>

<span data-ttu-id="55475-118">Windows Installer interprète la [stratégie TransformsAtSource](transformsatsource-policy.md) comme étant identique à la stratégie TransformsSecure.</span><span class="sxs-lookup"><span data-stu-id="55475-118">Windows Installer interprets the [TransformsAtSource policy](transformsatsource-policy.md) to be the same as the TransformsSecure policy.</span></span>

## <a name="registry-key"></a><span data-ttu-id="55475-119">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="55475-119">Registry Key</span></span>

<span data-ttu-id="55475-120">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="55475-120">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="55475-121">Type de données</span><span class="sxs-lookup"><span data-stu-id="55475-121">Data Type</span></span>

<span data-ttu-id="55475-122">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="55475-122">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="55475-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55475-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55475-124">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="55475-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



