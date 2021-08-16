---
title: Message TB_HASACCELERATOR (commctrl. h)
description: Récupère le nombre de boutons de la barre d’outils qui contiennent le caractère d’accélérateur spécifié.
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- TB_HASACCELERATOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_HASACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420f06e71c6920c266c96d8b2580549fa0eaace2bd3abdd37524502d4039aa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078283"
---
# <a name="tb_hasaccelerator-message"></a>TO \_ HASACCELERATOR message

\[Destiné à un usage interne ; non recommandé pour une utilisation dans les applications. Ce message n’est peut-être pas pris en charge dans les versions ultérieures de Windows.\]

Récupère le nombre de boutons de la barre d’outils qui contiennent le caractère d’accélérateur spécifié.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

**WCHAR** représentant le caractère d’accélérateur d’entrée à tester.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un **entier** qui reçoit le nombre de boutons qui ont le caractère d’accélérateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="security-considerations"></a>Considérations relatives à la sécurité

L’utilisation de ce message peut compromettre la sécurité de votre programme.

## <a name="remarks"></a>Remarques

Tout d’abord, le système interroge tous les boutons de barre d’outils pour faire correspondre les accélérateurs. Si aucune correspondance n’est trouvée, le système envoie la notification [TBN \_ MAPACCELERATOR](tbn-mapaccelerator.md) à la fenêtre parente, en demandant l’index du bouton qui contient le caractère d’accélérateur spécifié. Si le parent fournit un index, le nombre est défini sur 1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





