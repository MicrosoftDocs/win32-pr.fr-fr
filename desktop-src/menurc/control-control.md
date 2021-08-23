---
title: Contrôle de contrôle
description: Définit un contrôle défini par l’utilisateur.
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- Menus du contrôle de contrôle et autres ressources
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 069449b5eef83cef7b7bdfac1c61aacb0ceac97cbbdd6e6fb2c139c43b3bae13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663059"
---
# <a name="control-control"></a>Contrôle de contrôle

Définit un contrôle défini par l’utilisateur.

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*type*
</dt> <dd>

Nom redéfini, chaîne de caractères ou valeur d’entier non signé 16 bits qui définit la classe. Il peut s’agir de l’une des classes de contrôle ; pour obtenir la liste des classes de contrôle, consultez la première liste qui suit cette description. Si la valeur est un nom redéfini fourni par l’application, il doit s’agir d’une chaîne placée entre guillemets doubles (").

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Nom redéfini ou valeur entière qui spécifie le style du contrôle donné. La signification exacte du *style* dépend de la valeur de la *classe* . Les sections qui suivent cette description affichent les classes de contrôle et les styles correspondants.

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="remarks"></a>Remarques

Les six classes de contrôle possibles sont décrites dans les sections suivantes.

### <a name="the-button-control-class"></a>Classe de contrôle Button

Un contrôle Button est une petite fenêtre enfant rectangulaire que l’utilisateur peut activer ou désactiver en cliquant dessus avec la souris. Les contrôles Button peuvent être utilisés seuls ou dans des groupes, et peuvent être étiquetés ou affichés sans texte. En général, les contrôles de bouton changent d’apparence quand l’utilisateur clique dessus.

Les styles de bouton sont décrits dans la rubrique suivante : [styles de bouton](../controls/button-styles.md).

### <a name="the-combo-box-control-class"></a>Classe de contrôle de zone de liste déroulante

Les contrôles de zone de liste déroulante se composent d’un champ de sélection semblable à un contrôle d’édition plus une zone de liste. La zone de liste peut être affichée en permanence ou peut être déplacée lorsque l’utilisateur sélectionne une « zone contextuelle » en regard du champ de sélection.

Selon le style de la zone de liste déroulante, l’utilisateur peut ou ne peut pas modifier le contenu du champ de sélection. Si la zone de liste est visible, le fait de taper des caractères dans la zone de sélection entraîne la mise en surbrillance de la première entrée qui correspond aux caractères tapés. À l’inverse, la sélection d’un élément dans la zone de liste affiche le texte sélectionné dans le champ de sélection.

Les styles de contrôle de zone de liste déroulante sont décrits dans la rubrique suivante : [styles de zone de liste déroulante](../controls/combo-box-styles.md).

### <a name="the-edit-control-class"></a>Classe de contrôle d’édition

Un contrôle d’édition est une fenêtre enfant rectangulaire dans laquelle l’utilisateur peut entrer du texte à partir du clavier. L’utilisateur sélectionne le contrôle et lui donne le focus d’entrée, en cliquant sur la souris à l’intérieur ou en appuyant sur la touche TAB. L’utilisateur peut entrer du texte lorsque le contrôle affiche un point d’insertion clignotant. La souris peut être utilisée pour déplacer le curseur et sélectionner les caractères à remplacer, ou pour positionner le curseur en insérant des caractères. La touche Retour arrière peut être utilisée pour supprimer des caractères.

Les contrôles d’édition utilisent la police à espacement fixe et les caractères Unicode d’affichage. Elles développent les caractères de tabulation dans autant de caractères d’espace que nécessaire pour déplacer le curseur vers le taquet de tabulation suivant. Les taquets de tabulation sont supposés être à chaque huitième caractère.

Les styles de contrôle d’édition sont décrits dans la rubrique suivante : [modifier les styles de contrôle](../controls/edit-control-styles.md).

### <a name="the-list-box-control-class"></a>Classe de contrôle de zone de liste

Les contrôles de zone de liste sont constitués d’une liste de chaînes de caractères. Le contrôle est utilisé chaque fois qu’une application doit présenter une liste de noms, tels que des noms de fichiers, que l’utilisateur peut afficher et sélectionner. L’utilisateur peut sélectionner une chaîne en pointant sur la chaîne à l’aide de la souris et en cliquant sur un bouton de la souris. Lorsqu’une chaîne est sélectionnée, elle est mise en surbrillance et un message de notification est transmis à la fenêtre parente. Une barre de défilement peut être utilisée avec un contrôle de zone de liste pour faire défiler des listes qui sont trop longues ou trop larges pour la fenêtre de contrôle.

Les styles de contrôle de zone de liste sont décrits dans la rubrique suivante : [styles de zone de liste](../controls/list-box-styles.md).

### <a name="the-scroll-bar-control-class"></a>Classe de contrôle Scroll-Bar

Un contrôle de barre de défilement est un rectangle qui contient un curseur de défilement et qui a des flèches de direction aux deux extrémités. La barre de défilement envoie un message de notification à son parent chaque fois que l’utilisateur clique sur la souris dans le contrôle. Le parent est responsable de la mise à jour de la position du curseur, si nécessaire. Les contrôles de barre de défilement ont la même apparence et la même fonction que les barres de défilement utilisées dans les fenêtres ordinaires. Toutefois, contrairement aux barres de défilement, les contrôles de barre de défilement peuvent être positionnés n’importe où dans une fenêtre et utilisés chaque fois que nécessaire pour fournir une entrée de défilement pour une fenêtre.

Les styles de barre de défilement sont décrits dans la rubrique suivante : [styles de contrôle de barre de défilement](../controls/scroll-bar-control-styles.md).

### <a name="the-static-control-class"></a>Classe de contrôle statique

Les contrôles statiques sont des champs de texte, des zones et des rectangles simples qui peuvent être utilisés pour étiqueter, Box ou séparer d’autres contrôles. Les contrôles statiques ne prennent aucune entrée et ne fournissent aucune sortie.

Les styles de contrôle statiques sont décrits dans la rubrique suivante : [styles de contrôle statiques](../controls/static-control-styles.md).

 

 