---
description: l’interface IWiaImageFilter est une interface d’extension implémentée par les développeurs de filtre de traitement d’image et appelée par Windows acquisition d’images (WIA) 2,0.
ms.assetid: 2abe913b-bb2b-486d-a3f4-d5932433fc82
title: Interface IWiaImageFilter (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: d7c85a25d7478e0ad51a1d427e74b69a743bc4203ed57b8929a3e4ec856d94b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813979"
---
# <a name="iwiaimagefilter-interface"></a>Interface IWiaImageFilter

l’interface **IWiaImageFilter** est une interface d’extension implémentée par les développeurs de filtre de traitement d’image et appelée par Windows acquisition d’images (WIA) 2,0.

## <a name="members"></a>Membres

L’interface **IWiaImageFilter** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaImageFilter** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWiaImageFilter** possède ces méthodes.



| Méthode                                                                | Description                                                                                             |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ApplyProperties**](-wia-iwiaimagefilter-applyproperties.md)       | Permet au filtre de traitement d’image d’écrire des propriétés sur le pilote (et l’appareil).<br/>     |
| [**FilterPreviewImage**](-wia-iwiaimagefilter-filterpreviewimage.md) | Filtre l’image d’aperçu.<br/>                                                                   |
| [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md)     | Initialise le filtre. Appelée par WIA 2,0 avant chaque téléchargement d’image. <br/>                       |
| [**SetNewCallback**](-wia-iwiaimagefilter-setnewcallback.md)         | Définit un nouveau rappel d’application pour le filtre de traitement d’image à utiliser pour le transfert des appels.<br/> |



 

## <a name="remarks"></a>Remarques

Les développeurs de filtres de traitement d’images doivent implémenter cette interface et l’interface [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) .

WIA 2,0 appelle des méthodes de filtre. Elles ne sont jamais appelées directement à partir d’une application.

Microsoft fournit le composant WIA 2,0 Preview, qui met en cache l’image d’aperçu non filtrée d’origine obtenue à partir du scanneur. Une application utilise [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour co-créer une instance du composant WIA 2,0 Preview (CLSID \_ WiaPreview), qui charge le filtre à l’aide de [**IWiaItem2 :: GetExtension**](-wia-iwiaitem2-getextension.md). Le filtre est appelé automatiquement quand l’application appelle [**IWiaTransfer ::D lécharger**](-wia-iwiatransfer-download.md).

Le filtre de traitement d’image est toujours exécuté lors de l’analyse d’une image. Une application ne peut pas acquérir une image à partir du scanneur sans appliquer d’abord le filtre d’acquisition d’images.

Un filtre doit implémenter une luminosité et un contraste au minimum. L’interface utilisateur commune, qui fournit des contrôles de luminosité et de contraste à l’utilisateur, peut afficher des aperçus précis de l’utilisateur.

Un filtre de traitement d’image ne doit jamais modifier le membre *lMessage* de la structure [**WiaTransferParams**](-wia-wiatransferparams.md) .

Pour lire les propriétés requises, le filtre de traitement d’image doit appeler [**IWiaPropertyStorage :: GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) sur l’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) qu’il obtient de l’élément en appelant [IWiaImageFilter :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Le filtre peut ensuite instancier une instance [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) sur ce flux pour lire les propriétés des éléments. Le filtre de traitement d’image ne doit pas appeler [IWiaPropertyStorage :: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) directement, car cette méthode appelle le pilote `drvReadItemProperties` , mais le service WIA 2,0 a déjà verrouillé le pilote dans l' `drvAcquireItemData` appel afin que cet appel expire et échoue.

Les propriétés qui intéressent le filtre peuvent, par exemple, être les paramètres de luminosité et de contraste. En règle générale, le filtre doit également lire le format d’image, ainsi que la propriété Preview, [**WIA \_ DPS \_ preview**](-wia-wiaitempropscannerdevice.md), à partir de *pWiaItem2*. Ces propriétés sont toutes utilisées dans le processus de filtrage.

Les composants WIA 2,0 écrivent toujours des données non filtrées dans le filtre de traitement d’image. L’algorithme de traitement d’image implémenté par le flux du filtre peut filtrer les données plusieurs fois et n’a pas à se préoccuper de produire les mêmes résultats que de filtrer les données une seule fois.

Le filtre doit prêter attention à la propriété d' [**\_ \_ Aperçu du DPS WIA**](-wia-wiaitempropscannerdevice.md) , en particulier si certaines tâches liées aux filtres sont gérées dans le matériel. Par exemple, un certain pilote peut modifier la luminosité de la lampe dans le matériel du scanneur en fonction de la façon dont l’application a défini la luminosité dans un élément WIA 2,0. Au cours de la dernière analyse (lorsque l’application appelle [**IWiaTransfer ::D lécharger**](-wia-iwiatransfer-download.md)), le pilote modifie généralement la lampe physique du scanneur. Dans ce cas, il se peut que le filtre de traitement d’image n’ait pas de traitement de luminosité du tout. Toutefois, au cours d’une analyse de préversion, le pilote ne doit pas modifier la luminosité de la lampe. à la place, il convient de prendre en charge uniquement le filtre de traitement d’image. Il est important que le composant WIA 2,0 Preview et le filtre de traitement d’image renvoient des images exactes en fonction des propriétés définies dans l’élément.

Un filtre de traitement d’image doit prendre en charge tous les formats d’image pris en charge par le pilote.

Le filtre de traitement d’image reçoit toujours une image correspondant à la zone de sélection définie dans l’élément pour lequel nous obtenons l’image. Notez, toutefois, que l’image peut avoir été pivotée par le pilote en cas de prise en charge de la propriété de [**\_ \_ rotation IPS WIA**](-wia-wiaitempropscanneritem.md) .

Le filtre de traitement d’image est créé via [**IWiaItem2 :: GetExtension**](-wia-iwiaitem2-getextension.md), généralement pas par l’application, mais par les composants WIA 2,0 lorsqu’une application appelle [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) ou [**IWiaTransfer ::D lécharger**](-wia-iwiatransfer-download.md).

L’interface **IWiaImageFilter** , comme toutes les interfaces COM (Component Object Model), hérite des méthodes d’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Méthodes IUnknown                                        | Description                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Retourne des pointeurs aux interfaces prises en charge. |
| [IUnknown :: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrémente le décompte de références.               |
| [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Décrémente le décompte de références.               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
