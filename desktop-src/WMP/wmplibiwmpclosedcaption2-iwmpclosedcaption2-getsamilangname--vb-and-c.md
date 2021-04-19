---
title: Méthode IWMPClosedCaption2 getSAMILangName
description: La méthode getSAMILangName retourne le nom d’une langue prise en charge par le fichier SAMI actuel.
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- méthode getSAMILangName lecteur Windows Media
- méthode getSAMILangName lecteur Windows Media, interface IWMPClosedCaption2
- Interface IWMPClosedCaption2 lecteur Windows Media, méthode getSAMILangName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50df643fdd6b665de1275873fb8de9d5d094a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543920"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a>IWMPClosedCaption2 :: getSAMILangName, méthode

La méthode **getSAMILangName** retourne le nom d’une langue prise en charge par le fichier sami actuel.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String getSAMILangName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMILangName
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*nIndex* \[ dans\]
</dt> <dd>

**System. Int32** qui correspond à l’index de base zéro du nom de langage à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. String** qui est le nom de la langue tel que spécifié dans le fichier sami.

## <a name="remarks"></a>Notes

Les langues d’un fichier SAMI sont indexées dans l’ordre indiqué dans le fichier, à partir de zéro.

Cette méthode retourne une chaîne de longueur nulle (""), à moins qu’un fichier multimédia numérique soit ouvert (AxWindowsMediaPlayer. openState est égal à 13).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interface IWMPClosedCaption (VB et C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption. SAMILang (VB et C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption2 (VB et C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





