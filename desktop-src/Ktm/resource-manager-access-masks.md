---
description: KTM définit les masques d’accès d’inscription suivants à utiliser lors de l’ouverture d’un gestionnaire de ressources.
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: Masques d’accès Gestionnaire des ressources (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0f579a96ed80de100a5cb41cb9c4e9b847a060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115402"
---
# <a name="resource-manager-access-masks"></a><span data-ttu-id="39ad7-103">Masques d’accès Gestionnaire des ressources</span><span class="sxs-lookup"><span data-stu-id="39ad7-103">Resource Manager Access Masks</span></span>

<span data-ttu-id="39ad7-104">KTM définit les masques d’accès d’inscription suivants à utiliser lors de l’ouverture d’un gestionnaire de ressources.</span><span class="sxs-lookup"><span data-stu-id="39ad7-104">KTM defines the following enlistment access masks to be used when opening a resource manager.</span></span>

<dl> <dt>

<span data-ttu-id="39ad7-105"><span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**\_informations sur les requêtes RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="39ad7-105"><span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**RESOURCEMANAGER\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39ad7-106">L’appelant peut demander des informations sur le gestionnaire de ressources (RM).</span><span class="sxs-lookup"><span data-stu-id="39ad7-106">The caller can query for the resource manager (RM) information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39ad7-107"><span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**\_informations sur l’ensemble de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="39ad7-107"><span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**RESOURCEMANAGER\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39ad7-108">L’appelant peut définir les informations du gestionnaire de configuration.</span><span class="sxs-lookup"><span data-stu-id="39ad7-108">The caller can set the RM information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39ad7-109"><span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**Recover RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="39ad7-109"><span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**RESOURCEMANAGER\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39ad7-110">L’appelant peut récupérer le RM spécifié.</span><span class="sxs-lookup"><span data-stu-id="39ad7-110">The caller can recover the specified RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39ad7-111"><span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**inscription de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="39ad7-111"><span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**RESOURCEMANAGER\_ENLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39ad7-112">L’appelant peut inscrire un RM dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="39ad7-112">The caller can enlist an RM in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39ad7-113"><span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**NOTIFICATION d’accès à RESOURCEMANAGER \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39ad7-113"><span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**RESOURCEMANAGER\_GET\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39ad7-114">L’appelant peut recevoir une notification pour un RM.</span><span class="sxs-lookup"><span data-stu-id="39ad7-114">The caller can receive a notification for an RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39ad7-115"><span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**\_lecture générique \_ RESOURCEMANAGER**</span><span class="sxs-lookup"><span data-stu-id="39ad7-115"><span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**RESOURCEMANAGER\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39ad7-116">L’appelant dispose des privilèges suivants : \_ lecture des droits standard \_ , \_ \_ informations sur les requêtes RESOURCEMANAGER et \_ recover ResourceManager.</span><span class="sxs-lookup"><span data-stu-id="39ad7-116">The caller has the following privileges: STANDARD\_RIGHTS\_READ, RESOURCEMANAGER\_QUERY\_INFORMATION, and RESOURCEMANAGER\_RECOVER.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39ad7-117"><span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**\_écriture générique \_ RESOURCEMANAGER**</span><span class="sxs-lookup"><span data-stu-id="39ad7-117"><span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**RESOURCEMANAGER\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39ad7-118">L’appelant dispose des privilèges suivants : \_ écriture des droits standard \_ , \_ \_ informations sur le jeu de données, inscription ResourceManager et notification d’accès à \_ ResourceManager \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="39ad7-118">The caller has the following privileges: STANDARD\_RIGHTS\_WRITE, RESOURCEMANAGER\_SET\_INFORMATION, RESOURCEMANAGER\_ENLIST, and RESOURCEMANAGER\_GET\_NOTIFICATION.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39ad7-119"><span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**\_Exécution générique \_ RESOURCEMANAGER**</span><span class="sxs-lookup"><span data-stu-id="39ad7-119"><span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**RESOURCEMANAGER\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39ad7-120">L’appelant dispose des privilèges suivants : \_ droits d' \_ exécution standard, \_ inscription ResourceManager et \_ \_ notification d’accès à ResourceManager.</span><span class="sxs-lookup"><span data-stu-id="39ad7-120">The caller has the following privileges: STANDARD\_RIGHTS\_EXECUTE, RESOURCEMANAGER\_ENLIST, and RESOURCEMANAGER\_GET\_NOTIFICATION.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39ad7-121"><span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**\_tout \_ accès à RESOURCEMANAGER**</span><span class="sxs-lookup"><span data-stu-id="39ad7-121"><span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**RESOURCEMANAGER\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39ad7-122">L’appelant dispose des privilèges suivants : \_ droits standard \_ requis.</span><span class="sxs-lookup"><span data-stu-id="39ad7-122">The caller has the following privilege: STANDARD\_RIGHTS\_REQUIRED.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39ad7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39ad7-123">Requirements</span></span>



| <span data-ttu-id="39ad7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39ad7-124">Requirement</span></span> | <span data-ttu-id="39ad7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="39ad7-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39ad7-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39ad7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="39ad7-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39ad7-127">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="39ad7-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39ad7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="39ad7-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39ad7-129">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="39ad7-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="39ad7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="39ad7-131"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="39ad7-131"><dt>WinNT.h</dt></span></span> </dl> |



 

 




