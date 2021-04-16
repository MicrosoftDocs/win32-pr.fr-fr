---
title: Ressource icône
description: Définit une bitmap qui définit la forme de l’icône à utiliser pour une application donnée ou une icône animée.
ms.assetid: a8e3205e-e17a-4daf-a599-4dc89cb1e640
keywords:
- ICÔNES des menus des ressources et d’autres ressources
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f762c4f4b459d51a0243a9cdbd7367deda7b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507878"
---
# <a name="icon-resource"></a>Ressource icône

Définit une bitmap qui définit la forme de l’icône à utiliser pour une application donnée ou une icône animée.

``` syntax
nameID ICON filename
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nom unique ou valeur d’entier non signé 16 bits identifiant la ressource.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extension*
</dt> <dd>

Nom du fichier qui contient la ressource. Le nom doit être un nom de fichier valide ; il doit s’agir d’un chemin d’accès complet si le fichier ne se trouve pas dans le répertoire de travail actuel. Le chemin d’accès doit être une chaîne entre guillemets.

</dd> </dl>

Certains attributs sont également pris en charge pour la compatibilité descendante. Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).

## <a name="remarks"></a>Notes

Les ressources icône et curseur peuvent contenir plusieurs images.

## <a name="examples"></a>Exemples

L’exemple suivant définit deux ressources d’icône :

``` syntax
desk1   ICON "desk.ico"
11      ICON "custom.ico"
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des icônes](./using-icons.md)
</dt> </dl>

 

 