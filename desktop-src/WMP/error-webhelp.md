---
title: Erreur. Webhelp, méthode
description: la méthode webhelp lance la Lecteur Windows Media page d’aide Web pour afficher des informations supplémentaires sur la première erreur de la file d’attente des erreurs (index zéro). | Erreur. Webhelp, méthode
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- Lecteur Windows Media de la méthode webhelp
- webhelp method Lecteur Windows Media, classe Error
- Lecteur Windows Media de la classe Error, méthode webhelp
topic_type:
- apiref
api_name:
- Error.webHelp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fee647d8f3ddca89ed36c224caab05543715864347700d35ae8e80ee45078cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118577873"
---
# <a name="errorwebhelp-method"></a>Erreur. Webhelp, méthode

la méthode **webhelp** lance la Lecteur Windows Media page d’aide Web pour afficher des informations supplémentaires sur la première erreur de la file d’attente des erreurs (index zéro).

## <a name="syntax"></a>Syntaxe


```JScript
Error.webHelp()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

les pages d’aide Web contiennent toujours les informations les plus récentes et les plus détaillées sur les erreurs de Lecteur Windows Media. Cette méthode transfère automatiquement les autres informations requises par l’aide Web, telles que la version du système d’exploitation utilisée.

Pour accéder directement aux pages d’aide Web, utilisez le code d’erreur suivant et les liens du centre d’aide et de support.

-   [Lecteur Windows Media Informations sur le code d’erreur](https://support.microsoft.com/kb/886273)
-   [Lecteur Windows Media Centre de solutions](https://support.microsoft.com/ph/7763#tab0)

**Lecteur Windows Media 10 Mobile :** Cette méthode fonctionne toujours, mais n’effectue pas l’opération prévue.

## <a name="examples"></a>Exemples

l’exemple suivant crée un élément bouton HTML qui lance la page d’aide Web de Microsoft Lecteur Windows Media. L’objet **Player** a été créé avec ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  
       NAME = "WHBUTTON"  
       VALUE = "More Info"

OnClick = "Player.error.webHelp();

">

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Error, objet**](error-object.md)
</dt> </dl>

 

 





