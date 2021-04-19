---
title: IMsTscSecuredSettings propriété StartProgram
description: Spécifie le programme à démarrer sur le serveur distant lors de la connexion.
ms.assetid: bd2a5ced-468b-48db-ad51-9940577a0310
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété StartProgram
- Services Bureau à distance de la propriété StartProgram, interface IMsTscSecuredSettings
- Services Bureau à distance de l’interface IMsTscSecuredSettings, propriété StartProgram
- Services Bureau à distance de la propriété StartProgram, interface IMsRdpClientSecuredSettings
- Services Bureau à distance de l’interface IMsRdpClientSecuredSettings, propriété StartProgram
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.StartProgram
- IMsTscSecuredSettings.get_StartProgram
- IMsTscSecuredSettings.put_StartProgram
- IMsRdpClientSecuredSettings.StartProgram
- IMsRdpClientSecuredSettings.get_StartProgram
- IMsRdpClientSecuredSettings.put_StartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e79612855117f48e629e9a06246f3fad922d37f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516098"
---
# <a name="imstscsecuredsettingsstartprogram-property"></a><span data-ttu-id="4f6f8-108">IMsTscSecuredSettings :: StartProgram, propriété</span><span class="sxs-lookup"><span data-stu-id="4f6f8-108">IMsTscSecuredSettings::StartProgram property</span></span>

<span data-ttu-id="4f6f8-109">Spécifie le programme à démarrer sur le serveur distant lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="4f6f8-109">Specifies the program to be started on the remote server upon connection.</span></span>

<span data-ttu-id="4f6f8-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4f6f8-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f6f8-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f6f8-111">Syntax</span></span>


```C++
HRESULT put_StartProgram(
  [in]  BSTR newVal
);

HRESULT get_StartProgram(
  [out] BSTR *pStartProgram
);
```



## <a name="property-value"></a><span data-ttu-id="4f6f8-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4f6f8-112">Property value</span></span>

<span data-ttu-id="4f6f8-113">Nom du nouveau programme de démarrage.</span><span class="sxs-lookup"><span data-stu-id="4f6f8-113">The name of the new start program.</span></span> <span data-ttu-id="4f6f8-114">La longueur maximale de cette chaîne est **le \_ chemin d’accès maximal**-1 caractères.</span><span class="sxs-lookup"><span data-stu-id="4f6f8-114">The maximum length of this string is **MAX\_PATH**-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4f6f8-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4f6f8-115">Error codes</span></span>

<span data-ttu-id="4f6f8-116">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="4f6f8-116">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f6f8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4f6f8-117">Remarks</span></span>

<span data-ttu-id="4f6f8-118">Si la valeur de cette propriété n’est pas définie, la commande d’interpréteur de commandes de l’utilisateur de la session est exécutée.</span><span class="sxs-lookup"><span data-stu-id="4f6f8-118">If the value of this property is not set, the session user's shell command will be run.</span></span> <span data-ttu-id="4f6f8-119">La commande d’interpréteur de commandes sera lue à partir de la valeur de Registre suivante sur le serveur :</span><span class="sxs-lookup"><span data-stu-id="4f6f8-119">The shell command will be read from the following registry value on the server:</span></span>

<span data-ttu-id="4f6f8-120">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **Shell**</span><span class="sxs-lookup"><span data-stu-id="4f6f8-120">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**WinLogon**\\**Shell**</span></span>

<span data-ttu-id="4f6f8-121">Pour plus d’informations, consultez la rubrique [fourniture de la sécurité du client RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="4f6f8-121">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="4f6f8-122">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4f6f8-122">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f6f8-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f6f8-123">Requirements</span></span>



| <span data-ttu-id="4f6f8-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f6f8-124">Requirement</span></span> | <span data-ttu-id="4f6f8-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f6f8-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f6f8-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f6f8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4f6f8-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f6f8-127">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="4f6f8-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f6f8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4f6f8-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f6f8-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4f6f8-130">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4f6f8-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f6f8-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f6f8-131"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="4f6f8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4f6f8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f6f8-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f6f8-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="4f6f8-134">IID</span><span class="sxs-lookup"><span data-stu-id="4f6f8-134">IID</span></span><br/>                      | <span data-ttu-id="4f6f8-135">IID \_ IMsTscSecuredSettings est défini en tant que c9d65442-A0F9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="4f6f8-135">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f6f8-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f6f8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f6f8-137">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="4f6f8-137">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="4f6f8-138">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="4f6f8-138">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





