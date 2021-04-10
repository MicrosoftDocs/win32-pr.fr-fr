---
title: GUESTOSVERSIONINFOEX, structure (VPCCOMInterfaces. h)
description: Contient les informations de version du système d’exploitation pour le système d’exploitation invité.
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- GUESTOSVERSIONINFOEX structure Virtual PC
topic_type:
- apiref
api_name:
- GUESTOSVERSIONINFOEX
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633838affb9a9ff1453a0c49de9588428b038fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104278"
---
# <a name="guestosversioninfoex-structure"></a><span data-ttu-id="b8edd-104">GUESTOSVERSIONINFOEX, structure</span><span class="sxs-lookup"><span data-stu-id="b8edd-104">GUESTOSVERSIONINFOEX structure</span></span>

<span data-ttu-id="b8edd-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b8edd-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b8edd-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b8edd-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b8edd-107">Contient les informations de version du système d’exploitation pour le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="b8edd-107">Contains operating system version information for the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8edd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8edd-108">Syntax</span></span>


```C++
typedef struct _GUESTOSVERSIONINFOEX {
  long    dwOSVersionInfoSize;
  long    dwMajorVersion;
  long    dwMinorVersion;
  long    dwBuildNumber;
  long    dwPlatformId;
  wchar_t szCSDVersion[128];
  short   wServicePackMajor;
  short   wServicePackMinor;
  short   wSuiteMask;
  byte    wProductType;
  byte    wReserved;
} GUESTOSVERSIONINFOEX;
```



## <a name="members"></a><span data-ttu-id="b8edd-109">Membres</span><span class="sxs-lookup"><span data-stu-id="b8edd-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="b8edd-110">**dwOSVersionInfoSize**</span><span class="sxs-lookup"><span data-stu-id="b8edd-110">**dwOSVersionInfoSize**</span></span>
</dt> <dd>

<span data-ttu-id="b8edd-111">Taille de cette structure de données, en octets.</span><span class="sxs-lookup"><span data-stu-id="b8edd-111">The size of this data structure, in bytes.</span></span> <span data-ttu-id="b8edd-112">Affectez à ce membre la valeur `sizeof(GUESTOSVERSIONINFOEX)` .</span><span class="sxs-lookup"><span data-stu-id="b8edd-112">Set this member to `sizeof(GUESTOSVERSIONINFOEX)`.</span></span>

</dd> <dt>

<span data-ttu-id="b8edd-113">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="b8edd-113">**dwMajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="b8edd-114">Numéro de version principale.</span><span class="sxs-lookup"><span data-stu-id="b8edd-114">The major version number.</span></span>

</dd> <dt>

<span data-ttu-id="b8edd-115">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="b8edd-115">**dwMinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="b8edd-116">Numéro de version secondaire.</span><span class="sxs-lookup"><span data-stu-id="b8edd-116">The minor version number.</span></span>

</dd> <dt>

<span data-ttu-id="b8edd-117">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="b8edd-117">**dwBuildNumber**</span></span>
</dt> <dd>

<span data-ttu-id="b8edd-118">Numéro de build.</span><span class="sxs-lookup"><span data-stu-id="b8edd-118">The build number.</span></span>

</dd> <dt>

<span data-ttu-id="b8edd-119">**dwPlatformId**</span><span class="sxs-lookup"><span data-stu-id="b8edd-119">**dwPlatformId**</span></span>
</dt> <dd>

<span data-ttu-id="b8edd-120">Plateforme du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b8edd-120">The operating system platform.</span></span> <span data-ttu-id="b8edd-121">Ce membre peut être de la **\_ plateforme ver \_ Win32 \_ NT** (2).</span><span class="sxs-lookup"><span data-stu-id="b8edd-121">This member can be **VER\_PLATFORM\_WIN32\_NT** (2).</span></span>

</dd> <dt>

<span data-ttu-id="b8edd-122">**szCSDVersion**</span><span class="sxs-lookup"><span data-stu-id="b8edd-122">**szCSDVersion**</span></span>
</dt> <dd>

<span data-ttu-id="b8edd-123">Chaîne terminée par le caractère null, telle que « Service Pack 3 », qui indique le dernier Service Pack installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="b8edd-123">A null-terminated string, such as "Service Pack 3", that indicates the latest Service Pack installed on the system.</span></span> <span data-ttu-id="b8edd-124">Si aucun Service Pack n’a été installé, la chaîne est vide.</span><span class="sxs-lookup"><span data-stu-id="b8edd-124">If no Service Pack has been installed, the string is empty.</span></span>

</dd> <dt>

<span data-ttu-id="b8edd-125">**wServicePackMajor**</span><span class="sxs-lookup"><span data-stu-id="b8edd-125">**wServicePackMajor**</span></span>
</dt> <dd>

<span data-ttu-id="b8edd-126">Numéro de version principale du dernier Service Pack installé.</span><span class="sxs-lookup"><span data-stu-id="b8edd-126">The major version number of the latest Service Pack installed.</span></span>

</dd> <dt>

<span data-ttu-id="b8edd-127">**wServicePackMinor**</span><span class="sxs-lookup"><span data-stu-id="b8edd-127">**wServicePackMinor**</span></span>
</dt> <dd>

<span data-ttu-id="b8edd-128">Numéro de version mineure du dernier Service Pack installé.</span><span class="sxs-lookup"><span data-stu-id="b8edd-128">The minor version number of the latest Service Pack installed.</span></span>

</dd> <dt>

<span data-ttu-id="b8edd-129">**wSuiteMask**</span><span class="sxs-lookup"><span data-stu-id="b8edd-129">**wSuiteMask**</span></span>
</dt> <dd>

<span data-ttu-id="b8edd-130">Masque de masque qui identifie les suites de produits disponibles sur le système.</span><span class="sxs-lookup"><span data-stu-id="b8edd-130">A bitmask that identifies the product suites available on the system.</span></span> <span data-ttu-id="b8edd-131">Ce membre peut être une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b8edd-131">This member can be a combination of the following values.</span></span>



| <span data-ttu-id="b8edd-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8edd-132">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="b8edd-133">Signification</span><span class="sxs-lookup"><span data-stu-id="b8edd-133">Meaning</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <span data-ttu-id="b8edd-134"><dt>**Ver \_ SUITE \_ BackOffice**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-134"><dt>**VER\_SUITE\_BACKOFFICE**</dt> <dt>0x00000004</dt></span></span> </dl>                                            | <span data-ttu-id="b8edd-135">Les composants Microsoft BackOffice sont installés.</span><span class="sxs-lookup"><span data-stu-id="b8edd-135">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <span data-ttu-id="b8edd-136"><dt>**Ver \_ Panneau \_ de suite**</dt> <dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-136"><dt>**VER\_SUITE\_BLADE**</dt> <dt>0x00000400</dt></span></span> </dl>                                                           | <span data-ttu-id="b8edd-137">Windows Server 2003, Web Edition est installé.</span><span class="sxs-lookup"><span data-stu-id="b8edd-137">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <span data-ttu-id="b8edd-138"><dt>**Ver \_ SUITE de \_ \_ serveurs de calcul**</dt> <dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-138"><dt>**VER\_SUITE\_COMPUTE\_SERVER**</dt> <dt>0x00004000</dt></span></span> </dl>                               | <span data-ttu-id="b8edd-139">Windows Server 2003, Compute Cluster Edition est installé.</span><span class="sxs-lookup"><span data-stu-id="b8edd-139">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <span data-ttu-id="b8edd-140"><dt>**Ver \_ SUITE \_ Datacenter**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-140"><dt>**VER\_SUITE\_DATACENTER**</dt> <dt>0x00000080</dt></span></span> </dl>                                            | <span data-ttu-id="b8edd-141">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition ou Windows 2000 Datacenter Server est installé.</span><span class="sxs-lookup"><span data-stu-id="b8edd-141">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <span data-ttu-id="b8edd-142"><dt>**Ver \_ SUITE \_ Enterprise**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-142"><dt>**VER\_SUITE\_ENTERPRISE**</dt> <dt>0x00000002</dt></span></span> </dl>                                            | <span data-ttu-id="b8edd-143">Windows Server 2008 entreprise, Windows Server 2003, Enterprise Edition ou Windows 2000 Advanced Server est installé.</span><span class="sxs-lookup"><span data-stu-id="b8edd-143">Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="b8edd-144">Reportez-vous à la section Remarques pour plus d’informations sur cet indicateur de bit.</span><span class="sxs-lookup"><span data-stu-id="b8edd-144">Refer to the Remarks section for more information about this bit flag.</span></span><br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <span data-ttu-id="b8edd-145"><dt>**Ver \_ SUITE \_ EMBEDDEDNT**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-145"><dt>**VER\_SUITE\_EMBEDDEDNT**</dt> <dt>0x00000040</dt></span></span> </dl>                                            | <span data-ttu-id="b8edd-146">Windows XP Embedded est installé.</span><span class="sxs-lookup"><span data-stu-id="b8edd-146">Windows XP Embedded is installed.</span></span><br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <span data-ttu-id="b8edd-147"><dt>**Ver \_ 0x00000200 \_ personnel de suite**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-147"><dt>**VER\_SUITE\_PERSONAL**</dt> <dt>0x00000200</dt></span></span> </dl>                                                  | <span data-ttu-id="b8edd-148">Windows Vista Édition familiale Premium, Windows Vista Édition familiale basique ou Windows XP Édition familiale est installé.</span><span class="sxs-lookup"><span data-stu-id="b8edd-148">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <span data-ttu-id="b8edd-149"><dt>**Ver \_ SUITE \_ SINGLEUSERTS**</dt> <dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-149"><dt>**VER\_SUITE\_SINGLEUSERTS**</dt> <dt>0x00000100</dt></span></span> </dl>                                      | <span data-ttu-id="b8edd-150">Bureau à distance est pris en charge, mais une seule session interactive est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b8edd-150">Remote Desktop is supported, but only one interactive session is supported.</span></span> <span data-ttu-id="b8edd-151">Cette valeur est définie, sauf si le système s’exécute en mode serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="b8edd-151">This value is set unless the system is running in application server mode.</span></span><br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <span data-ttu-id="b8edd-152"><dt>**Ver \_ SUITE \_ SMALLBUSINESS**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-152"><dt>**VER\_SUITE\_SMALLBUSINESS**</dt> <dt>0x00000001</dt></span></span> </dl>                                   | <span data-ttu-id="b8edd-153">Microsoft Small Business Server a été installé sur le système, mais il a peut-être été mis à niveau vers une autre version de Windows.</span><span class="sxs-lookup"><span data-stu-id="b8edd-153">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span> <span data-ttu-id="b8edd-154">Reportez-vous à la section Remarques pour plus d’informations sur cet indicateur de bit.</span><span class="sxs-lookup"><span data-stu-id="b8edd-154">Refer to the Remarks section for more information about this bit flag.</span></span><br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <span data-ttu-id="b8edd-155"><dt>**Ver \_ SUITE \_ \_ restreinte**</dt> <dt>0x00000020</dt> de la suite</span><span class="sxs-lookup"><span data-stu-id="b8edd-155"><dt>**VER\_SUITE\_SMALLBUSINESS\_RESTRICTED**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="b8edd-156">Microsoft Small Business Server est installé avec la licence client restrictive en vigueur.</span><span class="sxs-lookup"><span data-stu-id="b8edd-156">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="b8edd-157">Reportez-vous à la section Remarques pour plus d’informations sur cet indicateur de bit.</span><span class="sxs-lookup"><span data-stu-id="b8edd-157">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <span data-ttu-id="b8edd-158"><dt>**Ver \_ 0x00002000 \_ \_ serveur de stockage**</dt> de la suite <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-158"><dt>**VER\_SUITE\_STORAGE\_SERVER**</dt> <dt>0x00002000</dt></span></span> </dl>                               | <span data-ttu-id="b8edd-159">Windows Storage Server 2003 R2 ou Windows Storage Server 2003 est installé.</span><span class="sxs-lookup"><span data-stu-id="b8edd-159">Windows Storage Server 2003 R2 or Windows Storage Server 2003is installed.</span></span><br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <span data-ttu-id="b8edd-160"><dt>**Ver \_ \_Terminal de suite**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-160"><dt>**VER\_SUITE\_TERMINAL**</dt> <dt>0x00000010</dt></span></span> </dl>                                                  | <span data-ttu-id="b8edd-161">Les services Terminal Server sont installés.</span><span class="sxs-lookup"><span data-stu-id="b8edd-161">Terminal Services is installed.</span></span> <span data-ttu-id="b8edd-162">Cette valeur est toujours définie.</span><span class="sxs-lookup"><span data-stu-id="b8edd-162">This value is always set.</span></span><br/> <span data-ttu-id="b8edd-163">Si la valeur terminal de la **\_ suite \_ ver** est définie mais que la **suite de \_ \_ SINGLEUSERTS** de version n’est pas définie, le système s’exécute en mode serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="b8edd-163">If **VER\_SUITE\_TERMINAL** is set but **VER\_SUITE\_SINGLEUSERTS** is not set, the system is running in application server mode.</span></span><br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <span data-ttu-id="b8edd-164"><dt>**Ver \_ SUITE \_ 0x00008000 \_ serveur**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-164"><dt>**VER\_SUITE\_WH\_SERVER**</dt> <dt>0x00008000</dt></span></span> </dl>                                              | <span data-ttu-id="b8edd-165">Windows Server famille est installé.</span><span class="sxs-lookup"><span data-stu-id="b8edd-165">Windows Home Server is installed.</span></span><br/>                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="b8edd-166">**wProductType**</span><span class="sxs-lookup"><span data-stu-id="b8edd-166">**wProductType**</span></span>
</dt> <dd>

<span data-ttu-id="b8edd-167">Toutes les informations supplémentaires sur le système.</span><span class="sxs-lookup"><span data-stu-id="b8edd-167">Any additional information about the system.</span></span> <span data-ttu-id="b8edd-168">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b8edd-168">This member can be one of the following values.</span></span>



| <span data-ttu-id="b8edd-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8edd-169">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="b8edd-170">Signification</span><span class="sxs-lookup"><span data-stu-id="b8edd-170">Meaning</span></span>                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <span data-ttu-id="b8edd-171"><dt>**Ver \_ \_ \_ Contrôleur de domaine NT**</dt> <dt>0x0000002</dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-171"><dt>**VER\_NT\_DOMAIN\_CONTROLLER**</dt> <dt>0x0000002</dt></span></span> </dl> | <span data-ttu-id="b8edd-172">Le système est un contrôleur de domaine et le système d’exploitation est Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b8edd-172">The system is a domain controller and the operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <span data-ttu-id="b8edd-173"><dt>**Ver \_ 0x0000003 NT \_ Server**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-173"><dt>**VER\_NT\_SERVER**</dt> <dt>0x0000003</dt></span></span> </dl>                                   | <span data-ttu-id="b8edd-174">Le système d’exploitation est Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b8edd-174">The operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/> <span data-ttu-id="b8edd-175">Notez qu’un serveur qui est également un contrôleur de domaine est signalé en tant que **\_ \_ \_ contrôleur de domaine NT**, pas **ver \_ NT \_ Server**.</span><span class="sxs-lookup"><span data-stu-id="b8edd-175">Note that a server that is also a domain controller is reported as **VER\_NT\_DOMAIN\_CONTROLLER**, not **VER\_NT\_SERVER**.</span></span><br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <span data-ttu-id="b8edd-176"><dt>**Ver \_ \_Station de travail NT**</dt> <dt>0x0000001</dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-176"><dt>**VER\_NT\_WORKSTATION**</dt> <dt>0x0000001</dt></span></span> </dl>                    | <span data-ttu-id="b8edd-177">Le système d’exploitation est Windows 7, Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="b8edd-177">The operating system is Windows 7, Windows Vista, Windows XP, or Windows 2000 Professional.</span></span><br/>                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="b8edd-178">**wReserved**</span><span class="sxs-lookup"><span data-stu-id="b8edd-178">**wReserved**</span></span>
</dt> <dd>

<span data-ttu-id="b8edd-179">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="b8edd-179">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8edd-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8edd-180">Requirements</span></span>



| <span data-ttu-id="b8edd-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8edd-181">Requirement</span></span> | <span data-ttu-id="b8edd-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8edd-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8edd-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8edd-183">Minimum supported client</span></span><br/> | <span data-ttu-id="b8edd-184">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8edd-184">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8edd-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8edd-185">Minimum supported server</span></span><br/> | <span data-ttu-id="b8edd-186">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8edd-186">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b8edd-187">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b8edd-187">End of client support</span></span><br/>    | <span data-ttu-id="b8edd-188">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b8edd-188">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b8edd-189">Produit</span><span class="sxs-lookup"><span data-stu-id="b8edd-189">Product</span></span><br/>                  | <span data-ttu-id="b8edd-190">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b8edd-190">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b8edd-191">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8edd-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8edd-192"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8edd-192"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8edd-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8edd-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8edd-194">**IVMGuestOS::GetOsVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="b8edd-194">**IVMGuestOS::GetOsVersionInfo**</span></span>](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

