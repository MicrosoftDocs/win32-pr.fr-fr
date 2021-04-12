---
title: Méthode RemoteControl de la classe Win32_TSRemoteControlSetting
description: La méthode RemoteControl définit la propriété LevelOfControl.
ms.assetid: 341f4f8d-17be-4482-834a-b771e041cfec
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoteControl
- Services Bureau à distance de la méthode RemoteControl, classe Win32_TSRemoteControlSetting
- Win32_TSRemoteControlSetting de la classe Services Bureau à distance, méthode RemoteControl
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting.RemoteControl
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476269c2f619b7ea46bc6546f106d7ccd2a486e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317229"
---
# <a name="remotecontrol-method-of-the-win32_tsremotecontrolsetting-class"></a><span data-ttu-id="dadcd-106">Méthode RemoteControl de la \_ classe Win32 TSRemoteControlSetting</span><span class="sxs-lookup"><span data-stu-id="dadcd-106">RemoteControl method of the Win32\_TSRemoteControlSetting class</span></span>

<span data-ttu-id="dadcd-107">La méthode **RemoteControl** définit la propriété **LevelOfControl** .</span><span class="sxs-lookup"><span data-stu-id="dadcd-107">The **RemoteControl** method sets the **LevelOfControl** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="dadcd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dadcd-108">Syntax</span></span>


```mof
uint32 RemoteControl(
  [in] uint32 LevelOfControl
);
```



## <a name="parameters"></a><span data-ttu-id="dadcd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dadcd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dadcd-110">*LevelOfControl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dadcd-110">*LevelOfControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadcd-111">Nouvelle valeur de la propriété **LevelOfControl** , qui spécifie si la session est uniquement affichée par l’utilisateur distant ou affichée et contrôlée par le biais d’un clavier et d’une souris.</span><span class="sxs-lookup"><span data-stu-id="dadcd-111">New value for the **LevelOfControl** property, which specifies whether the session will only be viewed by the remote user, or viewed and controlled through a keyboard and mouse.</span></span> <span data-ttu-id="dadcd-112">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="dadcd-112">For more information, see the Remarks section.</span></span> <span data-ttu-id="dadcd-113">Les valeurs suivantes sont admises :</span><span class="sxs-lookup"><span data-stu-id="dadcd-113">The following values are supported.</span></span>

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="dadcd-114"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Désactiver** (0)</span><span class="sxs-lookup"><span data-stu-id="dadcd-114"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="dadcd-115">Le contrôle à distance est désactivé.</span><span class="sxs-lookup"><span data-stu-id="dadcd-115">Remote control is disabled.</span></span>

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span data-ttu-id="dadcd-116"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span><span class="sxs-lookup"><span data-stu-id="dadcd-116"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dadcd-117">L’utilisateur du contrôle à distance a le contrôle total de la session de l’utilisateur, avec l’autorisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dadcd-117">The user of remote control has full control of the user's session, with the user's permission.</span></span>

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span data-ttu-id="dadcd-118"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span><span class="sxs-lookup"><span data-stu-id="dadcd-118"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dadcd-119">L’utilisateur du contrôle à distance a le contrôle total de la session de l’utilisateur ; l’autorisation de l’utilisateur n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dadcd-119">The user of remote control has full control of the user's session; the user's permission is not required.</span></span>

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span data-ttu-id="dadcd-120"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span><span class="sxs-lookup"><span data-stu-id="dadcd-120"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dadcd-121">L’utilisateur du contrôle à distance peut afficher la session à distance, avec l’autorisation de l’utilisateur. l’utilisateur distant ne peut pas contrôler activement la session.</span><span class="sxs-lookup"><span data-stu-id="dadcd-121">The user of remote control can view the session remotely, with the user's permission; the remote user cannot actively control the session.</span></span>

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span data-ttu-id="dadcd-122"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span><span class="sxs-lookup"><span data-stu-id="dadcd-122"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dadcd-123">L’utilisateur du contrôle à distance peut afficher la session à distance, mais ne contrôle pas activement la session ; l’autorisation de l’utilisateur n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dadcd-123">The user of remote control can view the session remotely, but not actively control the session; the user's permission is not required.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dadcd-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dadcd-124">Return value</span></span>

<span data-ttu-id="dadcd-125">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="dadcd-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="dadcd-126">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="dadcd-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="dadcd-127">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="dadcd-127">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="dadcd-128">Notes</span><span class="sxs-lookup"><span data-stu-id="dadcd-128">Remarks</span></span>

<span data-ttu-id="dadcd-129">Le contrôle total d’une session signifie que l’utilisateur distant peut contrôler activement la session de l’utilisateur à l’aide d’un clavier et d’une souris.</span><span class="sxs-lookup"><span data-stu-id="dadcd-129">Full control of a session means that the remote user can actively control the user's session with a keyboard and mouse.</span></span>

<span data-ttu-id="dadcd-130">Lorsqu’un utilisateur tente d’établir une connexion de contrôle à distance, le système affiche un message au client distant, en demandant l’autorisation d’afficher ou de participer activement à la session à distance.</span><span class="sxs-lookup"><span data-stu-id="dadcd-130">When a user attempts to establish a remote-control connection, the system displays a message to the remote client, requesting permission to either view or participate actively in the remote session.</span></span>

<span data-ttu-id="dadcd-131">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="dadcd-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dadcd-132">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="dadcd-132">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="dadcd-133">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="dadcd-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dadcd-134">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="dadcd-134">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="dadcd-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dadcd-135">Requirements</span></span>



| <span data-ttu-id="dadcd-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dadcd-136">Requirement</span></span> | <span data-ttu-id="dadcd-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="dadcd-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dadcd-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dadcd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="dadcd-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dadcd-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dadcd-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dadcd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="dadcd-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dadcd-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dadcd-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dadcd-142">Namespace</span></span><br/>                | <span data-ttu-id="dadcd-143">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="dadcd-143">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="dadcd-144">MOF</span><span class="sxs-lookup"><span data-stu-id="dadcd-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dadcd-145"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dadcd-145"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="dadcd-146">DLL</span><span class="sxs-lookup"><span data-stu-id="dadcd-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dadcd-147"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dadcd-147"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dadcd-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dadcd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dadcd-149">**\_TSRemoteControlSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="dadcd-149">**Win32\_TSRemoteControlSetting**</span></span>](win32-tsremotecontrolsetting.md)
</dt> </dl>

 

