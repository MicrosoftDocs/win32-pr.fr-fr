---
description: Contient des informations utilisées lors de la création d’un contexte de tablette.
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: Structure TABLET_CONTEXT_SETTINGS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_CONTEXT_SETTINGS
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9357281409ed4c48b4c6013a7a2be2997d58b094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953103"
---
# <a name="tablet_context_settings-structure"></a>Structure des paramètres de \_ contexte de tablette \_

Contient des informations utilisées lors de la création d’un contexte de tablette.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _TABLET_CONTEXT_SETTINGS {
  ULONG cPktProps;
  GUID  *pguidPktProps;
  ULONG cPktBtns;
  GUID  *pguidPktBtns;
  DWORD *pdwBtnDnMask;
  DWORD *pdwBtnUpMask;
  LONG  lXMargin;
  LONG  lYMargin;
} TABLET_CONTEXT_SETTINGS;
```



## <a name="members"></a>Membres

<dl> <dt>

**cPktProps**
</dt> <dd>

Nombre de propriétés dans un paquet.

</dd> <dt>

**pguidPktProps**
</dt> <dd>

Identificateurs uniques pour les propriétés du paquet.

</dd> <dt>

**cPktBtns**
</dt> <dd>

Nombre de boutons.

</dd> <dt>

**pguidPktBtns**
</dt> <dd>

Identificateurs uniques pour les boutons.

</dd> <dt>

**pdwBtnDnMask**
</dt> <dd>

Masque de bouton enfoncé.

</dd> <dt>

**pdwBtnUpMask**
</dt> <dd>

Masque de bouton haut.

</dd> <dt>

**lXMargin**
</dt> <dd>

Marge de direction X.

</dd> <dt>

**lYMargin**
</dt> <dd>

Marge de direction Y.

</dd> </dl>

## <a name="remarks"></a>Notes

En règle générale, une application obtient les valeurs par défaut à partir de la [**méthode ITablet :: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifie les valeurs en fonction de leurs besoins, puis passe la structure des paramètres modifiés à la [**méthode ITablet :: CreateContext**](itablet-createcontext.md).

Cette structure détermine les événements qu’une application obtiendra, la manière dont ils seront traités et la façon dont ils seront remis à l’application ou à Windows lui-même.

Les masques de bouton définissent ensemble les genres d’événements qui seront traités par le contexte.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                     |



 

 




