---
description: Lors de l’utilisation de la directive INF RegisterDlls pour inscrire automatiquement des dll, les appelants de SetupInstallFromInfSection peuvent recevoir des notifications sur chaque fichier tel qu’il est inscrit ou désinscrit.
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: Message d’SPFILENOTIFY_STARTREGISTRATION (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe795af38c21c17bf4e81692985d4bfe50dc8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524365"
---
# <a name="spfilenotify_startregistration-message"></a><span data-ttu-id="19c66-103">\_Message SPFILENOTIFY STARTREGISTRATION</span><span class="sxs-lookup"><span data-stu-id="19c66-103">SPFILENOTIFY\_STARTREGISTRATION message</span></span>

<span data-ttu-id="19c66-104">Lors de l’utilisation de la directive INF **RegisterDlls** pour inscrire automatiquement des dll, les appelants de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) peuvent recevoir des notifications sur chaque fichier tel qu’il est inscrit ou désinscrit.</span><span class="sxs-lookup"><span data-stu-id="19c66-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="19c66-105">Pour envoyer une notification **SPFILENOTIFY \_ STARTREGISTRATION** à la routine de rappel une fois avant d’inscrire un fichier, incluez le REGISTERCALLBACKAWARE de spinst plus la valeur de \_ l’argument spinst \_ dans le paramètre *Flags* de **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="19c66-105">To send a **SPFILENOTIFY\_STARTREGISTRATION** notification to the callback routine once before registering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="19c66-106">Pour envoyer une notification d’annulation de l’inscription, incluez le REGISTERCALLBACKAWARE de SPINst \_ plus \_ UNREGSVR de rotation dans le paramètre *Flags* .</span><span class="sxs-lookup"><span data-stu-id="19c66-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="19c66-107">La routine de rappel spécifiée par le paramètre *MsgHandler* de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) doit être le [type \_ \_ callback de fichier PSP](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="19c66-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="19c66-108">Définissez le paramètre de *contexte* sur le même *contexte* que celui spécifié dans **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="19c66-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="19c66-109">Définissez le paramètre de *notification* sur **SPFILENOTIFY \_ STARTREGISTRATION**.</span><span class="sxs-lookup"><span data-stu-id="19c66-109">Set the *Notification* parameter to **SPFILENOTIFY\_STARTREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="19c66-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19c66-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19c66-111">*Param1*</span><span class="sxs-lookup"><span data-stu-id="19c66-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="19c66-112">Pointeur vers une structure d' [**\_ État de \_ contrôle \_ de Registre SP**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) contenant des informations sur le fichier en cours d’inscription ou non inscrit.</span><span class="sxs-lookup"><span data-stu-id="19c66-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="19c66-113">Le membre **cbSize** doit être défini sur la taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="19c66-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="19c66-114">Le membre de **nom** de fichier doit être défini sur le chemin d’accès complet du fichier en cours d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="19c66-114">The **FileName** member should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="19c66-115">**Win32Error** n’est pas utilisé et doit être défini sur aucune \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="19c66-115">**Win32Error** is not used and should be set to NO\_ERROR.</span></span> <span data-ttu-id="19c66-116">**FailureCode** n’est pas utilisé et doit être défini sur SPREG \_ Success.</span><span class="sxs-lookup"><span data-stu-id="19c66-116">**FailureCode** is not used and should be set to SPREG\_SUCCESS.</span></span>

</dd> <dt>

<span data-ttu-id="19c66-117">*Param2*</span><span class="sxs-lookup"><span data-stu-id="19c66-117">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="19c66-118">Si le fichier est en cours d’enregistrement, *param2* doit être défini sur un pointeur désignant une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="19c66-118">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="19c66-119">Si l’inscription du fichier est annulée, la valeur de *param2* doit être un pointeur vers la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="19c66-119">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19c66-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19c66-120">Return value</span></span>

<span data-ttu-id="19c66-121">Après avoir reçu la notification, la fonction de rappel peut retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="19c66-121">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="19c66-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="19c66-122">Return code</span></span>                                                                                  | <span data-ttu-id="19c66-123">Description</span><span class="sxs-lookup"><span data-stu-id="19c66-123">Description</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="19c66-124"><dt>**\_abandon FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="19c66-124"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="19c66-125">N’enregistrez pas le fichier et ne l’annulez pas et arrêtez le traitement de la section INF.</span><span class="sxs-lookup"><span data-stu-id="19c66-125">Do not register or unregister the file and stop processing the INF section.</span></span><br/>             |
| <dl> <span data-ttu-id="19c66-126"><dt>**FILEOP \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="19c66-126"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="19c66-127">Enregistrez ou annulez l’enregistrement du fichier et poursuivez le traitement de la section INF.</span><span class="sxs-lookup"><span data-stu-id="19c66-127">Register or unregister the file and continue processing the INF section.</span></span><br/>                |
| <dl> <span data-ttu-id="19c66-128"><dt>**ignorer le fichier \_**</dt></span><span class="sxs-lookup"><span data-stu-id="19c66-128"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="19c66-129">Ignorer l’inscription ou annuler l’inscription du fichier, mais poursuivre le traitement de la section INF</span><span class="sxs-lookup"><span data-stu-id="19c66-129">Skip registration or unregistration of the file but continue processing the INF section</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="19c66-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19c66-130">Requirements</span></span>



| <span data-ttu-id="19c66-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19c66-131">Requirement</span></span> | <span data-ttu-id="19c66-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="19c66-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19c66-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19c66-133">Minimum supported client</span></span><br/> | <span data-ttu-id="19c66-134">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19c66-134">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="19c66-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19c66-135">Minimum supported server</span></span><br/> | <span data-ttu-id="19c66-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19c66-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19c66-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="19c66-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="19c66-138"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="19c66-138"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19c66-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19c66-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19c66-140">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="19c66-140">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="19c66-141">Notifications</span><span class="sxs-lookup"><span data-stu-id="19c66-141">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="19c66-142">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="19c66-142">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="19c66-143">**SPFILENOTIFY \_ ENDREGISTRATION**</span><span class="sxs-lookup"><span data-stu-id="19c66-143">**SPFILENOTIFY\_ENDREGISTRATION**</span></span>](spfilenotify-endregistration.md)
</dt> </dl>

 

