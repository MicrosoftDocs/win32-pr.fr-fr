---
description: L’exemple décrit dans la section intitulée création d’un &conditionnel \# 0034 ; Veuillez patienter.
ms.assetid: b563e306-6d10-4298-9a71-9e749224ccd2
title: Ajout de texte stocké dans une propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d43910b946db737d2b306d7c75f6683401eee0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092809"
---
# <a name="adding-text-stored-in-a-property"></a>Ajout de texte stocké dans une propriété

L’exemple décrit dans la section intitulée [création d’un conditionnel «Veuillez patienter... « La boîte de message](authoring-a-conditional-please-wait-------message-box.md) affiche une boîte de dialogue avec le texte suivant : «Veuillez patienter pendant l’exécution du coût de l’espace disque ». Pour ce faire, il suffit de placer un [contrôle de texte](text-control.md) dans la boîte de dialogue et d’entrer la chaîne de texte dans la colonne de texte de la table de [contrôle](control-table.md). Dans ce cas, les informations sur le style de police doivent être incorporées dans la chaîne. L’auteur doit définir la police et le style de police en ajoutant un préfixe { \\ *style*} à la chaîne de caractères. Où *style* est un identificateur de style de police figurant dans la colonne TextStyle de la [table TextStyle](textstyle-table.md). Cette méthode d’ajout de texte est illustrée plusieurs fois dans [un exemple d’installation](an-installation-example.md).

L’auteur d’une interface utilisateur peut également stocker du texte dans une propriété. L’exemple suivant illustre cela et montre comment ControlEvents peut être utilisé pour afficher des chaînes de texte de remplacement.

L’objectif de cet exemple est encore de placer une boîte de dialogue **WaitForCosting** pendant l’exécution d’une tâche en arrière-plan. La différence avec le nouveau scénario est que si l’utilisateur annule la boîte de dialogue **WaitForCosting** , puis tente d’activer le contrôle avant la fin de la tâche en arrière-plan, la boîte de **WaitForCosting** réapparaît et affiche un autre message : «le coût de l’espace disque est toujours en cours d’exécution. Vous pouvez continuer à attendre ou revenir à la zone de sélection principale pour quitter cette séquence.»

**Pour afficher une boîte de dialogue « Veuillez patienter » qui affiche d’autres messages**

1.  Commencez par ajouter une boîte de dialogue **WaitForCosting** conditionnelle à une boîte de dialogue de sélection, comme décrit dans [création d’un conditionnel «Veuillez patienter... « MessageBox »](authoring-a-conditional-please-wait-------message-box.md).
2.  Placez un [contrôle de texte](text-control.md) dans la boîte de dialogue **WaitForCosting** en créant un enregistrement dans la [table de contrôle](control-table.md). Entrez l’identificateur de la boîte de dialogue **WaitForCosting** dans la colonne boîte de dialogue \_ . Entrez l’identificateur du contrôle de texte dans la colonne de contrôle. Spécifiez le type de contrôle sous forme de texte dans la colonne Type.
3.  Spécifiez l' [attribut de contrôle de position](position-control-attribute.md) pour le contrôle de texte en entrant les coordonnées horizontales et verticales du coin supérieur gauche du contrôle dans les colonnes X et Y de la table de [contrôle](control-table.md). Utilisez des pixels comme unités de distance.
4.  Spécifiez la largeur et la hauteur du contrôle de texte en entrant ces dimensions dans les colonnes de largeur et de hauteur de la [table de contrôle](control-table.md). Utilisez des pixels comme unités de longueur.
5.  Les \_ colonnes de propriétés et de contrôle suivantes de la table de contrôle n’affectent pas les contrôles de texte et peuvent être laissées vides dans ce cas.
6.  Spécifiez les attributs de contrôle pour le contrôle de texte qui sont associés aux indicateurs binaires. Ajoutez les valeurs de bit individuelles et entrez le total dans la colonne attributs de la table de contrôle. Il s’agit des attributs de contrôle [visibles](visible-control-attribute.md), [enfoncés](sunken-control-attribute.md), [activés](enabled-control-attribute.md), [transparents](transparent-control-attribute.md), [nowrap](nowrap-control-attribute.md)et [NoPrefix](noprefix-control-attribute.md) . La combinaison de bits qui affichent un contrôle de texte sur un arrière-plan opaque, avec le texte de retour à la valeur 0, entrez donc 0 ou laissez la colonne d’attributs vide.
7.  La colonne de texte de la table de contrôle peut être laissée vide. Le contrôle de texte affiche la chaîne de texte correspondant à la valeur de l’attribut de contrôle de [texte](text-control-attribute.md) . La méthode de définition de cet attribut est décrite dans les étapes suivantes de cette procédure.
8.  Ajoutez un enregistrement dans la [table de propriétés](property-table.md) pour définir la propriété de message FirstMessage. Cette propriété est une chaîne qui contient le style et le texte de la police pour le premier message. Entrez le nom FirstMessage dans la colonne propriété. Dans la colonne valeur, entrez la chaîne : « { \\ WaitStyle} Veuillez patienter pendant que l’espace disque est terminé. » Où WaitStyle est un identificateur pour l’un des styles de police figurant dans la colonne TextStyle de la [table TextStyle](textstyle-table.md).
9.  Ajoutez un enregistrement dans la [table de propriétés](property-table.md) pour définir la propriété de message SecondMessage. Cette propriété est une chaîne qui contient le style de police et le texte du deuxième message. Entrez le nom SecondMessage dans la colonne propriété. Dans la colonne valeur, entrez la chaîne : «{ \\ WaitStyle} le coût de l’espace disque est toujours en cours d’exécution. Vous pouvez continuer à attendre ou revenir à la zone de sélection principale pour quitter cette séquence.»
10. Ajoutez un enregistrement dans la [table de propriétés](property-table.md) pour définir la propriété de message WaitMessage. Cette propriété est une chaîne qui contient le style de police et le texte du message affiché dans la boîte de dialogue **WaitForCosting** si l’utilisateur tente d’activer un bouton de commande avant que l’évaluation des coûts soit terminée. Entrez le nom WaitMessage dans la colonne propriété. Dans la colonne valeur de la table de propriétés, entrez : FirstMessage.
11. Ajoutez un [ControlEvent, SetProperty](setproperty-controlevent.md) à la [table ControlEvent,](controlevent-table.md) qui initialise WaitMessage à FirstMessage chaque fois qu’une **nouvelle** boîte de dialogue de sélection s’ouvre. Entrez l’identificateur de la boîte de dialogue qui s’affiche juste avant la boîte de dialogue de sélection dans la colonne boîte de dialogue de la boîte de dialogue \_ . Entrez l’identificateur du contrôle dans la boîte de dialogue utilisée pour ouvrir la boîte de dialogue de sélection dans la \_ colonne de contrôle. Entrez \[ WaitMessage \] dans la colonne d’événement. Entrez \[ FirstMessage \] dans la colonne argument. Entrez 1 dans la colonne condition et laissez la colonne classement vide.
12. Ajoutez un [ControlEvent, SetProperty](setproperty-controlevent.md) à la [table ControlEvent,](controlevent-table.md) qui définit WaitMessage sur SecondMessage si l’utilisateur ferme la boîte de dialogue **WaitForCosting** avant la fin de l’utilisation du coût de l’espace disque. Entrez l’identificateur de la boîte de dialogue **WaitForCosting** dans la colonne boîte de dialogue \_ . Entrez l’identificateur du contrôle de texte dans la colonne de contrôle \_ . Entrez \[ WaitMessage \] dans la colonne d’événement. Entrez \[ SecondMessage \] dans la colonne argument. Entrez NOT [**CostingComplete**](costingcomplete.md) dans la colonne condition et laissez la colonne Ordering vide.
13. L’étape suivante lie l’attribut de contrôle de texte au ControlEvent, qui génère la boîte de dialogue **WaitForCosting** . Ainsi, le programme d’installation transmet la valeur de la propriété WaitMessage à l’attribut de contrôle de texte chaque fois que l’utilisateur ouvre une boîte de dialogue **WaitForCosting** .
14. Abonnez l’attribut de contrôle de texte du contrôle de texte au [ControlEvent, SpawnWaitDialog](spawnwaitdialog-controlevent.md) qui ouvre la boîte de dialogue **WaitForCosting** en ajoutant un enregistrement à la [table EventMapping](eventmapping-table.md). Entrez l’identificateur de la boîte de dialogue **WaitForCosting** dans la colonne boîte de dialogue \_ . Entrez l’identificateur du contrôle de texte dans la colonne de contrôle \_ . Entrez SpawnWaitDialog dans la colonne d’événement. Entrez le texte, l’identificateur de l’attribut de contrôle de texte, dans la colonne attribut de la table EventMapping.

 

 



