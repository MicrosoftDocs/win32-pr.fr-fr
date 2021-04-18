---
title: IRemoteDesktopClientTouchPointer, propriété activée
description: Indique si la fonctionnalité de pointeur tactile est activée sur le contrôle client du conteneur d’applications RDP.
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété Enabled
- Propriété Enabled Services Bureau à distance, IRemoteDesktopClientTouchPointer, interface
- Services Bureau à distance de l’interface IRemoteDesktopClientTouchPointer, propriété Enabled
topic_type:
- apiref
api_name:
- IRemoteDesktopClientTouchPointer.Enabled
- IRemoteDesktopClientTouchPointer.get_Enabled
- IRemoteDesktopClientTouchPointer.put_Enabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd534a9f8ec77903f196bbdfa10e1823a18dff4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509334"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a><span data-ttu-id="3e450-106">IRemoteDesktopClientTouchPointer :: Enabled, propriété</span><span class="sxs-lookup"><span data-stu-id="3e450-106">IRemoteDesktopClientTouchPointer::Enabled property</span></span>

<span data-ttu-id="3e450-107">Indique si la fonctionnalité de pointeur tactile est activée sur le contrôle client du conteneur d’applications RDP.</span><span class="sxs-lookup"><span data-stu-id="3e450-107">Whether the touch pointer feature is enabled on the RDP app container client control.</span></span>

<span data-ttu-id="3e450-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3e450-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e450-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e450-109">Syntax</span></span>


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a><span data-ttu-id="3e450-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3e450-110">Property value</span></span>

<span data-ttu-id="3e450-111">**true** si la fonctionnalité du pointeur tactile est activée ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="3e450-111">**true** if the touch pointer feature is enabled; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e450-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e450-112">Requirements</span></span>



| <span data-ttu-id="3e450-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e450-113">Requirement</span></span> | <span data-ttu-id="3e450-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e450-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e450-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e450-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3e450-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3e450-116">Windows 8</span></span><br/>                                                                                |
| <span data-ttu-id="3e450-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e450-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3e450-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e450-118">Windows Server 2012</span></span><br/>                                                                      |
| <span data-ttu-id="3e450-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3e450-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="3e450-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e450-120"><dt>MsTscAx.dll</dt></span></span> </dl>              |
| <span data-ttu-id="3e450-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3e450-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e450-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e450-122"><dt>MsTscAx.dll</dt></span></span> </dl>              |
| <span data-ttu-id="3e450-123">IID</span><span class="sxs-lookup"><span data-stu-id="3e450-123">IID</span></span><br/>                      | <span data-ttu-id="3e450-124">IID \_ IRemoteDesktopClientTouchPointer est défini en tant que 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9</span><span class="sxs-lookup"><span data-stu-id="3e450-124">IID\_IRemoteDesktopClientTouchPointer is defined as 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3e450-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e450-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e450-126">**IRemoteDesktopClientTouchPointer**</span><span class="sxs-lookup"><span data-stu-id="3e450-126">**IRemoteDesktopClientTouchPointer**</span></span>](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer)
</dt> </dl>

 

