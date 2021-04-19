---
description: 'Version accessible à distance de la méthode IMFMediaTypeHandler :: GetCurrentMediaType.'
ms.assetid: f7f69adb-2a4a-47a9-bb92-ad9d005b962f
title: RemoteGetCurrentMediaType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc168198e8402d83538c046967d1d851ae2532b1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106524765"
---
# <a name="remotegetcurrentmediatype"></a>RemoteGetCurrentMediaType

Version accessible à distance de la méthode [**IMFMediaTypeHandler :: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) .

``` syntax
[call_as(GetCurrentMediaType)]
HRESULT RemoteGetCurrentMediaType(
    BYTE **ppbData,
    DWORD *pcbData
);
```

## <a name="remarks"></a>Notes

Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode. La méthode n’apparaît pas dans le vtable pour l’interface. Si [**GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.

Cette interface est disponible sur les plateformes suivantes si les composants redistribuables du kit de développement logiciel (SDK) Windows Media format 11 sont installés :

-   Windows XP avec Service Pack 2 (SP2) et versions ultérieures.
-   Windows XP Media Center Edition 2005 avec KB900325 (Windows XP Media Center Edition 2005) et KB925766 (correctif cumulatif de mise à jour d’octobre 2006 pour Windows XP Édition Media Center) installé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/>                                              |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
</dt> </dl>

 

 




