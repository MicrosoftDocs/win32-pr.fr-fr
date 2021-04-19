---
description: La méthode SetExternalT120Address est appelée par une application pour configurer une adresse T. 120 externe pour l’échange de données.
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: 'IH323LineEx :: SetExternalT120Address, méthode (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09756aaf77ba36497b3059f7e93829d7d6a57b42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541049"
---
# <a name="ih323lineexsetexternalt120address-method"></a><span data-ttu-id="dcbfc-103">IH323LineEx :: SetExternalT120Address, méthode</span><span class="sxs-lookup"><span data-stu-id="dcbfc-103">IH323LineEx::SetExternalT120Address method</span></span>

<span data-ttu-id="dcbfc-104">\[**SetExternalT120Address** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dcbfc-104">\[**SetExternalT120Address** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dcbfc-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="dcbfc-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dcbfc-106">La méthode **SetExternalT120Address** est appelée par une application pour configurer une adresse T. 120 externe pour l’échange de données.</span><span class="sxs-lookup"><span data-stu-id="dcbfc-106">The **SetExternalT120Address** method is called by an application to configure an external T.120 address for data exchange.</span></span> <span data-ttu-id="dcbfc-107">La fonctionnalité T. 120 sera publiée au cours de la négociation H. 245, et l’adresse sera utilisée dans l’accusé de réception du canal logique ouvert afin que l’autre point de terminaison puisse configurer T. 120 sessions avec le service à l’écoute sur cette adresse.</span><span class="sxs-lookup"><span data-stu-id="dcbfc-107">T.120 capability will be advertised during the H.245 negotiation, and the address will be used in the open logic channel acknowledgement so that the other endpoint can set up T.120 sessions with the service listening on that address.</span></span> <span data-ttu-id="dcbfc-108">Si cette fonction n’est pas appelée, le fournisseur de services H. 323 ne publiera pas la fonctionnalité T. 120.</span><span class="sxs-lookup"><span data-stu-id="dcbfc-108">If this function is not called, the H.323 service provider will not advertise T.120 capability.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcbfc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcbfc-109">Syntax</span></span>


```C++
HRESULT SetExternalT120Address(
  [in] BOOL  fEnable,
  [in] DWORD dwIP,
  [in] WORD  wPort
);
```



## <a name="parameters"></a><span data-ttu-id="dcbfc-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcbfc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcbfc-111">*fEnable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dcbfc-111">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcbfc-112">**True** pour activer la fonctionnalité T. 120 ; **False** pour désactiver la fonctionnalité T. 120.</span><span class="sxs-lookup"><span data-stu-id="dcbfc-112">**TRUE** to enable T.120 capability; **FALSE** to disable T.120 capability.</span></span>

</dd> <dt>

<span data-ttu-id="dcbfc-113">*dwIP* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dcbfc-113">*dwIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcbfc-114">**Valeur DWORD** contenant l’adresse IP dans l’ordre d’octet de l’hôte du service T. 120 externe.</span><span class="sxs-lookup"><span data-stu-id="dcbfc-114">**DWORD** containing the IP address in host byte order of the external T.120 service.</span></span>

</dd> <dt>

<span data-ttu-id="dcbfc-115">*wPort* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dcbfc-115">*wPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcbfc-116">**Mot** contenant le port du service T. 120 externe.</span><span class="sxs-lookup"><span data-stu-id="dcbfc-116">**WORD** containing the port of the external T.120 service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcbfc-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dcbfc-117">Return value</span></span>

<span data-ttu-id="dcbfc-118">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="dcbfc-118">This method can return one of these values.</span></span>



| <span data-ttu-id="dcbfc-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dcbfc-119">Return code</span></span>                                                                          | <span data-ttu-id="dcbfc-120">Description</span><span class="sxs-lookup"><span data-stu-id="dcbfc-120">Description</span></span>                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="dcbfc-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dcbfc-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="dcbfc-122">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="dcbfc-122">Method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dcbfc-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcbfc-123">Requirements</span></span>



| <span data-ttu-id="dcbfc-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcbfc-124">Requirement</span></span> | <span data-ttu-id="dcbfc-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcbfc-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dcbfc-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="dcbfc-126">TAPI version</span></span><br/> | <span data-ttu-id="dcbfc-127">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="dcbfc-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="dcbfc-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcbfc-128">Header</span></span><br/>       | <dl> <span data-ttu-id="dcbfc-129"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcbfc-129"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="dcbfc-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dcbfc-130">Library</span></span><br/>      | <dl> <span data-ttu-id="dcbfc-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcbfc-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="dcbfc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dcbfc-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="dcbfc-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcbfc-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




