---
title: Structure CB_CONNECTION_INFO (Cbclient. h)
description: Contient des informations sur une demande de connexion entrante.
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- CB_CONNECTION_INFO structure Services Bureau à distance
- Pointeur de structure PCB_CONNECTION_INFO Services Bureau à distance
topic_type:
- apiref
api_name:
- CB_CONNECTION_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36370a4faa823f509d1f3356768add0ece9a6904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384212"
---
# <a name="cb_connection_info-structure"></a><span data-ttu-id="3bafc-105">Structure des informations de \_ connexion CB \_</span><span class="sxs-lookup"><span data-stu-id="3bafc-105">CB\_CONNECTION\_INFO structure</span></span>

<span data-ttu-id="3bafc-106">Contient des informations sur une demande de connexion entrante.</span><span class="sxs-lookup"><span data-stu-id="3bafc-106">Contains information about an incoming connection request.</span></span> <span data-ttu-id="3bafc-107">Cette structure est utilisée avec la méthode [**IConnectionBrokerClient :: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="3bafc-107">This structure is used with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bafc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bafc-108">Syntax</span></span>


```C++
typedef struct {
  WCHAR            UserName[CB_USERNAME_LENGTH];
  WCHAR            Domain[CB_DOMAINNAME_LENGTH];
  WCHAR            InitialProgram[CB_INITAPP_LENGTH];
  CB_RESOURCE_TYPE Resource;
  WCHAR            PluginName[CB_PLUGINNAME_LENGTH];
  WCHAR            FarmName[CB_FARMNAME_LENGTH];
  DWORD            dwVendorInfoLength;
  PBYTE            pVendorSpecificInfo;
} CB_CONNECTION_INFO, *PCB_CONNECTION_INFO;
```



## <a name="members"></a><span data-ttu-id="3bafc-109">Membres</span><span class="sxs-lookup"><span data-stu-id="3bafc-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="3bafc-110">**UserName**</span><span class="sxs-lookup"><span data-stu-id="3bafc-110">**UserName**</span></span>
</dt> <dd>

<span data-ttu-id="3bafc-111">Nom de l’utilisateur qui demande une session.</span><span class="sxs-lookup"><span data-stu-id="3bafc-111">The name of the user requesting a session.</span></span>

</dd> <dt>

<span data-ttu-id="3bafc-112">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="3bafc-112">**Domain**</span></span>
</dt> <dd>

<span data-ttu-id="3bafc-113">Nom du domaine dont le **nom d’utilisateur** est membre.</span><span class="sxs-lookup"><span data-stu-id="3bafc-113">The name of the domain that **UserName** is a member of.</span></span>

</dd> <dt>

<span data-ttu-id="3bafc-114">**InitialProgram**</span><span class="sxs-lookup"><span data-stu-id="3bafc-114">**InitialProgram**</span></span>
</dt> <dd>

<span data-ttu-id="3bafc-115">Chemin d’accès complet et nom de fichier du programme initial qui est démarré lorsque la session est démarrée.</span><span class="sxs-lookup"><span data-stu-id="3bafc-115">The fully qualified path and file name of the initial program that is started when the session is started.</span></span> <span data-ttu-id="3bafc-116">Affectez à ce membre une chaîne vide si aucun programme initial ne doit être démarré.</span><span class="sxs-lookup"><span data-stu-id="3bafc-116">Set this member to an empty string if no initial program should be started.</span></span>

</dd> <dt>

<span data-ttu-id="3bafc-117">**Ressource**</span><span class="sxs-lookup"><span data-stu-id="3bafc-117">**Resource**</span></span>
</dt> <dd>

<span data-ttu-id="3bafc-118">Valeur de l’énumération de [**\_ \_ type de ressource CB**](cb-resource-type.md) qui spécifie le type de ressource auquel la connexion entrante est connectée.</span><span class="sxs-lookup"><span data-stu-id="3bafc-118">A value of the [**CB\_RESOURCE\_TYPE**](cb-resource-type.md) enumeration that specifies the type of resource that the incoming connection is connecting to.</span></span> <span data-ttu-id="3bafc-119">Si le membre **PluginName** a la **valeur null**, ce membre est utilisé par l’connexion Bureau à distance Broker pour déterminer le plug-in à appeler pour déterminer l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="3bafc-119">If the **PluginName** member is **NULL**, this member is used to by the Remote Desktop Connection Broker to determine which plug-in to invoke for determining the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="3bafc-120">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="3bafc-120">**PluginName**</span></span>
</dt> <dd>

<span data-ttu-id="3bafc-121">Nom du plug-in à appeler pour déterminer l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="3bafc-121">The name of the plug-in to invoke to determine the target computer.</span></span> <span data-ttu-id="3bafc-122">Si ce paramètre a la **valeur null**, le membre de **ressource** est utilisé pour déterminer le plug-in à appeler.</span><span class="sxs-lookup"><span data-stu-id="3bafc-122">If this parameter is **NULL**, the **Resource** member is used to determine which plug-in to invoke.</span></span>

</dd> <dt>

<span data-ttu-id="3bafc-123">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="3bafc-123">**FarmName**</span></span>
</dt> <dd>

<span data-ttu-id="3bafc-124">Nom de la batterie de serveurs qui contient les ordinateurs, dont l’un sera l’ordinateur cible sur lequel la connexion sera redirigée.</span><span class="sxs-lookup"><span data-stu-id="3bafc-124">The name of the farm that contains the computers, one of which will be the target computer where the connection will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="3bafc-125">**dwVendorInfoLength**</span><span class="sxs-lookup"><span data-stu-id="3bafc-125">**dwVendorInfoLength**</span></span>
</dt> <dd>

<span data-ttu-id="3bafc-126">Ce membre est réservé pour un usage ultérieur.</span><span class="sxs-lookup"><span data-stu-id="3bafc-126">This member is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="3bafc-127">**pVendorSpecificInfo**</span><span class="sxs-lookup"><span data-stu-id="3bafc-127">**pVendorSpecificInfo**</span></span>
</dt> <dd>

<span data-ttu-id="3bafc-128">Ce membre est réservé pour un usage ultérieur.</span><span class="sxs-lookup"><span data-stu-id="3bafc-128">This member is reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3bafc-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3bafc-129">Requirements</span></span>



| <span data-ttu-id="3bafc-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3bafc-130">Requirement</span></span> | <span data-ttu-id="3bafc-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bafc-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3bafc-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3bafc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3bafc-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3bafc-133">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="3bafc-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3bafc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3bafc-135">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3bafc-135">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="3bafc-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="3bafc-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bafc-137"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bafc-137"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bafc-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bafc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bafc-139">**IConnectionBrokerClient::GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="3bafc-139">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





