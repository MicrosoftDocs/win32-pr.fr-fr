---
description: La méthode SetMediaType spécifie le type de média pour la connexion sur la broche d’entrée de la accroche d’échantillon.
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: 'ISampleGrabber :: SetMediaType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a39aa79e9311fe3491d0925fdc1b2dd3b1cc65c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541603"
---
# <a name="isamplegrabbersetmediatype-method"></a>ISampleGrabber :: SetMediaType, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `SetMediaType` méthode spécifie le type de média pour la connexion sur la broche d’entrée de la accroche d’échantillon.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMediaType(
   const AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pType* 
</dt> <dd>

Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) spécifie le type de média requis. Il n’est pas nécessaire de définir tous les membres de structure ; Pour plus d’informations, consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Par défaut, l’exemple de la accroche n’a pas de type de média préféré. Pour vous assurer que l’exemple d’accroche se connecte au filtre correct, appelez cette méthode avant de générer le graphique de filtre.

Cette méthode restreint la plage de types de médias que le filtre acceptera. Quand le filtre se connecte, il tente de faire correspondre le type de média donné dans *PTYPE*. Pour ce faire, il compare le type, le sous-type et les GUID de type de format principaux, dans cet ordre. Pour chacun de ces GUID, si *PTYPE* a la valeur Guid \_ null, l’exemple de la accroche accepte le type de média sans aucune autre vérification. Si *PTYPE* a une autre valeur, l’exemple d’accroche le compare au GUID dans le type de connexion. À moins que les deux GUID correspondent exactement, l’accroche d’échantillon rejette la connexion.

Pour les types de média vidéo, la accroche d’échantillon ignore le bloc de format. Par conséquent, elle accepte toute taille vidéo et fréquence d’images. Quand vous appelez `SetMediaType` , affectez la valeur **null** au bloc de format (**pbFormat**) et la taille (**cbFormat**) à zéro. Pour les types de média audio, l’exemple de accroche examine la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) et nécessite que l’autre filtre se connecte avec ce format, à moins que le bloc de format de *PTYPE* soit null ou que la balise format soit de **type** Wave \_ \_ PCM et que les autres membres de la structure soient nuls.

Exemple 1 :

-   Type majeur : \_ vidéo MediaType
-   Sous-type : GUID \_ null
-   Type de format : GUID \_ null

L’exemple de la accroche accepte tout type de vidéo dans lequel le type de principal est égal à la vidéo de MEDIATYPE \_ . Il ne vérifie pas le sous-type.

Exemple 2 :

-   Type majeur : \_ vidéo MediaType
-   Sous-type : MEDIASUBTYPE \_ Rgb24
-   Type de format : GUID \_ null

À présent, l’exemple de la accroche vérifie le sous-type et n’accepte que les vidéos RVB 24.

**Limitations :** Quel que soit le type que vous avez défini, le filtre d’accroche d’échantillon rejette tous les types vidéo avec une orientation verticale ( *bihauteur* négative) ou un type de format \_ VideoInfo2. Dans ce cas, bien que la `SetMediaType` méthode aboutisse, le filtre ne se connecte pas.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

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

 

 
