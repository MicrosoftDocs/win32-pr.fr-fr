---
title: Message ICM_DECOMPRESSEX_BEGIN (VFW. h)
description: Le \_ message DECOMPRESSEX de \_ début ICM indique à un pilote de compression vidéo de préparer la décompression des données.
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- Message ICM_DECOMPRESSEX_BEGIN Windows Multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742956"
---
# <a name="icm_decompressex_begin-message"></a>Message de début de \_ DECOMPRESSEX ICM \_

Le **message \_ DECOMPRESSEX de \_ début ICM** indique à un pilote de compression vidéo de préparer la décompression des données.


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

Lorsque le pilote reçoit ce message, il doit allouer des tampons et effectuer des opérations qui prennent du temps pour pouvoir traiter efficacement les messages [**\_ DECOMPRESSEX ICM**](icm-decompressex.md) .

Si vous souhaitez que le pilote décompresse les données directement à l’écran, envoyez le message d’accueil de [**\_ \_ dessin ICM**](icm-draw-begin.md) .

Les messages End **\_ DECOMPRESSEX \_ Begin** et [**ICM \_ DECOMPRESSEX \_ end**](icm-decompressex-end.md) ne sont pas imbriqués. Si votre pilote reçoit **des \_ DECOMPRESSEX \_ ICM** avant que la décompression ne soit arrêtée avec l' **\_ \_ extrémité DECOMPRESSEX ICM**, il doit redémarrer la décompression avec les nouveaux paramètres.

## <a name="requirements"></a>Configuration requise



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

 

 





