---
title: Méthode ClosedCaption. getSAMILangID
description: La méthode getSAMILangID récupère l’identificateur de paramètres régionaux (LCID) d’une langue prise en charge par le fichier SAMI actuel.
ms.assetid: 35f8379a-a2f5-4b22-b1ad-3c5cc5bc5e3d
keywords:
- Lecteur Windows Media de la méthode getSAMILangID
- méthode getSAMILangID Lecteur Windows Media, classe ClosedCaption
- Lecteur Windows Media de la classe ClosedCaption, méthode getSAMILangID
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7317bff13b0dcf29157e4a31c1b854fff781d93460633b64485670fab64e6f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764039"
---
# <a name="closedcaptiongetsamilangid-method"></a>Méthode ClosedCaption. getSAMILangID

La méthode **getSAMILangID** récupère l’identificateur de paramètres régionaux (LCID) d’une langue prise en charge par le fichier sami actuel.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = ClosedCaption.getSAMILangID(
  index
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

**Nombre** (**long**) spécifiant l’index du LCID à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un **nombre** (**long**) contenant le LCID de la langue avec l’index spécifié.

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
</dt> </dl>

 

 





