---
title: THÈME. openDialog
description: La méthode openDialog ouvre une boîte de dialogue de fichier.
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- thème. openDialog Lecteur Windows Media
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d57218105aa081ddebcb98fadbdb40b4bbd42511de9df94e204320ce78cf03c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134552"
---
# <a name="themeopendialog"></a>THÈME. openDialog

La méthode **openDialog** ouvre une boîte de dialogue de fichier.

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*
</dt> <dd>

**Chaîne** qui spécifie le type de la boîte de dialogue. Doit être défini sur « fichier \_ ouvert ».

</dd> <dt>

<span id="parameters"></span><span id="PARAMETERS"></span>*paramètres*
</dt> <dd>

**Chaîne** qui peut être utilisée pour obtenir des informations supplémentaires. Doit être défini sur « FILES \_ ALLMEDIA ».

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne une **chaîne** contenant l’URL du fichier sélectionné ou «» (chaîne vide) si l’utilisateur clique sur Annuler.

## <a name="remarks"></a>Remarques

Cette méthode peut être utilisée pour les fichiers sur les disques durs locaux ou sur les lecteurs réseau.

## <a name="examples"></a>Exemples


```JScript
<THEME>
  <VIEW id="View1" 
    backgroundImage="greenstone.bmp" 
    width=500 height=300 author="Microsoft Corp.">
    <BUTTON 
      id="Open" 
      image="Open.png" 
      onclick="jscript:
        player.URL = theme.openDialog('FILE_OPEN','FILES_ALLMEDIA')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément THEMe**](theme-element.md)
</dt> </dl>

 

 





