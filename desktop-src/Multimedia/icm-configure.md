---
title: Message ICM_CONFIGURE (VFW. h)
description: Le \_ message de configuration ICM informe un pilote de compression vidéo qu’il doit afficher sa boîte de dialogue de configuration ou interroge un pilote de compression vidéo pour déterminer s’il dispose d’une boîte de dialogue de configuration.
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- Message ICM_CONFIGURE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_CONFIGURE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9faae26fcf132abfa424b0db7a88670735d30727
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536918"
---
# <a name="icm_configure-message"></a><span data-ttu-id="4947e-104">\_Message de configuration ICM</span><span class="sxs-lookup"><span data-stu-id="4947e-104">ICM\_CONFIGURE message</span></span>

<span data-ttu-id="4947e-105">Le message de **\_ configuration ICM** informe un pilote de compression vidéo qu’il doit afficher sa boîte de dialogue de configuration ou interroge un pilote de compression vidéo pour déterminer s’il dispose d’une boîte de dialogue de configuration.</span><span class="sxs-lookup"><span data-stu-id="4947e-105">The **ICM\_CONFIGURE** message notifies a video compression driver to display its configuration dialog box or queries a video compression driver to determine if it has a configuration dialog box.</span></span> <span data-ttu-id="4947e-106">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) .</span><span class="sxs-lookup"><span data-stu-id="4947e-106">You can send this message explicitly or by using the [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) macro.</span></span>


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="4947e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4947e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4947e-108"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="4947e-108"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="4947e-109">Handle de la fenêtre parente de la boîte de dialogue affichée.</span><span class="sxs-lookup"><span data-stu-id="4947e-109">Handle to the parent window of the displayed dialog box.</span></span> <span data-ttu-id="4947e-110">Vous pouvez déterminer si un pilote a une boîte de dialogue de configuration en spécifiant 1 dans ce paramètre, comme dans la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) .</span><span class="sxs-lookup"><span data-stu-id="4947e-110">You can determine if a driver has a configuration dialog box by specifying  1 in this parameter, as in the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4947e-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4947e-111">Return Value</span></span>

<span data-ttu-id="4947e-112">Retourne ICERR \_ OK si le pilote prend en charge ce message ou ICERR \_ non pris en charge dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4947e-112">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4947e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="4947e-113">Remarks</span></span>

<span data-ttu-id="4947e-114">Ce message est différent du message [**de \_ configuration du DRV**](drv-configure.md) utilisé pour la configuration matérielle.</span><span class="sxs-lookup"><span data-stu-id="4947e-114">This message is different from the [**DRV\_CONFIGURE**](drv-configure.md) message used for hardware configuration.</span></span> <span data-ttu-id="4947e-115">La boîte de dialogue de ce message doit permettre à l’utilisateur de définir et de modifier l’état interne référencé par les messages [**ICM \_ GETSTATE**](icm-getstate.md) et [**ICM \_ SETSTATE**](icm-setstate.md) .</span><span class="sxs-lookup"><span data-stu-id="4947e-115">The dialog box for this message should let the user set and edit the internal state referenced by the [**ICM\_GETSTATE**](icm-getstate.md) and [**ICM\_SETSTATE**](icm-setstate.md) messages.</span></span> <span data-ttu-id="4947e-116">Par exemple, cette boîte de dialogue peut permettre à l’utilisateur de modifier des paramètres affectant le niveau de qualité et d’autres options de compression similaires.</span><span class="sxs-lookup"><span data-stu-id="4947e-116">For example, this dialog box can let the user change parameters affecting the quality level and other similar compression options.</span></span>

## <a name="requirements"></a><span data-ttu-id="4947e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4947e-117">Requirements</span></span>



| <span data-ttu-id="4947e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4947e-118">Requirement</span></span> | <span data-ttu-id="4947e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4947e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4947e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4947e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4947e-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4947e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4947e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4947e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4947e-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4947e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4947e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4947e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4947e-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4947e-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4947e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4947e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4947e-127">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="4947e-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="4947e-128">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="4947e-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





