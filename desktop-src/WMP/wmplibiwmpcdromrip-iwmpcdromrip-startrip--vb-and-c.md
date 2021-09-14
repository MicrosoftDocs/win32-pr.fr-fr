---
title: Méthode IWMPCdromRip startRip
description: La méthode startRip RIP le CD.
ms.assetid: 3569e29c-e593-4bdd-8afb-74e39721cf80
keywords:
- Lecteur Windows Media de la méthode startRip
- méthode startRip Lecteur Windows Media, interface IWMPCdromRip
- Lecteur Windows Media de l’interface IWMPCdromRip, méthode startRip
topic_type:
- apiref
api_name:
- IWMPCdromRip.startRip
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327ac9009cf1b8fb9ccfbcc460cde78ef40b3802
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118529"
---
# <a name="iwmpcdromripstartrip-method"></a>IWMPCdromRip :: startRip, méthode

La méthode **startRip** RIP le CD.

## <a name="syntax"></a>Syntaxe


```CSharp
public void startRip();
```


```VB

Public Sub startRip()
Implements IWMPCdromRip.startRip
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

l’extraction d’un CD à l’aide de l’interface **IWMPCdromRip** a le même effet que l’extraction de musique à l’aide de l’interface utilisateur Lecteur Windows Media. Le contenu extrait est automatiquement ajouté à la bibliothèque en fonction des préférences de l’utilisateur. pour plus d’informations sur les préférences de l’utilisateur pour l’extraction de cd, consultez « extraction de musique à partir de cd » dans l’aide de Lecteur Windows Media.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPCdromRip (VB et C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**IWMPCdromRip.stopRip**](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)
</dt> <dt>

[**Extraction d’un CD**](ripping-a-cd.md)
</dt> </dl>

 

 





