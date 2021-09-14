---
title: Énumération TITLEBAR_TYPE (Softkbdc. h)
description: Les éléments de l' \_ énumération de type TITLEBAR sont utilisés pour spécifier les types de titlebars qui sont disponibles pour une fenêtre de clavier temporaire.
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- TITLEBAR_TYPE l’infrastructure des services de texte d’énumération
topic_type:
- apiref
api_name:
- TITLEBAR_TYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ae1af1aba106a9f319cee080d0963992034a75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008799"
---
# <a name="titlebar_type-enumeration"></a>\_Énumération de type TITLEBAR

Les éléments de l’énumération de **\_ type TITLEBAR** sont utilisés pour spécifier les types de titlebars qui sont disponibles pour une fenêtre de clavier temporaire.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagTITLEBAR_TYPE { 
  TITLEBAR_NONE                = 0,
  TITLEBAR_GRIPPER_HORIZ_ONLY  = 1,
  TITLEBAR_GRIPPER_VERTI_ONLY  = 2,
  TITLEBAR_GRIPPER_BUTTON      = 3
} TITLEBAR_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TITLEBAR \_ aucun**
</dt> <dd>

La fenêtre du clavier logiciel n’utilise pas de TitleBar.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**préhension de TITLEBAR \_ \_ horizontale \_ uniquement**
</dt> <dd>

La fenêtre de clavier temporaire utilise uniquement une barre de redimensionnement horizontale.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**redimensionnement de TITLEBAR vers le \_ \_ vert \_ uniquement**
</dt> <dd>

La fenêtre de clavier temporaire utilise uniquement une barre de redimensionnement verticale.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**\_bouton de redimensionnement de la TITLEBAR \_**
</dt> <dd>

La fenêtre de clavier temporaire utilise uniquement un bouton de manipulation.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 Professional<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| MIDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |



 

 





