---
description: Contient le CLSID d’un chargeur de topologie pour la session multimédia.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: Attribut MF_SESSION_TOPOLOADER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9568193bbdbd46485015b6e5975db26fca2b552b23b7c227576e4e6544d69af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955128"
---
# <a name="mf_session_topoloader-attribute"></a>\_Attribut TOPOLOADER de session MF \_

Contient le CLSID d’un chargeur de topologie pour la session multimédia.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Remarques

Vous pouvez utiliser cet attribut pour fournir un chargeur de topologie personnalisé pour la session multimédia.

Définissez cet attribut à l’aide du paramètre *pConfiguration* de la fonction [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou de la fonction [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Si cet attribut est défini, la session multimédia appelle **CoCreateInstance** avec le CLSID spécifié lors de la création du chargeur de topologie. L’objet créé par ce CLSID doit exposer l’interface [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .

Si cet attribut n’est pas défini, la session multimédia crée le chargeur de topologie par défaut fourni dans Media Foundation.

Un chargeur de topologie doit prendre en charge les cloisonnements multithread. Vous devez enregistrer le chargeur de topologie en tant que ThreadingModel = « both ». En outre, si vous utilisez le chargeur de topologie à l’intérieur du chemin d’accès de média protégé (PMP), le chargeur de topologie doit être un composant approuvé. Pour plus d’informations, consultez [chemin d’accès au média protégé](protected-media-path.md).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Attributs de session multimédia](media-session-attributes.md)
</dt> <dt>

[Chargeurs de topologie personnalisés](custom-topology-loaders.md)
</dt> </dl>

 

 




