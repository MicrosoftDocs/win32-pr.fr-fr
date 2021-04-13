---
title: IMsRdpClientSecuredSettings propriété AudioRedirectionMode
description: Spécifie les paramètres de redirection audio, qui spécifient s’il faut rediriger les sons ou lire des sons sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 6aa63a50-a714-4a9b-a4ec-c0551920467a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AudioRedirectionMode
- Services Bureau à distance de la propriété AudioRedirectionMode, interface IMsRdpClientSecuredSettings
- Services Bureau à distance de l’interface IMsRdpClientSecuredSettings, propriété AudioRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.AudioRedirectionMode
- IMsRdpClientSecuredSettings.get_AudioRedirectionMode
- IMsRdpClientSecuredSettings.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 858342811ec97def95031ebed0605b5a81cf80fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519226"
---
# <a name="imsrdpclientsecuredsettingsaudioredirectionmode-property"></a><span data-ttu-id="e3fb1-106">IMsRdpClientSecuredSettings :: AudioRedirectionMode, propriété</span><span class="sxs-lookup"><span data-stu-id="e3fb1-106">IMsRdpClientSecuredSettings::AudioRedirectionMode property</span></span>

<span data-ttu-id="e3fb1-107">Spécifie les paramètres de redirection audio, qui spécifient s’il faut rediriger les sons ou lire des sons sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="e3fb1-107">Specifies the audio redirection settings, which specify whether to redirect sounds or play sounds at the Remote Desktop Session Host (RD Session Host) server.</span></span>

<span data-ttu-id="e3fb1-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e3fb1-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3fb1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3fb1-109">Syntax</span></span>


```C++
HRESULT put_AudioRedirectionMode(
  [in]  LONG audioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] LONG *paudioRedirectionMode
);
```



## <a name="property-value"></a><span data-ttu-id="e3fb1-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e3fb1-110">Property value</span></span>

<span data-ttu-id="e3fb1-111">Nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="e3fb1-111">The new settings.</span></span> <span data-ttu-id="e3fb1-112">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e3fb1-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="e3fb1-113">0</span><span class="sxs-lookup"><span data-stu-id="e3fb1-113">0</span></span>
</dt> <dd>

<span data-ttu-id="e3fb1-114">Rediriger les sons vers le client.</span><span class="sxs-lookup"><span data-stu-id="e3fb1-114">Redirect sounds to the client.</span></span> <span data-ttu-id="e3fb1-115">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e3fb1-115">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="e3fb1-116">1</span><span class="sxs-lookup"><span data-stu-id="e3fb1-116">1</span></span>
</dt> <dd>

<span data-ttu-id="e3fb1-117">Émettre des sons sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="e3fb1-117">Play sounds at the remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="e3fb1-118">2</span><span class="sxs-lookup"><span data-stu-id="e3fb1-118">2</span></span>
</dt> <dd>

<span data-ttu-id="e3fb1-119">Désactiver la redirection du son ; ne lisez pas les sons sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="e3fb1-119">Disable sound redirection; do not play sounds at the server.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="e3fb1-120">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="e3fb1-120">Error codes</span></span>

<span data-ttu-id="e3fb1-121">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="e3fb1-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3fb1-122">Notes</span><span class="sxs-lookup"><span data-stu-id="e3fb1-122">Remarks</span></span>

<span data-ttu-id="e3fb1-123">Ces propriétés ne peuvent pas être définies lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="e3fb1-123">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="e3fb1-124">Pour plus d’informations, consultez la rubrique [fourniture de la sécurité du client RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="e3fb1-124">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="e3fb1-125">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e3fb1-125">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3fb1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3fb1-126">Requirements</span></span>



| <span data-ttu-id="e3fb1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3fb1-127">Requirement</span></span> | <span data-ttu-id="e3fb1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3fb1-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3fb1-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3fb1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e3fb1-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3fb1-130">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="e3fb1-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3fb1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e3fb1-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3fb1-132">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="e3fb1-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e3fb1-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="e3fb1-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3fb1-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="e3fb1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e3fb1-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3fb1-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3fb1-136"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="e3fb1-137">IID</span><span class="sxs-lookup"><span data-stu-id="e3fb1-137">IID</span></span><br/>                      | <span data-ttu-id="e3fb1-138">IID \_ IMsRdpClientSecuredSettings est défini en tant que 605befcf-39c1-45cc-A811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="e3fb1-138">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3fb1-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3fb1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3fb1-140">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="e3fb1-140">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





