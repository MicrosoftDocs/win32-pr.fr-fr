---
description: ICE17 vérifie les situations indiquées dans l’exemple à la fin de cette rubrique.
ms.assetid: a1d9a6e9-4d21-4544-a813-dc82e11f5a26
title: ICE17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c296273e1de5ae633b2708c92cf0376018e6d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866301"
---
# <a name="ice17"></a>ICE17

ICE17 vérifie les situations indiquées dans l’exemple à la fin de cette rubrique.

## <a name="result"></a>Résultats

ICE17 affiche un message d’erreur ou d’avertissement pour chacune des situations de l’exemple. Les exemples de ces messages sont présentés dans le tableau suivant.



| Erreur ou avertissement ICE17                                                                                                                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PushButton : Button1 de la boîte de dialogue : MyDialog n’a pas d’événement défini dans la table ControlEvent,. Error <br/>                                                                                                                | Il existe un [contrôle PUSHBUTTON](pushbutton-control.md) qui n’est pas listé dans la [table ControlEvent,](controlevent-table.md). Si ICE17 retourne cette erreur sur un PushButton pour lequel l’attribut **Enable Control** ou l’attribut **Control visible** n’est pas défini dans la colonne Attributes de la [table Control](control-table.md), vérifiez si le contrôle a également une entrée dans la [table ControlCondition](controlcondition-table.md). Le contrôle peut être activé de manière inattendue, ou visible, si la valeur dans la colonne condition devient true, Enable ou Show.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| Bitmap : bitmap1 de contrôle : bitmap1 de la boîte de dialogue : MyDialog n’est pas dans la table binaire. Error <br/>                                                                                                                              | Il existe un contrôle [bitmap](bitmap-control.md) ou un [contrôle Icon](icon-control.md), mais l’image bitmap ou l’icône correspondante ne figure pas dans la [table binaire](binary-table.md). Ajoutez la bitmap ou l’icône à la table binaire.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| RadioButtonGroup : RadioButton1 de contrôle : RadioButton1 de la boîte de dialogue : MyDialog n’est pas dans la table de RadioButton. Avertissement <br/>                                                                                                   | Il existe un [contrôle RadioButtonGroup](radiobuttongroup-control.md) avec des valeurs dans la colonne de propriété et la colonne d’attribut de la [table de contrôle](control-table.md); le bit [indirect](indirect-control-attribute.md) n’est pas défini dans la colonne attributs. ICE17 publie un avertissement, car le programme d’installation utilise la valeur de la propriété comme clé étrangère dans la table RadioButton, mais la valeur est absente de la clé primaire de cette table. Si le bit [indirect](indirect-control-attribute.md) est défini, la propriété indiquée pour le contrôle n’est pas utilisée en tant que propriété ; au lieu de cela, il est utilisé comme nom de la propriété qui est réellement utilisée.<br/> Cet avertissement peut être ignoré si le contrôle est créé au moment de l’exécution. Par exemple, le [contrôle ListBox](listbox-control.md) pour dans la [boîte de dialogue FilesInUse](filesinuse-dialog.md) est uniquement créé au moment de l’exécution si des fichiers sont en cours d’utilisation pendant l’installation.<br/> |
| ListBox : ListBox1 du contrôle : ListBox1 de la boîte de dialogue : MyDialog n’est pas dans la table ListBox. Avertissement <br/>                                                                                                                        | Il existe un [contrôle ListBox](listbox-control.md) avec une valeur dans la colonne propriété de la [table de contrôle](control-table.md) et pour lequel le bit [indirect](indirect-control-attribute.md) n’est pas défini dans la colonne attributs. ICE17 publie un avertissement, car le programme d’installation utilise la valeur de la propriété comme clé étrangère dans la [table ListBox](listbox-table.md), mais la valeur est absente de la clé primaire de cette table. Si le bit [indirect](indirect-control-attribute.md) est défini, le contrôle modifie la valeur d’une propriété dont le nom correspond à la valeur de la propriété associée à ce contrôle.<br/> Cet avertissement peut être ignoré si le contrôle est créé au moment de l’exécution. Par exemple, le [contrôle ListBox](listbox-control.md) pour dans la [boîte de dialogue FilesInUse](filesinuse-dialog.md) est uniquement créé au moment de l’exécution si des fichiers sont en cours d’utilisation pendant l’installation.<br/>                                |
| ComboBox : ComboBox1 du contrôle : ComboBox1 de la boîte de dialogue : ByDialog n’est pas dans l’avertissement de table ComboBox <br/>                                                                                                                     | Il existe un [contrôle de zone de liste déroulante](combobox-control.md) avec une valeur dans la colonne propriété de la [table de contrôle](control-table.md) et pour lequel le bit [indirect](indirect-control-attribute.md) n’est pas défini dans la colonne attributs. ICE17 publie un avertissement, car le programme d’installation utilise la valeur de la propriété comme clé étrangère dans la table de la [zone de liste déroulante](combobox-table.md), mais la valeur est absente de la clé primaire de cette table. Si le bit [indirect](indirect-control-attribute.md) est défini, le contrôle modifie la valeur d’une propriété dont le nom correspond à la valeur de la propriété associée à ce contrôle.<br/> Cet avertissement peut être ignoré si le contrôle est créé au moment de l’exécution. Par exemple, le [contrôle ListBox](listbox-control.md) pour dans la [boîte de dialogue FilesInUse](filesinuse-dialog.md) est uniquement créé au moment de l’exécution si des fichiers sont en cours d’utilisation pendant l’installation.<br/>                            |
| ListView : ListView1 de Control : ListView1 de la boîte de dialogue : MyDialog n’est pas dans la table ListView. Avertissement <br/>                                                                                                                    | Il existe un [contrôle ListView](listview-control.md) avec une valeur dans la colonne propriété de la [table de contrôle](control-table.md) et pour lequel le bit [indirect](indirect-control-attribute.md) n’est pas défini dans la colonne attributs. ICE17 publie un avertissement, car le programme d’installation utilise la valeur de la propriété comme clé étrangère dans la [table ListView](listview-table.md), mais la valeur est absente de la clé primaire de cette table. Si le bit [indirect](indirect-control-attribute.md) est défini, le contrôle modifie la valeur d’une propriété dont le nom correspond à la valeur de la propriété associée à ce contrôle.<br/> Cet avertissement peut être ignoré si le contrôle est créé au moment de l’exécution. Par exemple, le [contrôle ListBox](listbox-control.md) pour dans la [boîte de dialogue FilesInUse](filesinuse-dialog.md) est uniquement créé au moment de l’exécution si des fichiers sont en cours d’utilisation pendant l’installation.<br/>                            |
| Bitmap : 'Bitmap2 'pour le contrôle : 'button2 'de la boîte de dialogue : 'MyDialog’introuvable dans l’erreur de table binaire <br/>                                                                                                                         | Il y a un contrôle de [bouton de commande](pushbutton-control.md) ou un contrôle de [case à cocher](checkbox-control.md) pour lequel la colonne de texte de la [table de contrôle](control-table.md) ne contient pas de clé étrangère dans l’enregistrement de la [table binaire](binary-table.md) contenant la bitmap ou l’icône.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Bitmap : 'Bitmap3 'pour le contrôle : 'RadioButton2 'de la boîte de dialogue : 'MyDialog’introuvable dans la table binaire ou<br/> Icône : 'icon1 'pour le contrôle : 'RadioButton3 'de la boîte de dialogue : 'MyDialog’introuvable dans la table binaire<br/> Error <br/> | Il existe un [contrôle RadioButtonGroup](radiobuttongroup-control.md) pour lequel la colonne text de la [table RadioButton](radiobutton-table.md) ne contient pas de clé étrangère dans l’enregistrement de la [table binaire](binary-table.md) contenant la bitmap ou l’icône.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Contrôle d’image : le « button3 » de la boîte de dialogue « MyDialog » a à la fois une erreur d’icône et d’attributs bitmap. <br/>                                                                                                                     | Il y a un contrôle de [bouton](pushbutton-control.md)de commande, [case à cocher](checkbox-control.md)ou [RadioButtonGroup](radiobuttongroup-control.md) avec le bit d' [icône](icon-control-attribute.md) ou le bit de [bitmap](bitmap-control-attribute.md) défini dans la colonne attributs de la [table de contrôle](control-table.md). Vous ne pouvez pas définir les deux attributs ensemble.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="example"></a>Exemple

[Table de contrôle](control-table.md) (partielle)



| Dialogue\_ | Contrôler      | Type             | Attributs | Propriété     | Texte       |
|----------|--------------|------------------|------------|--------------|------------|
| MyDialog | Button1      | Boutons       | 0          |              | Ok         |
| MyDialog | Bitmap1      | Bitmap           | 0          |              | Bitmap1    |
| MyDialog | RadioButton1 | RadioButtonGroup | 0          | RadioButton1 |            |
| MyDialog | ListBox1     | ListBox          | 0          | ListBox1     |            |
| MyDialog | ComboBox1    | Liste déroulante         | 0          | ComboBox1    |            |
| MyDialog | ListView1    | Affichage de liste         | 0          | ListView1    |            |
| MyDialog | Button2      | Boutons       | 262 144     |              | Bitmap2    |
| MyDialog | RadioButton2 | RadioButtonGroup | 262 144     |              | Property2  |
| MyDialog | RadioButton3 | RadioButtonGroup | 524 288     |              | Property3  |
| MyDialog | Button3      | Boutons       | 786432     |              | Ambiguous1 |



 

[Table RadioButton](radiobutton-table.md) (partielle)



| Propriété\_ | Commande | Texte    |
|------------|-------|---------|
| Property2  | 1     | Bitmap3 |
| Property3  | 2     | Icon1   |



 

Les tableaux suivants sont vides :

-   [Table ControlEvent,](controlevent-table.md)
-   [Table ListBox](listbox-table.md)
-   [Table ComboBox](combobox-table.md)
-   [Tableau ListView](listview-table.md)
-   [Table binaire](binary-table.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 




