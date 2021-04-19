---
title: IWMPSettings, propriété baseURL
description: La propriété baseURL obtient ou définit l’URL de base utilisée pour la résolution de chemin d’accès relative avec des commandes de script d’URL incorporées dans le contenu multimédia numérique.
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- propriété baseURL lecteur Windows Media
- propriété baseURL lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, propriété baseURL
topic_type:
- apiref
api_name:
- IWMPSettings.baseURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 393575a93bf904f6fe312b13647ad5a7557b15bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528607"
---
# <a name="iwmpsettingsbaseurl-property"></a>IWMPSettings :: baseURL, propriété

La propriété **baseURL** obtient ou définit l’URL de base utilisée pour la résolution de chemin d’accès relative avec des commandes de script d’URL incorporées dans le contenu multimédia numérique.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a>Valeur de la propriété

**System. String** qui est l’URL de base.

## <a name="remarks"></a>Notes

Cette propriété spécifie l’URL HTTP de base qui est transmise en tant que paramètre de commande par l’événement **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** . L’URL de base est concaténée avec l’URL relative, comme suit :

1.  Une barre oblique finale (/) est ajoutée à la valeur récupérée par la propriété **baseURL** .
2.  Un point de début, une barre oblique inverse ou un caractère de barre oblique (., \\ et/) est supprimé de l’URL relative.
3.  L’URL relative est ajoutée à la fin de l’URL de base.
4.  Tous les caractères de barre oblique dans l’URL complète résultante sont pointés dans la même direction (convertis en barres obliques ou en arrière) en fonction de la direction de la première barre oblique rencontrée dans la nouvelle URL.

**Remarque**

Le contrôle du lecteur Windows Media ne prend pas en charge l’utilisation de deux points (..) dans l’URL relative pour indiquer le parent de l’emplacement actuel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Événement AxWindowsMediaPlayer. commande (VB et C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interface IWMPSettings (VB et C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





