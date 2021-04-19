---
title: THÈME. showErrorDialog
description: La méthode showErrorDialog affiche la boîte de dialogue d’erreur standard.
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- THEMe. showErrorDialog Windows Media Player
topic_type:
- apiref
api_name:
- THEME.showErrorDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdc1f9df13ec460ce780507e1bde38a2996f915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528532"
---
# <a name="themeshowerrordialog"></a>THÈME. showErrorDialog

La méthode **showErrorDialog** affiche la boîte de dialogue d’erreur standard.

``` syntax
        theme.showErrorDialog()
```

## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si **Settings. enableErrorDialogs** a la valeur false, cette méthode peut être utilisée pour afficher la boîte de dialogue d’erreur par programmation. S’il n’y a pas d’erreurs dans la file d’attente des erreurs, la boîte de dialogue d’erreur ne s’affiche pas.

Pour le lecteur Windows Media série 9 ou version ultérieure, cette méthode doit être appelée à partir du gestionnaire d’événements d’erreur. Le lecteur Windows Media série 9 ou version ultérieure efface la file d’attente d’erreurs pour les apparences après le déclenchement de l’événement d’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément THEMe**](theme-element.md)
</dt> <dt>

[**Paramètres. enableErrorDialogs**](settings-enableerrordialogs.md)
</dt> </dl>

 

 





