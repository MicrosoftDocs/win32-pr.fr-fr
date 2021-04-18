---
description: Dictez l’autorité des packages d’applications.
ms.assetid: 047439EA-789B-41CF-87C2-66CFB3F20908
title: Constantes SID du conteneur d’application (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 300b5ed110bbdc88d32efb76b20f5ec0f8454970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520066"
---
# <a name="app-container-sid-constants"></a><span data-ttu-id="68481-103">Constantes SID du conteneur d’application</span><span class="sxs-lookup"><span data-stu-id="68481-103">App Container SID Constants</span></span>

<span data-ttu-id="68481-104">Les constantes SID spécifiques au conteneur d’application déterminent l’autorité de package d’application.</span><span class="sxs-lookup"><span data-stu-id="68481-104">The app container specific SID constants dictate the application package authority.</span></span> <span data-ttu-id="68481-105">Bien qu’un développeur puisse utiliser directement ces constantes, la plupart des développeurs n’ont pas besoin de définir ces SID de conteneur d’application.</span><span class="sxs-lookup"><span data-stu-id="68481-105">While a developer can use these constants directly, most developers do not need to define these app container SIDs.</span></span>

<dl> <span data-ttu-id="68481-106"><span id="SECURITY_APP_PACKAGE_AUTHORITY"></span><span id="security_app_package_authority"></span>**Sécurité \_ Application \_ package \_ Authority** ( {0,0,0,0,0,15} ) Security <span id="SECURITY_APP_PACKAGE_BASE_RID"></span> <span id="security_app_package_base_rid"></span> **\_ app \_ package \_ base \_ RID** (0x00000002L) sécurité package d’application builtin dénombrable package d’application de sécurité RID nombre ( <span id="SECURITY_BUILTIN_APP_PACKAGE_RID_COUNT"></span> <span id="security_builtin_app_package_rid_count"></span> 8L) sécurité fonctionnalité intégrée RID (0x00000003L) sécurité **\_ \_ \_ \_ \_** builtin fonctionnalité RID dénombrable fonctionnalité de sécurité décompte ( <span id="SECURITY_APP_PACKAGE_RID_COUNT"></span> <span id="security_app_package_rid_count"></span> **\_ \_ \_ \_** <span id="SECURITY_CAPABILITY_BASE_RID"></span> <span id="security_capability_base_rid"></span> **\_ \_ \_** <span id="SECURITY_BUILTIN_CAPABILITY_RID_COUNT"></span> <span id="security_builtin_capability_rid_count"></span> **\_ \_ \_ \_** <span id="SECURITY_CAPABILITY_RID_COUNT"></span> <span id="security_capability_rid_count"></span> 5L) **\_ \_ \_** <span id="SECURITY_BUILTIN_PACKAGE_ANY_PACKAGE"></span> <span id="security_builtin_package_any_package"></span> **\_ \_ package \_ \_ BuiltIn sécurité** RID (0x00000001L)</span><span class="sxs-lookup"><span data-stu-id="68481-106"><span id="SECURITY_APP_PACKAGE_AUTHORITY"></span><span id="security_app_package_authority"></span>**SECURITY\_APP\_PACKAGE\_AUTHORITY** ({0,0,0,0,0,15}) <span id="SECURITY_APP_PACKAGE_BASE_RID"></span><span id="security_app_package_base_rid"></span>**SECURITY\_APP\_PACKAGE\_BASE\_RID** (0x00000002L) <span id="SECURITY_BUILTIN_APP_PACKAGE_RID_COUNT"></span><span id="security_builtin_app_package_rid_count"></span>**SECURITY\_BUILTIN\_APP\_PACKAGE\_RID\_COUNT** (2L) <span id="SECURITY_APP_PACKAGE_RID_COUNT"></span><span id="security_app_package_rid_count"></span>**SECURITY\_APP\_PACKAGE\_RID\_COUNT** (8L) <span id="SECURITY_CAPABILITY_BASE_RID"></span><span id="security_capability_base_rid"></span>**SECURITY\_CAPABILITY\_BASE\_RID** (0x00000003L) <span id="SECURITY_BUILTIN_CAPABILITY_RID_COUNT"></span><span id="security_builtin_capability_rid_count"></span>**SECURITY\_BUILTIN\_CAPABILITY\_RID\_COUNT** (2L) <span id="SECURITY_CAPABILITY_RID_COUNT"></span><span id="security_capability_rid_count"></span>**SECURITY\_CAPABILITY\_RID\_COUNT** (5L) <span id="SECURITY_BUILTIN_PACKAGE_ANY_PACKAGE"></span><span id="security_builtin_package_any_package"></span>**SECURITY\_BUILTIN\_PACKAGE\_ANY\_PACKAGE** (0x00000001L)</span></span>
</dl>

## <a name="requirements"></a><span data-ttu-id="68481-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68481-107">Requirements</span></span>



| <span data-ttu-id="68481-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68481-108">Requirement</span></span> | <span data-ttu-id="68481-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="68481-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68481-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68481-110">Minimum supported client</span></span><br/> | <span data-ttu-id="68481-111">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68481-111">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="68481-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68481-112">Minimum supported server</span></span><br/> | <span data-ttu-id="68481-113">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68481-113">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="68481-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="68481-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="68481-115"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="68481-115"><dt>Winnt.h</dt></span></span> </dl> |



 

 




