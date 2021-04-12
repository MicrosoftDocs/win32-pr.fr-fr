---
title: Structure CB_TARGET_INFO (Cbclient. h)
description: Contient des informations sur l’ordinateur cible et les adresses IP où les connexions entrantes doivent être redirigées.
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- CB_TARGET_INFO structure Services Bureau à distance
- Pointeur de structure PCB_TARGET_INFO Services Bureau à distance
topic_type:
- apiref
api_name:
- CB_TARGET_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9bbb982636449075b758ac61178f5e97da47ce7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384211"
---
# <a name="cb_target_info-structure"></a><span data-ttu-id="c59f0-105">Structure des informations de la \_ cible CB \_</span><span class="sxs-lookup"><span data-stu-id="c59f0-105">CB\_TARGET\_INFO structure</span></span>

<span data-ttu-id="c59f0-106">Contient des informations sur l’ordinateur cible et les adresses IP où les connexions entrantes doivent être redirigées.</span><span class="sxs-lookup"><span data-stu-id="c59f0-106">Contains information about the target computer and IP addresses where incoming connections should be redirected.</span></span> <span data-ttu-id="c59f0-107">Cette structure est utilisée avec la méthode [**IConnectionBrokerClient :: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c59f0-107">This structure is used with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c59f0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c59f0-108">Syntax</span></span>


```C++
typedef struct {
  WCHAR ServerName[128];
  DWORD AddressCount;
  WCHAR Addresses[CB_MAX_ADDRESSES][CB_IPADDRESS_LEN];
} CB_TARGET_INFO, *PCB_TARGET_INFO;
```



## <a name="members"></a><span data-ttu-id="c59f0-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c59f0-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c59f0-110">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="c59f0-110">**ServerName**</span></span>
</dt> <dd>

<span data-ttu-id="c59f0-111">Représente le nom de domaine complet du serveur cible.</span><span class="sxs-lookup"><span data-stu-id="c59f0-111">Represents the fully qualified domain name of the target server.</span></span> <span data-ttu-id="c59f0-112">Pour un scénario de virtualisation des Bureau à distance (RDV), ce membre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c59f0-112">For a Remote Desktop virtualization (RDV) scenario, this member is **NULL**.</span></span> <span data-ttu-id="c59f0-113">Dans le cas d’un scénario d’hôte de session Bureau à distance, ce membre contient le nom du serveur sur lequel la connexion entrante est redirigée.</span><span class="sxs-lookup"><span data-stu-id="c59f0-113">For a Remote Desktop session host (RDSH) scenario, this member contains the server name where the incoming connection is redirected.</span></span>

</dd> <dt>

<span data-ttu-id="c59f0-114">**AddressCount**</span><span class="sxs-lookup"><span data-stu-id="c59f0-114">**AddressCount**</span></span>
</dt> <dd>

<span data-ttu-id="c59f0-115">Nombre d’entrées valides dans le tableau d' **adresses** .</span><span class="sxs-lookup"><span data-stu-id="c59f0-115">The number of valid entries in the **Addresses** array.</span></span>

</dd> <dt>

<span data-ttu-id="c59f0-116">**Adresses**</span><span class="sxs-lookup"><span data-stu-id="c59f0-116">**Addresses**</span></span>
</dt> <dd>

<span data-ttu-id="c59f0-117">Tableau de chaînes qui contient les adresses IP où les connexions entrantes sont redirigées.</span><span class="sxs-lookup"><span data-stu-id="c59f0-117">An array of strings that contain the IP addresses where the incoming connections are redirected.</span></span> <span data-ttu-id="c59f0-118">Le nombre d’éléments valides dans ce tableau est spécifié dans le membre **AddressCount** .</span><span class="sxs-lookup"><span data-stu-id="c59f0-118">The number of valid elements in this array is specified in the **AddressCount** member.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c59f0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c59f0-119">Requirements</span></span>



| <span data-ttu-id="c59f0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c59f0-120">Requirement</span></span> | <span data-ttu-id="c59f0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c59f0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c59f0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c59f0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c59f0-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c59f0-123">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="c59f0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c59f0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c59f0-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c59f0-125">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="c59f0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c59f0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c59f0-127"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c59f0-127"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c59f0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c59f0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c59f0-129">**IConnectionBrokerClient::GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="c59f0-129">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





