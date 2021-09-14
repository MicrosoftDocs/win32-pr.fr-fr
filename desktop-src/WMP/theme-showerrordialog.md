---
title: THÈME. showErrorDialog
description: La méthode showErrorDialog affiche la boîte de dialogue d’erreur standard.
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- thème. showErrorDialog Lecteur Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118553"
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

si **Paramètres. enableErrorDialogs** a la valeur false, cette méthode peut être utilisée pour afficher la boîte de dialogue d’erreur par programmation. S’il n’y a pas d’erreurs dans la file d’attente des erreurs, la boîte de dialogue d’erreur ne s’affiche pas.

pour Lecteur Windows Media série 9 ou version ultérieure, cette méthode doit être appelée à partir du gestionnaire d’événements d’erreur. Lecteur Windows Media série 9 ou version ultérieure efface la file d’attente d’erreurs pour les habillages après le déclenchement de l’événement d’erreur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément THEMe**](theme-element.md)
</dt> <dt>

[**Paramètres. enableErrorDialogs**](settings-enableerrordialogs.md)
</dt> </dl>

 

 





