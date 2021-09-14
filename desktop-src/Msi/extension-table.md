---
description: La table d’extension contient des informations sur les serveurs d’extension de nom de fichier qui doivent être générés dans le cadre de la publication du produit. Chaque ligne génère un ensemble de clés et de valeurs de registre.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Table d’extension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef52f7248f44dcb63255244bbd8abd4ac8181d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091269"
---
# <a name="extension-table"></a>Table d’extension

La table d’extension contient des informations sur les serveurs d’extension de nom de fichier qui doivent être générés dans le cadre de la publication du produit. Chaque ligne génère un ensemble de clés et de valeurs de registre.

La table d’extension contient les colonnes indiquées dans le tableau suivant.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| Extension   | [Text](text.md)             | O   | N        |
| Composant\_ | [Identificateur](identifier.md) | O   | N        |
| ProgId\_    | [Text](text.md)             | N   | O        |
| MIME\_      | [Text](text.md)             | N   | O        |
| Fonctionnalité\_   | [Identificateur](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Poste
</dt> <dd>

Extension associée à la ligne de table. L’extension peut comporter jusqu’à 255 caractères. Entrez l’extension dans ce champ sans la période précédente.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe de la première colonne de la table de [composants](component-table.md) . Cette colonne fait référence au composant qui contrôle l’installation de l’extension.

</dd> <dt>

<span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgId\_
</dt> <dd>

ID de programme associé à cette extension. Il s’agit d’une clé étrangère dans la table [ProgID](progid-table.md) .

</dd> <dt>

<span id="MIME_"></span><span id="mime_"></span>MIME\_
</dt> <dd>

Type de contenu qui doit être écrit pour la colonne d’extension.

Clé externe de la première colonne de la table [MIME](mime-table.md) .

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_
</dt> <dd>

Une clé externe dans la première colonne de la table de [fonctionnalités](feature-table.md) spécifiant la fonctionnalité qui fournit le serveur d’extension.

</dd> </dl>

## <a name="remarks"></a>Notes

La table d’extension est référencée lorsque l’action [RegisterExtensionInfo](registerextensioninfo-action.md) ou l’action [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) est exécutée.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE69](ice69.md)  
</dl>

 

 



