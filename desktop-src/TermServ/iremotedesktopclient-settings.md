---
title: Propriété des paramètres IRemoteDesktopClient
description: Récupère l’objet de paramètres pour le client de conteneur d’applications protocole RDP (Remote Desktop Protocol) (RDP).
ms.assetid: 59999489-9ad0-4b85-9643-3b8355b817c2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriétés de paramètres
- Propriété de paramètres Services Bureau à distance, interface IRemoteDesktopClient
- Services Bureau à distance de l’interface IRemoteDesktopClient, propriété de paramètres
topic_type:
- apiref
api_name:
- IRemoteDesktopClient.Settings
- IRemoteDesktopClient.get_Settings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e84324eaa12610d7ab898cbcb181e7712bc021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942412"
---
# <a name="iremotedesktopclientsettings-property"></a><span data-ttu-id="c95e7-106">IRemoteDesktopClient :: Settings, propriété</span><span class="sxs-lookup"><span data-stu-id="c95e7-106">IRemoteDesktopClient::Settings property</span></span>

<span data-ttu-id="c95e7-107">Récupère l’objet de paramètres pour le client de conteneur d’applications protocole RDP (Remote Desktop Protocol) (RDP).</span><span class="sxs-lookup"><span data-stu-id="c95e7-107">Retrieves the settings object for the Remote Desktop Protocol (RDP) app container client.</span></span>

<span data-ttu-id="c95e7-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c95e7-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c95e7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c95e7-109">Syntax</span></span>


```C++
HRESULT get_Settings(
  [out, retval] IRemoteDesktopClientSettings **Settings
);
```



## <a name="property-value"></a><span data-ttu-id="c95e7-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c95e7-110">Property value</span></span>

<span data-ttu-id="c95e7-111">Objet de paramètres pour le client RDP.</span><span class="sxs-lookup"><span data-stu-id="c95e7-111">The settings object for the RDP client.</span></span>

## <a name="requirements"></a><span data-ttu-id="c95e7-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c95e7-112">Requirements</span></span>



| <span data-ttu-id="c95e7-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c95e7-113">Requirement</span></span> | <span data-ttu-id="c95e7-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c95e7-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c95e7-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c95e7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c95e7-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c95e7-116">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="c95e7-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c95e7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c95e7-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c95e7-118">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="c95e7-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c95e7-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="c95e7-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c95e7-120"><dt>MsTscAx.dll</dt></span></span> </dl>  |
| <span data-ttu-id="c95e7-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c95e7-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c95e7-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c95e7-122"><dt>MsTscAx.dll</dt></span></span> </dl>  |
| <span data-ttu-id="c95e7-123">IID</span><span class="sxs-lookup"><span data-stu-id="c95e7-123">IID</span></span><br/>                      | <span data-ttu-id="c95e7-124">IID \_ IRemoteDesktopClient est défini en tant que 57D25668-625A-4905-BE4E-304CAA13F89C</span><span class="sxs-lookup"><span data-stu-id="c95e7-124">IID\_IRemoteDesktopClient is defined as 57D25668-625A-4905-BE4E-304CAA13F89C</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c95e7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c95e7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c95e7-126">**IRemoteDesktopClient**</span><span class="sxs-lookup"><span data-stu-id="c95e7-126">**IRemoteDesktopClient**</span></span>](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
</dt> </dl>

 

