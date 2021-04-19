---
description: Les qualificateurs facultatifs traitent les situations récurrentes non communes à toutes les implémentations compatibles CIM, qui ne sont pas requises pour interpréter ces qualificateurs.
ms.assetid: f31162d1-25e6-494a-bc7d-f66955b514a6
ms.tgt_platform: multiple
title: Qualificateurs facultatifs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Optional
api_type:
- NA
api_location: ''
ms.openlocfilehash: 36fe1b9ceee1211a3b09ce70e03044b7af57eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536632"
---
# <a name="optional-qualifiers"></a>Qualificateurs facultatifs

Les qualificateurs facultatifs traitent les situations récurrentes non communes à toutes les implémentations compatibles CIM, qui ne sont pas requises pour interpréter ces qualificateurs. Les qualificateurs facultatifs sont fournis dans la spécification pour éviter les qualificateurs définis par l’utilisateur aléatoires qui peuvent se produire dans ces situations récurrentes.

<dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Supprimer**
</dt> <dd>

Type de données : **booléen**

S’applique à : associations, références

Pour les associations, indique si l’Association qualifiée doit être supprimée si l’un des objets référencés dans l’Association est supprimé et si l’objet respectif référencé dans l’Association est qualifié avec **IfDeleted**. La valeur par défaut est **false**.

Pour les références, ce qualificateur indique si l’objet référencé doit être supprimé si l’Association contenant la référence est supprimée et qualifiée avec **IfDeleted**, ou si l’un des objets référencés dans l’Association est supprimé et que l’objet respectif référencé dans l’Association est qualifié avec **IfDeleted**.

Utilisation : les applications doivent suivre les associations et les références marquées avec le qualificateur **Delete** et supprimer l’Association ou la référence de manière appropriée. Si un objet de l’Association a été supprimé mais n’est pas marqué avec **IfDeleted**, l’Association ne doit pas être supprimée.

Cette règle d’utilisation doit être vérifiée lorsque le modèle de sécurité CIM est défini.

</dd> <dt>

<span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Complexes**
</dt> <dd>

Type de données : **booléen**

S’applique à : propriétés, références, classes, associations, méthodes

Indique si l’action implicite requiert un calcul extensif. La valeur par défaut est **false**.

</dd> <dt>

<span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**
</dt> <dd>

Type de données : **booléen**

S’applique à : associations et références

Indique si tous les objets d’une association qui sont qualifiés par **Delete** doivent être supprimés si l’objet référencé ou l’Association est supprimé. La valeur par défaut est **false**.

</dd> <dt>

<span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indexée**
</dt> <dd>

Type de données : **booléen**

S’applique à : propriétés, méthodes

Indique si une propriété de classe doit être indexée. En cas d’application aux propriétés dans les classes hébergées par le référentiel, cela a uniquement la signification de la création (au moment de la création de la classe) d’une recherche de requête secondaire rapide pour cette propriété.

Seule la valeur **true** (valeur par défaut) est autorisée.

</dd> <dt>

<span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Masquer**
</dt> <dd>

Type de données : **booléen**

S’applique à : associations, propriétés, méthodes, références, classes

Indique si l’Association est définie uniquement à des fins internes (par exemple, pour la définition de la sémantique de dépendance) et ne doit pas être affichée (par exemple, dans les mappages). La valeur par défaut est **false**.

</dd> <dt>

<span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Conséquent**
</dt> <dd>

Type de données : **booléen**

S’applique à : Properties, classes

Indique si la propriété ou la classe requiert une grande quantité d’espace de stockage. La valeur par défaut est **false**.

</dd> <dt>

<span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Non \_ null**
</dt> <dd>

Type de données : **booléen**

S’applique à : Properties

Indique si une propriété de classe ne peut pas prendre la valeur **null** (**VT \_ null**). Seule la valeur **true** (valeur par défaut) est autorisée.

Si ce qualificateur est spécifié, WMI n’autorise pas la création d’instances avec la propriété définie sur **null**, et les propriétés **null** retournent le code d’erreur **\_ \_ \_ null non conforme WBEM E** .

Notez que la [**clé**](standard-qualifiers.md) et les qualificateurs **indexés** impliquent déjà ce comportement.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Moteur**
</dt> <dd>

Type de données : **chaîne**

S’applique à : any

Indique que l’élément de schéma est dynamique et donc rempli par un fournisseur. La valeur par défaut est **null**. Ce qualificateur est un handle spécifique à l’implémentation de l’instrumentation.

</dd> <dt>

<span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Pratiqué**
</dt> <dd>

Type de données : **booléen**

S’applique à : any

Indique que l’élément spécifié a été proposé pour faire partie d’une version ultérieure des schémas CIM, mais qu’il ne fait pas encore partie du schéma standard. Au lieu de cela, l’élément est disponible pour permettre aux utilisateurs d’expérimenter, d’implémenter et de fournir des commentaires sur. En fonction des commentaires, l’élément peut être ajouté à la norme comme présenté, modifié ou supprimé. La valeur par défaut est **false**. Une implémentation n’a pas besoin de prendre en charge un élément avec ce qualificateur.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

Type de données : **chaîne**

S’applique à : propriétés, références, méthodes, paramètres

Type spécifique assigné à un élément de données. La valeur par défaut est **null**.

Utilisation : vous devez utiliser le qualificateur **SyntaxType** avec ce qualificateur.

</dd> <dt>

<span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**
</dt> <dd>

Type de données : **chaîne**

S’applique à : propriétés, références, méthodes, paramètres

Format du qualificateur de **syntaxe** . La valeur par défaut est **null**.

Utilisation : vous devez utiliser le qualificateur de **syntaxe** avec ce qualificateur.

</dd> <dt>

<span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**
</dt> <dd>

Type de données : **chaîne**

S’applique à : classes, propriétés, méthodes, associations, indications, références

Circonstances dans lesquelles un déclencheur est déclenché. La valeur par défaut est **null**. Les types de déclencheurs varient selon la construction du modèle méta.

Pour les classes et les associations, les valeurs autorisées sont les suivantes :

Créer

DELETE

Update

Accès

Pour les propriétés et les références, les valeurs autorisées sont : Update et Access.

Pour les méthodes, les valeurs autorisées sont avant et après.

Pour les indications, la valeur légale est levée.

</dd> <dt>

<span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**
</dt> <dd>

Type de données : **tableau de chaînes**

S’applique à : Properties

Ensemble de valeurs indiquant que la valeur de la propriété associée est inconnue (la propriété ne peut pas être considérée comme ayant une valeur valide ou explicite). La valeur par défaut est **null**.

Les conventions et restrictions utilisées pour définir des valeurs inconnues sont les mêmes que celles applicables au qualificateur [**ValueMap**](standard-qualifiers.md) .

Notez que ce qualificateur ne peut pas être substitué. Il est déraisonnable de permettre à une sous-classe de traiter une valeur comme une valeur connue quand elle est traitée comme inconnue par une classe parente.

</dd> <dt>

<span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**
</dt> <dd>

Type de données : **tableau de chaînes**

S’applique à : Properties

Ensemble de valeurs indiquant que la valeur de la propriété associée n’est pas prise en charge (la propriété ne peut pas être considérée comme ayant une valeur valide ou explicite). La valeur par défaut est **null**.

Les conventions et restrictions utilisées pour définir des valeurs non prises en charge sont les mêmes que celles applicables au qualificateur [**ValueMap**](standard-qualifiers.md) .

Notez que ce qualificateur ne peut pas être substitué. Il est déraisonnable de permettre à une sous-classe de traiter une valeur comme une valeur prise en charge qui est traitée comme inconnue par une classe parente.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Qualificateurs WMI](wmi-qualifiers.md)
</dt> <dt>

[Ajout d’un qualificateur](adding-a-qualifier.md)
</dt> </dl>

 

 




