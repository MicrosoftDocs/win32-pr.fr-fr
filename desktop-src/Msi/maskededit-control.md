---
description: Le contrôle MaskedEdit est un contrôle de champ d’édition qui contient un masque dans le champ de texte du contrôle. Vous pouvez associer le contrôle à une propriété de valeur de chaîne en entrant le nom de la propriété dans la colonne propriété de la table de contrôle.
ms.assetid: 8cc14683-3dbb-404f-87af-09a5f5b90b19
title: MaskedEdit (contrôle)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7568df9969ebabab6311e519d0a5a625feb8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539356"
---
# <a name="maskededit-control"></a>MaskedEdit (contrôle)

Le contrôle MaskedEdit est un contrôle de champ d’édition qui contient un masque dans le champ de texte du contrôle. Vous pouvez associer le contrôle à une propriété de valeur de chaîne en entrant le nom de la propriété dans la colonne propriété de la [table de contrôle](control-table.md).

Vous pouvez utiliser le contrôle MaskedEdit pour créer un modèle pour l’entrée utilisateur d’informations, telles qu’un numéro de téléphone ou un code d’ID de produit. Par exemple, la propriété [**PIDKEY**](pidkey.md) peut être entrée par l’utilisateur via un contrôle MaskedEdit spécifié en affectant à la propriété [**PIDTemplate**](pidtemplate.md) une chaîne semblable à la suivante :

12345<\#\#\# -%%%%%%%>@@@@@

La chaîne définit le modèle de masquage de l’entrée de la propriété [**PIDKEY**](pidkey.md) par l’utilisateur. Le segment visible de la chaîne est entouré d’une paire de crochets (<>).

Le tableau suivant identifie la syntaxe du masque.



| Caractère | Signification                                                                                                                                                                                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <      | Extrémité gauche du segment visible du modèle. Ce caractère et tout ce qui se trouve à sa gauche sont masqués dans l’interface utilisateur. Il ne doit y avoir qu’une seule instance de ce caractère dans le modèle.                                                                               |
| >      | Extrémité droite du segment visible du modèle. Ce caractère et tout ce qui se trouve à droite sont masqués dans l’interface utilisateur. Ce caractère est remplacé par un tiret pendant la validation. Si un segment visible commence par <, il doit se terminer par un > correspondant. |
| \#        | Ce caractère peut être un chiffre (chiffres).                                                                                                                                                                                                                                                    |
| %         | Ce caractère peut être un autre chiffre (numérique) qui permet au masque de contrôler la façon dont une action personnalisée différencie les champs.                                                                                                                                                          |
| @         | Ce caractère peut être un chiffre aléatoire (chiffres). Ce caractère ne doit pas apparaître dans la partie visible du modèle.                                                                                                                                                                       |
| &         | Ce caractère peut être n’importe quel caractère.                                                                                                                                                                                                                                                        |
| ^         | Ce caractère peut être un autre caractère qui permet au masque de contrôler la façon dont une action personnalisée différencie les champs.                                                                                                                                                                |
| ?         | Ce caractère peut être un autre caractère qui permet au masque de contrôler la façon dont une action personnalisée différencie les champs.                                                                                                                                                                |
| \`        | Les points d’accent grave \` (valeur ASCII 96) peuvent représenter un caractère de remplacement qui permet au masque de contrôler la façon dont une action personnalisée différencie les champs.                                                                                                                                 |
| \_        | Ce caractère est un trait de soulignement littéral.                                                                                                                                                                                                                                           |
| =         | Ce caractère est l’indicateur de fin de champ. Doit suivre un \# ,%, ^ ou \` . Cela crée une position d’entrée supplémentaire du même type que les positions précédentes et met fin au champ avec un séparateur « - ».                                                                                 |



 

Tout autre caractère est traité comme une constante littérale.

Pour les caractères qui peuvent être modifiés, le contrôle crée des fenêtres de modification distinctes avec une fenêtre pour chaque bloc de caractères contigus du même genre.

## <a name="control-attributes"></a>Attributs du contrôle

Pour modifier la valeur d’un attribut qui utilise un événement, abonnez le contrôle à un événement de contrôle dans la [table EventMapping](eventmapping-table.md) et répertoriez l’identificateur d’attribut dans la colonne d’attribut. Entrez l’identificateur de l’événement de contrôle dans la colonne d’événement. Vous pouvez utiliser les attributs suivants avec le contrôle MaskedEdit.



| Attribut                                                          | Bit hexadécimal                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Il s’agit du nom d’une propriété indirecte associée au contrôle. Si le bit d’attribut indirect est défini, le contrôle affiche ou modifie la valeur de la propriété qui porte ce nom. Si le bit d’attribut indirect est défini, ce nom est également la valeur de la propriété qui est indiquée dans la colonne propriété de la [table de contrôle](control-table.md).                                                                                                                                   |
| [Position](position-control-attribute.md)                         |                                  | Position du contrôle dans la boîte de dialogue. Entrez la largeur, la hauteur et les coordonnées du contrôle du coin gauche du contrôle dans les colonnes de largeur, de hauteur, X et Y de la [table de contrôle](control-table.md). Utilisez les [unités d’installation](installer-units.md) pour la longueur et la distance.<br/>                                                                                                                                                                                                            |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Il s’agit du nom de la propriété associée à ce contrôle. Si le bit d’attribut indirect n’est pas défini, le contrôle affiche ou modifie la valeur de la propriété qui porte ce nom. Cet attribut est spécifié dans la colonne propriété de la [table de contrôle](control-table.md).                                                                                                                                                                                                           |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valeur actuelle de la propriété qui est affichée ou modifiée par ce contrôle. Si le bit d’attribut indirect n’est pas défini, il s’agit de la valeur de PropertyName. Si le bit d’attribut indirect est défini, il s’agit de la valeur de IndirectPropertyName. Si l’attribut change, le contrôle reflète la nouvelle valeur.                                                                                                                                                                                                |
| [Text](text-control-attribute.md)                                 |                                  | Pour définir la police et le style de police d’une chaîne de texte, ajoutez le préfixe { \\ style} ou {&style} à la chaîne de caractères affichés. Où style est un identificateur figurant dans la colonne style de la [table TextStyle](textstyle-table.md). Si aucun de ces deux n’est présent, mais que la propriété [**DefaultUIFont**](defaultuifont.md) est définie en tant que style de texte valide, cette police est utilisée. La chaîne qui spécifie le modèle de masquage suit ce préfixe et utilise la syntaxe décrite précédemment dans cette rubrique. |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Contrôle masqué. Contrôle visible.<br/> Incluez ce bit dans le mot de bits de la colonne attributs dans la [table de contrôle](control-table.md) pour rendre le contrôle visible ou masqué lors de sa création.<br/> Vous pouvez également masquer ou afficher un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                 |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Contrôle dans un état désactivé. Contrôle dans un état activé.<br/> Incluez ce bit dans le mot de bits dans la colonne attributs du [tableau de contrôle](control-table.md) pour activer le contrôle lors de la création.<br/> Vous pouvez également activer ou désactiver un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                          |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Affiche le style visuel par défaut. Affiche le contrôle avec une apparence 3D enfoncée.<br/> Incluez ces bits dans le mot de bits dans la colonne attributs de la [table de contrôle](control-table.md).<br/>                                                                                                                                                                                                                                                                                          |
| [Indirect](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Le contrôle affiche ou modifie la valeur de la propriété dans la colonne propriété de la [table de contrôle](control-table.md). Le contrôle affiche ou modifie la valeur de la propriété qui a l’identificateur figurant dans la colonne propriété de la [table de contrôle](control-table.md).<br/> Détermine si la propriété associée à ce contrôle est référencée indirectement.<br/>                                                                                                 |



 

## <a name="remarks"></a>Notes

Le contrôle MaskedEdit crée une fenêtre parente de la classe **Button** avec les styles **BS \_ OwnerDraw** et **WS \_ ex \_ CONTROLPARENT** . Elle crée plusieurs fenêtres enfants dans cette fenêtre.

-   Pour les parties de texte constantes, elle crée des fenêtres STATIQUEs avec les styles **DD \_ gauche** et **WS \_ enfant** .
-   Pour les champs modifiables, elle crée une fenêtre d’édition avec les styles **WS \_ enfant**, **WS \_ Border** et **WS \_ TABSTOP** .
-   Pour les champs numériques, la fenêtre a également le style de **\_ nombre es** .

Les autres caractères alphanumériques digit,% et alternatifs, ^, ? et et les \` champs permettent aux actions personnalisées de faire la différence entre les champs d’une manière qui peut être contrôlée par le masque, par exemple, ^ peut être utilisé pour les champs qui doivent être en majuscules.

 

 




