---
title: EDITTEXT, contrôle
description: Définit un contrôle d’édition appartenant à la classe d’édition.
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- Menus du contrôle EDITTEXT et autres ressources
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b287f01b89aaa3e378309e8f98f777acc475bcca962557305021aaf471926ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847389"
---
# <a name="edittext-control"></a>EDITTEXT, contrôle

Définit un contrôle d’édition appartenant à la classe d’édition. Il crée une zone rectangulaire dans laquelle l’utilisateur peut taper et modifier du texte. Le contrôle affiche un curseur quand l’utilisateur clique sur la souris. L’utilisateur peut ensuite utiliser le clavier pour entrer du texte ou modifier le texte existant. La modification des clés inclut les touches retour arrière et supprimer. L’utilisateur peut également utiliser la souris pour sélectionner les caractères à supprimer ou pour sélectionner l’emplacement d’insertion de nouveaux caractères.

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles de contrôle. Cette valeur peut être une combinaison des styles de modification de classe et des styles suivants **: WS \_ TABSTOP**, **WS \_ Group**, **WS \_ VSCROLL**, **WS \_ HSCROLL** et **WS \_ désactivé**.

Si vous ne spécifiez pas de style, le style par défaut est `ES_LEFT | WS_BORDER | WS_TABSTOP` .

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de l’instruction **EDITTEXT** :

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôles d’édition](../controls/about-edit-controls.md)
</dt> </dl>

 

 