---
title: DoReaderMode fonction)
description: Active le mode lecteur dans une fenêtre.
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- DoReaderMode, fonction Windows contrôles
topic_type:
- apiref
api_name:
- DoReaderMode
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63b71538e41e4b70155da8352e531b620fbe5de7f62746713c3a2a58f3adddf2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002689"
---
# <a name="doreadermode-function"></a>DoReaderMode fonction)

\[**DoReaderMode** est disponible via Windows XP avec Service Pack 2 (SP2). Elle n’est peut-être pas disponible dans les versions ultérieures.\]

Active le mode lecteur dans une fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI DoReaderMode(
  _In_ PREADERMODEINFO prmi
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PRMI* \[ dans\]
</dt> <dd>

Type : **PREADERMODEINFO**

Pointeur vers une structure [**READERMODEINFO**](readermodeinfo.md) qui contient les informations d’initialisation pour le mode lecteur.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Le mode lecteur est activé via des appareils pris en charge par un clic de souris, généralement à l’aide d’un troisième bouton de la souris ou d’une roulette de défilement. Le déplacement suivant de la souris dans une zone spécifiée fait défiler le contenu de cette zone plutôt que de déplacer un pointeur. En dehors de cette zone, le pointeur de la souris est affiché et fonctionne normalement. Un deuxième clic sur le bouton ou la roulette de défilement libère l’appareil du mode lecteur.

> [!Note]  
> Cette fonction n’est pas déclarée dans un en-tête public. Pour l’utiliser, vous devez y accéder en tant qu’ordinal 383 à partir de Comctl32.dll.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista, Windows les \[ applications de bureau vista uniquement\]<br/>                                                   |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (version 4,72 ou ultérieure)</dt> </dl> |



 

 





