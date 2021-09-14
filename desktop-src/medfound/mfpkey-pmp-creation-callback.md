---
description: Définit un rappel qui crée la session de média PMP pendant la résolution de la source.
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: MFPKEY_PMP_Creation_Callback, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b18e04a15e035a9e4dc04a4039ce230342031a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235950"
---
# <a name="mfpkey_pmp_creation_callback-property"></a>\_Propriété de \_ rappel de création PMP MFPKEY \_

Définit un rappel qui crée la [session de média PMP](pmp-media-session.md) pendant la résolution de la source.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**IUnknown\***

VT \_ inconnu

**punkVal**



## <a name="remarks"></a>Notes

Certains contenus protégés peuvent nécessiter l’utilisation de cette propriété. Dans ce cas, le processus de résolution source échoue avec le code d’erreur **MF \_ E \_ Resolution \_ requiert un \_ \_ \_ rappel de création PMP**.

Pour utiliser cette propriété, procédez comme suit.

1.  Appelez [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) pour créer une banque de propriétés.
2.  Implémentez l’interface de rappel [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
3.  Définissez la \_ \_ \_ propriété de rappel de création MFPKEY PMP sur la Banque de propriétés. La valeur est un pointeur vers l’implémentation de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
4.  Appelez [**IMFSourceResolver :: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl). Transmettez un pointeur vers la Banque de propriétés dans le paramètre *pProps* .

Dans la méthode [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de votre interface de rappel, procédez comme suit.

1.  Appelez [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) pour créer la [session de média PMP](pmp-media-session.md).
2.  Appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sur la session de média PMP sur un pointeur vers l’interface [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) .
3.  Appelez [**IMFAsyncResult :: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) sur l’objet de résultat qui est passé dans le paramètre *pAsyncResult* de [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Interrogez le pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) retourné pour l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
4.  Appelez [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) avec les paramètres suivants :
    -   *dwQueue*: **\_ \_ file d’attente \_ de rappel MFASYNC standard**
    -   *pCallback*: pointeur [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) obtenu à l’étape 3.
    -   *pState*: pointeur [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) obtenu à l’étape 2.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Session média PMP](pmp-media-session.md)
</dt> <dt>

[Chemin du média protégé](protected-media-path.md)
</dt> <dt>

[Résolveur source](source-resolver.md)
</dt> </dl>

 

 
