---
title: Message ICM_DECOMPRESSEX_QUERY (VFW. h)
description: le \_ message de requête ICM DECOMPRESSEX \_ interroge un pilote de compression vidéo pour déterminer s’il prend en charge un format d’entrée spécifique ou s’il peut décompresser un format d’entrée spécifique dans un format de sortie spécifique.
ms.assetid: 7778a52d-2ed8-495c-8656-c6beb1863499
keywords:
- message ICM_DECOMPRESSEX_QUERY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b2ef5999b9e0619ccbd9ccabd9bc5223b3bf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195315"
---
# <a name="icm_decompressex_query-message"></a>ICM \_ \_Message de requête DECOMPRESSEX

le message de **\_ \_ requête ICM DECOMPRESSEX** interroge un pilote de compression vidéo pour déterminer s’il prend en charge un format d’entrée spécifique ou s’il peut décompresser un format d’entrée spécifique dans un format de sortie spécifique.


```C++
ICM_DECOMPRESSEX_QUERY 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Pointeur vers une structure [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) contenant le format d’entrée.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Taille, en octets, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK si la décompression spécifiée est prise en charge ou ICERR BADFORMAT dans le \_ cas contraire.

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

 

 





