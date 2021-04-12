---
title: IMsRdpClientAdvancedSettings propriété SasSequence
description: Spécifie la séquence d’accès sécurisé (SAS) que le client utilisera pour accéder à l’écran de connexion sur le serveur.
ms.assetid: ec1dc7b1-2bf1-447b-a768-08f28982a995
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SasSequence
- Services Bureau à distance de la propriété SasSequence, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété SasSequence
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SasSequence
- IMsRdpClientAdvancedSettings.get_SasSequence
- IMsRdpClientAdvancedSettings.put_SasSequence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf38a4e1f048e67613b92b3629aa96cca281b1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464319"
---
# <a name="imsrdpclientadvancedsettingssassequence-property"></a><span data-ttu-id="f7b14-106">IMsRdpClientAdvancedSettings :: SasSequence, propriété</span><span class="sxs-lookup"><span data-stu-id="f7b14-106">IMsRdpClientAdvancedSettings::SasSequence property</span></span>

<span data-ttu-id="f7b14-107">Spécifie la séquence d’accès sécurisé (SAS) que le client utilisera pour accéder à l’écran de connexion sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="f7b14-107">Specifies the secure access sequence (SAS) the client will use to access the login screen on the server.</span></span>

<span data-ttu-id="f7b14-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f7b14-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b14-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7b14-109">Syntax</span></span>


```C++
HRESULT put_SasSequence(
  [in]  LONG sasSequence
);

HRESULT get_SasSequence(
  [out] LONG *psasSequence
);
```



## <a name="property-value"></a><span data-ttu-id="f7b14-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f7b14-110">Property value</span></span>

<span data-ttu-id="f7b14-111">Valeur de **type long** qui contient l’indicateur SAS.</span><span class="sxs-lookup"><span data-stu-id="f7b14-111">A **LONG** value that contains the SAS indicator.</span></span> <span data-ttu-id="f7b14-112">La seule valeur prise en charge est 0xaa03, qui indique la séquence de touches CTRL + ALT + SUPPR standard.</span><span class="sxs-lookup"><span data-stu-id="f7b14-112">The only supported value is 0xaa03, which indicates the standard CTRL+ALT+DELETE sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b14-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f7b14-113">Remarks</span></span>

<span data-ttu-id="f7b14-114">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f7b14-114">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b14-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7b14-115">Requirements</span></span>



| <span data-ttu-id="f7b14-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7b14-116">Requirement</span></span> | <span data-ttu-id="f7b14-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7b14-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b14-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7b14-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b14-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7b14-119">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="f7b14-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7b14-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b14-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7b14-121">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="f7b14-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f7b14-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="f7b14-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7b14-123"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f7b14-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f7b14-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7b14-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7b14-125"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f7b14-126">IID</span><span class="sxs-lookup"><span data-stu-id="f7b14-126">IID</span></span><br/>                      | <span data-ttu-id="f7b14-127">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="f7b14-127">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f7b14-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7b14-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b14-129">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f7b14-129">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





