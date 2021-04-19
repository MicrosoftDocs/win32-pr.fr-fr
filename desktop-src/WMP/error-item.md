---
title: Erreur. Item, méthode
description: La méthode Item récupère un objet ErrorItem à partir de la file d’attente des erreurs.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- méthode Item lecteur Windows Media
- méthode Item lecteur Windows Media, classe d’erreur
- Classe d’erreur lecteur Windows Media, méthode d’élément
topic_type:
- apiref
api_name:
- Error.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5545df50fce05ff5a10a5f870d1ec07648434fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520788"
---
# <a name="erroritem-method"></a>Erreur. Item, méthode

La méthode **Item** récupère un objet **ErrorItem** à partir de la file d’attente des erreurs.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

**Nombre** (**long**) contenant l’index de l’objet **ErrorItem** à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **ErrorItem** .

## <a name="remarks"></a>Notes

Le lecteur Windows Media peut générer un certain nombre d’erreurs en réponse à une condition d’erreur. Cette méthode permet de récupérer une erreur spécifique dans la file d’attente à l’aide d’un numéro d’index. Les numéros d’index de la file d’attente d’erreurs commencent par zéro.

Vous devez définir des *paramètres*. **enableErrorDialogs** sur false si vous choisissez d’afficher des messages d’erreur personnalisés.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise l' *erreur*. objet **Item** dans un gestionnaire d’événements pour avertir l’utilisateur de l’erreur la plus récente. L’objet **Player** a été créé avec ID = "Player".


```JScript
<SCRIPT LANGUAGE="JScript"  FOR=Player EVENT=error()>

// Store the most recent error item number.
var max = Player.error.errorCount - 1 

// Store the most recent error in an error item object.
var errItem = Player.error.item(max);

// Use the error item object to store the error info.
errDesc = errItem.errorDescription;
errNum = errItem.errorCode;

// Display the error info.
alert(errNum + "\n" + errDesc);

</SCRIPT> 

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Error, objet**](error-object.md)
</dt> <dt>

[**Objet ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





