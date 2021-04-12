---
description: 'Appelle le filtre de segmentation du pilote et passe l’image non filtrée mise en cache par la méthode IWiaPreview :: GetNewPreview au filtre.'
ms.assetid: 4ae817b5-7091-432e-b004-0e53ae14fdb2
title: IWiaPreview ::D méthode etectRegions (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 40665d2aae6e1e2dffa4356540afb05d45050492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201494"
---
# <a name="iwiapreviewdetectregions-method"></a>IWiaPreview ::D méthode etectRegions

Appelle le filtre de segmentation du pilote et passe l’image non filtrée mise en cache par la méthode [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) au filtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DetectRegions(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Non utilisé. A la valeur zéro (0).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                               | Description                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | L'opération a réussi.<br/>              |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl> | Le pilote ne prend pas en charge la segmentation.<br/> |
| <dl> <dt>**dispose**</dt> </dl>  | Code d’erreur COM standard.<br/>                |



 

## <a name="remarks"></a>Notes

Une application doit appeler [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) avant d’appeler cette fonction.

Lorsque le composant d’évaluation WIA (Windows Image Acquisition) 2,0 appelle **IWiaPreview ::D etectregions**, il appelle le filtre de segmentation de pilote et passe l’interface [**IWiaItem2**](-wia-iwiaitem2.md) précédemment passée à [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md). Il passe également l’image mise en cache en interne au filtre. Le filtre de segmentation utilise l’image mise en cache pour créer les extensions enfants.

Si une application modifie des propriétés de l’interface [**IWiaItem2**](-wia-iwiaitem2.md) après avoir appelé [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md), les propriétés d’origine doivent être restaurées avant que l’application n’appelle **IWiaPreview ::D etectregions**. Utilisez [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) et [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) pour restaurer les propriétés d’origine.

**IWiaPreview ::D etectregions** est utilisé pour déterminer les « sous-régions » de l’image mise en cache. Pour chaque sous-région détectée, un nouvel élément enfant WIA 2,0 est créé sous l’interface [**IWiaItem2**](-wia-iwiaitem2.md) . Pour chaque élément enfant, le filtre de segmentation doit définir les valeurs des propriétés WIA 2,0 suivantes : WIA \_ IPS \_ xpos, WIA \_ IPS \_ Posy, WIA \_ IPS \_ XEXTENT et WIA \_ IPS \_ YEXTENT. Un filtre plus avancé définit d’autres propriétés WIA 2,0, telles que \_ les adresses IP WIA par \_ \_ \_ décroisement X et les adresses IP WIA, décroissant \_ \_ Y, si le pilote prend en charge l’annulation de la distorsion. Les \_ Propriétés WIA IPS \_ xpos, WIA \_ IPS \_ Posy, WIA \_ IPS \_ XEXTENT et WIA \_ IPS \_ YEXTENT représentent le rectangle englobant de la zone à analyser.

Le pilote ne prend peut-être pas en charge la segmentation. Avant d’appeler **IWiaPreview ::D etectregions**, une application vérifie généralement si le pilote prend en charge la \_ propriété de \_ segmentation IPS WIA. Si la propriété n’est pas implémentée, la segmentation n’est pas prise en charge et **IWiaPreview ::D etectregions** échoue et retourne E \_ NOTIMPL.

L’application doit nettoyer les éléments enfants créés en appelant **IWiaPreview ::D etectregions**. Par exemple, si une application effectue un appel supplémentaire à **IWiaPreview ::D etectregions** sur le même élément, elle doit nettoyer les éléments enfants précédents.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




