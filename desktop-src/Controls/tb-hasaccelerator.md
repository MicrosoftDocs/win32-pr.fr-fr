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
ms.openlocfilehash: 2544eae629876e4527ea4e47477b50ea59b796c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116686"
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

## <a name="return-value"></a>Valeur de retour

La valeur de retour n’est pas utilisée.

## <a name="security-considerations"></a>Considérations relatives à la sécurité

L’utilisation de ce message peut compromettre la sécurité de votre programme.

## <a name="remarks"></a>Notes

Tout d’abord, le système interroge tous les boutons de barre d’outils pour faire correspondre les accélérateurs. Si aucune correspondance n’est trouvée, le système envoie la notification [TBN \_ MAPACCELERATOR](tbn-mapaccelerator.md) à la fenêtre parente, en demandant l’index du bouton qui contient le caractère d’accélérateur spécifié. Si le parent fournit un index, le nombre est défini sur 1.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





