---
description: La table ComPlus contient les informations nécessaires pour installer les applications COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Table ComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526286"
---
# <a name="complus-table"></a>Table ComPlus

La table ComPlus contient les informations nécessaires pour installer les applications COM+.

La table ComPlus contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| -\_ | [Identificateur](identifier.md) | O   | N        |
| ExpType     | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la première colonne de la [table de composants](component-table.md). Il s’agit du composant qui contient l’application COM+.

</dd> <dt>

<span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType
</dt> <dd>

Exportez les indicateurs utilisés lors de la génération du fichier. msi. Pour plus d’informations, consultez la documentation COM+ dans le kit de développement logiciel (SDK) Microsoft Windows.

</dd> </dl>

## <a name="remarks"></a>Notes

Consultez l’action [RegisterComPlus](registercomplus-action.md) et l' [action UnregisterComPlus](unregistercomplus-action.md).

Consultez [installation d’une application com+ avec l’Windows Installer](installing-a-com--application-with-the-windows-installer.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
</dl>

 

 



