---
description: La table ModuleComponents contient une liste des composants qui se trouvent dans le module de fusion.
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: Table ModuleComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25216833022ada7592511091c6954222d8ebf354e732c95a54e8857948963541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926479"
---
# <a name="modulecomponents-table"></a>Table ModuleComponents

La table ModuleComponents contient une liste des composants qui se trouvent dans le module de fusion.

La table ModuleComponents contient les colonnes suivantes.



| Colonne    | Type                         | Clé | Nullable |
|-----------|------------------------------|-----|----------|
| Composant | [Identificateur](identifier.md) | O   | N        |
| ModuleID  | [Identificateur](identifier.md) | O   | N        |
| Langage  | [Integer](integer.md)       | O   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>-
</dt> <dd>

Identificateur qui fait référence à un composant dans le module de fusion. La colonne de composant est une clé étrangère de la [table des composants](component-table.md). L’entrée dans la colonne de composant doit respecter la Convention d’affectation de noms pour [nommer les clés primaires dans les bases de données de module de fusion](naming-primary-keys-in-merge-module-databases.md).

</dd> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Identificateur du module de fusion. Il s’agit d’une clé étrangère de la [table ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Sous
</dt> <dd>

L’identificateur de langue décrit la langue par défaut pour le module de fusion. L’identificateur de langue est au format décimal, par exemple, l’anglais des États-Unis est 1033. Clé étrangère vers la [table ModuleSignature](modulesignature-table.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

Les transformations de langage doivent être en mesure de mettre à jour cette table si le module de fusion prend en charge plusieurs langues.

 

 



