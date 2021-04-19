---
title: Propriété fullscreen IMsTscSecuredSettings
description: Spécifie l’État plein écran du contrôle client.
ms.assetid: f65c2fa3-b2d0-4e64-bf1e-08394c91eda8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété fullscreen
- Services Bureau à distance de propriété fullscreen, interface IMsTscSecuredSettings
- Services Bureau à distance de l’interface IMsTscSecuredSettings, propriété fullscreen
- Services Bureau à distance de propriété fullscreen, interface IMsRdpClientSecuredSettings
- Services Bureau à distance de l’interface IMsRdpClientSecuredSettings, propriété fullscreen
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.Fullscreen
- IMsTscSecuredSettings.get_Fullscreen
- IMsTscSecuredSettings.put_Fullscreen
- IMsRdpClientSecuredSettings.Fullscreen
- IMsRdpClientSecuredSettings.get_Fullscreen
- IMsRdpClientSecuredSettings.put_Fullscreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c3b3208edf3476fcd110d7729d97d9817cb929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513031"
---
# <a name="imstscsecuredsettingsfullscreen-property"></a><span data-ttu-id="56ede-108">IMsTscSecuredSettings :: fullscreen, propriété</span><span class="sxs-lookup"><span data-stu-id="56ede-108">IMsTscSecuredSettings::Fullscreen property</span></span>

<span data-ttu-id="56ede-109">Spécifie l’État plein écran du contrôle client.</span><span class="sxs-lookup"><span data-stu-id="56ede-109">Specifies the full-screen state of the client control.</span></span>

<span data-ttu-id="56ede-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="56ede-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="56ede-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56ede-111">Syntax</span></span>


```C++
HRESULT put_Fullscreen(
  [in]  BOOL fFullScreen
);

HRESULT get_Fullscreen(
  [out] BOOL *pfFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="56ede-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="56ede-112">Property value</span></span>

<span data-ttu-id="56ede-113">Affectez la valeur **true** à ce paramètre si le contrôle doit utiliser le mode plein écran et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="56ede-113">Set this parameter to **TRUE** if the control should use full-screen mode and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="56ede-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="56ede-114">Error codes</span></span>

<span data-ttu-id="56ede-115">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="56ede-115">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="56ede-116">Notes</span><span class="sxs-lookup"><span data-stu-id="56ede-116">Remarks</span></span>

<span data-ttu-id="56ede-117">Pour plus d’informations sur cette méthode, consultez la page [fourniture de la sécurité du client RDP](providing-for-rdp-client-security.md).</span><span class="sxs-lookup"><span data-stu-id="56ede-117">For more information about this method, see [Providing for RDP Client Security](providing-for-rdp-client-security.md).</span></span>

<span data-ttu-id="56ede-118">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="56ede-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

<span data-ttu-id="56ede-119">Notez que, bien que l’utilisation de cette propriété soit limitée aux zones de sécurité des URL d’Internet Explorer autorisées, un utilisateur peut toujours passer en mode plein écran après l’établissement de la connexion en appuyant sur la combinaison de [touches de raccourci](terminal-services-shortcut-keys.md) du mode plein écran (Ctrl + Alt + Attn).</span><span class="sxs-lookup"><span data-stu-id="56ede-119">Note that although the use of this property is restricted to the allowed Internet Explorer URL security zones, a user can always change to full-screen mode after the connection has been established by pressing the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

<span data-ttu-id="56ede-120">Cette méthode peut être appelée pendant l’établissement de la connexion cliente.</span><span class="sxs-lookup"><span data-stu-id="56ede-120">This method can be called while the client connection is established.</span></span>

<span data-ttu-id="56ede-121">Vous devez appeler la méthode [**IMsRdpClientNonScriptable3 ::p ut \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) avant d’appeler la méthode **IMsTscSecuredSettings ::P ut \_ fullscreen** ou [**IMsRdpClient ::p ut \_ fullscreen**](imsrdpclient-fullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="56ede-121">You must call the [**IMsRdpClientNonScriptable3::put\_ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) method before you call the **IMsTscSecuredSettings::put\_Fullscreen** method or the [**IMsRdpClient::put\_Fullscreen**](imsrdpclient-fullscreen.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="56ede-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56ede-122">Requirements</span></span>



| <span data-ttu-id="56ede-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56ede-123">Requirement</span></span> | <span data-ttu-id="56ede-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="56ede-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="56ede-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56ede-125">Minimum supported client</span></span><br/> | <span data-ttu-id="56ede-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56ede-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="56ede-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56ede-127">Minimum supported server</span></span><br/> | <span data-ttu-id="56ede-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56ede-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="56ede-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="56ede-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="56ede-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56ede-130"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="56ede-131">DLL</span><span class="sxs-lookup"><span data-stu-id="56ede-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56ede-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56ede-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="56ede-133">IID</span><span class="sxs-lookup"><span data-stu-id="56ede-133">IID</span></span><br/>                      | <span data-ttu-id="56ede-134">IID \_ IMsTscSecuredSettings est défini en tant que c9d65442-A0F9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="56ede-134">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="56ede-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56ede-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ede-136">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="56ede-136">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="56ede-137">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="56ede-137">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





