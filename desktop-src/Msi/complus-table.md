---
description: La table ComPlus contient les informations nécessaires pour installer les applications COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Table ComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77885688226689e5d81e074b1a9a28ef3801aaeba5febf51165377ac9ad9e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144970"
---
# <a name="complus-table"></a>Table ComPlus

La table ComPlus contient les informations nécessaires pour installer les applications COM+.

La table ComPlus contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| Composant\_ | [Identificateur](identifier.md) | O   | N        |
| ExpType     | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la première colonne de la [table de composants](component-table.md). Il s’agit du composant qui contient l’application COM+.

</dd> <dt>

<span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType
</dt> <dd>

Exportez les indicateurs utilisés lors de la génération du fichier .msi. pour plus d’informations, consultez la documentation COM+ dans le kit de développement logiciel (SDK) de Microsoft Windows.

</dd> </dl>

## <a name="remarks"></a>Remarques

Consultez l’action [RegisterComPlus](registercomplus-action.md) et l' [action UnregisterComPlus](unregistercomplus-action.md).

consultez [installation d’une Application COM+ avec l’Windows Installer](installing-a-com--application-with-the-windows-installer.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
</dl>

 

 



