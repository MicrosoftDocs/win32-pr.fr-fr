---
title: Méthode ClosedCaption. getSAMIStyleName
description: La méthode getSAMIStyleName récupère le nom d’un style pris en charge par le fichier SAMI actuel.
ms.assetid: c2ffedf8-4622-44fe-9d92-b52ed3bf3b9a
keywords:
- Lecteur Windows Media de la méthode getSAMIStyleName
- méthode getSAMIStyleName Lecteur Windows Media, classe ClosedCaption
- Lecteur Windows Media de la classe ClosedCaption, méthode getSAMIStyleName
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMIStyleName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7b7a8a23c47a464e1b192a4a652d87043765260a1016c707fa8d6c85c22b575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135802"
---
# <a name="closedcaptiongetsamistylename-method"></a>Méthode ClosedCaption. getSAMIStyleName

La méthode **getSAMIStyleName** récupère le nom d’un style pris en charge par le fichier sami actuel.

## <a name="syntax"></a>Syntaxe


```JScript
strRetVal = ClosedCaption.getSAMIStyleName(
  index
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

**Number** (**long**) spécifiant l’index du nom de style à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne une **chaîne** contenant le nom du style tel que spécifié dans le fichier sami.

## <a name="remarks"></a>Remarques

Les styles d’un fichier SAMI sont indexés dans l’ordre indiqué dans le fichier, à partir de zéro.

Cette méthode ne peut pas être utilisée tant qu’un fichier multimédia numérique n’est pas ouvert (*lecteur*.**openState** est égal à 13).

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objet ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**ClosedCaption.SAMIStyle**](closedcaption-samistyle.md)
</dt> </dl>

 

 





