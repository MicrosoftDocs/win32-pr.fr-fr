---
title: Message ICM_DECOMPRESSEX_BEGIN (VFW. h)
description: le \_ message ICM DECOMPRESSEX \_ BEGIN notifie un pilote de compression vidéo pour préparer la décompression des données.
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- message ICM_DECOMPRESSEX_BEGIN Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ea082c91d48a9964348b762ce13631cd80af30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195316"
---
# <a name="icm_decompressex_begin-message"></a>ICM \_ DECOMPRESSEX le \_ message de début

le message **ICM \_ DECOMPRESSEX \_ BEGIN** notifie un pilote de compression vidéo pour préparer la décompression des données.


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Pointeur vers une structure [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) contenant les formats d’entrée et de sortie.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Taille, en octets, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK si la décompression spécifiée est prise en charge ou ICERR BADFORMAT dans le \_ cas contraire.

## <a name="remarks"></a>Notes

lorsque le pilote reçoit ce message, il doit allouer des tampons et effectuer toutes les opérations qui prennent du temps afin qu’il puisse traiter [**ICM messages \_ DECOMPRESSEX**](icm-decompressex.md) efficacement.

si vous souhaitez que le pilote décompresse les données directement à l’écran, envoyez le message [**ICM \_ DRAW \_ BEGIN**](icm-draw-begin.md) .

les messages de fin de **ICM \_ DECOMPRESSEX \_ BEGIN** et [**ICM \_ DECOMPRESSEX \_**](icm-decompressex-end.md) ne sont pas imbriqués. si votre pilote reçoit **ICM \_ DECOMPRESSEX \_ BEGIN** avant que la décompression ne soit arrêtée avec **ICM \_ \_ terminaison DECOMPRESSEX**, il doit redémarrer la décompression avec les nouveaux paramètres.

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

 

 





