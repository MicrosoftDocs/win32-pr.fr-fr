---
title: Méthode IWMPClosedCaption2 getSAMILangID
description: La méthode getSAMILangID retourne l’identificateur de paramètres régionaux (LCID) d’une langue prise en charge par le fichier SAMI actuel.
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- Lecteur Windows Media de la méthode getSAMILangID
- méthode getSAMILangID Lecteur Windows Media, interface IWMPClosedCaption2
- Lecteur Windows Media de l’interface IWMPClosedCaption2, méthode getSAMILangID
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0fc62222f98d6c056bb8ce9ffd328582a6764202bb8446617471d3f7cb4a5ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506428"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a>IWMPClosedCaption2 :: getSAMILangID, méthode

La méthode **getSAMILangID** retourne l’identificateur de paramètres régionaux (LCID) d’une langue prise en charge par le fichier sami actuel.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 getSAMILangID(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangID( _
  ByVal nIndex As System.Int32 _
) As System.Int32
Implements IWMPClosedCaption2.getSAMILangID
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*nIndex* \[ dans\]
</dt> <dd>

**System. Int32** qui correspond à l’index de base zéro du LCID à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. Int32** qui est le LCID de la langue avec l’index spécifié.

## <a name="remarks"></a>Remarques

Les langues d’un fichier SAMI sont indexées dans l’ordre indiqué dans le fichier, à partir de zéro.

Cette méthode retourne la valeur 0, sauf si un fichier multimédia numérique est ouvert (AxWindowsMediaPlayer. openState est égal à 13).

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

[**Interface IWMPClosedCaption2 (VB et C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





