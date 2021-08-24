---
title: Méthode ClosedCaption. getSAMILangName
description: La méthode getSAMILangName récupère le nom d’une langue prise en charge par le fichier SAMI actuel.
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- Lecteur Windows Media de la méthode getSAMILangName
- méthode getSAMILangName Lecteur Windows Media, classe ClosedCaption
- Lecteur Windows Media de la classe ClosedCaption, méthode getSAMILangName
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d4150289eb7637d1772443a5437c6d245993ea0825a37d11bd7ec5accae918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764029"
---
# <a name="closedcaptiongetsamilangname-method"></a>Méthode ClosedCaption. getSAMILangName

La méthode **getSAMILangName** récupère le nom d’une langue prise en charge par le fichier sami actuel.

## <a name="syntax"></a>Syntaxe


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

**Nombre** (**long**) spécifiant l’index du nom de la langue à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne une **chaîne** contenant le nom de la langue tel que spécifié dans le fichier sami.

## <a name="remarks"></a>Remarques

Les langues d’un fichier SAMI sont indexées dans l’ordre indiqué dans le fichier, à partir de zéro.

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

[**ClosedCaption.SAMILang**](closedcaption-samilang.md)
</dt> </dl>

 

 





