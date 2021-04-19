---
description: 'Version accessible à distance de la méthode IMFPMPHost :: CreateObjectByCLSID.'
ms.assetid: be96be6d-47de-4d2b-81fc-13079de33888
title: RemoteCreateObjectByCLSID (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e57307ece851484675d01a699037647efad771d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520392"
---
# <a name="remotecreateobjectbyclsid"></a><span data-ttu-id="4f2ee-103">RemoteCreateObjectByCLSID</span><span class="sxs-lookup"><span data-stu-id="4f2ee-103">RemoteCreateObjectByCLSID</span></span>

<span data-ttu-id="4f2ee-104">Version accessible à distance de la méthode [**IMFPMPHost :: CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) .</span><span class="sxs-lookup"><span data-stu-id="4f2ee-104">Remotable version of the [**IMFPMPHost::CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) method.</span></span>

``` syntax
[call_as(CreateObjectByCLSID)]
HRESULT RemoteCreateObjectByCLSID( 
    REFCLSID clsid,
    BYTE *pbData, 
    DWORD cbData, 
    REFIID riid,
    void **ppv
);
```

## <a name="remarks"></a><span data-ttu-id="4f2ee-105">Notes</span><span class="sxs-lookup"><span data-stu-id="4f2ee-105">Remarks</span></span>

<span data-ttu-id="4f2ee-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4f2ee-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="4f2ee-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="4f2ee-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="4f2ee-108">Si [**CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="4f2ee-108">If [**CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f2ee-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f2ee-109">Requirements</span></span>



| <span data-ttu-id="4f2ee-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f2ee-110">Requirement</span></span> | <span data-ttu-id="4f2ee-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f2ee-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f2ee-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f2ee-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4f2ee-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f2ee-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4f2ee-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f2ee-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4f2ee-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f2ee-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4f2ee-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f2ee-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f2ee-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f2ee-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="4f2ee-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4f2ee-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="4f2ee-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f2ee-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="4f2ee-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f2ee-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f2ee-121">**IMFPMPHost**</span><span class="sxs-lookup"><span data-stu-id="4f2ee-121">**IMFPMPHost**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost)
</dt> <dt>

[<span data-ttu-id="4f2ee-122">Session média PMP</span><span class="sxs-lookup"><span data-stu-id="4f2ee-122">PMP Media Session</span></span>](pmp-media-session.md)
</dt> <dt>

[<span data-ttu-id="4f2ee-123">Chemin du média protégé</span><span class="sxs-lookup"><span data-stu-id="4f2ee-123">Protected Media Path</span></span>](protected-media-path.md)
</dt> </dl>

 

 




