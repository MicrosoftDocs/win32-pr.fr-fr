---
description: La méthode GetConnectedMediaType récupère le type de média pour la connexion sur la broche d’entrée de la accroche d’échantillon.
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: 'ISampleGrabber :: GetConnectedMediaType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetConnectedMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 03dc0c9763bdea75569f9447becb749bf284ae2ad7d77427f6dfc2f0aac58382
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818058"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a>ISampleGrabber :: GetConnectedMediaType, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetConnectedMediaType` méthode récupère le type de média pour la connexion sur la broche d’entrée de la accroche d’échantillon.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetConnectedMediaType(
   AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pType* 
</dt> <dd>

Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) allouée par l’appelant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs suivantes.



| Code de retour                                                                                           | Description                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_pointeur E**</dt> </dl>             | Argument de pointeur **null** .<br/>   |
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>                     |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | Le filtre n’est pas connecté.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode copie le type de média dans la structure de **\_ \_ type de média am** spécifiée par *PTYPE*. L’appelant doit libérer le bloc de format du type de média. Vous pouvez utiliser la fonction **CoTaskMemFree** ou la fonction [**FreeMediaType**](freemediatype.md) dans la bibliothèque de classes de base.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de l’exemple d’accrochage](using-the-sample-grabber.md)
</dt> <dt>

[**Interface ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 




