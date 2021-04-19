---
description: Lors de l’utilisation de la directive INF RegisterDlls pour inscrire automatiquement des dll, les appelants de SetupInstallFromInfSection peuvent recevoir des notifications sur chaque fichier tel qu’il est inscrit ou désinscrit.
ms.assetid: 6304f406-c9f8-41cc-a7b7-5ef606f62efb
title: Message d’SPFILENOTIFY_ENDREGISTRATION (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8992d318d605110d74521efdb8a9c911aeeb9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522429"
---
# <a name="spfilenotify_endregistration-message"></a><span data-ttu-id="6641a-103">\_Message SPFILENOTIFY ENDREGISTRATION</span><span class="sxs-lookup"><span data-stu-id="6641a-103">SPFILENOTIFY\_ENDREGISTRATION message</span></span>

<span data-ttu-id="6641a-104">Lors de l’utilisation de la directive INF **RegisterDlls** pour inscrire automatiquement des dll, les appelants de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) peuvent recevoir des notifications sur chaque fichier tel qu’il est inscrit ou désinscrit.</span><span class="sxs-lookup"><span data-stu-id="6641a-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="6641a-105">Pour envoyer une **notification \_ ENDREGISTRATION SPFILENOTIFY** à une routine de rappel après avoir inscrit ou annulé l’inscription d’un fichier, incluez \_ le REGISTERCALLBACKAWARE de spinst plus l’ajout de la valeur de spinst \_ dans le paramètre *Flags* de **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="6641a-105">To send a **SPFILENOTIFY\_ENDREGISTRATION** notification to a callback routine once after registering or unregistering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="6641a-106">Pour envoyer une notification d’annulation de l’inscription, incluez le REGISTERCALLBACKAWARE de SPINst \_ plus \_ UNREGSVR de rotation dans le paramètre *Flags* .</span><span class="sxs-lookup"><span data-stu-id="6641a-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="6641a-107">La routine de rappel spécifiée par le paramètre *MsgHandler* de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) doit être le [type \_ \_ callback de fichier PSP](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="6641a-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="6641a-108">Définissez le paramètre de *contexte* sur le même *contexte* que celui spécifié dans **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="6641a-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="6641a-109">Définissez le paramètre de *notification* sur **SPFILENOTIFY \_ ENDREGISTRATION**.</span><span class="sxs-lookup"><span data-stu-id="6641a-109">Set the *Notification* parameter to **SPFILENOTIFY\_ENDREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_ENDREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="6641a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6641a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6641a-111">*Param1*</span><span class="sxs-lookup"><span data-stu-id="6641a-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="6641a-112">Pointeur vers une structure d' [**\_ État de \_ contrôle \_ de Registre SP**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) contenant des informations sur le fichier en cours d’inscription ou non inscrit.</span><span class="sxs-lookup"><span data-stu-id="6641a-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="6641a-113">Le membre **cbSize** doit être défini sur la taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="6641a-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="6641a-114">Le **nom** de fichier doit être défini sur le chemin d’accès complet du fichier en cours d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6641a-114">**FileName** should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="6641a-115">**Win32Error** doit être défini sur un [code d’erreur système](/windows/desktop/Debug/system-error-codes) indiquant un code d’erreur étendu.</span><span class="sxs-lookup"><span data-stu-id="6641a-115">**Win32Error** should be set to a [system error code](/windows/desktop/Debug/system-error-codes) indicating an extended error code.</span></span> <span data-ttu-id="6641a-116">**FailureCode** doit être défini sur l’un des codes d’échec valides indiquant le résultat de l’inscription.</span><span class="sxs-lookup"><span data-stu-id="6641a-116">**FailureCode** should be set to one of the valid failure codes indicating the outcome of the registration.</span></span> <span data-ttu-id="6641a-117">Pour connaître les codes d’erreur valides, consultez [**\_ État du \_ contrôle \_ d’inscription SP**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).</span><span class="sxs-lookup"><span data-stu-id="6641a-117">For valid failure codes see [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).</span></span>

</dd> <dt>

<span data-ttu-id="6641a-118">*Param2*</span><span class="sxs-lookup"><span data-stu-id="6641a-118">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="6641a-119">Si le fichier est en cours d’enregistrement, *param2* doit être défini sur un pointeur désignant une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="6641a-119">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="6641a-120">Si l’inscription du fichier est annulée, la valeur de *param2* doit être un pointeur vers la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="6641a-120">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6641a-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6641a-121">Return value</span></span>

<span data-ttu-id="6641a-122">Après avoir reçu la notification, la fonction de rappel peut retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6641a-122">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="6641a-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6641a-123">Return code</span></span>                                                                                  | <span data-ttu-id="6641a-124">Description</span><span class="sxs-lookup"><span data-stu-id="6641a-124">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="6641a-125"><dt>**\_abandon FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="6641a-125"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="6641a-126">Arrêtez le traitement de la section INF.</span><span class="sxs-lookup"><span data-stu-id="6641a-126">Stop processing the INF section.</span></span><br/>     |
| <dl> <span data-ttu-id="6641a-127"><dt>**FILEOP \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="6641a-127"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="6641a-128">Poursuivez le traitement de la section INF.</span><span class="sxs-lookup"><span data-stu-id="6641a-128">Continue processing the INF section.</span></span><br/> |
| <dl> <span data-ttu-id="6641a-129"><dt>**ignorer le fichier \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6641a-129"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="6641a-130">Continuer le traitement de la section INF</span><span class="sxs-lookup"><span data-stu-id="6641a-130">Continue processing the INF section</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="6641a-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6641a-131">Requirements</span></span>



| <span data-ttu-id="6641a-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6641a-132">Requirement</span></span> | <span data-ttu-id="6641a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="6641a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6641a-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6641a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6641a-135">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6641a-135">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6641a-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6641a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6641a-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6641a-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6641a-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="6641a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6641a-139"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6641a-139"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6641a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6641a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6641a-141">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="6641a-141">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="6641a-142">Notifications</span><span class="sxs-lookup"><span data-stu-id="6641a-142">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="6641a-143">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="6641a-143">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="6641a-144">**SPFILENOTIFY \_ STARTREGISTRATION**</span><span class="sxs-lookup"><span data-stu-id="6641a-144">**SPFILENOTIFY\_STARTREGISTRATION**</span></span>](spfilenotify-startregistration.md)
</dt> </dl>

 

