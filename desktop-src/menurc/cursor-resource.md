---
title: Ressource curseur
description: Définit une bitmap qui définit la forme du curseur sur l’écran d’affichage ou un curseur animé.
ms.assetid: c087abca-5502-4625-8c9b-464e1718571f
keywords:
- Menus des ressources de curseur et autres ressources
topic_type:
- apiref
api_name:
- CURSOR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594f406420b3b18f88b8890ca4248345ba77fa8e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106511487"
---
# <a name="cursor-resource"></a>Ressource curseur

Définit une bitmap qui définit la forme du curseur sur l’écran d’affichage ou un curseur animé.

``` syntax
nameID CURSOR filename
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nom unique ou entier 16 bits non signé identifiant la ressource.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extension*
</dt> <dd>

Nom du fichier qui contient la ressource. Le nom doit être un nom de fichier valide ; il doit s’agir d’un chemin d’accès complet si le fichier ne se trouve pas dans le répertoire de travail actuel. Le chemin d’accès doit être une chaîne entre guillemets.

</dd> </dl>

Certains attributs sont également pris en charge pour la compatibilité descendante. Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).

## <a name="remarks"></a>Notes

Les ressources icône et curseur peuvent contenir plusieurs images.

## <a name="examples"></a>Exemples

L’exemple suivant définit deux ressources de curseur ; un par nom (Cursor1) et l’autre par numéro (2) :

``` syntax
cursor1 CURSOR "bullseye.cur"
2       CURSOR "d:\\cursor\\arrow.cur" 
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de curseurs](./using-cursors.md)
</dt> </dl>

 

 