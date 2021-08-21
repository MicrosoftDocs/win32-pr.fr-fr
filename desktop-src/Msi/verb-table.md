---
description: La table de verbes contient des informations sur les verbes de commande associées aux extensions de noms de fichiers qui doivent être générées dans le cadre de la publication du produit. Chaque ligne génère un ensemble de clés et de valeurs de registre.
ms.assetid: 3749095c-f0c0-498c-969f-a6c445cfdd62
title: Table de verbes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fc546cd3db5fecb3861120fa15b1ffa3f21327b889599b77a1b067193c886c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499109"
---
# <a name="verb-table"></a>Table de verbes

La table de verbes contient des informations sur les verbes de commande associées aux extensions de noms de fichiers qui doivent être générées dans le cadre de la publication du produit. Chaque ligne génère un ensemble de clés et de valeurs de registre.

La table de verbes contient les colonnes suivantes.



| Colonne      | Type                       | Clé | Nullable |
|-------------|----------------------------|-----|----------|
| Extension\_ | [Text](text.md)           | O   | N        |
| Verbe        | [Text](text.md)           | O   | N        |
| Séquence    | [Integer](integer.md)     | N   | Y        |
| Commande     | [Correct](formatted.md) | N   | O        |
| Argument    | [Correct](formatted.md) | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Poste\_
</dt> <dd>

Extension associée à la ligne de table. Cette colonne est une clé externe de la première colonne de la [table d’extension](extension-table.md).

</dd> <dt>

<span id="Verb"></span><span id="verb"></span><span id="VERB"></span>DoVerb
</dt> <dd>

Verbe pour la commande.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence
</dt> <dd>

Séquence des commandes. Seuls les verbes pour lesquels la colonne Sequence est non NULL sont utilisés pour préparer une liste triée pour la valeur par défaut de la clé de l’interpréteur de commandes. Le verbe avec la valeur la plus faible dans cette colonne devient le verbe par défaut.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Commande
</dt> <dd>

Texte localisable affiché dans le menu contextuel.

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument
</dt> <dd>

Valeur pour les arguments de commande.

Notez que la résolution des propriétés dans le champ argument est limitée. Une propriété mise en forme en tant que \[ *propriété* \] dans ce champ ne peut être résolue que si la propriété a déjà la valeur prévue lorsque le composant propriétaire du verbe est installé. Par exemple, pour que l’argument « \[ \#MyDoc.doc\] » soit résolu à la valeur correcte, le même processus doit installer le fichier MyDoc.doc et le composant qui possède le verbe.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette table est référencée lorsque l' [action RegisterExtensionInfo](registerextensioninfo-action.md) ou l' [action UnregisterExtensionInfo](unregisterextensioninfo-action.md) est exécutée.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



