---
description: Obtient un nouveau flux pour l’élément spécifié.
ms.assetid: fe25843c-2051-42fe-8737-eea39f6aeab9
title: 'IWiaTransferCallback :: GetNextStream, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.GetNextStream
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: fb2e92c9cade1dfd48efc3051b617997bf8473e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514628"
---
# <a name="iwiatransfercallbackgetnextstream-method"></a>IWiaTransferCallback :: GetNextStream, méthode

Obtient un nouveau flux pour l’élément spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNextStream(
  [in]  LONG    lFlags,
  [in]  BSTR    bstrItemName,
  [in]  BSTR    bstrFullItemName,
  [out] IStream **ppDestination
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Actuellement inutilisé. Doit être défini sur zéro (0).

</dd> <dt>

*bstrItemName* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie le nom de l’élément pour lequel créer un flux.

</dd> <dt>

*bstrFullItemName* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie le nom complet de l’élément pour lequel créer un flux.

</dd> <dt>

*ppDestination* \[ à\]
</dt> <dd>

Type : **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***

Reçoit l’adresse d’un pointeur vers le nouvel objet [IStream](/windows/win32/api/objidl/nn-objidl-istream) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Lorsque cette méthode est implémentée par un filtre de traitement d’image, le minipilote WIA (Windows Image Acquisition) 2,0 l’appelle lors de l’acquisition d’images pour récupérer le flux de destination à partir du client.

**IWiaTransferCallback :: GetNextStream** d’un filtre doit déléguer à la méthode de rappel de l’application. Le filtre utilise le flux retourné par l’implémentation **IWiaTransferCallback :: GetNextStream** du rappel d’application pour créer son propre flux qu’il transmet au service WIA 2,0. Le filtrage est effectué lorsque le flux du filtre appelle la méthode [IStream :: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) .

Le flux du filtre ne peut pas faire d’hypothèses sur le nombre d’octets qui y sont écrits à chaque écriture, car les données d’image non filtrées peuvent provenir du composant WIA 2,0 Preview et non du pilote. Le composant d’aperçu WIA 2,0 écrit toujours l’intégralité des données d’image non filtrées dans le flux du filtre une seule fois, ce qui signifie que le flux du filtre a une source en écriture. Si le pilote et le composant d’aperçu écrivent dans le flux du filtre, le flux du filtre ne peut pas supposer, par exemple, qu’il recevra l’en-tête complet la première fois que [IStream :: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) est appelé, alors que son pilote correspondant écrit toujours les données d’en-tête en premier dans une écriture. Elle ne peut pas non plus supposer qu’une écriture suivante ne contient qu’une seule ligne de numérisation. Le flux de filtrage peut donc avoir à compter le nombre d’octets écrits pour déterminer, par exemple, où les données de l’image démarrent.

L’implémentation **IWiaTransferCallback :: GetNextStream** du filtre de traitement d’image doit lire les propriétés nécessaires à son traitement d’image à partir de l’élément pour lequel l’image est acquise. Le filtre ne lit pas les propriétés directement à partir du *pWiaItem2* passé dans [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md). Au lieu de cela, le filtre doit appeler [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) sur cet élément WIA 2,0 pour obtenir l’élément WIA 2,0 réel. Cela est dû au fait que l’image en cours d’acquisition peut être un élément enfant de *pWiaItem2*. Par exemple, lors d’une acquisition de dossiers, le filtre utilise *pWiaItem2* pour obtenir les éléments enfants de *pWiaItem2* dans **IWiaTransferCallback :: GetNextStream** (lors d’une acquisition de dossier, le pilote retourne les images représentées par les éléments enfants de *pWiaItem2*). Il en va de même lorsque le composant WIA 2,0 Preview appelle le filtre de traitement d’image en passant un élément enfant WIA de l' 2,0 acquisition d’images.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
