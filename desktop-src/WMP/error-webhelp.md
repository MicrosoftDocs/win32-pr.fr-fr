---
title: Erreur. Webhelp, méthode
description: La méthode Webhelp ouvre la page d’aide Web du lecteur Windows Media pour afficher des informations supplémentaires sur la première erreur de la file d’attente des erreurs (index zéro). | Erreur. Webhelp, méthode
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- méthode Webhelp lecteur Windows Media
- méthode Webhelp lecteur Windows Media, classe d’erreur
- Classe d’erreur lecteur Windows Media, méthode Webhelp
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
ms.openlocfilehash: 862376be956bc8b37a778f5c9d1d2238c876208d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537622"
---
# <a name="errorwebhelp-method"></a>Erreur. Webhelp, méthode

La méthode **Webhelp** ouvre la page d’aide Web du lecteur Windows Media pour afficher des informations supplémentaires sur la première erreur de la file d’attente des erreurs (index zéro).

## <a name="syntax"></a>Syntaxe


```JScript
Error.webHelp()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Les pages d’aide Web contiennent toujours les informations les plus récentes et les plus détaillées sur les erreurs du lecteur Windows Media. Cette méthode transfère automatiquement les autres informations requises par l’aide Web, telles que la version du système d’exploitation utilisée.

Pour accéder directement aux pages d’aide Web, utilisez le code d’erreur suivant et les liens du centre d’aide et de support.

-   [Informations de code d’erreur du lecteur Windows Media](https://support.microsoft.com/kb/886273)
-   [Centre de solutions du lecteur Windows Media](https://support.microsoft.com/ph/7763#tab0)

**Lecteur Windows Media 10 Mobile :** Cette méthode fonctionne toujours, mais n’effectue pas l’opération prévue.

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément bouton HTML qui lance la page d’aide Web du lecteur Microsoft Windows Media. L’objet **Player** a été créé avec ID = "Player".


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

 

 





