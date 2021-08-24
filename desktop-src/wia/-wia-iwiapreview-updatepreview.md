---
description: 'Obtient l’image non filtrée mise en cache par la méthode IWiaPreview :: GetNewPreview.'
ms.assetid: 121b6866-cca1-4170-9bdf-225491f942f5
title: 'IWiaPreview :: UpdatePreview, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.UpdatePreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: b5f48462d926d96acebf4a74f0a843d82f9cd97190585b954565d5da649ff9f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549689"
---
# <a name="iwiapreviewupdatepreview-method"></a>IWiaPreview :: UpdatePreview, méthode

Obtient l’image non filtrée mise en cache par la méthode [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lOptions* \[ dans\]
</dt> <dd>

Type : **long**

Spécifie si l’application requiert que le composant WIA 2,0 Preview transmette une sous-région de l’image mise en cache ou la totalité de l’image mise en cache au filtre de traitement d’image.

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**


</dt> <dd>

Transmettez la totalité de l’image mise en cache au filtre de traitement d’image.

</dd> </dl> </dd> <dt>

*pChildWiaItem* \[ dans\]
</dt> <dd>

Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Spécifie un pointeur vers l’élément [**IWiaItem2**](-wia-iwiaitem2.md) , qui est un enfant de l’élément **IWiaItem2** spécifié par le paramètre *pWiaItem2* de la méthode [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) . Ou, si l’application requiert une version préliminaire de l’ensemble du plateau, spécifie un pointeur vers le paramètre *pWiaItem2* de la méthode **IWiaPreview :: GetNewPreview** . Quand *pChildWiaItem* est un enfant du paramètre *pWiaItem2* de **IWiaPreview :: GetNewPreview**, cet élément enfant est généralement créé par le filtre de segmentation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode passe l’image mise en cache et non filtrée via le filtre de traitement d’image, qui écrit ensuite les données filtrées dans le flux fourni par l’application. Le composant d’aperçu WIA 2,0 récupère ce flux en appelant la méthode [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) du filtre de traitement d’image, qui appelle ensuite l’implémentation **GetNextStream** du rappel de l’application. Avant d’appeler **IWiaPreview :: UpdatePreview**, une application doit d’abord appeler [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) pour acquérir l’image à partir du scanneur ; dans le cas contraire, la méthode retourne une erreur.

Le composant WIA 2,0 Preview stocke l’image non filtrée téléchargée à partir du pilote. Il est possible que l’élément WIA 2,0 passé dans **IWiaPreview :: UpdatePreview** ne représente qu’une petite zone de l’image téléchargée à partir du pilote. Si c’est le cas, le composant WIA 2,0 Preview supprime en fait cette région de l’image mise en cache avant de la transmettre au filtre de traitement d’image, qui à son tour transmet les données de l’image filtrée à l’application.

Pour qu’une application transmette la totalité de l’image mise en cache au filtre de traitement d’image (qui à son tour la transmet à l’application), elle doit affecter à *lOptions* la valeur **WiaPreviewReturnOriginalImage** lors de l’appel de **IWiaPreview :: UpdatePreview**. Lors de la définition de *lOptions* sur **WiaPreviewReturnOriginalImage**, l’application doit s’assurer que les paramètres d’étendue ([**WIA \_ IPS \_ XEXTENT**](-wia-wiaitempropscanneritem.md) et **WIA \_ \_ YEXTENT**) de l’élément transmis à **IWiaPreview :: UpdatePreview** correspondent à l’image en cache intégral. Le filtre de traitement d’image n’a pas besoin d’être différent dans ce cas ; Il filtre simplement l’image, en fonction des propriétés de *pChildWiaItem* (en général, dans ce cas, *pChildWiaItem* est le même élément que celui qui a été passé à [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md)). Les différentes sous-régions sont ignorées et l’image entière est filtrée à l’aide des mêmes paramètres. Une application peut faire cela pour plusieurs raisons.

1.  Il se peut que l’application ne prenne pas en charge la modification des paramètres (tels que la [**\_ \_ luminosité IPS WIA**](-wia-wiaitempropscanneritem.md) et le **\_ \_ contraste des adresses IP WIA**) individuellement pour chaque région que le filtre de segmentation détecte (ou qu’il ne souhaite peut-être même pas utiliser le filtre de segmentation). Il est plus facile pour l’application d’appeler **IWiaPreview :: UpdatePreview** avec **WiaPreviewReturnOriginalImage** afin qu’elle reçoive toujours l’image complète à partir du composant WIA 2,0 Preview.
2.  Le composant WIA 2,0 Preview ne prend pas en charge le format d’image de l’image d’aperçu. dans ce cas, il ne peut pas effectuer les actions nécessaires pour couper la région souhaitée. la prise en charge du format d’image du composant WIA 2,0 Preview est limitée aux formats pour lesquels il existe Windows GDI+ des encodeurs et des décodeurs 1,1. Ces formats sont des bitmaps (BMP) (bitmap qui comprend BITMAPFILEHEADER), GIF (Graphics Interchange Format), JPEG, PNG (Portable Network Graphics) et TIFF (Tagged Image File Format).

Notez que si l’application transmet **WiaPreviewReturnOriginalImage** à **IWiaPreview :: UpdatePreview**, le composant WIA 2,0 Preview peut prendre en charge n’importe quel format d’image ou de pixel.

**IWiaPreview :: UpdatePreview** définit la [**propriété \_ \_ preview DPS WIA**](-wia-wiaitempropscannerdevice.md) (et la réinitialise avant qu’elle ne soit retournée, sauf si elle a été définie auparavant). Cela permet au pilote (et au matériel) et au filtre de traitement d’image de savoir que l’élément est une analyse de préversion.

Une application doit s’assurer *que pChildWiaItem* a le même format d’image (WIA) et la même résolution ([**WIA \_ IPS \_ XRES**](-wia-wiaitempropscanneritem.md) and **WIA \_ IPS \_ YRES**) que *pWiaItem* avait lors de sa transmission dans [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md).[**\_ \_**](-wia-wiaitempropcommonitem.md) Le format de l’élément enfant doit correspondre au format de l’image mise en cache du composant WIA 2,0 Preview (le composant WIA 2,0 Preview n’effectue aucune conversion d’image).

## <a name="examples"></a>Exemples

UpdateRegion doit être appelé chaque fois qu’un utilisateur modifie, par exemple, la luminosité ou le contraste pour l’élément enfant représenté par `dwRegionNumber` . Cet élément enfant a été créé précédemment par le filtre de segmentation ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md). L’image écrite dans l' [IStream](/windows/win32/api/objidl/nn-objidl-istream) est retournée par la méthode [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) de l’interface de rappel de transfert. Le code pour GetSubRegionItem est omis dans cet exemple.

Une fois que cette fonction a été appelée, une application redessine généralement la région à l’écran.


```C++
HRESULT
UpdateRegion(
   IN  DWORD dwRegionNumber)
{
   IWiaItem2 *pSubRegion = GetSubRegionItem(dwRegionNumber);

   return m_pWiaPreview->UpdatePreview(0,pSubRegion);
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
