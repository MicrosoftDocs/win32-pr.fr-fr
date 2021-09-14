---
title: IWMPControls3 propriété currentAudioLanguageIndex
description: La propriété currentAudioLanguageIndex obtient ou définit l’index de base un qui correspond au langage audio pour la lecture.
ms.assetid: 3ed60827-c4e9-4455-b95e-b6eebf7a9a08
keywords:
- Lecteur Windows Media de la propriété currentAudioLanguageIndex
- Lecteur Windows Media de la propriété currentAudioLanguageIndex, interface IWMPControls3
- Lecteur Windows Media de l’interface IWMPControls3, propriété currentAudioLanguageIndex
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguageIndex
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fb36eea4038322cacd7f233892151ab77e5eea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010744"
---
# <a name="iwmpcontrols3currentaudiolanguageindex-property"></a>IWMPControls3 :: currentAudioLanguageIndex, propriété

La propriété **currentAudioLanguageIndex** obtient ou définit l’index de base un qui correspond au langage audio pour la lecture.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 currentAudioLanguageIndex {get; set;}
```


```VB

Public Property currentAudioLanguageIndex As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui est l’index de base un de la langue.

## <a name="remarks"></a>Notes

pour le contenu multimédia Windows, les propriétés et les méthodes associées à la sélection de la langue ne prennent en charge qu’une seule sortie.

Utilisez la propriété **audioLanguageCount** pour connaître le nombre de langues audio prises en charge.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPControls3 (VB et C#)**](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. audioLanguageCount (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguage (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageDescription (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageID (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





