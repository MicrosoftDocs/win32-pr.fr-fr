---
title: Message ICM_CONFIGURE (VFW. h)
description: le \_ message ICM configurer indique à un pilote de compression vidéo d’afficher sa boîte de dialogue de configuration ou interroge un pilote de compression vidéo pour déterminer s’il dispose d’une boîte de dialogue de configuration.
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- message ICM_CONFIGURE Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021187"
---
# <a name="icm_configure-message"></a>ICM \_ CONFIGURER le message

le message **ICM \_ configurer** indique à un pilote de compression vidéo d’afficher sa boîte de dialogue de configuration ou interroge un pilote de compression vidéo pour déterminer s’il dispose d’une boîte de dialogue de configuration. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) .


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle de la fenêtre parente de la boîte de dialogue affichée. Vous pouvez déterminer si un pilote a une boîte de dialogue de configuration en spécifiant 1 dans ce paramètre, comme dans la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK si le pilote prend en charge ce message ou ICERR \_ non pris en charge dans le cas contraire.

## <a name="remarks"></a>Notes

Ce message est différent du message [**de \_ configuration du DRV**](drv-configure.md) utilisé pour la configuration matérielle. la boîte de dialogue de ce message doit permettre à l’utilisateur de définir et de modifier l’état interne référencé par les messages [**ICM \_ GETSTATE**](icm-getstate.md) et [**ICM \_ SETSTATE**](icm-setstate.md) . Par exemple, cette boîte de dialogue peut permettre à l’utilisateur de modifier des paramètres affectant le niveau de qualité et d’autres options de compression similaires.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de compression vidéo](video-compression-manager.md)
</dt> <dt>

[Messages de compression vidéo](video-compression-messages.md)
</dt> </dl>

 

 





