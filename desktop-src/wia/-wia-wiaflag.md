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
# <a name="wiaflag"></a>WiaFlag

Indicateurs utilisés par les méthodes [**IWiaDevMgr :: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2 :: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md), [**IWiaItem ::D eviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)et [**IWiaItem2 ::D evicedlg**](-wia-iwiaitem2-devicedlg.md) pour contrôler l’opération de la boîte de dialogue.



| Constante                                                                                                                                                                                                                | Description                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DEVICE_DIALOG_SINGLE_IMAGE"></span><span id="wia_device_dialog_single_image"></span><dl> <dt>**IMAGE unique de la boîte de dialogue de l' \_ appareil WIA \_ \_ \_**</dt> </dl>     | Limitez la sélection d’image à une seule image dans la boîte de dialogue acquisition d’image d’appareil.<br/>                                                                                                           |
| <span id="WIA_DEVICE_DIALOG_USE_COMMON_UI"></span><span id="wia_device_dialog_use_common_ui"></span><dl> <dt>**\_boîte de dialogue de l’appareil WIA \_ \_ utiliser \_ \_ l’interface utilisateur commune**</dt> </dl> | Utilisez l’interface utilisateur du système, si elle est disponible, au lieu de l’interface utilisateur fournie par le fournisseur. Si l’interface utilisateur système n’est pas disponible, l’interface utilisateur du fournisseur est utilisée. Si aucune interface utilisateur n’est disponible, la fonction retourne E \_ NOTIMPL.<br/>      |
| <span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span><dl> <dt>**WIA- \_ Sélectionner un \_ appareil \_ par défaut**</dt> </dl>               | Forcez la méthode [**IWiaDevMgr :: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) ou [**IWiaDevMgr2 :: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) à afficher la boîte de dialogue **Sélectionner un périphérique** .<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




