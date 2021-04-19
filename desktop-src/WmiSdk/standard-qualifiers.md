---
description: Toutes les implémentations compatibles CIM doivent gérer un ensemble standard de qualificateurs.
ms.assetid: 671ea769-f68d-4788-96f5-c4f86ab3b00e
ms.tgt_platform: multiple
title: Qualificateurs standard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: 710e93e53f9e414a44dc14ebafea426f5d7f9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527808"
---
# <a name="standard-qualifiers"></a>Qualificateurs standard

Toutes les implémentations compatibles CIM doivent gérer un ensemble standard de qualificateurs. Aucun objet spécifique n’a tous les qualificateurs listés. En règle générale, les classes d’extension fournissent des qualificateurs supplémentaires pour faciliter la configuration des instances de classe et d’autres opérations sur la classe.

Il incombe au fournisseur d’appliquer les qualificateurs. WMI n’applique pas de qualificateurs, mais les utilise uniquement pour informer l’utilisateur de la façon dont la propriété est utilisée.

> [!Note]  
> WMI est conforme à la spécification CIM 2,5.

 

Les qualificateurs présentent les limitations suivantes :

-   Tous les qualificateurs standard ne peuvent pas être utilisés ensemble.
-   Tous les qualificateurs ne peuvent pas être appliqués à toutes les constructions, telles que l’Association ou la référence. Ces limitations sont identifiées dans la liste s’applique à.
-   Pour une construction particulière, telle que l’Association ou la référence, l’utilisation des qualificateurs légaux peut être plus contraignante, car certains qualificateurs s’excluent mutuellement, l’utilisation d’un qualificateur peut impliquer certaines restrictions sur la valeur d’une autre, et ainsi de suite. Ces règles d’utilisation sont documentées.
-   Les qualificateurs légaux sont hérités par des entités telles que des propriétés, des méthodes, des instances ou des sous-classes uniquement, et non par des associations ou des références. Par exemple, le qualificateur **MaxLen** qui s’applique aux propriétés n’est pas hérité par les références.

La liste suivante répertorie les qualificateurs WMI standard.

<dt>

<span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Abstraction**
</dt> <dd>

Type de données : **booléen**

S’applique à : classes, associations, indications

Indique si la classe est abstraite et sert uniquement de base pour les nouvelles classes. La valeur par défaut est **false**. Vous ne pouvez pas créer d’instances de classes abstraites. L’absence de ce qualificateur indique que la classe n’est pas abstraite ; par conséquent, ce qualificateur est requis pour toutes les classes abstraites.

</dd> <dt>

<span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Rassemble**
</dt> <dd>

Type de données : **booléen**

S’applique à : références

Indique si la référence est le composant parent d’une association d’agrégation. La valeur par défaut est **false**.

Utilisation : les **qualificateurs Aggregation et** **Aggregate** sont utilisés ensemble l'   **agrégation** qualifie l’Association, et **Aggregate** spécifie la référence parente.

</dd> <dt>

<span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Agréger**
</dt> <dd>

Type de données : **booléen**

S’applique à : associations

Indique si l’Association est une agrégation. La valeur par défaut est **false**. Utilisé avec **Aggregate**. Ce qualificateur est requis pour toutes les associations d’agrégation.

</dd> <dt>

<span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Affecté**
</dt> <dd>

Type de données : **chaîne**

S’applique à : propriétés, références, méthodes

Autre nom pour une propriété ou une méthode dans le schéma. La valeur par défaut est **null**.

</dd> <dt>

<span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**
</dt> <dd>

Type de données : **chaîne**

S’applique à : propriétés, paramètres

Type du tableau qualifié.

Les valeurs autorisées sont :

-   Bag (valeur par défaut)
-   indexé
-   ordered

Utilisation : appliquez ce type de qualificateur uniquement aux propriétés et aux paramètres qui sont des tableaux (définis à l’aide de la syntaxe de crochet).

</dd> <dt>

<span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Pixels**
</dt> <dd>

Type de données : **tableau de chaînes**

S’applique à : propriétés, méthodes, paramètres

Carte de positions de bits significatives où chaque position significative peut être « on » ou « OFF ». Chaque bit « on » correspond à une valeur correspondante dans le tableau **BitValue** . En ayant plusieurs bits « on », plusieurs valeurs simultanées dans le tableau **BitValue** sont indiquées. La valeur par défaut est **null**.

Pour plus d’informations, consultez [bitmap et BitValue](bitmap-and-bitvalues.md).

</dd> <dt>

<span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValue**
</dt> <dd>

Type de données : **tableau de chaînes**

S’applique à : propriétés, méthodes, paramètres

Traduction d’une valeur de position de bit en une **chaîne** associée. La valeur par défaut est **null**.

Pour plus d’informations, consultez [bitmap et BitValue](bitmap-and-bitvalues.md).

</dd> <dt>

<span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Constructeur**
</dt> <dd>

Type de données : **booléen**

S’applique à : méthodes

Indique si la méthode crée des instances. Ces méthodes ne sont pas contractions pour agir sur une seule instance ou une seule classe. Par exemple, un constructeur peut créer des instances d’association ainsi que des instances de la classe qui définit le constructeur.

Le qualificateur du **constructeur** est destiné uniquement à des fins d’information et il n’est pas prévu qu’il soit traité par le gestionnaire d’objets. Le gestionnaire d’objets n’a pas besoin d’appeler des méthodes de constructeur lors de la création d’un objet. De même, lorsqu’un constructeur est appelé, le gestionnaire d’objets n’a pas à appeler de méthodes de constructeur définies pour toute classe parente de la classe d’origine. La valeur par défaut est **false**.

</dd> <dt>

<span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**
</dt> <dd>

Type de données : **chaîne**

S’applique à : classes

Nom de la méthode par laquelle les instances de cette classe sont créées. La valeur est soit « PutInstance », soit le nom d’une autre méthode qui crée les instances. La valeur par défaut est **null**.

Utilisation : ce qualificateur ne peut être utilisé que si le qualificateur **SupportsCreate** est présent.

</dd> <dt>

<span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**
</dt> <dd>

Type de données : **chaîne**

S’applique à : classes

Nom de la méthode par laquelle les instances de cette classe sont supprimées. La valeur est soit « DeleteInstance », soit le nom d’une autre méthode qui supprime les instances. La valeur par défaut est **null**.

Utilisation : ce qualificateur ne peut être utilisé que si le qualificateur **SupportsDelete** est présent.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Type de données : **chaîne**

S’applique à : any

Description d’un élément nommé. La valeur par défaut est **null**.

</dd> <dt>

<span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destructeur**
</dt> <dd>

Type de données : **booléen**

S’applique à : méthodes

Indique si la méthode supprime des instances. Les méthodes qui utilisent le qualificateur de **destructeur** suppriment la ou les instances auxquelles le destructeur est appliqué, et ne sont pas contractions pour agir sur une instance ou une classe unique. Par exemple, un destructeur peut supprimer des instances d’association ainsi que des instances de la classe qui définit le destructeur.

Le qualificateur du **destructeur** est destiné uniquement à des fins d’information et il n’est pas prévu qu’il soit traité par le gestionnaire d’objets. Le gestionnaire d’objets n’a aucune obligation d’appeler une méthode qui a le qualificateur de **destructeur** lorsqu’une instance est supprimée. En outre, lorsqu’un destructeur est appelé, le gestionnaire d’objets n’a pas à appeler les méthodes de destructeur définies pour toute classe parente de la classe d’origine. La valeur par défaut est **false**.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**NomComplet**
</dt> <dd>

Type de données : **chaîne**

S’applique à : any

Nom affiché dans l’interface utilisateur au lieu du nom réel de l’élément. La valeur par défaut est **null**.

</dd> <dt>

<span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**
</dt> <dd>

Type de données : **chaîne**

S’applique à : any

L’élément de type de chaîne qualifié contient une instance incorporée. La valeur de qualificateur spécifie le nom d’une classe CIM dans le même espace de noms que la classe qui possède l’élément qualifié. L’instance incorporée est une instance de la classe spécifiée, y compris les instances de ses sous-classes. La valeur par défaut est **null**.

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gabarit**
</dt> <dd>

Type de données : **booléen**

S’applique à : any

Indique si la propriété représente un entier non négatif, qui peut augmenter ou diminuer, mais ne dépassent jamais une valeur maximale. La valeur par défaut est **false**.

La valeur maximale de la propriété ne peut pas être supérieure à 2 ^*n* -1. *N* peut être 8, 16, 32 ou 64 selon le type de données de la propriété à laquelle ce qualificateur est appliqué. La valeur d’une jauge a sa valeur maximale chaque fois que les informations qui sont modélisées sont supérieures ou égales à cette valeur maximale. Si les informations qui sont modélisées descendent ensuite en dessous de la valeur maximale, la jauge diminue également. Ce qualificateur ne s’applique qu’aux propriétés dont le type de données est unsigned Integer.

</dd> <dt>

<span id="In"></span><span id="in"></span><span id="IN"></span>**Dans**
</dt> <dd>

Type de données : **booléen**

S’applique à : paramètres

Indique si le paramètre est utilisé pour passer des valeurs à une méthode. La valeur par défaut est **true**.

</dd> <dt>

<span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, out**
</dt> <dd>

Type de données : **booléen**

S’applique à : paramètres

Indique si le paramètre est à la fois un paramètre d’entrée et de sortie.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Essentiel**](key-qualifier.md)
</dt> <dd>

Type de données : **booléen**

S’applique à : propriétés, références

Indique si la propriété fait partie du handle d’espace de noms. Si plusieurs propriétés ont le qualificateur de [**clé**](key-qualifier.md) , toutes ces propriétés forment collectivement la clé (une clé composée). Lorsqu’elles sont prises en compte, les propriétés de clé doivent fournir une référence unique pour chaque instance de classe. Si ce qualificateur est placé sur une propriété, seule la valeur **true** est autorisée.

</dd> <dt>

<span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Différé**
</dt> <dd>

S’applique à : Properties

Indique que la propriété est gourmande en ressources pour retourner et requiert beaucoup de temps processeur et de mémoire. WMI améliore les performances des requêtes en ne tentant pas de retourner les propriétés marquées avec le qualificateur **Lazy** .

</dd> <dt>

<span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**
</dt> <dd>

Type de données : **tableau de chaînes**

S’applique à : classes, propriétés, associations, indications, références

Ensemble de valeurs qui indiquent un chemin d’accès à un emplacement où vous pouvez trouver plus d’informations sur l’origine d’une propriété, d’une classe, d’une association, d’une indication ou d’une référence. La chaîne de mappage peut être un chemin d’accès de répertoire, une URL, une clé de Registre, un fichier include, une référence à une classe CIM ou un autre format. La valeur par défaut est **null**.

</dd> <dt>

<span id="Max"></span><span id="max"></span><span id="MAX"></span>**Max**
</dt> <dd>

Type de données : **int**

S’applique à : références

Nombre maximal de valeurs qu’une référence donnée peut avoir pour chaque ensemble d’autres valeurs de référence dans l’Association. La valeur par défaut est **null**. Par exemple, si une association associe une instance à des instances B et qu’il ne doit y avoir qu’une instance pour chaque instance B, la référence à un doit avoir au maximum un qualificateur.

</dd> <dt>

<span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**
</dt> <dd>

Type de données : **int**

S’applique à : propriétés, méthodes, paramètres

Longueur maximale (en caractères) d’un élément de données de **type chaîne** et indique la prise en charge des tableaux de longueur fixe.

Si un tableau de longueur fixe est rencontré, le qualificateur **MaxLen** contient la longueur fixe trouvée lors de l’analyse. Si un tableau de longueur variable est rencontré, ce qualificateur n’est pas utilisé. **MaxLen** est utilisé pour suggérer le nombre maximal d’éléments qui doivent être stockés dans un tableau. Lors du remplacement de la valeur par défaut, toute valeur entière non signée (**UInt32**) peut être spécifiée. La valeur **null** (valeur par défaut) implique une longueur illimitée.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**
</dt> <dd>

Type de données : **int**

S’applique à : propriétés, méthodes, paramètres

Valeur maximale de l’objet. La valeur par défaut est **null**.

</dd> <dt>

<span id="Min"></span><span id="min"></span><span id="MIN"></span>**Min**
</dt> <dd>

Type de données : **int**

S’applique à : références

Cardinalité minimale de la référence (nombre minimal de valeurs qu’une référence donnée peut avoir pour chaque ensemble d’autres valeurs de référence dans l’Association). La valeur par défaut est 0.

Par exemple, si une association associe des instances à B et qu’il doit y avoir au moins une instance pour chaque instance B, la référence à un doit avoir au minimum un qualificateur.

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**
</dt> <dd>

Type de données : **int**

S’applique à : propriétés, méthodes, paramètres

Indique la valeur minimale de l’objet. La valeur par défaut est **null**.

</dd> <dt>

<span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**
</dt> <dd>

Type de données : **tableau de chaînes**

S’applique à : Properties

Ensemble de valeurs qui indiquent la correspondance entre la propriété d’un objet et d’autres propriétés dans le schéma CIM. La valeur par défaut est **null**.

Les propriétés d’objet sont identifiées à l’aide de la syntaxe suivante.

<schema name> "\_" <class or association name> "." <property name>

</dd> <dt>

<span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Non locale**
</dt> <dd>

Type de données : **chaîne**

S’applique à : références

Emplacement d’une instance, dont la valeur est <*namespacetype*>://<*namespacehandle*> la valeur par défaut est **null**.

Utilisation : ce qualificateur ne peut pas être utilisé avec le qualificateur **NonlocalType** .

</dd> <dt>

<span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**
</dt> <dd>

Type de données : **chaîne**

S’applique à : références

Type d’emplacement d’une instance. Sa valeur est <namespacetype> . La valeur par défaut est **null**.

Utilisation : ce qualificateur ne peut pas être utilisé avec le qualificateur non **local** .

</dd> <dt>

<span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**
</dt> <dd>

Type de données : **chaîne**

S’applique à : Properties

Valeur qui indique que la propriété associée est **null** (la propriété n’a pas de valeur valide ou explicite). La valeur par défaut est **null**.

Les conventions et restrictions utilisées pour définir les valeurs **null** sont les mêmes que celles applicables au qualificateur **ValueMap** . Notez que ce qualificateur ne peut pas être substitué. Il est déraisonnable de permettre à une sous-classe de retourner une valeur **null** différente de celle de la classe parente.

</dd> <dt>

<span id="Out"></span><span id="out"></span><span id="OUT"></span>**À**
</dt> <dd>

Type de données : **booléen**

S’applique à : paramètres

Indique si le paramètre retourne des valeurs à partir d’une méthode. La valeur par défaut est **false**.

</dd> <dt>

<span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Remplacer**
</dt> <dd>

Type de données : **chaîne**

S’applique à : propriétés, méthodes, références

Classe parente ou construction subordonnée (propriété, méthode ou référence) qui est remplacée par la propriété, la méthode ou la référence du même nom dans la classe dérivée. La valeur par défaut est **null**.

Le format est le suivant :

\[<> de la *classe* . \] < *construction subordonnée*>

Si le nom de la classe est omis, le remplacement s’applique à la construction subordonnée dans la classe parente de la hiérarchie de classes.

Utilisation : le qualificateur **override** ne peut faire référence qu’à des constructions basées sur le même méta-modèle. La modification d’un nom ou d’une signature de construction au cours d’une opération de remplacement n’est pas autorisée.

</dd> <dt>

<span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**
</dt> <dd>

S’applique à : classes

Indique si la valeur de propriété d’une sous-classe remplace la valeur dans une classe parente. L’implication fonctionnelle est que, si vous exécutez une requête sur la classe parente, et si votre clause **Where** comprend cette propriété, le parent doit retourner une instance avec la valeur substituée. Par conséquent, la gestion Windows ajuste la clause **Where** de la requête envoyée à la classe parente pour exclure les références à cette propriété.

</dd> <dt>

<span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagées**
</dt> <dd>

Type de données : **chaîne**

S’applique à : Properties

Nom de la clé qui est propagée. La valeur par défaut est **null**.

L’utilisation de ce qualificateur suppose l’existence d’un seul qualificateur faible sur une référence qui a la classe conteneur comme cible. La propriété associée doit avoir la même valeur que la propriété nommée par le qualificateur dans la classe de l’autre côté de l’Association faible. Le format est le suivant :

\[<> de la *classe* . \] < *construction subordonnée*>

Utilisation : quand le qualificateur **propagé** est utilisé, le qualificateur de [**clé**](key-qualifier.md) doit être spécifié avec la valeur **true**.

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>**En lecture**
</dt> <dd>

Type de données : **booléen**

S’applique à : Properties

Indique si la propriété est lisible. La valeur par défaut est **true**.

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Obligatoire**
</dt> <dd>

Type de données : **booléen**

S’applique à : Properties

Indique si une valeur non null est requise pour la propriété. La valeur par défaut est **false**.

</dd> <dt>

<span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Faisant**
</dt> <dd>

Type de données : **chaîne**

S’applique à : classes, associations, indications, schémas

Numéro de révision mineure de l’objet de schéma. La valeur par défaut est **null**.

Utilisation : le qualificateur de **version** doit être présent pour fournir le numéro de version principale lorsque le qualificateur de **révision** est utilisé.

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Schéma**
</dt> <dd>

Type de données : **chaîne**

S’applique à : propriétés, méthodes

Nom du schéma dans lequel la fonctionnalité est définie. La valeur par défaut est **null**.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Code**
</dt> <dd>

Type de données : **chaîne**

S’applique à : classes, associations, indications, références

Emplacement d’une instance. La valeur par défaut est **null**.

La valeur du qualificateur est <*namespacetype*>://<*namespacehandle*>.

Utilisation : le qualificateur **source** ne peut pas être utilisé avec le qualificateur **SourceType** .

</dd> <dt>

<span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**Telle**
</dt> <dd>

Type de données : **chaîne**

S’applique à : classes, associations, indications, références

Type d’emplacement d’une instance. La valeur de ce qualificateur est <> *NamespaceType* . La valeur par défaut est **null**.

Utilisation : le qualificateur **SourceType** ne peut pas être utilisé avec le qualificateur **source** .

</dd> <dt>

<span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**
</dt> <dd>

Type de données : **booléen**

S’applique à : classes

Indique si la classe prend en charge la création d’instances de. La valeur par défaut est **false**.

</dd> <dt>

<span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**
</dt> <dd>

Type de données : **booléen**

S’applique à : classes

Indique si la classe prend en charge la suppression des instances de. La valeur par défaut est **false**.

</dd> <dt>

<span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**
</dt> <dd>

Type de données : **booléen**

S’applique à : classes

Indique si la classe prend en charge la modification (mise à jour) des instances de. La valeur par défaut est **false**.

</dd> <dt>

<span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminaux**
</dt> <dd>

Type de données : **booléen**

S’applique à : classes

Indique si la classe peut avoir des sous-classes. La valeur par défaut est **false**.

Si une sous-classe est déclarée, le compilateur génère une erreur.

Utilisation : ce qualificateur ne peut pas coexister avec le qualificateur **abstract** . Si les qualificateurs **Terminal** et **abstract** sont tous les deux spécifiés, le compilateur génère une erreur.

</dd> <dt>

<span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Sections**
</dt> <dd>

Type de données : **chaîne**

S’applique à : propriétés, méthodes, paramètres

Type d’unité dans laquelle l’élément de données associé est exprimé. La valeur par défaut est **null**.

Par exemple, un élément de données de taille peut avoir la valeur « octets » pour les **unités**.

</dd> <dt>

<span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**
</dt> <dd>

Type de données : **tableau de chaînes**

S’applique à : propriétés, méthodes, paramètres

Ensemble de valeurs autorisées pour une propriété, un type de retour de méthode ou un paramètre de méthode. La valeur par défaut est **null**.

Utilisation : ce qualificateur peut être utilisé seul ou en combinaison avec le qualificateur **values** . En cas d’utilisation en association avec le qualificateur **values** , l’emplacement de la valeur dans le tableau **ValueMap** fournit l’emplacement de l’entrée correspondante dans le tableau **values** . Utilisez le qualificateur **ValueMap** uniquement avec des valeurs de chaîne et d’entier. La syntaxe de la représentation d’une valeur entière dans le tableau de mappage des valeurs est digit \[ + \| = \] \[ \* digit \] . Le contenu, le nombre maximal de chiffres et la valeur représentée sont limités par le type de la propriété associée. Par exemple, UInt8 ne peut pas être signé, doit être inférieur à quatre chiffres et doit représenter une valeur inférieure à 256.

</dd> <dt>

<span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Valeurs**
</dt> <dd>

Type de données : **tableau de chaînes**

S’applique à : propriétés, méthodes, paramètres

Ensemble de valeurs traduisant une valeur entière en une chaîne associée. La valeur par défaut est **null**.

Cette propriété spécifie également un tableau de valeurs de chaîne à mapper à une propriété d’énumération. Ce qualificateur peut être appliqué à une propriété de type entier ou à une propriété de type chaîne, et le mappage peut être implicite ou explicite. Si le mappage est implicite, les valeurs de propriété de type entier ou chaîne représentent des positions ordinales dans le tableau de **valeurs** . Si le mappage est explicite, la propriété doit être un entier et les valeurs de propriété valides sont répertoriées dans le tableau défini par le qualificateur **ValueMap** . Pour plus d’informations, consultez [mappage des valeurs](value-map.md).

Si aucun qualificateur **ValueMap** n’est présent, le tableau de **valeurs** est indexé (relatif à zéro) à l’aide de la valeur dans la propriété, le type de retour de méthode ou le paramètre de méthode associé. Si un qualificateur **ValueMap** est présent, l’index des valeurs est défini par l’emplacement de la valeur de la propriété dans le mappage des valeurs.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**
</dt> <dd>

Type de données : **chaîne**

S’applique à : classes, schémas, associations, indications

Numéro de version principale de l’objet de schéma. La valeur par défaut est **null**. Le numéro de version est incrémenté lorsque des modifications sont apportées au schéma qui modifie l’interface.

</dd> <dt>

<span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Très**
</dt> <dd>

Type de données : **booléen**

S’applique à : références

Indique si les clés de la classe référencée incluent les clés des autres participants de l’Association. La valeur par défaut est **false**.

Ce qualificateur est utilisé lorsque l’identité de la classe référencée dépend de l’identité des autres participants de l’Association. Une seule référence à une classe donnée peut être faible. Les autres classes de l’Association doivent définir une clé. Les clés des autres classes de l’Association sont répétées dans la classe référencée et sont marquées avec un qualificateur **propagé** .

</dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Ecrire**
</dt> <dd>

Type de données : **booléen**

S’applique à : Properties

Indique que les applications ou les scripts peuvent modifier la valeur de la propriété. Le compte qui exécute l’application doit avoir accès à l’espace de noms qui contient des instances de la classe. L’implémentation du fournisseur peut également limiter l’accès aux données du fournisseur. La valeur **true** indique que la propriété est lisible et accessible en écriture par les consommateurs qui sont autorisés à accéder à WMI et au fournisseur. La valeur par défaut est **false**.

Une propriété qui n’a pas de qualificateur d' **écriture** peut encore être accessible en écriture. L’implémentation du fournisseur peut autoriser la modification de toutes les propriétés dans les classes de fournisseur, que le qualificateur d' **écriture** soit présent ou non.

</dd> <dt>

<span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**
</dt> <dd>

Type de données : **booléen**

S’applique à : Properties

Indique si la propriété peut être accessible en écriture lors de la création de l’instance. Ce qualificateur peut être utilisé conjointement avec le qualificateur **WriteAtCreate** . La valeur par défaut est **false**.

</dd> <dt>

<span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**
</dt> <dd>

Type de données : **booléen**

S’applique à : Properties

Indique si la propriété est accessible en écriture à la mise à jour de l’instance. Ce qualificateur peut être utilisé conjointement avec le qualificateur **WriteAtCreate** . La valeur par défaut est **false**.

</dd> </dl>

## <a name="examples"></a>Exemples

Pour plus d’informations sur la récupération des qualificateurs, consultez l’exemple de code PowerShell [WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) dans la Galerie technet.

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

 

 




