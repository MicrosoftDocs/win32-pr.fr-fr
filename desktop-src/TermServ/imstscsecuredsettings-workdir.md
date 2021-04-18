---
title: IMsTscSecuredSettings propriété WorkDir
description: Spécifie le répertoire de travail du programme de démarrage.
ms.assetid: e67f7274-be47-42c4-9267-a05bb93e6725
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété WorkDir
- Services Bureau à distance de la propriété WorkDir, interface IMsTscSecuredSettings
- Services Bureau à distance de l’interface IMsTscSecuredSettings, propriété WorkDir
- Services Bureau à distance de la propriété WorkDir, interface IMsRdpClientSecuredSettings
- Services Bureau à distance de l’interface IMsRdpClientSecuredSettings, propriété WorkDir
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.WorkDir
- IMsTscSecuredSettings.get_WorkDir
- IMsTscSecuredSettings.put_WorkDir
- IMsRdpClientSecuredSettings.WorkDir
- IMsRdpClientSecuredSettings.get_WorkDir
- IMsRdpClientSecuredSettings.put_WorkDir
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0a80b35ba682012150b4277d800bc4a3582e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513039"
---
# <a name="imstscsecuredsettingsworkdir-property"></a><span data-ttu-id="857d3-108">IMsTscSecuredSettings :: WorkDir, propriété</span><span class="sxs-lookup"><span data-stu-id="857d3-108">IMsTscSecuredSettings::WorkDir property</span></span>

<span data-ttu-id="857d3-109">Spécifie le répertoire de travail du programme de démarrage.</span><span class="sxs-lookup"><span data-stu-id="857d3-109">Specifies the working directory of the start program.</span></span>

<span data-ttu-id="857d3-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="857d3-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="857d3-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="857d3-111">Syntax</span></span>


```C++
HRESULT put_WorkDir(
  [in]  BSTR newVal
);

HRESULT get_WorkDir(
  [out] BSTR *pWorkDir
);
```



## <a name="property-value"></a><span data-ttu-id="857d3-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="857d3-112">Property value</span></span>

<span data-ttu-id="857d3-113">Nouveau répertoire de travail.</span><span class="sxs-lookup"><span data-stu-id="857d3-113">The new working directory.</span></span> <span data-ttu-id="857d3-114">La longueur maximale de cette chaîne est **le \_ chemin d’accès maximal**-1 caractères.</span><span class="sxs-lookup"><span data-stu-id="857d3-114">The maximum length of this string is **MAX\_PATH**-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="857d3-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="857d3-115">Error codes</span></span>

<span data-ttu-id="857d3-116">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="857d3-116">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="857d3-117">Notes</span><span class="sxs-lookup"><span data-stu-id="857d3-117">Remarks</span></span>

<span data-ttu-id="857d3-118">Pour plus d’informations, consultez la rubrique [fourniture de la sécurité du client RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="857d3-118">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="857d3-119">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="857d3-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="857d3-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="857d3-120">Requirements</span></span>



| <span data-ttu-id="857d3-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="857d3-121">Requirement</span></span> | <span data-ttu-id="857d3-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="857d3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="857d3-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="857d3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="857d3-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="857d3-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="857d3-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="857d3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="857d3-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="857d3-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="857d3-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="857d3-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="857d3-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="857d3-128"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="857d3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="857d3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="857d3-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="857d3-130"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="857d3-131">IID</span><span class="sxs-lookup"><span data-stu-id="857d3-131">IID</span></span><br/>                      | <span data-ttu-id="857d3-132">IID \_ IMsTscSecuredSettings est défini en tant que c9d65442-A0F9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="857d3-132">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="857d3-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="857d3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="857d3-134">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="857d3-134">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="857d3-135">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="857d3-135">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





