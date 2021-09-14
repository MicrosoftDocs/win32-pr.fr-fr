---
description: La table ComPlus contient les informations nécessaires pour installer les applications COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Table ComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092125"
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

## <a name="remarks"></a>Notes

Consultez l’action [RegisterComPlus](registercomplus-action.md) et l' [action UnregisterComPlus](unregistercomplus-action.md).

consultez [installation d’une Application COM+ avec l’Windows Installer](installing-a-com--application-with-the-windows-installer.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
</dl>

 

 



