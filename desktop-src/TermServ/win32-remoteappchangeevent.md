---
title: Classe Win32_RemoteAppChangeEvent
description: Représente une modification apportée aux paramètres RemoteApp de Windows Server 2008 R2 sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 3434ee4e-283e-4147-a73b-c131e8af6c57
ms.tgt_platform: multiple
keywords:
- Win32_RemoteAppChangeEvent de la classe Services Bureau à distance
- Win32_RemoteAppChangeEvent de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RemoteAppChangeEvent
- Win32_RemoteAppChangeEvent.SECURITY_DESCRIPTOR
- Win32_RemoteAppChangeEvent.TIME_CREATED
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5355d057038e97e9f381646134ff6487541f67f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103675"
---
# <a name="win32_remoteappchangeevent-class"></a><span data-ttu-id="2552c-105">\_Classe RemoteAppChangeEvent Win32</span><span class="sxs-lookup"><span data-stu-id="2552c-105">Win32\_RemoteAppChangeEvent class</span></span>

<span data-ttu-id="2552c-106">Représente une modification apportée aux paramètres RemoteApp de Windows Server 2008 R2 sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="2552c-106">Represents a change to Windows Server 2008 R2 RemoteApp settings on the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2552c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2552c-107">Syntax</span></span>

``` syntax
class Win32_RemoteAppChangeEvent : ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="2552c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="2552c-108">Members</span></span>

<span data-ttu-id="2552c-109">La classe **Win32 \_ RemoteAppChangeEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2552c-109">The **Win32\_RemoteAppChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="2552c-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2552c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2552c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2552c-111">Properties</span></span>

<span data-ttu-id="2552c-112">La classe **Win32 \_ RemoteAppChangeEvent** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2552c-112">The **Win32\_RemoteAppChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2552c-113">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="2552c-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2552c-114">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="2552c-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2552c-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2552c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2552c-116">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="2552c-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="2552c-117">Cette propriété est héritée de l' [**\_ \_ événement**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="2552c-117">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="2552c-118">Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="2552c-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="2552c-119">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="2552c-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2552c-120">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2552c-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2552c-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2552c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2552c-122">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="2552c-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="2552c-123">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="2552c-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="2552c-124">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="2552c-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="2552c-125">Cette propriété est héritée de l' [**\_ \_ événement**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="2552c-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="2552c-126">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2552c-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2552c-127">Notes</span><span class="sxs-lookup"><span data-stu-id="2552c-127">Remarks</span></span>

<span data-ttu-id="2552c-128">Pour se connecter à l’espace de noms « root \\ cimv2 \\ licences TS », le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="2552c-128">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="2552c-129">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**, qui peut être défini à l’aide de la fonction com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="2552c-129">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="2552c-130">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="2552c-130">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="2552c-131">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="2552c-131">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="2552c-132">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="2552c-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2552c-133">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2552c-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2552c-134">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="2552c-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2552c-135">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2552c-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2552c-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2552c-136">Requirements</span></span>



| <span data-ttu-id="2552c-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2552c-137">Requirement</span></span> | <span data-ttu-id="2552c-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="2552c-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2552c-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2552c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2552c-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2552c-140">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2552c-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2552c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2552c-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2552c-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2552c-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2552c-143">Namespace</span></span><br/>                | <span data-ttu-id="2552c-144">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="2552c-144">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2552c-145">MOF</span><span class="sxs-lookup"><span data-stu-id="2552c-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2552c-146"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2552c-146"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="2552c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="2552c-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2552c-148"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2552c-148"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

