---
description: 'Indicateurs utilisés par les méthodes IWiaDevMgr :: GetImageDlg, IWiaDevMgr2 :: GetImageDlg, IWiaItem ::D eviceDlg et IWiaItem2 ::D eviceDlg pour contrôler l’opération de la boîte de dialogue.'
ms.assetid: 468a3c9e-64f8-456d-aad9-fa7c6876fbe6
title: WiaFlag (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DEVICE_DIALOG_SINGLE_IMAGE
- WIA_DEVICE_DIALOG_USE_COMMON_UI
- WIA_SELECT_DEVICE_NODEFAULT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: c906f22e168ca29aadd2e9450fac6225c8b91c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519308"
---
# <a name="wiaflag"></a><span data-ttu-id="7ca42-103">WiaFlag</span><span class="sxs-lookup"><span data-stu-id="7ca42-103">WiaFlag</span></span>

<span data-ttu-id="7ca42-104">Indicateurs utilisés par les méthodes [**IWiaDevMgr :: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2 :: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md), [**IWiaItem ::D eviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)et [**IWiaItem2 ::D evicedlg**](-wia-iwiaitem2-devicedlg.md) pour contrôler l’opération de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="7ca42-104">Flags used by the [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md), [**IWiaItem::DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg), and [**IWiaItem2::DeviceDlg**](-wia-iwiaitem2-devicedlg.md) methods to control the dialog box operation.</span></span>



| <span data-ttu-id="7ca42-105">Constante</span><span class="sxs-lookup"><span data-stu-id="7ca42-105">Constant</span></span>                                                                                                                                                                                                                | <span data-ttu-id="7ca42-106">Description</span><span class="sxs-lookup"><span data-stu-id="7ca42-106">Description</span></span>                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DEVICE_DIALOG_SINGLE_IMAGE"></span><span id="wia_device_dialog_single_image"></span><dl> <span data-ttu-id="7ca42-107"><dt>**IMAGE unique de la boîte de dialogue de l' \_ appareil WIA \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca42-107"><dt>**WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE**</dt></span></span> </dl>     | <span data-ttu-id="7ca42-108">Limitez la sélection d’image à une seule image dans la boîte de dialogue acquisition d’image d’appareil.</span><span class="sxs-lookup"><span data-stu-id="7ca42-108">Restrict image selection to a single image in the device image acquisition dialog box.</span></span><br/>                                                                                                           |
| <span id="WIA_DEVICE_DIALOG_USE_COMMON_UI"></span><span id="wia_device_dialog_use_common_ui"></span><dl> <span data-ttu-id="7ca42-109"><dt>**\_boîte de dialogue de l’appareil WIA \_ \_ utiliser \_ \_ l’interface utilisateur commune**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca42-109"><dt>**WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI**</dt></span></span> </dl> | <span data-ttu-id="7ca42-110">Utilisez l’interface utilisateur du système, si elle est disponible, au lieu de l’interface utilisateur fournie par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7ca42-110">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="7ca42-111">Si l’interface utilisateur système n’est pas disponible, l’interface utilisateur du fournisseur est utilisée.</span><span class="sxs-lookup"><span data-stu-id="7ca42-111">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="7ca42-112">Si aucune interface utilisateur n’est disponible, la fonction retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="7ca42-112">If neither UI is available, the function returns E\_NOTIMPL.</span></span><br/>      |
| <span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span><dl> <span data-ttu-id="7ca42-113"><dt>**WIA- \_ Sélectionner un \_ appareil \_ par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca42-113"><dt>**WIA\_SELECT\_DEVICE\_NODEFAULT**</dt></span></span> </dl>               | <span data-ttu-id="7ca42-114">Forcez la méthode [**IWiaDevMgr :: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) ou [**IWiaDevMgr2 :: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) à afficher la boîte de dialogue **Sélectionner un périphérique** .</span><span class="sxs-lookup"><span data-stu-id="7ca42-114">Force the [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) or [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) method to display the **Select Device** dialog box.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7ca42-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ca42-115">Requirements</span></span>



| <span data-ttu-id="7ca42-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ca42-116">Requirement</span></span> | <span data-ttu-id="7ca42-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ca42-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca42-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ca42-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7ca42-119">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ca42-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="7ca42-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ca42-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7ca42-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ca42-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7ca42-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ca42-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ca42-123"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ca42-123"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




