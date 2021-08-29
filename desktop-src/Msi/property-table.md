---
description: La table des propriétés contient les noms et les valeurs des propriétés de toutes les propriétés définies dans l’installation. Les propriétés avec des valeurs NULL ne sont pas présentes dans la table.
ms.assetid: 1f4215b2-dc71-4e6e-bc2e-3b43316806b9
title: Table de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a7f72d1ee8cbbf05e39754ba1d06700f7b5d5f2e03c0a7ef3cb9b03b7d00f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145352"
---
# <a name="property-table"></a>Table de propriétés

La table des propriétés contient les noms et les valeurs des propriétés de toutes les propriétés définies dans l’installation. Les propriétés avec des valeurs NULL ne sont pas présentes dans la table.

La table de propriétés contient les colonnes suivantes.



| Colonne   | Type                         | Clé | Nullable |
|----------|------------------------------|-----|----------|
| Propriété | [Identificateur](identifier.md) | O   | N        |
| Valeur    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété
</dt> <dd>

Nom d'une propriété. Consultez [Propriétés](properties.md).

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Valeur de chaîne localisable pour la propriété. Cela peut ne jamais avoir la valeur null ou être une chaîne vide.

</dd> </dl>

## <a name="remarks"></a>Remarques

Notez que vous ne pouvez pas utiliser la table de propriétés pour affecter à une propriété la valeur d’une autre propriété. Le programme d’installation ne fait rien de la chaîne de texte entrée dans la colonne valeur avant de définir la propriété dans la colonne propriété. Si FirstProperty est entré dans la colonne de propriété et \[ SecondProperty \] dans la colonne valeur, la valeur de FirstProperty est définie sur la chaîne de texte « \[ SecondProperty \] » et non sur la valeur de la propriété SecondProperty. Cela est nécessaire pour empêcher la création de références circulaires dans la table de propriétés. Au lieu de cela, vous pouvez définir une propriété sur une autre à l’aide d’un [type d’action personnalisé 51](custom-action-type-51.md).

Notez que la propriété [**AdminProperties**](adminproperties.md) peut être utilisée pour remplacer les valeurs de la table de propriétés lors d’une [installation administrative](administrative-installation.md).

N’utilisez pas de propriétés pour les mots de passe ou d’autres informations qui doivent rester sécurisées. Le programme d’installation peut écrire la valeur d’une propriété créée dans la table de propriétés, ou créée au moment de l’exécution, dans un journal ou dans le registre système.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE05](ice05.md)  
[ICE06](ice06.md)  
[ICE16](ice16.md)  
[ICE24](ice24.md)  
[ICE31](ice31.md)  
[ICE34](ice34.md)  
[ICE36](ice36.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE48](ice48.md)  
[ICE52](ice52.md)  
[ICE61](ice61.md)  
[ICE73](ice73.md)  
[ICE74](ice74.md)  
[ICE80](ice80.md)  
[ICE87](ice87.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
[ICE99](ice99.md)  
</dl>

 

 



