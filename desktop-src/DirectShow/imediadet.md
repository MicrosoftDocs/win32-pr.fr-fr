---
description: L’interface IMediaDet récupère des informations sur un fichier multimédia, telles que le nombre de flux, le type de média, la durée et la fréquence d’images de chaque flux.
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: Interface IMediaDet (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ca5c87a1424872491aba5dcf4e01011872e9ff36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543587"
---
# <a name="imediadet-interface"></a>Interface IMediaDet

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IMediaDet` interface récupère des informations sur un fichier multimédia, telles que le nombre de flux, ainsi que le type de média, la durée et la fréquence d’images de chaque flux. Il contient également des méthodes pour récupérer des frames individuels à partir d’un flux vidéo. L’objet [détecteur de média (MediaDet)](media-detector--mediadet.md) expose cette interface.

Pour obtenir des informations sur un fichier à l’aide de cette interface, procédez comme suit :

1.  Créez une instance de l’objet MediaDet en appelant **CoCreateInstance**. L’ID de classe est CLSID \_ MediaDet.
2.  Appelez [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) pour spécifier le nom du fichier source.
3.  Appelez [**IMediaDet :: obtenir \_ OutputStreams**](imediadet-get-outputstreams.md) pour obtenir le nombre de flux de sortie dans la source.
4.  Appelez [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md) pour spécifier un flux particulier.
5.  Appelez l’une des méthodes suivantes :
    -   [**IMediaDet :: obtient la \_ cadence**](imediadet-get-framerate.md)
    -   [**IMediaDet :: obtient \_ StreamLength**](imediadet-get-streamlength.md)
    -   [**IMediaDet :: obtient \_ StreamMediaType**](imediadet-get-streammediatype.md)
    -   [**IMediaDet :: obtient \_ StreamType**](imediadet-get-streamtype.md)

Pour récupérer une image vidéo, appelez [**IMediaDet :: GetBitmapBits**](imediadet-getbitmapbits.md) ou [**IMediaDet :: WriteBitmapBits**](imediadet-writebitmapbits.md). Le frame retourné est toujours au format RGB 24 bits.

> [!Note]  
> N’utilisez pas le même objet MediaDet avec plusieurs fichiers. Pour obtenir des informations ou des images vidéo à partir de plusieurs fichiers, utilisez des instances MediaDet distinctes.

 

L’interface **IMediaDet** ne prend pas en charge les formats [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . vous ne pouvez donc pas utiliser cette interface pour obtenir des champs entrelacés ou des informations sur l’entrelacement. En outre, si le décodeur en amont prend en charge uniquement **VIDEOINFOHEADER2**, vous ne pouvez pas utiliser `IMediaDet` . Cela peut être le cas avec un décodeur MPEG-2, par exemple. En outre, l' `IMediaDet` interface ignore tous les flux du fichier qui ne sont pas des données vidéo ou audio. Par exemple, si le fichier contient un flux audio, un flux de données et un flux vidéo, la méthode **obtenir \_ OutputStreams** ne signale que deux flux (l’audio et la vidéo).

## <a name="members"></a>Membres

L’interface **IMediaDet** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMediaDet** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IMediaDet** possède ces méthodes.



| Méthode                                                        | Description                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)  | Bascule le détecteur de média en mode de manipulation bitmap et recherche le graphique de filtre à une heure spécifiée.<br/> |
| [**Obtient \_ CurrentStream**](imediadet-get-currentstream.md)     | Récupère le numéro de flux actuellement utilisé par le détecteur de média.<br/>                               |
| [**récupérer le \_ nom de fichier**](imediadet-get-filename.md)               | Récupère le nom du fichier source actuellement utilisé par le détecteur de média.<br/>                     |
| [**recevoir le \_ filtre**](imediadet-get-filter.md)                   | Récupère un pointeur vers le filtre source actuellement utilisé par le détecteur de média.<br/>                  |
| [**recevoir une \_ cadence**](imediadet-get-framerate.md)             | Récupère la fréquence d’images du flux actuel.<br/>                                                 |
| [**Obtient \_ OutputStreams**](imediadet-get-outputstreams.md)     | Récupère le nombre de flux audio et vidéo contenus dans la source du média.<br/>                  |
| [**Obtient \_ StreamLength**](imediadet-get-streamlength.md)       | Récupère la durée du flux actuel.<br/>                                                   |
| [**Obtient \_ StreamMediaType**](imediadet-get-streammediatype.md) | Récupère le type de média du flux actuel.<br/>                                                 |
| [**Obtient \_ StreamType**](imediadet-get-streamtype.md)           | Récupère l’identificateur global unique (GUID) pour le type de média du flux actuel.<br/>       |
| [**Obtient \_ StreamTypeB**](imediadet-get-streamtypeb.md)         | Récupère une chaîne représentant le GUID du type de média pour le flux actuel.<br/>              |
| [**GetBitmapBits**](imediadet-getbitmapbits.md)              | Récupère une image vidéo à l’heure du média spécifiée.<br/>                                            |
| [**GetSampleGrabber**](imediadet-getsamplegrabber.md)        | Récupère un pointeur vers l’interface [**ISampleGrabber**](isamplegrabber.md) .<br/>                  |
| [**put \_ CurrentStream**](imediadet-put-currentstream.md)     | Spécifie le numéro de flux du détecteur de média à utiliser.<br/>                                      |
| [**Placer le \_ nom de fichier**](imediadet-put-filename.md)               | Spécifie le nom du fichier source pour le détecteur de média à utiliser.<br/>                            |
| [**Placer le \_ filtre**](imediadet-put-filter.md)                   | Spécifie un filtre source pour le détecteur de média à utiliser.<br/>                                        |
| [**WriteBitmapBits**](imediadet-writebitmapbits.md)          | Récupère une image vidéo à l’heure du média spécifiée et l’écrit dans un fichier.<br/>                    |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
