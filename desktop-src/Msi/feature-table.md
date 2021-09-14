---
description: La table des fonctionnalités définit la structure de l’arborescence logique des fonctionnalités et contient les colonnes indiquées dans le tableau suivant.
ms.assetid: 1faee1d5-6e39-43ea-bf92-a0b3986a13a1
title: Tableau des fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa91df750c4994a2d8a2308705213e48c864518
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091245"
---
# <a name="feature-table"></a>Tableau des fonctionnalités

La table des fonctionnalités définit la structure de l’arborescence logique des fonctionnalités et contient les colonnes indiquées dans le tableau suivant.



| Colonne          | Type                         | Clé | Nullable |
|-----------------|------------------------------|-----|----------|
| Fonctionnalité         | [Identificateur](identifier.md) | O   | N        |
| Parent de la fonctionnalité \_ | [Identificateur](identifier.md) | N   | O        |
| Intitulé           | [Text](text.md)             | N   | O        |
| Description     | [Text](text.md)             | N   | O        |
| Affichage         | [Integer](integer.md)       | N   | O        |
| Level           | [Integer](integer.md)       | N   | N        |
| Répertoire\_     | [Identificateur](identifier.md) | N   | O        |
| Attributs      | [Integer](integer.md)       | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Feature"></span><span id="feature"></span><span id="FEATURE"></span>Fonctionnalité
</dt> <dd>

Clé primaire utilisée pour identifier un enregistrement de fonctionnalité spécifique. La valeur de ce champ ne doit pas dépasser une longueur maximale de 38 caractères.

</dd> <dt>

<span id="Feature_Parent"></span><span id="feature_parent"></span><span id="FEATURE_PARENT"></span>Parent de la fonctionnalité \_
</dt> <dd>

Clé facultative d’un enregistrement parent dans la même table.

La clé pointe vers la colonne de fonctionnalité. Si la fonctionnalité parent n’est pas sélectionnée, cette fonctionnalité n’est pas installée. Une valeur null dans ce champ indique que cette fonctionnalité n’a pas de parent et qu’il s’agit d’un élément racine. La \_ colonne parente de la fonctionnalité ne doit pas être égale à la colonne de fonctionnalité du même enregistrement.

> [!Note]  
> La profondeur maximale de toutes les fonctionnalités est de 16. Une [erreur 2701](windows-installer-error-messages.md) se produit si une fonctionnalité qui dépasse cette profondeur maximale existe.

 

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Bonhomme
</dt> <dd>

Chaîne de texte abrégée qui identifie une fonctionnalité.

Cette chaîne est listée en tant qu’élément par le [contrôle SelectionTree](selectiontree-control.md) de la [boîte de dialogue de sélection](selection-dialog.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Chaîne de texte plus longue qui décrit une fonctionnalité.

Cette chaîne localisable est affichée par le [contrôle Text](text-control.md) de la [boîte de dialogue de sélection](selection-dialog.md).

</dd> <dt>

<span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>Vidéo
</dt> <dd>

Le nombre dans ce champ spécifie l’ordre dans lequel la fonctionnalité doit être affichée dans l’interface utilisateur.

La valeur détermine également si la fonctionnalité est affichée initialement développée ou réduite. Si la valeur est null ou 0 (zéro), l’enregistrement n’est pas affiché.

-   Si la valeur est impaire, le nœud Feature est développé initialement.
-   Si la valeur est pair, le nœud de fonctionnalité est réduit au départ.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Niveau
</dt> <dd>

Niveau d’installation initial de cette fonctionnalité. Le traitement de la [table de conditions](condition-table.md) peut modifier la valeur de niveau.

Un niveau d’installation de 0 (zéro) désactive l’élément et l’empêche de s’afficher. Une fonctionnalité avec un niveau d’installation de 0 (zéro) n’est pas installée lors de l’installation, y compris les installations administratives. Pour plus d’informations, consultez les informations sur le niveau d’installation dans la section Remarques de cette rubrique.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_
</dt> <dd>

La \_ colonne Directory spécifie le nom d’un répertoire qui peut être configuré par une [boîte de dialogue de sélection](selection-dialog.md).

Étant donné que ce champ est une clé dans la [table de répertoires](directory-table.md), le répertoire spécifié doit figurer dans la première colonne de la table de répertoires. Vous devez entrer une [propriété publique](public-properties.md) dans cette colonne pour rendre le répertoire configurable et afficher un bouton **Parcourir** dans la [boîte de dialogue de sélection](selection-dialog.md).

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs
</dt> <dd>

L’option d’exécution à distance pour les fonctionnalités qui ne sont pas installées et pour lesquelles aucune demande d’état de fonctionnalité n’est effectuée à l’aide de l’une des propriétés suivantes.

-   [**Propriété ADDLOCAL**](addlocal.md)
-   [**Propriété ADDSOURCE**](addsource.md)
-   [**Propriété ADDDEFAULT**](adddefault.md)
-   [**Propriété COMPADDLOCAL**](compaddlocal.md)
-   [**Propriété COMPADDSOURCE**](compaddsource.md)
-   [**Propriété FILEADDLOCAL**](fileaddlocal.md)
-   [**Propriété FILEADDSOURCE**](fileaddsource.md)
-   [**SUPPRIMER la propriété**](remove.md)
-   [**RÉINSTALLER la propriété**](reinstall.md)
-   [**Propriété ADVERTISE**](advertise.md)

Ajoutez les bits indiqués à la valeur totale de cette colonne pour inclure une option d’exécution à distance.

-   Si ce champ est vide, la valeur par défaut est 0 (zéro), msidbFeatureAttributesFavorLocal.
-   Si le niveau d’installation de la fonctionnalité est 0 (zéro), ou supérieur ou égal au niveau d’installation actuel, aucune modification n’est apportée à l’état de la fonctionnalité.



| Nom                                         | Decimal | Valeur hexadécimale | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|---------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msidbFeatureAttributesFavorLocal             | 0       | 0x0000      | Les composants de cette fonctionnalité qui ne sont pas marqués pour l’installation à partir de la source sont installés localement. Un composant partagé par deux fonctionnalités ou plus, dont certains ont la valeur msidbFeatureAttributesFavorLocal et d’autres à msidbFeatureAttributesFavorSource, est installé localement. Les composants marqués msidbComponentAttributesSourceOnly dans la [table des composants](component-table.md) sont toujours exécutés à partir du CD/serveur source. Les msidbFeatureAttributesFavorLocal bits et msidbFeatureAttributesFavorSource fonctionnent avec des fonctionnalités qui ne sont pas listées par la [**propriété advertise**](advertise.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| msidbFeatureAttributesFavorSource            | 1       | 0x0001      | Les composants de cette fonctionnalité non marqués pour une installation locale sont installés pour s’exécuter à partir du CD-ROM ou du serveur source. Un composant partagé par deux fonctionnalités ou plus, dont certains ont la valeur msidbFeatureAttributesFavorLocal et d’autres à msidbFeatureAttributesFavorSource, est installé pour s’exécuter localement. Les composants marqués msidbComponentAttributesLocalOnly dans la [table des composants](component-table.md) sont toujours installés localement. Les msidbFeatureAttributesFavorLocal bits et msidbFeatureAttributesFavorSource fonctionnent avec des fonctionnalités qui ne sont pas listées par la [**propriété advertise**](advertise.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesFollowParent           | 2       | 0x0002      | Définissez cet attribut et l’état de la fonctionnalité est le même que l’état du parent de la fonctionnalité. Vous ne pouvez pas utiliser cette option si la fonctionnalité se trouve à la racine d’une arborescence de fonctionnalités. Omettez cet attribut et l’état de la fonctionnalité est déterminé en fonction des msidbFeatureAttributesDisallowAdvertise et msidbFeatureAttributesFavorLocal et msidbFeatureAttributesFavorSource.<br/> Pour garantir que l’état de la fonctionnalité enfant suit toujours l’état de son parent, même lorsque l’enfant et le parent sont initialement définis comme absents dans le contrôle SelectionTree, vous devez inclure msidbFeatureAttributesFollowParent et msidbFeatureAttributesUIDisallowAbsent dans les attributs de la fonctionnalité enfant.<br/> Notez que si vous définissez msidbFeatureAttributesFollowParent sans définir msidbFeatureAttributesUIDisallowAbsent, le programme d’installation ne peut pas forcer la fonctionnalité enfant à sortir de l’État absent. Dans ce cas, la fonctionnalité enfant correspond à l’état d’installation du parent uniquement si l’enfant a une valeur autre que absent.<br/> Définissez msidbFeatureAttributesFollowParent et msidbFeatureAttributesUIDisallowAbsent pour vous assurer qu’une fonctionnalité enfant suit l’état de la fonctionnalité parente.<br/> |
| msidbFeatureAttributesFavorAdvertise         | 4       | 0x0004      | Définissez cet attribut et l’état de la fonctionnalité est publier. Si la fonctionnalité est indiquée par la [**propriété AddDefault**](adddefault.md) , ce bit est ignoré et l’état de la fonctionnalité est déterminé en fonction de MsidbFeatureAttributesFavorLocal et msidbFeatureAttributesFavorSource. Omettez cet attribut et l’état de la fonctionnalité est déterminé en fonction des msidbFeatureAttributesDisallowAdvertise et msidbFeatureAttributesFavorLocal et msidbFeatureAttributesFavorSource.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| msidbFeatureAttributesDisallowAdvertise      | 8       | 0x0008      | Notez que ce bit fonctionne uniquement avec les fonctionnalités répertoriées par la [**propriété publier**](advertise.md). Définissez cet attribut pour empêcher la publication de la fonctionnalité.<br/> Définissez cet attribut et si la fonctionnalité indiquée n’est pas un parent ou un enfant, la fonctionnalité est installée conformément à msidbFeatureAttributesFavorLocal et msidbFeatureAttributesFavorSource.<br/> Définissez cet attribut pour le parent d’une fonctionnalité de liste et le parent est installé.<br/> Définissez cet attribut pour l’enfant d’une fonctionnalité indiquée et l’état de l’enfant est absent.<br/> Omettez cet attribut et si la fonctionnalité indiquée n’est pas un parent ou un enfant, l’état de la fonctionnalité est publier.<br/> Omettez cet attribut et si la fonctionnalité indiquée est un parent ou un enfant, l’état des deux fonctionnalités est publier.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| msidbFeatureAttributesUIDisallowAbsent       | 16      | 0x0010      | Définissez cet attribut et l’interface utilisateur n’affiche pas d’option permettant de changer l’état de la fonctionnalité en absent. La définition de cet attribut force la fonctionnalité à l’état d’installation, que la fonctionnalité soit visible ou non dans l’interface utilisateur. Omettez cet attribut et l’interface utilisateur affiche une option permettant de changer l’état de la fonctionnalité en absent.<br/> Définissez msidbFeatureAttributesFollowParent et msidbFeatureAttributesUIDisallowAbsent pour vous assurer qu’une fonctionnalité enfant suit l’état de la fonctionnalité parente.<br/> La définition de cet attribut affecte non seulement l’interface utilisateur, mais force également la fonctionnalité à l’état d’installation si la fonctionnalité est visible dans l’interface utilisateur ou non.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesNoUnsupportedAdvertise | 32      | 0x0020      | définissez cet attribut et la publication est désactivée pour la fonctionnalité si le shell du système d’exploitation ne prend pas en charge les descripteurs de Windows Installer. Omettez cet attribut et la publication n’est pas désactivée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Certains attributs sont exclusifs les uns des autres. Si vous tentez de définir ces attributs ensemble sur la même fonctionnalité, le package d’installation échoue la [**validation du package**](package-validation.md).

-   N’utilisez pas msidbFeatureAttributesFavorAdvertise avec msidbFeatureAttributesDisallowAdvertise.
-   N’utilisez pas msidbFeatureAttributesNoUnsupportedAdvertise avec msidbFeatureAttributesDisallowAdvertise ensemble.
-   N’utilisez pas msidbFeatureAttributesFollowParent avec msidbFeatureAttributesFavorSource.
-   Notez que les valeurs msidbFeatureAttributesFollowParent et msidbFeatureAttributesFavorLocal s’excluent mutuellement. Si la valeur msidbFeatureAttributesFollowParent est utilisée, la valeur de msidbFeatureAttributesFavorLocal est supposée n’existe pas.

</dd> </dl>

Notez que si une fonctionnalité enfant est installée, sa fonctionnalité parente est également installée. Si une fonctionnalité parente est installée, sa fonctionnalité enfant n’est pas nécessairement installée, sauf si ses attributs msidbFeatureAttributesFollowParent et msidbFeatureAttributesUIDisallowAbsent sont définis. Cette relation hiérarchique de l’installation des fonctionnalités parent et enfant est également utilisée pour les installations et installations de l’interface utilisateur qui utilisent des propriétés de ligne de commande.

## <a name="remarks"></a>Notes

Plusieurs colonnes temporaires supplémentaires sont ajoutées à cette table lorsqu’elle est chargée en mémoire pour les calculs utilisés par la sélection de l’interface utilisateur et de l’évaluation des coûts.

Un composant peut être partagé entre deux ou plusieurs fonctionnalités ou applications. Si deux fonctionnalités ou plus font référence au même composant, alors ce composant est sélectionné pour l’installation si l’une des fonctionnalités associées est sélectionnée. Cela peut également être la raison pour laquelle les fonctionnalités enfants ne sont pas désinstallées lorsqu’une fonctionnalité parente est supprimée. si la fonctionnalité enfant est constituée de composants requis par d’autres fonctionnalités ou applications, le Windows Installer ne supprime pas la fonctionnalité enfant.

Pour plus d’informations, consultez contrôle de la [sélection des fonctionnalités États](controlling-feature-selection-states.md).

Niveau d’installation :

-   Pour n’importe quelle installation, il existe un niveau d’installation défini, qui est une valeur intégrale comprise entre 1 et 32 767. La valeur initiale est déterminée par la [**propriété INSTALLLEVEL**](installlevel.md), qui est définie dans la [table de propriétés](property-table.md).
-   Une fonctionnalité est installée uniquement si la valeur de niveau de fonctionnalité est inférieure ou égale au niveau d’installation actuel. L’interface utilisateur peut être créée de sorte que lorsque l’installation est initialisée, le programme d’installation permet à l’utilisateur de modifier le niveau d’installation de n’importe quelle fonctionnalité du tableau des fonctionnalités. Par exemple, un auteur peut définir des valeurs de niveau d’installation qui représentent des options d’installation spécifiques, telles que **personnalisée**, **standard** ou **minimale**, puis créer une boîte de dialogue qui utilise [SetInstallLevel ControlEvents](setinstalllevel-controlevent.md) pour permettre à l’utilisateur de sélectionner l’un de ces États.
-   En fonction de l’état sélectionné par l’utilisateur, la boîte de dialogue affecte à la propriété niveau d’installation la valeur correspondante. Si l’auteur affecte un niveau **standard** de 100 et que l’utilisateur sélectionne **standard**, seules les fonctionnalités dont le niveau est inférieur ou égal à 100 sont installées. En outre, l’option **personnalisée** peut aboutir à une autre boîte de dialogue qui contient un [contrôle SelectionTree](selectiontree-control.md). Le contrôle SelectionTree permet ensuite à l’utilisateur de changer individuellement si chaque fonctionnalité est installée ou non.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE10](ice10.md)  
[ICE14](ice14.md)  
[ICE21](ice21.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE45](ice45.md)  
[ICE47](ice47.md)  
[ICE50](ice50.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE67](ice67.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
[ICE94](ice94.md)  
</dl>

 

 




