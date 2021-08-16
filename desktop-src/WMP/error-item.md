---
title: Erreur. Item, méthode
description: La méthode Item récupère un objet ErrorItem à partir de la file d’attente des erreurs.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- méthode item Lecteur Windows Media
- item, méthode Lecteur Windows Media, classe Error
- Lecteur Windows Media de la classe Error, méthode item
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
ms.openlocfilehash: 5e9fbd9f402a659af27db42c34cb0c58e2097270b73eb0eeff382544979dc0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339694"
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

## <a name="remarks"></a>Remarques

Lecteur Windows Media pouvez générer un certain nombre d’erreurs en réponse à une condition d’erreur. Cette méthode permet de récupérer une erreur spécifique dans la file d’attente à l’aide d’un numéro d’index. Les numéros d’index de la file d’attente d’erreurs commencent par zéro.

vous devez définir *Paramètres*. **enableErrorDialogs** sur false si vous choisissez d’afficher des messages d’erreur personnalisés.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise l' *erreur*. objet **Item** dans un gestionnaire d’événements pour avertir l’utilisateur de l’erreur la plus récente. L’objet **Player** a été créé avec ID = "Player".


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

 

 





