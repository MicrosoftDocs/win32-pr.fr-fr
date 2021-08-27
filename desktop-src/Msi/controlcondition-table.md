---
description: La table ControlCondition permet à un auteur de spécifier des actions spéciales à appliquer aux contrôles en fonction du résultat d’une instruction conditionnelle. Par exemple, à l’aide de cette table, l’auteur peut choisir de masquer un contrôle en fonction de la propriété VersionNT.
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: Table ControlCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637d9470af21ad1f8a15c2697ba34a6c9866c822c21c6f3a85241bac1309f76b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105249"
---
# <a name="controlcondition-table"></a>Table ControlCondition

La table ControlCondition permet à un auteur de spécifier des actions spéciales à appliquer aux contrôles en fonction du résultat d’une instruction conditionnelle. Par exemple, à l’aide de cette table, l’auteur peut choisir de masquer un contrôle en fonction de la propriété [**VersionNT**](versionnt.md) .

La table ControlCondition contient les colonnes suivantes.



| Colonne    | Type                         | Clé | Nullable |
|-----------|------------------------------|-----|----------|
| Boîte de dialogue\_  | [Identificateur](identifier.md) | O   | N        |
| contrôle\_ | [Identificateur](identifier.md) | O   | N        |
| Action    | [Text](text.md)             | O   | N        |
| Condition | [Condition](condition.md)   | O   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogue\_
</dt> <dd>

Clé externe de la première colonne de la [table de boîtes de dialogue](dialog-table.md). La combinaison de ce champ avec le champ de contrôle \_ identifie un contrôle unique.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Régulation\_
</dt> <dd>

Clé externe de la deuxième colonne de la [table de contrôle](control-table.md). Combinaison de ce champ le champ de la boîte de dialogue \_ identifie un contrôle unique.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel
</dt> <dd>

Action qui doit être exécutée sur le contrôle. Les actions possibles sont présentées dans le tableau suivant.



| Valeur   | Signification                     |
|---------|-----------------------------|
| Default | Définir le contrôle comme valeur par défaut. |
| Désactiver | Désactivez le contrôle.        |
| Activer  | Activez le contrôle.         |
| Masquer    | Masquez le contrôle.           |
| Afficher    | Affichez le contrôle.        |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat
</dt> <dd>

Instruction conditionnelle qui spécifie les conditions dans lesquelles l’action doit être déclenchée. Cette colonne ne peut pas être vide. Si cette instruction ne prend pas la valeur TRUE, l’action n’a pas lieu. S’il est défini sur 1, l’action est toujours appliquée. Pour plus d’informations sur la syntaxe des instructions conditionnelles, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

Si vous souhaitez masquer et désactiver un contrôle de [bouton de commande](pushbutton-control.md) ou un contrôle de [case à cocher](checkbox-control.md) en fonction d’une instruction conditionnelle dans le champ condition de la table ControlCondition, vous devez utiliser quatre enregistrements pour chaque contrôle afin de désactiver et masquer le contrôle. Les contrôles de bouton de commande ou de case à cocher qui ont été masqués sont toujours accessibles par les touches de raccourci.

Par exemple, les enregistrements suivants masquent et désactivent ControlA sur DIALOGA lorsque le produit est installé. Le contrôle sera visible et activé lorsque le produit n’est pas installé.



| Boîte de dialogue  | Contrôler  | Action  | Condition                      |
|---------|----------|---------|--------------------------------|
| Boîte de dialogue | ControlA | Masquer    | [**Installé**](installed.md) |
| Boîte de dialogue | ControlA | Désactiver | Installé                      |
| Boîte de dialogue | ControlA | Afficher    | NON installé                  |
| Boîte de dialogue | ControlA | Activer  | NON installé                  |



 

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



