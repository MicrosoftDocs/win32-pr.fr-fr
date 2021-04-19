---
description: Récupère un masque de bits qui identifie les suites de produits disponibles sur le système. Si cette fonction est appelée dans une application qui s’exécute dans le contexte d’un silo de serveurs, le masque de suite du silo de serveurs est récupéré à la place.
ms.assetid: 1D6434FD-D7BD-45F9-B7C3-238890AF9928
title: RtlGetSuiteMask, fonction (Ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetSuiteMask
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ed8d8906273d18125131251636bc6199d166547b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520645"
---
# <a name="rtlgetsuitemask-function"></a><span data-ttu-id="43e9e-104">RtlGetSuiteMask fonction)</span><span class="sxs-lookup"><span data-stu-id="43e9e-104">RtlGetSuiteMask function</span></span>

<span data-ttu-id="43e9e-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="43e9e-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="43e9e-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="43e9e-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="43e9e-107">Récupère un masque de bits qui identifie les suites de produits disponibles sur le système.</span><span class="sxs-lookup"><span data-stu-id="43e9e-107">Retrieves a bit mask that identifies the product suites available on the system.</span></span> <span data-ttu-id="43e9e-108">Si cette fonction est appelée dans une application qui s’exécute dans le contexte d’un silo de serveurs, le masque de suite du silo de serveurs est récupéré à la place.</span><span class="sxs-lookup"><span data-stu-id="43e9e-108">If this function is called in an application that runs in the context of a server silo, the suite mask for the server silo is retrieved instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="43e9e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43e9e-109">Syntax</span></span>


```C++
ULONG NTAPI RtlGetSuiteMask(void);
```



## <a name="parameters"></a><span data-ttu-id="43e9e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43e9e-110">Parameters</span></span>

<span data-ttu-id="43e9e-111">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="43e9e-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43e9e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43e9e-112">Return value</span></span>

<span data-ttu-id="43e9e-113">Masque de bits qui identifie les suites de produits disponibles sur le système.</span><span class="sxs-lookup"><span data-stu-id="43e9e-113">A bit mask that identifies the product suites available on the system.</span></span> <span data-ttu-id="43e9e-114">Le masque de bits peut inclure les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="43e9e-114">The bit mask can include the following values.</span></span>



| <span data-ttu-id="43e9e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43e9e-115">Return value</span></span>                                                                          | <span data-ttu-id="43e9e-116">Description</span><span class="sxs-lookup"><span data-stu-id="43e9e-116">Description</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43e9e-117"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-117"><dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="43e9e-118">Microsoft Small Business Server a été installé sur le système, mais il a peut-être été mis à niveau vers une autre version de Windows.</span><span class="sxs-lookup"><span data-stu-id="43e9e-118">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span> <span data-ttu-id="43e9e-119">Reportez-vous à la section Remarques pour plus d’informations sur cet indicateur de bit.</span><span class="sxs-lookup"><span data-stu-id="43e9e-119">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                           |
| <dl> <span data-ttu-id="43e9e-120"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-120"><dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="43e9e-121">Windows 10 entreprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition ou Windows 2000 Advanced Server est installé.</span><span class="sxs-lookup"><span data-stu-id="43e9e-121">Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="43e9e-122">Reportez-vous à la section Remarques pour plus d’informations sur cet indicateur de bit.</span><span class="sxs-lookup"><span data-stu-id="43e9e-122">Refer to the Remarks section for more information about this bit flag.</span></span><br/> |
| <dl> <span data-ttu-id="43e9e-123"><dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-123"><dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="43e9e-124">Les composants Microsoft BackOffice sont installés.</span><span class="sxs-lookup"><span data-stu-id="43e9e-124">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="43e9e-125"><dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-125"><dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="43e9e-126">Communications Server 2003, Communications Server 2005, Communications Server 2007 ou Communications Server 2007 R2 sont installés.</span><span class="sxs-lookup"><span data-stu-id="43e9e-126">Communications Server 2003, Communications Server 2005, Communications Server 2007, or Communications Server 2007 R2 is installed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="43e9e-127"><dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-127"><dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="43e9e-128">Les services Terminal Server sont installés.</span><span class="sxs-lookup"><span data-stu-id="43e9e-128">Terminal Services is installed.</span></span> <span data-ttu-id="43e9e-129">Cette valeur est toujours définie.</span><span class="sxs-lookup"><span data-stu-id="43e9e-129">This value is always set.</span></span><br/> <span data-ttu-id="43e9e-130">Si **TerminalServer** est défini mais que **SingleUserTS** n’est pas défini, le système s’exécute en mode serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="43e9e-130">If **TerminalServer** is set but **SingleUserTS** is not set, the system is running in application server mode.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="43e9e-131"><dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-131"><dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="43e9e-132">Microsoft Small Business Server est installé avec la licence client restrictive en vigueur.</span><span class="sxs-lookup"><span data-stu-id="43e9e-132">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="43e9e-133">Reportez-vous à la section Remarques pour plus d’informations sur cet indicateur de bit.</span><span class="sxs-lookup"><span data-stu-id="43e9e-133">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                                                            |
| <dl> <span data-ttu-id="43e9e-134"><dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-134"><dt>0x00000040</dt></span></span> </dl> | <span data-ttu-id="43e9e-135">Windows XP Embedded est installé.</span><span class="sxs-lookup"><span data-stu-id="43e9e-135">Windows XP Embedded is installed.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="43e9e-136"><dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-136"><dt>0x00000080</dt></span></span> </dl> | <span data-ttu-id="43e9e-137">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition ou Windows 2000 Datacenter Server est installé.</span><span class="sxs-lookup"><span data-stu-id="43e9e-137">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/>                                                                                                                     |
| <dl> <span data-ttu-id="43e9e-138"><dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-138"><dt>0x00000100</dt></span></span> </dl> | <span data-ttu-id="43e9e-139">Bureau à distance est pris en charge, mais une seule session interactive est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="43e9e-139">Remote Desktop is supported, but only one interactive session is supported.</span></span> <span data-ttu-id="43e9e-140">Cette valeur est définie, sauf si le système s’exécute en mode serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="43e9e-140">This value is set unless the system is running in application server mode.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="43e9e-141"><dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-141"><dt>0x00000200</dt></span></span> </dl> | <span data-ttu-id="43e9e-142">Windows Vista Édition familiale Premium, Windows Vista Édition familiale basique ou Windows XP Édition familiale est installé.</span><span class="sxs-lookup"><span data-stu-id="43e9e-142">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="43e9e-143"><dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-143"><dt>0x00000400</dt></span></span> </dl> | <span data-ttu-id="43e9e-144">Windows Server 2003, Web Edition est installé.</span><span class="sxs-lookup"><span data-stu-id="43e9e-144">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="43e9e-145"><dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-145"><dt>0x00002000</dt></span></span> </dl> | <span data-ttu-id="43e9e-146">Windows Storage Server 2003 R2 ou Windows Storage Server 2003 est installé.</span><span class="sxs-lookup"><span data-stu-id="43e9e-146">Windows Storage Server 2003 R2 or Windows Storage Server 2003 is installed.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="43e9e-147"><dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-147"><dt>0x00004000</dt></span></span> </dl> | <span data-ttu-id="43e9e-148">Windows Server 2003, Compute Cluster Edition est installé.</span><span class="sxs-lookup"><span data-stu-id="43e9e-148">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="43e9e-149"><dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-149"><dt>0x00008000</dt></span></span> </dl> | <span data-ttu-id="43e9e-150">Windows Server famille est installé.</span><span class="sxs-lookup"><span data-stu-id="43e9e-150">Windows Home Server is installed.</span></span><br/>                                                                                                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="43e9e-151">Notes</span><span class="sxs-lookup"><span data-stu-id="43e9e-151">Remarks</span></span>

<span data-ttu-id="43e9e-152">Vous ne devez pas compter uniquement sur l’indicateur 0x00000001 pour déterminer si Small Business Server a été installé sur le système, car cet indicateur et l’indicateur 0x00000020 sont définis lors de l’installation de cette suite de produits.</span><span class="sxs-lookup"><span data-stu-id="43e9e-152">You should not rely upon only the 0x00000001 flag to determine whether Small Business Server has been installed on the system, as both this flag and the 0x00000020 flag are set when this product suite is installed.</span></span> <span data-ttu-id="43e9e-153">Si vous mettez à niveau cette installation vers Windows Server, Standard Edition, l’indicateur 0x00000020 est désactivé, mais l’indicateur 0x00000001 reste défini.</span><span class="sxs-lookup"><span data-stu-id="43e9e-153">If you upgrade this installation to Windows Server, Standard Edition, the 0x00000020 flag will be cleared however, the 0x00000001 flag will remain set.</span></span> <span data-ttu-id="43e9e-154">Dans ce cas, cela indique que Small Business Server a été installé sur ce système.</span><span class="sxs-lookup"><span data-stu-id="43e9e-154">In this case, this indicates that Small Business Server was once installed on this system.</span></span> <span data-ttu-id="43e9e-155">Si cette installation est mise à niveau vers Windows Server édition entreprise, l’indicateur 0x00000001 reste défini.</span><span class="sxs-lookup"><span data-stu-id="43e9e-155">If this installation is further upgraded to Windows Server, Enterprise Edition, the 0x00000001 flag will remain set.</span></span>

## <a name="requirements"></a><span data-ttu-id="43e9e-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43e9e-156">Requirements</span></span>



| <span data-ttu-id="43e9e-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43e9e-157">Requirement</span></span> | <span data-ttu-id="43e9e-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="43e9e-158">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="43e9e-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43e9e-159">Minimum supported client</span></span><br/> | <span data-ttu-id="43e9e-160">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43e9e-160">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="43e9e-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43e9e-161">Minimum supported server</span></span><br/> | <span data-ttu-id="43e9e-162">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43e9e-162">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="43e9e-163">En-tête</span><span class="sxs-lookup"><span data-stu-id="43e9e-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="43e9e-164"><dt>Ntddk. h</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-164"><dt>Ntddk.h</dt></span></span> </dl>   |
| <span data-ttu-id="43e9e-165">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="43e9e-165">Library</span></span><br/>                  | <dl> <span data-ttu-id="43e9e-166"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-166"><dt>Ntdll.lib</dt></span></span> </dl> |
| <span data-ttu-id="43e9e-167">DLL</span><span class="sxs-lookup"><span data-stu-id="43e9e-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43e9e-168"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43e9e-168"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 




