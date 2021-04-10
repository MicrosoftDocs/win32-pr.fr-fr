---
title: Classe MDM_Policy_Config01_RemoteDesktopServices02
description: La \_ classe Config01 RemoteDesktopServices02 de la stratégie MDM \_ \_ configure les stratégies du service bureau à distance.
ms.assetid: d2c53be7-6dec-4603-b851-e9c979475496
keywords:
- Classe MDM_Policy_Config01_RemoteDesktopServices02
- Classe MDM_Policy_Config01_RemoteDesktopServices02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteDesktopServices02
- MDM_Policy_Config01_RemoteDesktopServices02.InstanceID
- MDM_Policy_Config01_RemoteDesktopServices02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a023ae44c7b8ab170d4efe9c38aaacdeca3cc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942106"
---
# <a name="mdm_policy_config01_remotedesktopservices02-class"></a><span data-ttu-id="7ead5-105">\_Classe RemoteDesktopServices02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="7ead5-105">MDM\_Policy\_Config01\_RemoteDesktopServices02 class</span></span>

<span data-ttu-id="7ead5-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="7ead5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7ead5-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="7ead5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7ead5-108">La \_ classe Config01 RemoteDesktopServices02 de la stratégie MDM \_ \_ configure les stratégies du service bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="7ead5-108">The MDM\_Policy\_Config01\_RemoteDesktopServices02 class configures the remote desktop service policies.</span></span>

<span data-ttu-id="7ead5-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7ead5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ead5-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ead5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteDesktopServices02
{
  string InstanceID;
  string ParentID;
  string AllowUsersToConnectRemotely;
  string ClientConnectionEncryptionLevel;
  string DoNotAllowDriveRedirection;
  string DoNotAllowPasswordSaving;
  string PromptForPasswordUponConnection;
  string RequireSecureRPCCommunication;
};
```

## <a name="members"></a><span data-ttu-id="7ead5-111">Membres</span><span class="sxs-lookup"><span data-stu-id="7ead5-111">Members</span></span>

<span data-ttu-id="7ead5-112">La **classe \_ \_ Config01 \_ RemoteDesktopServices02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7ead5-112">The **MDM\_Policy\_Config01\_RemoteDesktopServices02** class has these types of members:</span></span>

-   [<span data-ttu-id="7ead5-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7ead5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ead5-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7ead5-114">Properties</span></span>

<span data-ttu-id="7ead5-115">La **classe \_ \_ Config01 \_ RemoteDesktopServices02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7ead5-115">The **MDM\_Policy\_Config01\_RemoteDesktopServices02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7ead5-116">AllowUsersToConnectRemotely</span><span class="sxs-lookup"><span data-stu-id="7ead5-116">AllowUsersToConnectRemotely</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-allowuserstoconnectremotely)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead5-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7ead5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ead5-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7ead5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7ead5-119">ClientConnectionEncryptionLevel</span><span class="sxs-lookup"><span data-stu-id="7ead5-119">ClientConnectionEncryptionLevel</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-clientconnectionencryptionlevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead5-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7ead5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ead5-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7ead5-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7ead5-122">DoNotAllowDriveRedirection</span><span class="sxs-lookup"><span data-stu-id="7ead5-122">DoNotAllowDriveRedirection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowdriveredirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead5-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7ead5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ead5-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7ead5-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7ead5-125">DoNotAllowPasswordSaving</span><span class="sxs-lookup"><span data-stu-id="7ead5-125">DoNotAllowPasswordSaving</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowpasswordsaving)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead5-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7ead5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ead5-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7ead5-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7ead5-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7ead5-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead5-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7ead5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ead5-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7ead5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead5-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7ead5-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7ead5-132">**ID**</span><span class="sxs-lookup"><span data-stu-id="7ead5-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead5-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7ead5-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ead5-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7ead5-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead5-135">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7ead5-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7ead5-136">PromptForPasswordUponConnection</span><span class="sxs-lookup"><span data-stu-id="7ead5-136">PromptForPasswordUponConnection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-promptforpassworduponconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead5-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7ead5-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ead5-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7ead5-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7ead5-139">RequireSecureRPCCommunication</span><span class="sxs-lookup"><span data-stu-id="7ead5-139">RequireSecureRPCCommunication</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-requiresecurerpccommunication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead5-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7ead5-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ead5-141">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7ead5-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ead5-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ead5-142">Requirements</span></span>



| <span data-ttu-id="7ead5-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ead5-143">Requirement</span></span> | <span data-ttu-id="7ead5-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ead5-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ead5-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ead5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7ead5-146">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ead5-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ead5-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ead5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7ead5-148">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ead5-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7ead5-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7ead5-149">Namespace</span></span><br/>                | <span data-ttu-id="7ead5-150">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="7ead5-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7ead5-151">MOF</span><span class="sxs-lookup"><span data-stu-id="7ead5-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ead5-152"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ead5-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ead5-153">DLL</span><span class="sxs-lookup"><span data-stu-id="7ead5-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ead5-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ead5-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

